---
title: Parancsmagok párhuzamos futtatása PowerShell-feladatok használatával
description: Parancsok párhuzamos futtatása az -AsJob paraméter segítségével.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: beb7f0a89d2e254b348b79daf4f8d3bfdc562de5
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534223"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="53bcc-103">Parancsmagok párhuzamos futtatása PowerShell-feladatok használatával</span><span class="sxs-lookup"><span data-stu-id="53bcc-103">Running cmdlets in parallel using PowerShell jobs</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="53bcc-104">A PowerShell a [PowerShell-feladatok](/powershell/module/microsoft.powershell.core/about/about_jobs) révén támogatja az aszinkron műveleteket.</span><span class="sxs-lookup"><span data-stu-id="53bcc-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="53bcc-105">Az Azure PowerShell működése nagymértékben függ az Azure-hoz intézett hálózati hívások létrehozásától és a rájuk való várakozástól.</span><span class="sxs-lookup"><span data-stu-id="53bcc-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="53bcc-106">Gyakran lehet szüksége nem blokkoló hívás kezdeményezésére.</span><span class="sxs-lookup"><span data-stu-id="53bcc-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="53bcc-107">Az Azure PowerShell első osztályú [PS-feladattámogatást](/powershell/module/microsoft.powershell.core/about/about_jobs) biztosít ezen igény kielégítése céljából.</span><span class="sxs-lookup"><span data-stu-id="53bcc-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="53bcc-108">Környezetmegőrzés és PS-feladatok</span><span class="sxs-lookup"><span data-stu-id="53bcc-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="53bcc-109">A PS-feladatok külön folyamatokként futnak, ezért az Azure-kapcsolatát meg kell osztania azokkal.</span><span class="sxs-lookup"><span data-stu-id="53bcc-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="53bcc-110">Miután a `Connect-AzureRmAccount` használatával bejelentkezett Azure-fiókjába, a környezetet átadhatja egy feladatnak.</span><span class="sxs-lookup"><span data-stu-id="53bcc-110">After signing in to your Azure account with `Connect-AzureRmAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="53bcc-111">Ha azonban a környezet az `Enable-AzureRmContextAutosave` használatával történő automatikus mentését választotta, a környezet minden létrehozott feladattal automatikusan meg lesz osztva.</span><span class="sxs-lookup"><span data-stu-id="53bcc-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="53bcc-112">Automatikus feladatok az `-AsJob` kapcsolóval</span><span class="sxs-lookup"><span data-stu-id="53bcc-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="53bcc-113">Az Azure PowerShell a kényelem érdekében egyes hosszan futó parancsmagokhoz `-AsJob` kapcsolót is biztosít.</span><span class="sxs-lookup"><span data-stu-id="53bcc-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="53bcc-114">Az `-AsJob` kapcsoló még inkább megkönnyíti a PS-feladatok létrehozását.</span><span class="sxs-lookup"><span data-stu-id="53bcc-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="53bcc-115">A `Get-Job` és a `Get-AzureRmVM` segítségével bármikor ellenőrizheti a feladatot és annak állapotát.</span><span class="sxs-lookup"><span data-stu-id="53bcc-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

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

<span data-ttu-id="53bcc-116">Ha a feladat befejeződött, a `Receive-Job` használatával lekérheti a feladat eredményét.</span><span class="sxs-lookup"><span data-stu-id="53bcc-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="53bcc-117">A `Receive-Job` úgy adja vissza a parancsmag eredményét, mintha az `-AsJob` jelző nem lenne jelen.</span><span class="sxs-lookup"><span data-stu-id="53bcc-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="53bcc-118">Például a `Do-Action -AsJob``Receive-Job`-eredménye ugyanaz a típus, mint a `Do-Action` eredménye.</span><span class="sxs-lookup"><span data-stu-id="53bcc-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

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

## <a name="example-scenarios"></a><span data-ttu-id="53bcc-119">Példaforgatókönyvek</span><span class="sxs-lookup"><span data-stu-id="53bcc-119">Example Scenarios</span></span>

<span data-ttu-id="53bcc-120">Több virtuális gép egyszerre történő létrehozása:</span><span class="sxs-lookup"><span data-stu-id="53bcc-120">Create several VMs at once:</span></span>

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

<span data-ttu-id="53bcc-121">Ebben a példában a `Wait-Job` parancsmag felfüggeszti a szkriptet, amíg a feladatok futnak.</span><span class="sxs-lookup"><span data-stu-id="53bcc-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="53bcc-122">A szkript végrehajtása folytatódik, amint az összes feladat befejeződött.</span><span class="sxs-lookup"><span data-stu-id="53bcc-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="53bcc-123">Több feladatot fut párhuzamosan, a szkript pedig megvárja azok befejezését a továbblépés előtt.</span><span class="sxs-lookup"><span data-stu-id="53bcc-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

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
