---
title: Parancsmagok párhuzamos futtatása PowerShell-feladatok használatával
description: Parancsok párhuzamos futtatása az -AsJob paraméter segítségével.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: d312812ff3c9e4934ed2bfa7371a9e420668e852
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83384993"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a>Parancsmagok párhuzamos futtatása PowerShell-feladatok használatával

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

A PowerShell a [PowerShell-feladatok](/powershell/module/microsoft.powershell.core/about/about_jobs) révén támogatja az aszinkron műveleteket.
Az Azure PowerShell működése nagymértékben függ az Azure-hoz intézett hálózati hívások létrehozásától és a rájuk való várakozástól. Gyakran lehet szüksége nem blokkoló hívás kezdeményezésére. Az Azure PowerShell első osztályú [PS-feladattámogatást](/powershell/module/microsoft.powershell.core/about/about_jobs) biztosít ezen igény kielégítése céljából.

## <a name="context-persistence-and-psjobs"></a>Környezetmegőrzés és PS-feladatok

A PS-feladatok külön folyamatokként futnak, ezért az Azure-kapcsolatát meg kell osztania azokkal. Miután a `Connect-AzureRmAccount` használatával bejelentkezett Azure-fiókjába, a környezetet átadhatja egy feladatnak.

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

Ha azonban a környezet az `Enable-AzureRmContextAutosave` használatával történő automatikus mentését választotta, a környezet minden létrehozott feladattal automatikusan meg lesz osztva.

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a>Automatikus feladatok az `-AsJob` kapcsolóval

Az Azure PowerShell a kényelem érdekében egyes hosszan futó parancsmagokhoz `-AsJob` kapcsolót is biztosít.
Az `-AsJob` kapcsoló még inkább megkönnyíti a PS-feladatok létrehozását.

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

A `Get-Job` és a `Get-AzureRmVM` segítségével bármikor ellenőrizheti a feladatot és annak állapotát.

```azurepowershell-interactive
Get-Job $job
Get-AzureRmVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

Ha a feladat befejeződött, a `Receive-Job` használatával lekérheti a feladat eredményét.

> [!NOTE]
> A `Receive-Job` úgy adja vissza a parancsmag eredményét, mintha az `-AsJob` jelző nem lenne jelen.
> Például a `Do-Action -AsJob``Receive-Job`-eredménye ugyanaz a típus, mint a `Do-Action` eredménye.

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
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

Ebben a példában a `Wait-Job` parancsmag felfüggeszti a szkriptet, amíg a feladatok futnak. A szkript végrehajtása folytatódik, amint az összes feladat befejeződött. Több feladatot fut párhuzamosan, a szkript pedig megvárja azok befejezését a továbblépés előtt.

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
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
