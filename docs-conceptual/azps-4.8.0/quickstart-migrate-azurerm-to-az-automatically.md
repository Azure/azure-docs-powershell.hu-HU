---
title: PowerShell-szkriptek automatikus migrálása az AzureRM modulból az Az PowerShell-modulba
description: Ismerje meg, hogyan migrálhatók automatikusan a PowerShell-szkriptek az AzureRM modulból az Az PowerShell-modulba
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: 5945b573d467f1ff64e327c52124ffed1e4305aa
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427021"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="5ff72-103">Gyorsútmutató: PowerShell-szkriptek automatikus migrálása az AzureRM modulból az Az PowerShell-modulba</span><span class="sxs-lookup"><span data-stu-id="5ff72-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="5ff72-104">Ez a cikk ismerteti, hogyan lehet az Az.Tools.Migration PowerShell-modul használatával automatikusan frissíteni a PowerShell-szkripteket és -szkriptmodulokat az AzureRM modulból az Az PowerShell-modulba.</span><span class="sxs-lookup"><span data-stu-id="5ff72-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ff72-105">Az Az.Tools.Migration PowerShell-modul jelenleg nyilvános előzetes verzióban érhető el.</span><span class="sxs-lookup"><span data-stu-id="5ff72-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="5ff72-106">Erre az előzetes verzióra nem vonatkozik szolgáltatói szerződés.</span><span class="sxs-lookup"><span data-stu-id="5ff72-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="5ff72-107">Az előzetes verzió használata NEM javasolt éles számítási feladatok esetén.</span><span class="sxs-lookup"><span data-stu-id="5ff72-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="5ff72-108">Előfordulhat, hogy néhány funkció nem támogatott, vagy korlátozott képességekkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="5ff72-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="5ff72-109">További információ: [Kiegészítő használati feltételek a Microsoft Azure előzetes verziójú termékeihez](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span><span class="sxs-lookup"><span data-stu-id="5ff72-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

<span data-ttu-id="5ff72-110">Az Az.Tools.Migration PowerShell-modullal kapcsolatos visszajelzések és problémák bejelentéséhez használja a [GitHub-problémajelentést](https://github.com/Azure/azure-powershell-migration/issues) az `azure-powershell-migration` adattárban.</span><span class="sxs-lookup"><span data-stu-id="5ff72-110">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ff72-111">Követelmények</span><span class="sxs-lookup"><span data-stu-id="5ff72-111">Requirements</span></span>

* <span data-ttu-id="5ff72-112">Frissítse meglévő PowerShell-szkriptjeit az [AzureRM PowerShell-modul legújabb verziójára (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="5ff72-112">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="5ff72-113">Telepítse az Az.Tools.Migration PowerShell-modult.</span><span class="sxs-lookup"><span data-stu-id="5ff72-113">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="5ff72-114">1\. lépés: Egy frissítési terv létrehozása</span><span class="sxs-lookup"><span data-stu-id="5ff72-114">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="5ff72-115">A `New-AzUpgradeModulePlan` parancsmaggal hozzon létre egy frissítési tervet, amellyel migrálhatja szkriptjeit és moduljait az Az PowerShell-modulba.</span><span class="sxs-lookup"><span data-stu-id="5ff72-115">You use the `New-AzUpgradeModulePlan` cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="5ff72-116">A frissítési terv részletezi, hogy melyik fájlt és mely eltolási pontokat kell módosítani az AzureRM-ről az Az PowerShell-parancsmagokra való áttéréskor.</span><span class="sxs-lookup"><span data-stu-id="5ff72-116">The upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

> [!NOTE]
> <span data-ttu-id="5ff72-117">A `New-AzUpgradeModulePlan` parancsmag nem hajtja végre a tervet, csak létrehozza a frissítési lépéseket.</span><span class="sxs-lookup"><span data-stu-id="5ff72-117">The `New-AzUpgradeModulePlan` cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

<span data-ttu-id="5ff72-118">Tekintse át a frissítési terv eredményeit.</span><span class="sxs-lookup"><span data-stu-id="5ff72-118">Review the results of the upgrade plan.</span></span>

```powershell
# Show the entire upgrade plan
$Plan
```

<span data-ttu-id="5ff72-119">Futtassa a következő parancsot, amely kiszűri az eredmények közül azokat a parancsokat, amelyekhez figyelmeztetés vagy hiba tartozik.</span><span class="sxs-lookup"><span data-stu-id="5ff72-119">Run the following command to filter the results to commands that have warnings or errors.</span></span> <span data-ttu-id="5ff72-120">Ez a nagy méretű eredményhalmazok esetében segíthet a hibák gyors azonosításában a frissítés végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="5ff72-120">This may be helpful on large result sets to quickly identify errors before performing the upgrade.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="5ff72-121">2\. lépés: A frissítés végrehajtása</span><span class="sxs-lookup"><span data-stu-id="5ff72-121">Step 2: Perform the upgrade</span></span>

<span data-ttu-id="5ff72-122">A frissítési terv végrehajtásához az `Invoke-AzUpgradeModulePlan` parancsmagot kell futtatni.</span><span class="sxs-lookup"><span data-stu-id="5ff72-122">The upgrade plan is executed when you run the `Invoke-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="5ff72-123">Ez a parancs végrehajtja a megadott fájlok vagy mappák frissítését, kivéve a `New-AzUpgradeModulePlan` parancsmag által azonosított hibák esetében.</span><span class="sxs-lookup"><span data-stu-id="5ff72-123">This command performs an upgrade of the specified file or folders except for any errors that were identified by the `New-AzUpgradeModulePlan` cmdlet.</span></span>

<span data-ttu-id="5ff72-124">Ehhez a parancshoz meg kell adni, hogy a fájlok az eredeti helyükön legyenek-e módosítva, vagy mentse őket új helyre a parancs (az eredeti példányokat pedig hagyja módosítatlanul).</span><span class="sxs-lookup"><span data-stu-id="5ff72-124">This command requires you to specify if the files should be modified in place or if new files should be saved alongside your original files (leaving originals unmodified).</span></span>

> [!CAUTION]
> <span data-ttu-id="5ff72-125">A parancsnak nincs visszavonási művelete.</span><span class="sxs-lookup"><span data-stu-id="5ff72-125">There is no undo operation.</span></span> <span data-ttu-id="5ff72-126">Mindig győződjön meg arról, hogy a frissítendő PowerShell-szkriptek és -modulok esetén rendelkezik biztonsági másolattal.</span><span class="sxs-lookup"><span data-stu-id="5ff72-126">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

> [!WARNING]
> <span data-ttu-id="5ff72-127">Az `Invoke-AzUpgradeModulePlan` parancsmag végleges károkat okozhat, ha meg van adva a `-FileEditMode ModifyExistingFiles` beállítás.</span><span class="sxs-lookup"><span data-stu-id="5ff72-127">The `Invoke-AzUpgradeModulePlan` cmdlet is destructive when the `-FileEditMode ModifyExistingFiles` option is specified!</span></span> <span data-ttu-id="5ff72-128">Ez helyben módosítja a szkripteket és függvényeket a `New-AzUpgradeModulePlan` parancsmag által létrehozott modulfrissítési tervnek megfelelően.</span><span class="sxs-lookup"><span data-stu-id="5ff72-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the `New-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="5ff72-129">A károk megelőzéséhez adja meg ehelyett a `-FileEditMode SaveChangesToNewFiles` beállítást.</span><span class="sxs-lookup"><span data-stu-id="5ff72-129">For the non-destructive option specify `-FileEditMode SaveChangesToNewFiles` instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

<span data-ttu-id="5ff72-130">Tekintse át a frissítési művelet eredményeit.</span><span class="sxs-lookup"><span data-stu-id="5ff72-130">Review the results of the upgrade operation.</span></span>

```powershell
# Show the results for the entire upgrade operation
$Results
```

<span data-ttu-id="5ff72-131">Ha bármilyen hibát kap eredményül, a következő paranccsal kérhet bővebb információkat a hibás eredményekről.</span><span class="sxs-lookup"><span data-stu-id="5ff72-131">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a><span data-ttu-id="5ff72-132">Korlátozások</span><span class="sxs-lookup"><span data-stu-id="5ff72-132">Limitations</span></span>

* <span data-ttu-id="5ff72-133">Az automatizált paraméternév-frissítés nem támogatott a szétterített paraméterkészletek esetében.</span><span class="sxs-lookup"><span data-stu-id="5ff72-133">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="5ff72-134">Ha a parancs ilyet talál a frissítési terv létrehozása közben, akkor egy figyelmeztetést ad vissza.</span><span class="sxs-lookup"><span data-stu-id="5ff72-134">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="5ff72-135">A fájlok írási és olvasási műveletei az alapértelmezett kódolás használatával történnek.</span><span class="sxs-lookup"><span data-stu-id="5ff72-135">File I/O operations use default encoding.</span></span> <span data-ttu-id="5ff72-136">A szokatlan fájlkódolási helyzetek problémákhoz vezethetnek.</span><span class="sxs-lookup"><span data-stu-id="5ff72-136">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="5ff72-137">A rendszer nem észleli az olyan AzureRM-parancsmagokat, amelyek a Pester egységtesztelési utasításaihoz tartozó argumentumokként lettek átadva.</span><span class="sxs-lookup"><span data-stu-id="5ff72-137">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="5ff72-138">Jelenleg kizárólag az Az PowerShell-modul 4.6.1-es verziója támogatott célként.</span><span class="sxs-lookup"><span data-stu-id="5ff72-138">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5ff72-139">Következő lépések</span><span class="sxs-lookup"><span data-stu-id="5ff72-139">Next steps</span></span>

<span data-ttu-id="5ff72-140">Ha többet is meg szeretne tudni az Az PowerShell-modulról, olvassa el [az Azure PowerShell dokumentációját](/powershell/azure/).</span><span class="sxs-lookup"><span data-stu-id="5ff72-140">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>