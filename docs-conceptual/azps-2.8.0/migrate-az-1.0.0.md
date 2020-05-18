---
title: Az AzureRM és az Azure PowerShell Az 1.0.0 közötti összes változás
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 1-es verziójában található kompatibilitástörő változások listáját.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: e5121d61b0f5f68ff3e1f33d774e3533adfeb64f
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "75035778"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="6225d-103">Az Az 1.0.0 kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="6225d-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="6225d-104">Ez a dokumentum részletes információkat tartalmaz az AzureRM 6.x és az új Az modul 1.x és újabb verziója közötti változásokról.</span><span class="sxs-lookup"><span data-stu-id="6225d-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="6225d-105">A tartalomjegyzék végigvezeti a teljes migrálási folyamaton, és bemutatja a modulspecifikus módosításokat is, amelyek befolyásolhatják a szkripteket.</span><span class="sxs-lookup"><span data-stu-id="6225d-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="6225d-106">Az AzureRM-ből az Az-be történő migrálás megkezdéséhez kapcsolódó általános tanácsokért lásd: [Migrálás megkezdése az AzureRM-ből az Az-be](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="6225d-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6225d-107">Az Az 1.0.0-s és az Az 2.0.0-s verziója között is történtek kompatibilitástörő változások.</span><span class="sxs-lookup"><span data-stu-id="6225d-107">There have been breaking changes between Az 1.0.0 and Az 2.0.0 as well.</span></span> <span data-ttu-id="6225d-108">Az AzureRM-ről Az-re való frissítést ismertető útmutató követése után tekintse meg az [Az 2.0.0 kompatibilitástörő változásait](migrate-az-2.0.0.md) bemutató cikket, amelyből megtudhatja, kell-e további módosításokat végeznie.</span><span class="sxs-lookup"><span data-stu-id="6225d-108">After following this guide for updating from AzureRM to Az, see the [Az 2.0.0 breaking changes](migrate-az-2.0.0.md) to find out if you need to make additional changes.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="6225d-109">Tartalomjegyzék</span><span class="sxs-lookup"><span data-stu-id="6225d-109">Table of Contents</span></span>

- [<span data-ttu-id="6225d-110">Általános kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="6225d-110">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="6225d-111">A parancsmag főnévi előtagjának változásai</span><span class="sxs-lookup"><span data-stu-id="6225d-111">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="6225d-112">A modul nevének változásai</span><span class="sxs-lookup"><span data-stu-id="6225d-112">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="6225d-113">Eltávolított modulok</span><span class="sxs-lookup"><span data-stu-id="6225d-113">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="6225d-114">Windows PowerShell 5.1 és .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="6225d-114">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="6225d-115">A felhasználói bejelentkezés ideiglenes eltávolítása a PSCredential használatával</span><span class="sxs-lookup"><span data-stu-id="6225d-115">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="6225d-116">Bejelentkezés alapértelmezett eszközkóddal a webböngészőben megjelenő kérdés helyett</span><span class="sxs-lookup"><span data-stu-id="6225d-116">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="6225d-117">A modul kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="6225d-117">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="6225d-118">Az.ApiManagement (korábban AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="6225d-118">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="6225d-119">Az.Billing (korábban AzureRM.Billing, AzureRM.Consumption és AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="6225d-119">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="6225d-120">Az.CognitiveServices (korábban AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="6225d-120">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="6225d-121">Az.Compute (korábban AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="6225d-121">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="6225d-122">Az.DataFactory (korábban AzureRM.DataFactories és AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="6225d-122">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="6225d-123">Az.DataLakeAnalytics (korábban AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="6225d-123">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="6225d-124">Az.DataLakeStore (korábban AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="6225d-124">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="6225d-125">Az.KeyVault (korábban AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="6225d-125">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="6225d-126">Az.Media (korábban AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="6225d-126">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="6225d-127">Az.Monitor (korábban AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="6225d-127">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="6225d-128">Az.Network (korábban AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="6225d-128">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="6225d-129">Az.OperationalInsights (korábban AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="6225d-129">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="6225d-130">Az.RecoveryServices (korábban AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup és AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="6225d-130">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="6225d-131">Az.Resources (korábban AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="6225d-131">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="6225d-132">Az.ServiceFabric (korábban AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="6225d-132">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="6225d-133">Az.Sql (korábban AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="6225d-133">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="6225d-134">Az.Storage (korábban Azure.Storage és AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="6225d-134">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="6225d-135">Az.Websites (korábban AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="6225d-135">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="6225d-136">Általános kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="6225d-136">General breaking changes</span></span>

<span data-ttu-id="6225d-137">Ez a szakasz részletesen bemutatja az Az modul újratervezésének részét képező általános kompatibilitástörő változásokat.</span><span class="sxs-lookup"><span data-stu-id="6225d-137">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="6225d-138">A parancsmag főnévi előtagjának változásai</span><span class="sxs-lookup"><span data-stu-id="6225d-138">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="6225d-139">Az AzureRM modulban a parancsmagok az `AzureRM` vagy az `Azure` főnévi előtagot használták.</span><span class="sxs-lookup"><span data-stu-id="6225d-139">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="6225d-140">Az Az egyszerűsíti és normalizálja a parancsmagok nevét, így minden parancsmag főnévi előtagja „Az” lesz.</span><span class="sxs-lookup"><span data-stu-id="6225d-140">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="6225d-141">Például:</span><span class="sxs-lookup"><span data-stu-id="6225d-141">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="6225d-142">A következőre módosult:</span><span class="sxs-lookup"><span data-stu-id="6225d-142">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="6225d-143">Az új parancsmagokra való áttérés megkönnyítése érdekében az Az két új parancsmagot vezet be: [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) és [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="6225d-143">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="6225d-144">Az `Enable-AzureRmAlias` a régebbi parancsmagok nevéhez hoz létre aliasokat az AzureRM-ben, amelyek az újabb Az-parancsmagok nevének felelnek meg.</span><span class="sxs-lookup"><span data-stu-id="6225d-144">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="6225d-145">A `-Scope` argumentum és az `Enable-AzureRmAlias` együttes használatával kiválaszthatja, hol legyenek engedélyezve az aliasok.</span><span class="sxs-lookup"><span data-stu-id="6225d-145">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="6225d-146">A következő AzureRM-szkript például:</span><span class="sxs-lookup"><span data-stu-id="6225d-146">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="6225d-147">Az `Enable-AzureRmAlias` használatával minimális változtatásokkal futtatható:</span><span class="sxs-lookup"><span data-stu-id="6225d-147">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="6225d-148">Az `Enable-AzureRmAlias -Scope CurrentUser` futtatása engedélyezi az aliasokat az összes megnyitott PowerShell-munkamenetben, így a parancsmag végrehajtása után az ehhez hasonló szkripteket egyáltalán nem kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6225d-148">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="6225d-149">A parancsmagok aliasaival kapcsolatos részletes információért tekintse meg az [Enable-AzureRmAlias referenciáját](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="6225d-149">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="6225d-150">Amikor készen áll az aliasok letiltására, a `Disable-AzureRmAlias` eltávolítja a létrehozott aliasokat.</span><span class="sxs-lookup"><span data-stu-id="6225d-150">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="6225d-151">Részletes információért tekintse meg a [Disable-AzureRmAlias referenciáját](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="6225d-151">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6225d-152">Az aliasok letiltásakor győződjön meg arról, hogy _minden_ olyan hatókörnél le lettek tiltva, amelyekhez engedélyezve voltak az aliasok.</span><span class="sxs-lookup"><span data-stu-id="6225d-152">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="6225d-153">A modul nevének változásai</span><span class="sxs-lookup"><span data-stu-id="6225d-153">Module Name Changes</span></span>

<span data-ttu-id="6225d-154">A modul neve a korábbi `AzureRM.*` helyett `Az.*` lett, kivéve a következő modulokban:</span><span class="sxs-lookup"><span data-stu-id="6225d-154">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="6225d-155">AzureRM modul</span><span class="sxs-lookup"><span data-stu-id="6225d-155">AzureRM module</span></span> | <span data-ttu-id="6225d-156">Az modul</span><span class="sxs-lookup"><span data-stu-id="6225d-156">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="6225d-157">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6225d-157">Azure.Storage</span></span> | <span data-ttu-id="6225d-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6225d-158">Az.Storage</span></span> |
| <span data-ttu-id="6225d-159">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6225d-159">Azure.AnalysisServices</span></span> | <span data-ttu-id="6225d-160">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6225d-160">Az.AnalysisServices</span></span> |
| <span data-ttu-id="6225d-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6225d-161">AzureRM.Profile</span></span> | <span data-ttu-id="6225d-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6225d-162">Az.Accounts</span></span> |
| <span data-ttu-id="6225d-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6225d-163">AzureRM.Insights</span></span> | <span data-ttu-id="6225d-164">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6225d-164">Az.Monitor</span></span> |
| <span data-ttu-id="6225d-165">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="6225d-165">AzureRM.DataFactories</span></span> | <span data-ttu-id="6225d-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6225d-166">Az.DataFactory</span></span> |
| <span data-ttu-id="6225d-167">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6225d-167">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="6225d-168">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6225d-168">Az.DataFactory</span></span> |
| <span data-ttu-id="6225d-169">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6225d-169">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="6225d-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6225d-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="6225d-171">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6225d-171">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="6225d-172">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6225d-172">Az.RecoveryServices</span></span> |
| <span data-ttu-id="6225d-173">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6225d-173">AzureRM.Tags</span></span> | <span data-ttu-id="6225d-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6225d-174">Az.Resources</span></span> |
| <span data-ttu-id="6225d-175">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6225d-175">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="6225d-176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6225d-176">Az.MachineLearning</span></span> |
| <span data-ttu-id="6225d-177">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="6225d-177">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="6225d-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6225d-178">Az.Billing</span></span> |
| <span data-ttu-id="6225d-179">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6225d-179">AzureRM.Consumption</span></span> | <span data-ttu-id="6225d-180">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6225d-180">Az.Billing</span></span> |

<span data-ttu-id="6225d-181">A modul nevének változása azt jelenti, hogy ha egy szkript a `#Requires` vagy az `Import-Module` használatával tölt be bizonyos modulokat, módosításokat kell végezni az új modul használatához.</span><span class="sxs-lookup"><span data-stu-id="6225d-181">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="6225d-182">Azoknál a moduloknál, ahol a parancsmag utótagja nem változott, ez azt jelenti, hogy a modul neve megváltozott, a művelet helyét jelző utótag viszont _nem_.</span><span class="sxs-lookup"><span data-stu-id="6225d-182">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="6225d-183">#Requires és Import-Module utasítások migrálása</span><span class="sxs-lookup"><span data-stu-id="6225d-183">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="6225d-184">Ha egy szkript `#Requires` vagy `Import-Module` használatával deklarálja egy AzureRM-modultól való függőségét, akkor frissíteni kell az új modulnevek használatára.</span><span class="sxs-lookup"><span data-stu-id="6225d-184">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="6225d-185">Például:</span><span class="sxs-lookup"><span data-stu-id="6225d-185">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="6225d-186">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6225d-186">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="6225d-187">`Import-Module` esetében:</span><span class="sxs-lookup"><span data-stu-id="6225d-187">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="6225d-188">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6225d-188">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="6225d-189">Teljesen minősített parancsmaghívások migrálása</span><span class="sxs-lookup"><span data-stu-id="6225d-189">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="6225d-190">Modulhoz minősített parancsmaghívásokat használó szkriptek, például:</span><span class="sxs-lookup"><span data-stu-id="6225d-190">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="6225d-191">Úgy kell módosítani, hogy az új modul- és parancsmagneveket használja:</span><span class="sxs-lookup"><span data-stu-id="6225d-191">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="6225d-192">Moduljegyzék-függőségek migrálása</span><span class="sxs-lookup"><span data-stu-id="6225d-192">Migrating module manifest dependencies</span></span>

<span data-ttu-id="6225d-193">Amennyiben egy modul AzureRM-modultól való függését egy moduljegyzék (.psd1) fájl fejezi ki, a modul `RequiredModules` szakaszában frissíteni kell a modulok nevét:</span><span class="sxs-lookup"><span data-stu-id="6225d-193">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="6225d-194">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6225d-194">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="6225d-195">Eltávolított modulok</span><span class="sxs-lookup"><span data-stu-id="6225d-195">Removed modules</span></span>

<span data-ttu-id="6225d-196">Az alábbi modulok lettek eltávolítva:</span><span class="sxs-lookup"><span data-stu-id="6225d-196">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="6225d-197">E szolgáltatások eszközeit már nem támogatja aktívan a rendszer.</span><span class="sxs-lookup"><span data-stu-id="6225d-197">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="6225d-198">Azt javasoljuk ügyfeleinknek, hogy amint lehetséges, térjenek át más szolgáltatások használatára.</span><span class="sxs-lookup"><span data-stu-id="6225d-198">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="6225d-199">Windows PowerShell 5.1 és .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="6225d-199">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="6225d-200">Az Az Windows PowerShell 5.1-gyel történő használatához szükséges a .NET-keretrendszer 4.7.2 telepítése.</span><span class="sxs-lookup"><span data-stu-id="6225d-200">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="6225d-201">A PowerShell Core 6.x vagy újabb verziójának használatához nincs szükség a .NET-keretrendszerre.</span><span class="sxs-lookup"><span data-stu-id="6225d-201">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="6225d-202">A felhasználói bejelentkezés ideiglenes eltávolítása a PSCredential használatával</span><span class="sxs-lookup"><span data-stu-id="6225d-202">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="6225d-203">A .NET Standard hitelesítési folyamatának változásai miatt ideiglenesen eltávolítjuk a PSCredential használatával történő felhasználói bejelentkezés lehetőségét.</span><span class="sxs-lookup"><span data-stu-id="6225d-203">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="6225d-204">A funkció a Windows PowerShell 5.1 2019. január 15-én megjelenő verziójában válik ismét elérhetővé.</span><span class="sxs-lookup"><span data-stu-id="6225d-204">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="6225d-205">Erről részletesen [ebben a GitHub-cikkben](https://github.com/Azure/azure-powershell/issues/7430) olvashat.</span><span class="sxs-lookup"><span data-stu-id="6225d-205">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="6225d-206">Bejelentkezés alapértelmezett eszközkóddal a webböngészőben megjelenő kérdés helyett</span><span class="sxs-lookup"><span data-stu-id="6225d-206">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="6225d-207">A .NET Standard hitelesítési folyamatának változásai miatt az interaktív bejelentkezések során az eszközről történő bejelentkezés lesz az alapértelmezett bejelentkezési folyamat.</span><span class="sxs-lookup"><span data-stu-id="6225d-207">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="6225d-208">A webböngésző-alapú bejelentkezés a Windows PowerShell 5.1 2019. január 15-én megjelenő verziójában válik ismét elérhetővé.</span><span class="sxs-lookup"><span data-stu-id="6225d-208">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="6225d-209">Ezt követően a felhasználók a Switch paramétert használva választhatják az eszközről történő bejelentkezést.</span><span class="sxs-lookup"><span data-stu-id="6225d-209">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="6225d-210">A modul kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="6225d-210">Module breaking changes</span></span>

<span data-ttu-id="6225d-211">Ez a szakasz részletesen bemutatja az egyes modulok és parancsmagok kompatibilitástörő változásait.</span><span class="sxs-lookup"><span data-stu-id="6225d-211">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="6225d-212">Az.ApiManagement (korábban AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="6225d-212">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="6225d-213">A következő parancsmagok lettek eltávolítva:</span><span class="sxs-lookup"><span data-stu-id="6225d-213">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="6225d-214">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6225d-214">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="6225d-215">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6225d-215">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="6225d-216">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6225d-216">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="6225d-217">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6225d-217">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="6225d-218">Ezeket a tulajdonságokat mostantól a **Set-AzApiManagement** parancsmaggal kell beállítani</span><span class="sxs-lookup"><span data-stu-id="6225d-218">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="6225d-219">A következő tulajdonságok lettek eltávolítva:</span><span class="sxs-lookup"><span data-stu-id="6225d-219">Removed the following properties:</span></span>
  - <span data-ttu-id="6225d-220">A `PsApiManagementHostnameConfiguration` típus `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` és `ScmHostnameConfiguration` tulajdonsága el lett távolítva a `PsApiManagementContext`ből.</span><span class="sxs-lookup"><span data-stu-id="6225d-220">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="6225d-221">Ezek helyett a `PsApiManagementCustomHostNameConfiguration` típus `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` és `ScmCustomHostnameConfiguration` tulajdonságát használja.</span><span class="sxs-lookup"><span data-stu-id="6225d-221">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="6225d-222">A `StaticIPs` tulajdonság el lett távolítva a PsApiManagementContextből.</span><span class="sxs-lookup"><span data-stu-id="6225d-222">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="6225d-223">Két új tulajdonságra lett osztva: ez a `PublicIPAddresses` és a `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="6225d-223">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="6225d-224">A kötelező `Location` tulajdonság el lett távolítva a New-AzureApiManagementVirtualNetwork parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="6225d-224">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="6225d-225">Az.Billing (korábban AzureRM.Billing, AzureRM.Consumption és AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="6225d-225">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="6225d-226">A `Get-AzConsumptionUsageDetail` parancsmag `InvoiceName` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-226">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="6225d-227">A szkripteknek a számlák készítéséhez más identitásparamétereket kell használniuk.</span><span class="sxs-lookup"><span data-stu-id="6225d-227">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="6225d-228">Az.CognitiveServices (korábban AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="6225d-228">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="6225d-229">A `Get-AzCognitiveServicesAccountSkus` parancsmag `GetSkusWithAccountParamSetName` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-229">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="6225d-230">A termékváltozatokat a fiók típusa és helye alapján lehet lekérdezni a ResourceGroupName és a fiók nevének használata helyett.</span><span class="sxs-lookup"><span data-stu-id="6225d-230">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="6225d-231">Az.Compute (korábban AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="6225d-231">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="6225d-232">A `PSVirtualMachine` és `PSVirtualMachineScaleSet` objektum `Identity` tulajdonsága mostantól nem tartalmazza az `IdentityIds` azonosítókat. A szkriptek a jövőben nem veszik figyelembe a mező értékét a feldolgozási döntések során.</span><span class="sxs-lookup"><span data-stu-id="6225d-232">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="6225d-233">A `PSVirtualMachineScaleSetVM` objektum `InstanceView` tulajdonságának típusa `VirtualMachineInstanceView` helyett `VirtualMachineScaleSetVMInstanceView` lett.</span><span class="sxs-lookup"><span data-stu-id="6225d-233">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="6225d-234">Az `UpgradePolicy` tulajdonság `AutoOSUpgradePolicy` és `AutomaticOSUpgrade` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-234">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="6225d-235">A `PSSnapshotUpdate` objektum `Sku` tulajdonságának típusa `DiskSku` helyett `SnapshotSku` lett.</span><span class="sxs-lookup"><span data-stu-id="6225d-235">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="6225d-236">A `VmScaleSetVMParameterSet` el lett távolítva az `Add-AzVMDataDisk` parancsmagból, mostantól nem lehet önálló adatlemezt hozzáadni egy ScaleSet-virtuálisgéphez.</span><span class="sxs-lookup"><span data-stu-id="6225d-236">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="6225d-237">Az.DataFactory (korábban AzureRM.DataFactories és AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="6225d-237">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="6225d-238">A `New-AzDataFactoryEncryptValue` parancsmagban kötelezővé vált a `GatewayName` paraméter használata.</span><span class="sxs-lookup"><span data-stu-id="6225d-238">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="6225d-239">A `New-AzDataFactoryGatewayKey` parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-239">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="6225d-240">A `Get-AzDataFactoryV2ActivityRun` parancsmag `LinkedServiceName` paramétere el lett távolítva. A szkriptek a jövőben nem veszik figyelembe a mező értékét a feldolgozási döntések során.</span><span class="sxs-lookup"><span data-stu-id="6225d-240">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="6225d-241">Az.DataLakeAnalytics (korábban AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="6225d-241">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="6225d-242">El lettek távolítva a következő elavult parancsmagok: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, és `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="6225d-242">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="6225d-243">Az.DataLakeStore (korábban AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="6225d-243">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="6225d-244">A következő parancsmagok `Encoding` paraméterének típusa `FileSystemCmdletProviderEncoding` helyett `System.Text.Encoding` lett.</span><span class="sxs-lookup"><span data-stu-id="6225d-244">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="6225d-245">Ez a módosítás eltávolítja a `String` és `Oem` kódolási értéket.</span><span class="sxs-lookup"><span data-stu-id="6225d-245">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="6225d-246">Az összes egyéb korábbi kódolási érték elérhető marad.</span><span class="sxs-lookup"><span data-stu-id="6225d-246">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="6225d-247">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6225d-247">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="6225d-248">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6225d-248">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="6225d-249">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6225d-249">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="6225d-250">A `New-AzDataLakeStoreAccount` és `Set-AzDataLakeStoreAccount` parancsmag elavult `Tags` tulajdonságaliasa el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-250">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="6225d-251">A következőt használó szkripteket:</span><span class="sxs-lookup"><span data-stu-id="6225d-251">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="6225d-252">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6225d-252">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="6225d-253">A `PSDataLakeStoreAccountBasic` objektum elavult tulajdonságai el lettek távolítva: `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier` és `FirewallAllowAzureIps`.</span><span class="sxs-lookup"><span data-stu-id="6225d-253">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="6225d-254">A `Get-AzDataLakeStoreAccount` által visszaadott `PSDatalakeStoreAccount` értéket használó szkriptek nem hivatkozhatnak ezekre a tulajdonságokra.</span><span class="sxs-lookup"><span data-stu-id="6225d-254">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="6225d-255">Az.KeyVault (korábban AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="6225d-255">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="6225d-256">A `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` és `PSKeyVaultSecretAttributes` objektum `PurgeDisabled` tulajdonsága el lett távolítva. A szkriptek a jövőben nem hivatkozhatnak a ```PurgeDisabled``` tulajdonságra a feldolgozási döntések során.</span><span class="sxs-lookup"><span data-stu-id="6225d-256">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="6225d-257">Az.Media (korábban AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="6225d-257">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="6225d-258">A `New-AzMediaService` parancsmag elavult `Tags` tulajdonságaliasa el lett távolítva. A következőt használó szkripteket:</span><span class="sxs-lookup"><span data-stu-id="6225d-258">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="6225d-259">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6225d-259">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="6225d-260">Az.Monitor (korábban AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="6225d-260">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="6225d-261">A `Categories` és a `Timegrains` többes számú paraméternév el lett távolítva. Ezek helyett a `Set-AzDiagnosticSetting` parancsmag egyes számú paraméterneveit kell használni. A következőt használó szkripteket:</span><span class="sxs-lookup"><span data-stu-id="6225d-261">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="6225d-262">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6225d-262">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="6225d-263">Az.Network (korábban AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="6225d-263">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="6225d-264">A `Get-AzServiceEndpointPolicyDefinition` parancsmag elavult `ResourceId` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-264">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="6225d-265">A `PSVirtualNetwork` objektum elavult `EnableVmProtection` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-265">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="6225d-266">Az elavult `Set-AzVirtualNetworkGatewayVpnClientConfig` parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-266">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="6225d-267">A szkriptek a jövőben nem hozhatnak feldolgozási döntéseket e mezők értéke alapján.</span><span class="sxs-lookup"><span data-stu-id="6225d-267">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="6225d-268">Az.OperationalInsights (korábban AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="6225d-268">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="6225d-269">A `Get-AzOperationalInsightsDataSource` alapértelmezett paraméterkészlete el lett távolítva. Mostantól a `ByWorkspaceNameByKind` az alapértelmezett paraméterkészlet.</span><span class="sxs-lookup"><span data-stu-id="6225d-269">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="6225d-270">Azokat a szkripteket, amelyek a következő használatával listázták az adatforrásokat:</span><span class="sxs-lookup"><span data-stu-id="6225d-270">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="6225d-271">Úgy kell módosítani, hogy megadjanak egy altípust:</span><span class="sxs-lookup"><span data-stu-id="6225d-271">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="6225d-272">Az.RecoveryServices (korábban AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup és AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="6225d-272">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="6225d-273">A `New/Set-AzRecoveryServicesAsrPolicy` parancsmag `Encryption` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-273">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="6225d-274">A `TargetStorageAccountName` paraméter megadása mostantól kötelező a `Restore-AzRecoveryServicesBackupItem` parancsmag felügyeltlemez-visszaállítási műveleteihez.</span><span class="sxs-lookup"><span data-stu-id="6225d-274">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="6225d-275">A `Restore-AzRecoveryServicesBackupItem` parancsmag `StorageAccountName` és `StorageAccountResourceGroupName` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-275">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="6225d-276">A `Get-AzRecoveryServicesBackupContainer` parancsmag `Name` paramétere el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="6225d-276">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="6225d-277">Az.Resources (korábban AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="6225d-277">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="6225d-278">A `New/Set-AzPolicyAssignment` parancsmag `Sku` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-278">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="6225d-279">A `New-AzADServicePrincipal` és `New-AzADSpCredential` parancsmag `Password` paramétere el lett távolítva. A jelszavak létrehozása automatikusan történik, a korábban jelszót biztosító szkripteket:</span><span class="sxs-lookup"><span data-stu-id="6225d-279">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="6225d-280">Úgy kell módosítani, hogy a kimenetből kérjék le a jelszót:</span><span class="sxs-lookup"><span data-stu-id="6225d-280">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="6225d-281">Az.ServiceFabric (korábban AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="6225d-281">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="6225d-282">Módosítottuk a következő parancsmag visszatérési típusait:</span><span class="sxs-lookup"><span data-stu-id="6225d-282">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="6225d-283">Az `ApplicationHealthPolicy` típus `ServiceTypeHealthPolicies` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-283">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="6225d-284">Az `ClusterUpgradeDeltaHealthPolicy` típus `ApplicationHealthPolicies` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-284">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="6225d-285">Az `ClusterUpgradePolicy` típus `OverrideUserUpgradePolicy` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-285">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="6225d-286">Ezek a módosítások a következő parancsmagokat érintik:</span><span class="sxs-lookup"><span data-stu-id="6225d-286">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="6225d-287">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6225d-287">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="6225d-288">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6225d-288">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="6225d-289">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6225d-289">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="6225d-290">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6225d-290">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="6225d-291">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6225d-291">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="6225d-292">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6225d-292">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="6225d-293">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6225d-293">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="6225d-294">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6225d-294">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="6225d-295">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6225d-295">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="6225d-296">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6225d-296">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="6225d-297">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6225d-297">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="6225d-298">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="6225d-298">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="6225d-299">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="6225d-299">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="6225d-300">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="6225d-300">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="6225d-301">Az.Sql (korábban AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="6225d-301">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="6225d-302">A `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` parancsmag `State` és `ResourceId` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-302">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="6225d-303">A következő, elavult parancsmagok el lettek távolítva: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing` és `Remove-AzSqlServerAuditing`.</span><span class="sxs-lookup"><span data-stu-id="6225d-303">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="6225d-304">A `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` parancsmag elavult `Current` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-304">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="6225d-305">A `Get-AzSqlServerServiceObjective` parancsmag elavult `DatabaseName` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-305">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="6225d-306">A `Set-AzSqlDatabaseDataMaskingPolicy` parancsmag elavult `PrivilegedLogin` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-306">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="6225d-307">Az.Storage (korábban Azure.Storage és AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="6225d-307">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="6225d-308">Annak érdekében, hogy létre lehessen hozni egy Oauth Storage-környezetet pusztán a tárfiók nevét használva, az új alapértelmezett paraméterkészlet a következő: `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="6225d-308">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="6225d-309">Például: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="6225d-309">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="6225d-310">A `Get-AzStorageUsage` parancsmagban kötelezővé vált a `Location` paraméter használata.</span><span class="sxs-lookup"><span data-stu-id="6225d-310">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="6225d-311">A Storage API-metódusok mostantól feladatalapú aszinkron mintát (TAP) használnak az egyidejű API-hívások helyett.</span><span class="sxs-lookup"><span data-stu-id="6225d-311">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="6225d-312">Az alábbi példák az új, aszinkron parancsokat mutatják be:</span><span class="sxs-lookup"><span data-stu-id="6225d-312">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="6225d-313">Blob-pillanatképek</span><span class="sxs-lookup"><span data-stu-id="6225d-313">Blob Snapshot</span></span>

<span data-ttu-id="6225d-314">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="6225d-314">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="6225d-315">Az:</span><span class="sxs-lookup"><span data-stu-id="6225d-315">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="6225d-316">Megosztási pillanatképek</span><span class="sxs-lookup"><span data-stu-id="6225d-316">Share Snapshot</span></span>

<span data-ttu-id="6225d-317">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="6225d-317">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="6225d-318">Az:</span><span class="sxs-lookup"><span data-stu-id="6225d-318">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="6225d-319">Blob helyreállítható törlésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="6225d-319">Undelete soft-deleted blob</span></span>

<span data-ttu-id="6225d-320">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="6225d-320">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="6225d-321">Az:</span><span class="sxs-lookup"><span data-stu-id="6225d-321">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="6225d-322">Blobszint beállítása</span><span class="sxs-lookup"><span data-stu-id="6225d-322">Set Blob Tier</span></span>

<span data-ttu-id="6225d-323">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="6225d-323">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="6225d-324">Az:</span><span class="sxs-lookup"><span data-stu-id="6225d-324">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="6225d-325">Az.Websites (korábban AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="6225d-325">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="6225d-326">A `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` és `PSSite` objektum elavult tulajdonságai el lettek távolítva.</span><span class="sxs-lookup"><span data-stu-id="6225d-326">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
