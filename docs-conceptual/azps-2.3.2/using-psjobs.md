---
title: Parancsmagok párhuzamos futtatása PowerShell-feladatok használatával
description: Parancsok párhuzamos futtatása az -AsJob paraméter segítségével.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 825a07e01194a07b747712a62384c7f162e63d7d
ms.sourcegitcommit: 0356a4694f77eda40eec8c3759b9bb7f28979eb6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2019
ms.locfileid: "67192903"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="cb69d-103">Parancsmagok párhuzamos futtatása PowerShell-feladatok használatával</span><span class="sxs-lookup"><span data-stu-id="cb69d-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="cb69d-104">A PowerShell a [PowerShell-feladatok](/powershell/module/microsoft.powershell.core/about/about_jobs) révén támogatja az aszinkron műveleteket.</span><span class="sxs-lookup"><span data-stu-id="cb69d-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="cb69d-105">Az Azure PowerShell működése nagymértékben függ az Azure-hoz intézett hálózati hívások létrehozásától és a rájuk való várakozástól.</span><span class="sxs-lookup"><span data-stu-id="cb69d-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="cb69d-106">Gyakran lehet szüksége nem blokkoló hívás kezdeményezésére.</span><span class="sxs-lookup"><span data-stu-id="cb69d-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="cb69d-107">Az Azure PowerShell első osztályú [PS-feladattámogatást](/powershell/module/microsoft.powershell.core/about/about_jobs) biztosít ezen igény kielégítése céljából.</span><span class="sxs-lookup"><span data-stu-id="cb69d-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="cb69d-108">Környezetmegőrzés és PS-feladatok</span><span class="sxs-lookup"><span data-stu-id="cb69d-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="cb69d-109">A PS-feladatok külön folyamatokként futnak, ezért az Azure-kapcsolatát meg kell osztania azokkal.</span><span class="sxs-lookup"><span data-stu-id="cb69d-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="cb69d-110">Miután a `Connect-AzAccount` használatával bejelentkezett Azure-fiókjába, a környezetet átadhatja egy feladatnak.</span><span class="sxs-lookup"><span data-stu-id="cb69d-110">After signing in to your Azure account with `Connect-AzAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList (Get-AzContext),$creds
```

<span data-ttu-id="cb69d-111">Ha azonban a környezet az `Enable-AzContextAutosave` használatával történő automatikus mentését választotta, a környezet minden létrehozott feladattal automatikusan meg lesz osztva.</span><span class="sxs-lookup"><span data-stu-id="cb69d-111">However, if you have chosen to have your context automatically saved with `Enable-AzContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -ArgumentList $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="cb69d-112">Automatikus feladatok az `-AsJob` kapcsolóval</span><span class="sxs-lookup"><span data-stu-id="cb69d-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="cb69d-113">Az Azure PowerShell a kényelem érdekében egyes hosszan futó parancsmagokhoz `-AsJob` kapcsolót is biztosít.</span><span class="sxs-lookup"><span data-stu-id="cb69d-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="cb69d-114">Az `-AsJob` kapcsoló még inkább megkönnyíti a PS-feladatok létrehozását.</span><span class="sxs-lookup"><span data-stu-id="cb69d-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="cb69d-115">A `Get-Job` és a `Get-AzVM` segítségével bármikor ellenőrizheti a feladatot és annak állapotát.</span><span class="sxs-lookup"><span data-stu-id="cb69d-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzVM`.</span></span>

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

<span data-ttu-id="cb69d-116">Ha a feladat befejeződött, a `Receive-Job` használatával lekérheti a feladat eredményét.</span><span class="sxs-lookup"><span data-stu-id="cb69d-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="cb69d-117">A `Receive-Job` úgy adja vissza a parancsmag eredményét, mintha az `-AsJob` jelző nem lenne jelen.</span><span class="sxs-lookup"><span data-stu-id="cb69d-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="cb69d-118">Például a `Do-Action -AsJob` `Receive-Job`-eredménye ugyanaz a típus, mint a `Do-Action` eredménye.</span><span class="sxs-lookup"><span data-stu-id="cb69d-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

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

## <a name="example-scenarios"></a><span data-ttu-id="cb69d-119">Példaforgatókönyvek</span><span class="sxs-lookup"><span data-stu-id="cb69d-119">Example Scenarios</span></span>

<span data-ttu-id="cb69d-120">Több virtuális gép egyszerre történő létrehozása:</span><span class="sxs-lookup"><span data-stu-id="cb69d-120">Create several VMs at once:</span></span>

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

<span data-ttu-id="cb69d-121">Ebben a példában a `Wait-Job` parancsmag felfüggeszti a szkriptet, amíg a feladatok futnak.</span><span class="sxs-lookup"><span data-stu-id="cb69d-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="cb69d-122">A szkript végrehajtása folytatódik, amint az összes feladat befejeződött.</span><span class="sxs-lookup"><span data-stu-id="cb69d-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="cb69d-123">Több feladatot fut párhuzamosan, a szkript pedig megvárja azok befejezését a továbblépés előtt.</span><span class="sxs-lookup"><span data-stu-id="cb69d-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

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
