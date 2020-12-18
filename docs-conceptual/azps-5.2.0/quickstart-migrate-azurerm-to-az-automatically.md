---
title: PowerShell-szkriptek automatikus migrálása az AzureRM modulból az Az PowerShell-modulba
description: Ismerje meg, hogyan migrálhatók automatikusan a PowerShell-szkriptek az AzureRM modulból az Az PowerShell-modulba
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/10/2020
ms.openlocfilehash: 6752fa0376c2f8887511455f56add0859f8961c8
ms.sourcegitcommit: 076ff98abc48e072eb1727532817487bac7507c6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/15/2020
ms.locfileid: "97488529"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="1b6c9-103">Gyorsútmutató: PowerShell-szkriptek automatikus migrálása az AzureRM modulból az Az PowerShell-modulba</span><span class="sxs-lookup"><span data-stu-id="1b6c9-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="1b6c9-104">Ez a cikk ismerteti, hogyan lehet az Az.Tools.Migration PowerShell-modul használatával automatikusan frissíteni a PowerShell-szkripteket és -szkriptmodulokat az AzureRM modulból az Az PowerShell-modulba.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b6c9-105">Az Az.Tools.Migration PowerShell-modul jelenleg nyilvános előzetes verzióban érhető el.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="1b6c9-106">Erre az előzetes verzióra nem vonatkozik szolgáltatói szerződés.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="1b6c9-107">Az előzetes verzió használata NEM javasolt éles számítási feladatok esetén.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="1b6c9-108">Előfordulhat, hogy néhány funkció nem támogatott, vagy korlátozott képességekkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="1b6c9-109">További információ: [Kiegészítő használati feltételek a Microsoft Azure előzetes verziójú termékeihez](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span><span class="sxs-lookup"><span data-stu-id="1b6c9-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b6c9-110">Követelmények</span><span class="sxs-lookup"><span data-stu-id="1b6c9-110">Requirements</span></span>

* <span data-ttu-id="1b6c9-111">Frissítse meglévő PowerShell-szkriptjeit az [AzureRM PowerShell-modul legújabb verziójára (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="1b6c9-111">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="1b6c9-112">Telepítse az Az.Tools.Migration PowerShell-modult.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-112">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="1b6c9-113">1\. lépés: Egy frissítési terv létrehozása</span><span class="sxs-lookup"><span data-stu-id="1b6c9-113">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="1b6c9-114">A **`New-AzUpgradeModulePlan`** parancsmaggal hozzon létre egy frissítési tervet, amellyel migrálhatja szkriptjeit és moduljait az Az PowerShell-modulba.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-114">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="1b6c9-115">A parancsmag nem módosítja a meglévő szkriptjeit.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-115">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="1b6c9-116">Adott szkript kiválasztásához használja a **`FilePath`** paramétert, egy adott mappa összes szkriptjének kiválasztásához pedig a **`DirectoryPath`** paramétert.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-116">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="1b6c9-117">A **`New-AzUpgradeModulePlan`** parancsmag nem hajtja végre a tervet, csak létrehozza a frissítési lépéseket.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-117">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="1b6c9-118">A következő példa a _`C:\Scripts`_ mappában található összes szkripthez hoz létre tervet.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-118">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="1b6c9-119">Az **`OutVariable`** paraméter megadásának eredményeképpen a rendszer visszaadja az eredményeket, és egyidejűleg egy **`Plan`** nevű változóban tárolja el őket.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-119">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="1b6c9-120">Amint az alábbi kimenetben látható, a frissítési terv részletezi, hogy melyik fájlt és mely eltolási pontokat kell módosítani az AzureRM-ről az Az PowerShell-parancsmagokra való áttéréskor.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-120">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

<span data-ttu-id="1b6c9-121">A frissítés elvégzése előtt meg kell tekintenie a problémákra vonatkozó terv eredményeit.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-121">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="1b6c9-122">A következő példa a parancsfájloknak és a parancsfájlok azon elemeinek listáját adja vissza, amelyek megakadályozzák, hogy a rendszer automatikusan frissítse őket.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-122">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="1b6c9-123">A következő kimenetben látható elemek nem frissülnek automatikusan, amíg nem javítja ki manuálisan a problémákat.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-123">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span> <span data-ttu-id="1b6c9-124">Az automatikus frissítést meggátló ismert problémák közé tartoznak a paramétercsomagolást használó parancsok.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-124">Known issues that can’t be upgraded automatically include any commands that use splatting.</span></span>

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="1b6c9-125">2\. lépés: A frissítés végrehajtása</span><span class="sxs-lookup"><span data-stu-id="1b6c9-125">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="1b6c9-126">A parancsnak nincs visszavonási művelete.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-126">There is no undo operation.</span></span> <span data-ttu-id="1b6c9-127">Mindig győződjön meg arról, hogy a frissítendő PowerShell-szkriptek és -modulok esetén rendelkezik biztonsági másolattal.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-127">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="1b6c9-128">Ha elégedett a tervvel, a frissítés az **`Invoke-AzUpgradeModulePlan`** parancsmaggal hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-128">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="1b6c9-129">Az eredeti parancsfájlokon végzett módosítások megakadályozásához a **`SaveChangesToNewFiles`** értéket adja meg a **`FileEditMode`** paraméter értékeként.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-129">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="1b6c9-130">Ha ezt a módot használja, a frissítés során másolat készül a kiválasztott szkriptekről, és a rendszer az _`_az_upgraded`_ karakterláncot fűzi hozzá a fájlnevekhez.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-130">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="1b6c9-131">Az **`Invoke-AzUpgradeModulePlan`** parancsmag végleges károkat okozhat, ha meg van adva a **`-FileEditMode ModifyExistingFiles`** beállítás.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-131">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="1b6c9-132">Ez a parancsmag helyben módosítja a szkripteket és függvényeket a **`New-AzUpgradeModulePlan`** parancsmag által létrehozott modulfrissítési tervnek megfelelően.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-132">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="1b6c9-133">A károk megelőzéséhez adja meg ehelyett a **`-FileEditMode SaveChangesToNewFiles`** beállítást.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-133">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

<span data-ttu-id="1b6c9-134">Ha bármilyen hibát kap eredményül, a következő paranccsal kérhet bővebb információkat a hibás eredményekről.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-134">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a><span data-ttu-id="1b6c9-135">Korlátozások</span><span class="sxs-lookup"><span data-stu-id="1b6c9-135">Limitations</span></span>

* <span data-ttu-id="1b6c9-136">Az automatizált paraméternév-frissítés nem támogatott a szétterített paraméterkészletek esetében.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-136">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="1b6c9-137">Ha a parancs ilyet talál a frissítési terv létrehozása közben, akkor egy figyelmeztetést ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-137">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="1b6c9-138">A fájlok írási és olvasási műveletei az alapértelmezett kódolás használatával történnek.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-138">File I/O operations use default encoding.</span></span> <span data-ttu-id="1b6c9-139">A szokatlan fájlkódolási helyzetek problémákhoz vezethetnek.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-139">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="1b6c9-140">A rendszer nem észleli az olyan AzureRM-parancsmagokat, amelyek a Pester egységtesztelési utasításaihoz tartozó argumentumokként lettek átadva.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-140">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="1b6c9-141">Jelenleg kizárólag az Az PowerShell-modul 4.6.1-es verziója támogatott célként.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-141">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="1b6c9-142">Útmutató a problémák bejelentéséhez</span><span class="sxs-lookup"><span data-stu-id="1b6c9-142">How to report issues</span></span>

<span data-ttu-id="1b6c9-143">Az Az.Tools.Migration PowerShell-modullal kapcsolatos visszajelzések és problémák bejelentéséhez használja a [GitHub-problémajelentést](https://github.com/Azure/azure-powershell-migration/issues) az `azure-powershell-migration` adattárban.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-143">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1b6c9-144">Következő lépések</span><span class="sxs-lookup"><span data-stu-id="1b6c9-144">Next steps</span></span>

<span data-ttu-id="1b6c9-145">Ha többet is meg szeretne tudni az Az PowerShell-modulról, olvassa el [az Azure PowerShell dokumentációját](/powershell/azure/).</span><span class="sxs-lookup"><span data-stu-id="1b6c9-145">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>