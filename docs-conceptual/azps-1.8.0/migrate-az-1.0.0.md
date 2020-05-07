---
title: Az AzureRM és az Azure PowerShell Az 1.0.0 közötti összes változás
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 1-es verziójában található kompatibilitástörő változások listáját.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: ea7593cf2b753b210ff2955b7bd450030ad83596
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "75035829"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="6b062-103">Az Az 1.0.0 kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="6b062-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="6b062-104">Ez a dokumentum részletes információkat tartalmaz az AzureRM 6.x és az új Az modul 1.x és újabb verziója közötti változásokról.</span><span class="sxs-lookup"><span data-stu-id="6b062-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="6b062-105">A tartalomjegyzék végigvezeti a teljes migrálási folyamaton, és bemutatja a modulspecifikus módosításokat is, amelyek befolyásolhatják a szkripteket.</span><span class="sxs-lookup"><span data-stu-id="6b062-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="6b062-106">Az AzureRM-ből az Az-be történő migrálás megkezdéséhez kapcsolódó általános tanácsokért lásd: [Migrálás megkezdése az AzureRM-ből az Az-be](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="6b062-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="6b062-107">Tartalomjegyzék</span><span class="sxs-lookup"><span data-stu-id="6b062-107">Table of Contents</span></span>

- [<span data-ttu-id="6b062-108">Általános kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="6b062-108">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="6b062-109">A parancsmag főnévi előtagjának változásai</span><span class="sxs-lookup"><span data-stu-id="6b062-109">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="6b062-110">A modul nevének változásai</span><span class="sxs-lookup"><span data-stu-id="6b062-110">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="6b062-111">Eltávolított modulok</span><span class="sxs-lookup"><span data-stu-id="6b062-111">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="6b062-112">Windows PowerShell 5.1 és .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="6b062-112">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="6b062-113">A felhasználói bejelentkezés ideiglenes eltávolítása a PSCredential használatával</span><span class="sxs-lookup"><span data-stu-id="6b062-113">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="6b062-114">Bejelentkezés alapértelmezett eszközkóddal a webböngészőben megjelenő kérdés helyett</span><span class="sxs-lookup"><span data-stu-id="6b062-114">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="6b062-115">A modul kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="6b062-115">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="6b062-116">Az.ApiManagement (korábban AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="6b062-116">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="6b062-117">Az.Billing (korábban AzureRM.Billing, AzureRM.Consumption és AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="6b062-117">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="6b062-118">Az.CognitiveServices (korábban AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="6b062-118">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="6b062-119">Az.Compute (korábban AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="6b062-119">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="6b062-120">Az.DataFactory (korábban AzureRM.DataFactories és AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="6b062-120">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="6b062-121">Az.DataLakeAnalytics (korábban AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="6b062-121">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="6b062-122">Az.DataLakeStore (korábban AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="6b062-122">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="6b062-123">Az.KeyVault (korábban AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="6b062-123">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="6b062-124">Az.Media (korábban AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="6b062-124">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="6b062-125">Az.Monitor (korábban AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="6b062-125">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="6b062-126">Az.Network (korábban AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="6b062-126">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="6b062-127">Az.OperationalInsights (korábban AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="6b062-127">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="6b062-128">Az.RecoveryServices (korábban AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup és AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="6b062-128">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="6b062-129">Az.Resources (korábban AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="6b062-129">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="6b062-130">Az.ServiceFabric (korábban AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="6b062-130">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="6b062-131">Az.Sql (korábban AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="6b062-131">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="6b062-132">Az.Storage (korábban Azure.Storage és AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="6b062-132">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="6b062-133">Az.Websites (korábban AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="6b062-133">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="6b062-134">Általános kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="6b062-134">General breaking changes</span></span>

<span data-ttu-id="6b062-135">Ez a szakasz részletesen bemutatja az Az modul újratervezésének részét képező általános kompatibilitástörő változásokat.</span><span class="sxs-lookup"><span data-stu-id="6b062-135">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="6b062-136">A parancsmag főnévi előtagjának változásai</span><span class="sxs-lookup"><span data-stu-id="6b062-136">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="6b062-137">Az AzureRM modulban a parancsmagok az `AzureRM` vagy az `Azure` főnévi előtagot használták.</span><span class="sxs-lookup"><span data-stu-id="6b062-137">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="6b062-138">Az Az egyszerűsíti és normalizálja a parancsmagok nevét, így minden parancsmag főnévi előtagja „Az” lesz.</span><span class="sxs-lookup"><span data-stu-id="6b062-138">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="6b062-139">Például:</span><span class="sxs-lookup"><span data-stu-id="6b062-139">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="6b062-140">A következőre módosult:</span><span class="sxs-lookup"><span data-stu-id="6b062-140">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="6b062-141">Az új parancsmagokra való áttérés megkönnyítése érdekében az Az két új parancsmagot vezet be: [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) és [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="6b062-141">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="6b062-142">Az `Enable-AzureRmAlias` a régebbi parancsmagok nevéhez hoz létre aliasokat az AzureRM-ben, amelyek az újabb Az-parancsmagok nevének felelnek meg.</span><span class="sxs-lookup"><span data-stu-id="6b062-142">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="6b062-143">A `-Scope` argumentum és az `Enable-AzureRmAlias` együttes használatával kiválaszthatja, hol legyenek engedélyezve az aliasok.</span><span class="sxs-lookup"><span data-stu-id="6b062-143">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="6b062-144">A következő AzureRM-szkript például:</span><span class="sxs-lookup"><span data-stu-id="6b062-144">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="6b062-145">Az `Enable-AzureRmAlias` használatával minimális változtatásokkal futtatható:</span><span class="sxs-lookup"><span data-stu-id="6b062-145">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="6b062-146">Az `Enable-AzureRmAlias -Scope CurrentUser` futtatása engedélyezi az aliasokat az összes megnyitott PowerShell-munkamenetben, így a parancsmag végrehajtása után az ehhez hasonló szkripteket egyáltalán nem kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6b062-146">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="6b062-147">A parancsmagok aliasaival kapcsolatos részletes információért tekintse meg az [Enable-AzureRmAlias referenciáját](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="6b062-147">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="6b062-148">Amikor készen áll az aliasok letiltására, a `Disable-AzureRmAlias` eltávolítja a létrehozott aliasokat.</span><span class="sxs-lookup"><span data-stu-id="6b062-148">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="6b062-149">Részletes információért tekintse meg a [Disable-AzureRmAlias referenciáját](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="6b062-149">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b062-150">Az aliasok letiltásakor győződjön meg arról, hogy _minden_ olyan hatókörnél le lettek tiltva, amelyekhez engedélyezve voltak az aliasok.</span><span class="sxs-lookup"><span data-stu-id="6b062-150">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="6b062-151">A modul nevének változásai</span><span class="sxs-lookup"><span data-stu-id="6b062-151">Module Name Changes</span></span>

<span data-ttu-id="6b062-152">A modul neve a korábbi `AzureRM.*` helyett `Az.*` lett, kivéve a következő modulokban:</span><span class="sxs-lookup"><span data-stu-id="6b062-152">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="6b062-153">AzureRM modul</span><span class="sxs-lookup"><span data-stu-id="6b062-153">AzureRM module</span></span> | <span data-ttu-id="6b062-154">Az modul</span><span class="sxs-lookup"><span data-stu-id="6b062-154">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="6b062-155">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6b062-155">Azure.Storage</span></span> | <span data-ttu-id="6b062-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6b062-156">Az.Storage</span></span> |
| <span data-ttu-id="6b062-157">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6b062-157">Azure.AnalysisServices</span></span> | <span data-ttu-id="6b062-158">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6b062-158">Az.AnalysisServices</span></span> |
| <span data-ttu-id="6b062-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6b062-159">AzureRM.Profile</span></span> | <span data-ttu-id="6b062-160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6b062-160">Az.Accounts</span></span> |
| <span data-ttu-id="6b062-161">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6b062-161">AzureRM.Insights</span></span> | <span data-ttu-id="6b062-162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6b062-162">Az.Monitor</span></span> |
| <span data-ttu-id="6b062-163">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="6b062-163">AzureRM.DataFactories</span></span> | <span data-ttu-id="6b062-164">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6b062-164">Az.DataFactory</span></span> |
| <span data-ttu-id="6b062-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6b062-165">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="6b062-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6b062-166">Az.DataFactory</span></span> |
| <span data-ttu-id="6b062-167">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6b062-167">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="6b062-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6b062-168">Az.RecoveryServices</span></span> |
| <span data-ttu-id="6b062-169">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6b062-169">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="6b062-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6b062-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="6b062-171">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6b062-171">AzureRM.Tags</span></span> | <span data-ttu-id="6b062-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6b062-172">Az.Resources</span></span> |
| <span data-ttu-id="6b062-173">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6b062-173">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="6b062-174">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6b062-174">Az.MachineLearning</span></span> |
| <span data-ttu-id="6b062-175">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="6b062-175">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="6b062-176">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6b062-176">Az.Billing</span></span> |
| <span data-ttu-id="6b062-177">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6b062-177">AzureRM.Consumption</span></span> | <span data-ttu-id="6b062-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6b062-178">Az.Billing</span></span> |

<span data-ttu-id="6b062-179">A modul nevének változása azt jelenti, hogy ha egy szkript a `#Requires` vagy az `Import-Module` használatával tölt be bizonyos modulokat, módosításokat kell végezni az új modul használatához.</span><span class="sxs-lookup"><span data-stu-id="6b062-179">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="6b062-180">Azoknál a moduloknál, ahol a parancsmag utótagja nem változott, ez azt jelenti, hogy a modul neve megváltozott, a művelet helyét jelző utótag viszont _nem_.</span><span class="sxs-lookup"><span data-stu-id="6b062-180">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="6b062-181">#Requires és Import-Module utasítások migrálása</span><span class="sxs-lookup"><span data-stu-id="6b062-181">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="6b062-182">Ha egy szkript `#Requires` vagy `Import-Module` használatával deklarálja egy AzureRM-modultól való függőségét, akkor frissíteni kell az új modulnevek használatára.</span><span class="sxs-lookup"><span data-stu-id="6b062-182">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="6b062-183">Például:</span><span class="sxs-lookup"><span data-stu-id="6b062-183">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="6b062-184">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6b062-184">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="6b062-185">`Import-Module` esetében:</span><span class="sxs-lookup"><span data-stu-id="6b062-185">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="6b062-186">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6b062-186">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="6b062-187">Teljesen minősített parancsmaghívások migrálása</span><span class="sxs-lookup"><span data-stu-id="6b062-187">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="6b062-188">Modulhoz minősített parancsmaghívásokat használó szkriptek, például:</span><span class="sxs-lookup"><span data-stu-id="6b062-188">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="6b062-189">Úgy kell módosítani, hogy az új modul- és parancsmagneveket használja:</span><span class="sxs-lookup"><span data-stu-id="6b062-189">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="6b062-190">Moduljegyzék-függőségek migrálása</span><span class="sxs-lookup"><span data-stu-id="6b062-190">Migrating module manifest dependencies</span></span>

<span data-ttu-id="6b062-191">Amennyiben egy modul AzureRM-modultól való függését egy moduljegyzék (.psd1) fájl fejezi ki, a modul `RequiredModules` szakaszában frissíteni kell a modulok nevét:</span><span class="sxs-lookup"><span data-stu-id="6b062-191">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="6b062-192">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6b062-192">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="6b062-193">Eltávolított modulok</span><span class="sxs-lookup"><span data-stu-id="6b062-193">Removed modules</span></span>

<span data-ttu-id="6b062-194">Az alábbi modulok lettek eltávolítva:</span><span class="sxs-lookup"><span data-stu-id="6b062-194">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="6b062-195">E szolgáltatások eszközeit már nem támogatja aktívan a rendszer.</span><span class="sxs-lookup"><span data-stu-id="6b062-195">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="6b062-196">Azt javasoljuk ügyfeleinknek, hogy amint lehetséges, térjenek át más szolgáltatások használatára.</span><span class="sxs-lookup"><span data-stu-id="6b062-196">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="6b062-197">Windows PowerShell 5.1 és .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="6b062-197">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="6b062-198">Az Az Windows PowerShell 5.1-gyel történő használatához szükséges a .NET-keretrendszer 4.7.2 telepítése.</span><span class="sxs-lookup"><span data-stu-id="6b062-198">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="6b062-199">A PowerShell Core 6.x vagy újabb verziójának használatához nincs szükség a .NET-keretrendszerre.</span><span class="sxs-lookup"><span data-stu-id="6b062-199">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="6b062-200">A felhasználói bejelentkezés ideiglenes eltávolítása a PSCredential használatával</span><span class="sxs-lookup"><span data-stu-id="6b062-200">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="6b062-201">A .NET Standard hitelesítési folyamatának változásai miatt ideiglenesen eltávolítjuk a PSCredential használatával történő felhasználói bejelentkezés lehetőségét.</span><span class="sxs-lookup"><span data-stu-id="6b062-201">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="6b062-202">A funkció a Windows PowerShell 5.1 2019. január 15-én megjelenő verziójában válik ismét elérhetővé.</span><span class="sxs-lookup"><span data-stu-id="6b062-202">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="6b062-203">Erről részletesen [ebben a GitHub-cikkben](https://github.com/Azure/azure-powershell/issues/7430) olvashat.</span><span class="sxs-lookup"><span data-stu-id="6b062-203">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="6b062-204">Bejelentkezés alapértelmezett eszközkóddal a webböngészőben megjelenő kérdés helyett</span><span class="sxs-lookup"><span data-stu-id="6b062-204">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="6b062-205">A .NET Standard hitelesítési folyamatának változásai miatt az interaktív bejelentkezések során az eszközről történő bejelentkezés lesz az alapértelmezett bejelentkezési folyamat.</span><span class="sxs-lookup"><span data-stu-id="6b062-205">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="6b062-206">A webböngésző-alapú bejelentkezés a Windows PowerShell 5.1 2019. január 15-én megjelenő verziójában válik ismét elérhetővé.</span><span class="sxs-lookup"><span data-stu-id="6b062-206">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="6b062-207">Ezt követően a felhasználók a Switch paramétert használva választhatják az eszközről történő bejelentkezést.</span><span class="sxs-lookup"><span data-stu-id="6b062-207">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="6b062-208">A modul kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="6b062-208">Module breaking changes</span></span>

<span data-ttu-id="6b062-209">Ez a szakasz részletesen bemutatja az egyes modulok és parancsmagok kompatibilitástörő változásait.</span><span class="sxs-lookup"><span data-stu-id="6b062-209">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="6b062-210">Az.ApiManagement (korábban AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="6b062-210">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="6b062-211">A következő parancsmagok lettek eltávolítva:</span><span class="sxs-lookup"><span data-stu-id="6b062-211">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="6b062-212">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b062-212">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="6b062-213">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6b062-213">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="6b062-214">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6b062-214">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="6b062-215">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6b062-215">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="6b062-216">Ezeket a tulajdonságokat mostantól a **Set-AzApiManagement** parancsmaggal kell beállítani</span><span class="sxs-lookup"><span data-stu-id="6b062-216">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="6b062-217">A következő tulajdonságok lettek eltávolítva:</span><span class="sxs-lookup"><span data-stu-id="6b062-217">Removed the following properties:</span></span>
  - <span data-ttu-id="6b062-218">A `PortalHostnameConfiguration` típus `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration`, `ScmHostnameConfiguration` és `PsApiManagementHostnameConfiguration` tulajdonsága el lett távolítva a `PsApiManagementContext`ből.</span><span class="sxs-lookup"><span data-stu-id="6b062-218">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="6b062-219">Ezek helyett a `PortalCustomHostnameConfiguration` típus `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration`, `ScmCustomHostnameConfiguration` és `PsApiManagementCustomHostNameConfiguration` tulajdonságát használja.</span><span class="sxs-lookup"><span data-stu-id="6b062-219">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="6b062-220">A `StaticIPs` tulajdonság el lett távolítva a PsApiManagementContextből.</span><span class="sxs-lookup"><span data-stu-id="6b062-220">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="6b062-221">Két új tulajdonságra lett osztva: ez a `PublicIPAddresses` és a `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="6b062-221">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="6b062-222">A kötelező `Location` tulajdonság el lett távolítva a New-AzureApiManagementVirtualNetwork parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="6b062-222">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="6b062-223">Az.Billing (korábban AzureRM.Billing, AzureRM.Consumption és AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="6b062-223">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="6b062-224">A `InvoiceName` parancsmag `Get-AzConsumptionUsageDetail` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-224">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="6b062-225">A szkripteknek a számlák készítéséhez más identitásparamétereket kell használniuk.</span><span class="sxs-lookup"><span data-stu-id="6b062-225">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="6b062-226">Az.CognitiveServices (korábban AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="6b062-226">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="6b062-227">A `GetSkusWithAccountParamSetName` parancsmag `Get-AzCognitiveServicesAccountSkus` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-227">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="6b062-228">A termékváltozatokat a fiók típusa és helye alapján lehet lekérdezni a ResourceGroupName és a fiók nevének használata helyett.</span><span class="sxs-lookup"><span data-stu-id="6b062-228">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="6b062-229">Az.Compute (korábban AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="6b062-229">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="6b062-230">A `IdentityIds` és `Identity` objektum `PSVirtualMachine` tulajdonsága mostantól nem tartalmazza az `PSVirtualMachineScaleSet` azonosítókat. A szkriptek a jövőben nem veszik figyelembe a mező értékét a feldolgozási döntések során.</span><span class="sxs-lookup"><span data-stu-id="6b062-230">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="6b062-231">A `InstanceView` objektum `PSVirtualMachineScaleSetVM` tulajdonságának típusa `VirtualMachineInstanceView` helyett `VirtualMachineScaleSetVMInstanceView` lett.</span><span class="sxs-lookup"><span data-stu-id="6b062-231">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="6b062-232">Az `AutoOSUpgradePolicy` tulajdonság `AutomaticOSUpgrade` és `UpgradePolicy` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-232">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="6b062-233">A `Sku` objektum `PSSnapshotUpdate` tulajdonságának típusa `DiskSku` helyett `SnapshotSku` lett.</span><span class="sxs-lookup"><span data-stu-id="6b062-233">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="6b062-234">A `VmScaleSetVMParameterSet` el lett távolítva az `Add-AzVMDataDisk` parancsmagból, mostantól nem lehet önálló adatlemezt hozzáadni egy ScaleSet-virtuálisgéphez.</span><span class="sxs-lookup"><span data-stu-id="6b062-234">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="6b062-235">Az.DataFactory (korábban AzureRM.DataFactories és AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="6b062-235">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="6b062-236">A `GatewayName` parancsmagban kötelezővé vált a `New-AzDataFactoryEncryptValue` paraméter használata.</span><span class="sxs-lookup"><span data-stu-id="6b062-236">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="6b062-237">A `New-AzDataFactoryGatewayKey` parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-237">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="6b062-238">A `LinkedServiceName` parancsmag `Get-AzDataFactoryV2ActivityRun` paramétere el lett távolítva. A szkriptek a jövőben nem veszik figyelembe a mező értékét a feldolgozási döntések során.</span><span class="sxs-lookup"><span data-stu-id="6b062-238">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="6b062-239">Az.DataLakeAnalytics (korábban AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="6b062-239">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="6b062-240">El lettek távolítva a következő elavult parancsmagok: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, és `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="6b062-240">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="6b062-241">Az.DataLakeStore (korábban AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="6b062-241">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="6b062-242">A következő parancsmagok `Encoding` paraméterének típusa `FileSystemCmdletProviderEncoding` helyett `System.Text.Encoding` lett.</span><span class="sxs-lookup"><span data-stu-id="6b062-242">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="6b062-243">Ez a módosítás eltávolítja a `String` és `Oem` kódolási értéket.</span><span class="sxs-lookup"><span data-stu-id="6b062-243">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="6b062-244">Az összes egyéb korábbi kódolási érték elérhető marad.</span><span class="sxs-lookup"><span data-stu-id="6b062-244">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="6b062-245">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b062-245">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="6b062-246">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6b062-246">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="6b062-247">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6b062-247">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="6b062-248">A `Tags` és `New-AzDataLakeStoreAccount` parancsmag elavult `Set-AzDataLakeStoreAccount` tulajdonságaliasa el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-248">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="6b062-249">A következőt használó szkripteket:</span><span class="sxs-lookup"><span data-stu-id="6b062-249">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="6b062-250">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6b062-250">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="6b062-251">A `Identity` objektum elavult tulajdonságai el lettek távolítva: `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` és `PSDataLakeStoreAccountBasic`.</span><span class="sxs-lookup"><span data-stu-id="6b062-251">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="6b062-252">A `PSDatalakeStoreAccount` által visszaadott `Get-AzDataLakeStoreAccount` értéket használó szkriptek nem hivatkozhatnak ezekre a tulajdonságokra.</span><span class="sxs-lookup"><span data-stu-id="6b062-252">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="6b062-253">Az.KeyVault (korábban AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="6b062-253">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="6b062-254">A `PurgeDisabled`, `PSKeyVaultKeyAttributes` és `PSKeyVaultKeyIdentityItem` objektum `PSKeyVaultSecretAttributes` tulajdonsága el lett távolítva. A szkriptek a jövőben nem hivatkozhatnak a ```PurgeDisabled``` tulajdonságra a feldolgozási döntések során.</span><span class="sxs-lookup"><span data-stu-id="6b062-254">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="6b062-255">Az.Media (korábban AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="6b062-255">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="6b062-256">A `Tags` parancsmag elavult `New-AzMediaService` tulajdonságaliasa el lett távolítva. A következőt használó szkripteket:</span><span class="sxs-lookup"><span data-stu-id="6b062-256">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="6b062-257">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6b062-257">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="6b062-258">Az.Monitor (korábban AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="6b062-258">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="6b062-259">A `Categories` és a `Timegrains` többes számú paraméternév el lett távolítva. Ezek helyett a `Set-AzDiagnosticSetting` parancsmag egyes számú paraméterneveit kell használni. A következőt használó szkripteket:</span><span class="sxs-lookup"><span data-stu-id="6b062-259">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="6b062-260">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="6b062-260">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="6b062-261">Az.Network (korábban AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="6b062-261">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="6b062-262">A `ResourceId` parancsmag elavult `Get-AzServiceEndpointPolicyDefinition` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-262">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="6b062-263">A `EnableVmProtection` objektum elavult `PSVirtualNetwork` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-263">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="6b062-264">Az elavult `Set-AzVirtualNetworkGatewayVpnClientConfig` parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-264">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="6b062-265">A szkriptek a jövőben nem hozhatnak feldolgozási döntéseket e mezők értéke alapján.</span><span class="sxs-lookup"><span data-stu-id="6b062-265">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="6b062-266">Az.OperationalInsights (korábban AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="6b062-266">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="6b062-267">A `Get-AzOperationalInsightsDataSource` alapértelmezett paraméterkészlete el lett távolítva. Mostantól a `ByWorkspaceNameByKind` az alapértelmezett paraméterkészlet.</span><span class="sxs-lookup"><span data-stu-id="6b062-267">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="6b062-268">Azokat a szkripteket, amelyek a következő használatával listázták az adatforrásokat:</span><span class="sxs-lookup"><span data-stu-id="6b062-268">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="6b062-269">Úgy kell módosítani, hogy megadjanak egy altípust:</span><span class="sxs-lookup"><span data-stu-id="6b062-269">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="6b062-270">Az.RecoveryServices (korábban AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup és AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="6b062-270">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="6b062-271">A `Encryption` parancsmag `New/Set-AzRecoveryServicesAsrPolicy` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-271">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="6b062-272">A `TargetStorageAccountName` paraméter megadása mostantól kötelező a `Restore-AzRecoveryServicesBackupItem` parancsmag felügyeltlemez-visszaállítási műveleteihez.</span><span class="sxs-lookup"><span data-stu-id="6b062-272">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="6b062-273">A `StorageAccountName` parancsmag `StorageAccountResourceGroupName` és `Restore-AzRecoveryServicesBackupItem` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-273">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="6b062-274">A `Name` parancsmag `Get-AzRecoveryServicesBackupContainer` paramétere el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="6b062-274">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="6b062-275">Az.Resources (korábban AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="6b062-275">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="6b062-276">A `Sku` parancsmag `New/Set-AzPolicyAssignment` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-276">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="6b062-277">A `Password` és `New-AzADServicePrincipal` parancsmag `New-AzADSpCredential` paramétere el lett távolítva. A jelszavak létrehozása automatikusan történik, a korábban jelszót biztosító szkripteket:</span><span class="sxs-lookup"><span data-stu-id="6b062-277">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="6b062-278">Úgy kell módosítani, hogy a kimenetből kérjék le a jelszót:</span><span class="sxs-lookup"><span data-stu-id="6b062-278">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="6b062-279">Az.ServiceFabric (korábban AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="6b062-279">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="6b062-280">Módosítottuk a következő parancsmag visszatérési típusait:</span><span class="sxs-lookup"><span data-stu-id="6b062-280">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="6b062-281">Az `ServiceTypeHealthPolicies` típus `ApplicationHealthPolicy` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-281">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="6b062-282">Az `ApplicationHealthPolicies` típus `ClusterUpgradeDeltaHealthPolicy` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-282">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="6b062-283">Az `OverrideUserUpgradePolicy` típus `ClusterUpgradePolicy` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-283">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="6b062-284">Ezek a módosítások a következő parancsmagokat érintik:</span><span class="sxs-lookup"><span data-stu-id="6b062-284">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="6b062-285">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6b062-285">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="6b062-286">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6b062-286">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="6b062-287">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6b062-287">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="6b062-288">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6b062-288">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="6b062-289">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6b062-289">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="6b062-290">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6b062-290">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="6b062-291">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6b062-291">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="6b062-292">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6b062-292">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="6b062-293">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6b062-293">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="6b062-294">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6b062-294">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="6b062-295">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6b062-295">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="6b062-296">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="6b062-296">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="6b062-297">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="6b062-297">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="6b062-298">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="6b062-298">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="6b062-299">Az.Sql (korábban AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="6b062-299">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="6b062-300">A `State` parancsmag `ResourceId` és `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-300">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="6b062-301">A következő, elavult parancsmagok el lettek távolítva: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing` és `Remove-AzSqlServerAuditing`.</span><span class="sxs-lookup"><span data-stu-id="6b062-301">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="6b062-302">A `Current` parancsmag elavult `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-302">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="6b062-303">A `DatabaseName` parancsmag elavult `Get-AzSqlServerServiceObjective` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-303">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="6b062-304">A `PrivilegedLogin` parancsmag elavult `Set-AzSqlDatabaseDataMaskingPolicy` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-304">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="6b062-305">Az.Storage (korábban Azure.Storage és AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="6b062-305">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="6b062-306">Annak érdekében, hogy létre lehessen hozni egy Oauth Storage-környezetet pusztán a tárfiók nevét használva, az új alapértelmezett paraméterkészlet a következő: `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="6b062-306">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="6b062-307">Például: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="6b062-307">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="6b062-308">A `Location` parancsmagban kötelezővé vált a `Get-AzStorageUsage` paraméter használata.</span><span class="sxs-lookup"><span data-stu-id="6b062-308">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="6b062-309">A Storage API-metódusok mostantól feladatalapú aszinkron mintát (TAP) használnak az egyidejű API-hívások helyett.</span><span class="sxs-lookup"><span data-stu-id="6b062-309">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="6b062-310">Az alábbi példák az új, aszinkron parancsokat mutatják be:</span><span class="sxs-lookup"><span data-stu-id="6b062-310">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="6b062-311">Blob-pillanatképek</span><span class="sxs-lookup"><span data-stu-id="6b062-311">Blob Snapshot</span></span>

<span data-ttu-id="6b062-312">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="6b062-312">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="6b062-313">Az:</span><span class="sxs-lookup"><span data-stu-id="6b062-313">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="6b062-314">Megosztási pillanatképek</span><span class="sxs-lookup"><span data-stu-id="6b062-314">Share Snapshot</span></span>

<span data-ttu-id="6b062-315">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="6b062-315">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="6b062-316">Az:</span><span class="sxs-lookup"><span data-stu-id="6b062-316">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="6b062-317">Blob helyreállítható törlésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="6b062-317">Undelete soft-deleted blob</span></span>

<span data-ttu-id="6b062-318">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="6b062-318">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="6b062-319">Az:</span><span class="sxs-lookup"><span data-stu-id="6b062-319">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="6b062-320">Blobszint beállítása</span><span class="sxs-lookup"><span data-stu-id="6b062-320">Set Blob Tier</span></span>

<span data-ttu-id="6b062-321">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="6b062-321">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="6b062-322">Az:</span><span class="sxs-lookup"><span data-stu-id="6b062-322">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="6b062-323">Az.Websites (korábban AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="6b062-323">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="6b062-324">A `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` és `PSSite` objektum elavult tulajdonságai el lettek távolítva.</span><span class="sxs-lookup"><span data-stu-id="6b062-324">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
