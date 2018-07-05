---
title: Parancsmagok párhuzamos futtatása PowerShell-feladatok használatával
description: Parancsok párhuzamos futtatása az -AsJob paraméter segítségével.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: a986824d952ccf6cd52dc86418899f3805a38973
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406530"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="a632f-103">Parancsmagok párhuzamos futtatása PowerShell-feladatok használatával</span><span class="sxs-lookup"><span data-stu-id="a632f-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="a632f-104">A PowerShell a [PowerShell-feladatok](/powershell/module/microsoft.powershell.core/about/about_jobs) révén támogatja az aszinkron műveleteket.</span><span class="sxs-lookup"><span data-stu-id="a632f-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="a632f-105">Az Azure PowerShell működése nagymértékben függ az Azure-hoz intézett hálózati hívások létrehozásától és a rájuk való várakozástól.</span><span class="sxs-lookup"><span data-stu-id="a632f-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="a632f-106">A fejlesztők munkája során gyakran előfordul, hogy több, nem blokkoló hívást szeretnének intézni az Azure-hoz egy szkripten belül, vagy az aktuális munkamenet blokkolása nélkül szeretnének Azure-erőforrásokat létrehozni az REPL-ben.</span><span class="sxs-lookup"><span data-stu-id="a632f-106">As a developer, you may often find yourself looking to make multiple non-blocking calls to Azure in a script, or you may find that you want to create Azure resources in the REPL without blocking the current session.</span></span> <span data-ttu-id="a632f-107">Az Azure PowerShell első osztályú [PS-feladattámogatást](/powershell/module/microsoft.powershell.core/about/about_jobs) biztosít ezen igények kielégítése céljából.</span><span class="sxs-lookup"><span data-stu-id="a632f-107">To address these needs, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="a632f-108">Környezetmegőrzés és PS-feladatok</span><span class="sxs-lookup"><span data-stu-id="a632f-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="a632f-109">A PS-feladatok külön folyamatokban futnak, ezért az Azure-kapcsolatára vonatkozó információkat megfelelően meg kell osztani a létrehozott feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="a632f-109">PSJobs are run in separate processes, which means that information about your Azure connection must be properly shared with the jobs you create.</span></span> <span data-ttu-id="a632f-110">Amikor az Azure-fiókját csatlakoztatja a PowerShell-munkamenetéhez a `Connect-AzureRmAccount` használatával, a környezetet átadhatja egy feladatnak.</span><span class="sxs-lookup"><span data-stu-id="a632f-110">Upon connecting your Azure account to your PowerShell session with `Connect-AzureRmAccount`, you can pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="a632f-111">Ha azonban a környezet az `Enable-AzureRmContextAutosave` használatával történő automatikus mentését választotta, a környezet minden létrehozott feladattal automatikusan meg lesz osztva.</span><span class="sxs-lookup"><span data-stu-id="a632f-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="a632f-112">Automatikus feladatok az `-AsJob` kapcsolóval</span><span class="sxs-lookup"><span data-stu-id="a632f-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="a632f-113">Az Azure PowerShell a kényelem érdekében egyes hosszan futó parancsmagokhoz `-AsJob` kapcsolót is biztosít.</span><span class="sxs-lookup"><span data-stu-id="a632f-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="a632f-114">Az `-AsJob` kapcsoló még inkább megkönnyíti a PS-feladatok létrehozását.</span><span class="sxs-lookup"><span data-stu-id="a632f-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="a632f-115">A `Get-Job` és a `Get-AzureRmVM` segítségével bármikor ellenőrizheti a feladatot és annak állapotát.</span><span class="sxs-lookup"><span data-stu-id="a632f-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

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

<span data-ttu-id="a632f-116">Ezt követően, ha a feladat befejeződött, a `Receive-Job` használatával lekérheti a feladat eredményét.</span><span class="sxs-lookup"><span data-stu-id="a632f-116">Subsequently, upon completion, you can obtain the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="a632f-117">A `Receive-Job` úgy adja vissza a parancsmag eredményét, mintha az `-AsJob` jelző nem lenne jelen.</span><span class="sxs-lookup"><span data-stu-id="a632f-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="a632f-118">Például a `Do-Action -AsJob` `Receive-Job`-eredménye ugyanaz a típus, mint a `Do-Action` eredménye.</span><span class="sxs-lookup"><span data-stu-id="a632f-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

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

## <a name="example-scenarios"></a><span data-ttu-id="a632f-119">Példaforgatókönyvek</span><span class="sxs-lookup"><span data-stu-id="a632f-119">Example Scenarios</span></span>

<span data-ttu-id="a632f-120">Több virtuális gép egyszerre történő létrehozása.</span><span class="sxs-lookup"><span data-stu-id="a632f-120">Create multiple VMs at once.</span></span>

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

<span data-ttu-id="a632f-121">Ebben a példában a `Wait-Job` parancsmag felfüggeszti a szkriptet, amíg a feladatok futnak.</span><span class="sxs-lookup"><span data-stu-id="a632f-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="a632f-122">A szkript végrehajtása folytatódik, amint az összes feladat befejeződött.</span><span class="sxs-lookup"><span data-stu-id="a632f-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="a632f-123">Ez lehetővé teszi, hogy több, párhuzamosan futó feladatot hozzon létre, majd megvárja azok befejezését a továbblépés előtt.</span><span class="sxs-lookup"><span data-stu-id="a632f-123">This allows you to create several jobs running in parallel then wait for completion before continuing.</span></span>

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
