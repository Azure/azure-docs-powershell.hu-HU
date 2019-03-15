---
title: Parancsmagok párhuzamos futtatása PowerShell-feladatok használatával
description: Parancsok párhuzamos futtatása az -AsJob paraméter segítségével.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 65d3a1d206d7318173a87a4e53c579155a85426c
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882276"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a>Parancsmagok párhuzamos futtatása PowerShell-feladatok használatával

A PowerShell a [PowerShell-feladatok](/powershell/module/microsoft.powershell.core/about/about_jobs) révén támogatja az aszinkron műveleteket.
Az Azure PowerShell működése nagymértékben függ az Azure-hoz intézett hálózati hívások létrehozásától és a rájuk való várakozástól. Gyakran lehet szüksége nem blokkoló hívás kezdeményezésére. Az Azure PowerShell első osztályú [PS-feladattámogatást](/powershell/module/microsoft.powershell.core/about/about_jobs) biztosít ezen igény kielégítése céljából.

## <a name="context-persistence-and-psjobs"></a>Környezetmegőrzés és PS-feladatok

A PS-feladatok külön folyamatokként futnak, ezért az Azure-kapcsolatát meg kell osztania azokkal. Miután a `Connect-AzAccount` használatával bejelentkezett Azure-fiókjába, a környezetet átadhatja egy feladatnak.

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzContext),$creds
```

Ha azonban a környezet az `Enable-AzContextAutosave` használatával történő automatikus mentését választotta, a környezet minden létrehozott feladattal automatikusan meg lesz osztva.

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a>Automatikus feladatok az `-AsJob` kapcsolóval

Az Azure PowerShell a kényelem érdekében egyes hosszan futó parancsmagokhoz `-AsJob` kapcsolót is biztosít.
Az `-AsJob` kapcsoló még inkább megkönnyíti a PS-feladatok létrehozását.

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

A `Get-Job` és a `Get-AzVM` segítségével bármikor ellenőrizheti a feladatot és annak állapotát.

```azurepowershell-interactive
Get-Job $job
Get-AzVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzVM' AzureLongRunningJob`1 Running True        localhost New-AzVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

Ha a feladat befejeződött, a `Receive-Job` használatával lekérheti a feladat eredményét.

> [!NOTE]
> A `Receive-Job` úgy adja vissza a parancsmag eredményét, mintha az `-AsJob` jelző nem lenne jelen.
> Például a `Do-Action -AsJob` `Receive-Job`-eredménye ugyanaz a típus, mint a `Do-Action` eredménye.

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a>Példaforgatókönyvek

Több virtuális gép egyszerre történő létrehozása:

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzVM
```

Ebben a példában a `Wait-Job` parancsmag felfüggeszti a szkriptet, amíg a feladatok futnak. A szkript végrehajtása folytatódik, amint az összes feladat befejeződött. Több feladatot fut párhuzamosan, a szkript pedig megvárja azok befejezését a továbblépés előtt.

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```
