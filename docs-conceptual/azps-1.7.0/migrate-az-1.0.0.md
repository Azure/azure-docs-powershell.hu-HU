---
title: A Microsoft Azure PowerShell Az 1.0.0 kompatibilitástörő változásai
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 1-es verziójában található kompatibilitástörő változások listáját.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/18/2019
ms.locfileid: "59364148"
---
# <a name="migration-guide-for-az-100"></a><span data-ttu-id="33424-103">Migrálási útmutató az Az 1.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="33424-103">Migration Guide for Az 1.0.0</span></span>

<span data-ttu-id="33424-104">Ez a dokumentum ismerteti, hogy milyen módosítások történtek az AzureRM 6.x-es verziói és az Az 1.0.0-s verzió között.</span><span class="sxs-lookup"><span data-stu-id="33424-104">This document describes the changes between the 6.x versions of AzureRM and Az version 1.0.0.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="33424-105">Tartalomjegyzék</span><span class="sxs-lookup"><span data-stu-id="33424-105">Table of Contents</span></span>
- [<span data-ttu-id="33424-106">Általános kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="33424-106">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="33424-107">A parancsmag főnévi előtagjának változásai</span><span class="sxs-lookup"><span data-stu-id="33424-107">Cmdlet Noun Prefix Changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="33424-108">A modul nevének változásai</span><span class="sxs-lookup"><span data-stu-id="33424-108">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="33424-109">Eltávolított modulok</span><span class="sxs-lookup"><span data-stu-id="33424-109">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="33424-110">Windows PowerShell 5.1 és .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="33424-110">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="33424-111">A felhasználói bejelentkezés ideiglenes eltávolítása a PSCredential használatával</span><span class="sxs-lookup"><span data-stu-id="33424-111">Temporary removal of User login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="33424-112">Bejelentkezés alapértelmezett eszközkóddal a webböngészőben megjelenő kérdés helyett</span><span class="sxs-lookup"><span data-stu-id="33424-112">Default Device Code login instead of Web Browser prompt</span></span>](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="33424-113">A modul kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="33424-113">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="33424-114">Az.ApiManagement (korábban AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="33424-114">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="33424-115">Az.Billing (korábban AzureRM.Billing, AzureRM.Consumption és AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="33424-115">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="33424-116">Az.CognitiveServices (korábban AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="33424-116">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="33424-117">Az.Compute (korábban AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="33424-117">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="33424-118">Az.DataFactory (korábban AzureRM.DataFactories és AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="33424-118">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="33424-119">Az.DataLakeAnalytics (korábban AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="33424-119">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="33424-120">Az.DataLakeStore (korábban AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="33424-120">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="33424-121">Az.KeyVault (korábban AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="33424-121">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="33424-122">Az.Media (korábban AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="33424-122">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="33424-123">Az.Monitor (korábban AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="33424-123">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="33424-124">Az.Network (korábban AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="33424-124">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="33424-125">Az.OperationalInsights (korábban AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="33424-125">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="33424-126">Az.RecoveryServices (korábban AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup és AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="33424-126">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="33424-127">Az.Resources (korábban AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="33424-127">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="33424-128">Az.ServiceFabric (korábban AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="33424-128">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="33424-129">Az.Sql (korábban AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="33424-129">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="33424-130">Az.Storage (korábban Azure.Storage és AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="33424-130">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="33424-131">Az.Websites (korábban AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="33424-131">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="33424-132">Általános kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="33424-132">General breaking changes</span></span>
### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="33424-133">A parancsmag főnévi előtagjának változásai</span><span class="sxs-lookup"><span data-stu-id="33424-133">Cmdlet Noun Prefix Changes</span></span>
<span data-ttu-id="33424-134">Az AzureRM-ben a parancsmagok az „AzureRM” vagy az „Azure” főnévi előtagot használják.</span><span class="sxs-lookup"><span data-stu-id="33424-134">In AzureRM, cmdlets used either 'AzureRM' or 'Azure' as a noun prefix.</span></span>  <span data-ttu-id="33424-135">Az Az egyszerűsíti és normalizálja a parancsmagok nevét, így minden parancsmag főnévi előtagja „Az” lesz.</span><span class="sxs-lookup"><span data-stu-id="33424-135">Az simplifies and normalizes cmndlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="33424-136">Például:</span><span class="sxs-lookup"><span data-stu-id="33424-136">For example:</span></span>
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="33424-137">A következőre módosult:</span><span class="sxs-lookup"><span data-stu-id="33424-137">Have changed to</span></span>
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="33424-138">Az új parancsmagokra való áttérés megkönnyítése érdekében az Az két új parancsmagot (```Enable-AzureRmAlias``` és ```Disable-AzureRmAlias```) tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="33424-138">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, ```Enable-AzureRmAlias``` and ```Disable-AzureRmAlias```.</span></span>  <span data-ttu-id="33424-139">Az ```Enable-AzureRmAlias``` az újabb Az-parancsmagok nevéhez aliasokat hoz létre a korábbi AzureRM-parancsmagok nevéből.</span><span class="sxs-lookup"><span data-stu-id="33424-139">```Enable-AzureRmAlias``` creates aliases from the older cmdlet names in AzureRM to the newer Az cmdlet names.</span></span>  <span data-ttu-id="33424-140">A parancsmag lehetővé teszi aliasok létrehozását az aktuális munkamenetben, vagy akár több munkamenet során, a felhasználói vagy a gépprofil váltása után.</span><span class="sxs-lookup"><span data-stu-id="33424-140">The cmdlet allows creating aliases in the current session, or across all sessions by changing your user or machine profile.</span></span> 

<span data-ttu-id="33424-141">A következő AzureRM-szkript például:</span><span class="sxs-lookup"><span data-stu-id="33424-141">For example, the following script in AzureRM:</span></span>
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="33424-142">Az ```Enable-AzureRmAlias``` használatával minimális változtatásokkal futtatható:</span><span class="sxs-lookup"><span data-stu-id="33424-142">Could be run with minimal changes using ```Enable-AzureRmAlias```:</span></span>
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="33424-143">Az ```Enable-AzureRmAlias -Scope CurrentUser``` futtatása elérhetővé teszi az aliasokat minden megnyitott PowerShell-munkamenetben, így a parancsmag végrehajtása után az ehhez hasonló szkripteket egyáltalán nem kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="33424-143">Running ```Enable-AzureRmAlias -Scope CurrentUser``` will enable the aliases for all powershell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="33424-144">A parancsmagok aliasaival kapcsolatos részletes információkért futtassa a ```Get-Help -Online Enable-AzureRmAlias``` parancsot a PowerShell-parancssorból.</span><span class="sxs-lookup"><span data-stu-id="33424-144">For complete details on the usage of the alias cmdlets, execute ```Get-Help -Online Enable-AzureRmAlias``` from the powershell prompt.</span></span>

<span data-ttu-id="33424-145">A ```Disable-AzureRmAlias``` eltávolítja az ```Enable-AzureRmAlias``` által létrehozott AzureRM-parancsmagaliasokat.</span><span class="sxs-lookup"><span data-stu-id="33424-145">```Disable-AzureRmAlias``` removes AzureRM cmdlet aliases created by ```Enable-AzureRmAlias```.</span></span>  <span data-ttu-id="33424-146">Részletes információkért futtassa a ```Get-Help -Online Disable-AzureRmAlias``` parancsot a PowerShell-parancssorból.</span><span class="sxs-lookup"><span data-stu-id="33424-146">For complete details, execute ```Get-Help -Online Disable-AzureRmAlias``` from the powershell prompt.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="33424-147">A modul nevének változásai</span><span class="sxs-lookup"><span data-stu-id="33424-147">Module Name Changes</span></span>
- <span data-ttu-id="33424-148">A modul neve a korábbi `AzureRM.*` helyett `Az.*` lett, kivéve a következő modulokban:</span><span class="sxs-lookup"><span data-stu-id="33424-148">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

<span data-ttu-id="33424-149">A modul nevének változása azt jelenti, hogy ha egy szkript a ```#Requires``` vagy az ```Import-Module``` használatával tölt be bizonyos modulokat, módosításokat kell végezni az új modul használatához.</span><span class="sxs-lookup"><span data-stu-id="33424-149">The changes in module names mean that any script that uses ```#Requires``` or ```Import-Module``` to load specific modules will need to be changed to use the new module instead.</span></span>

#### <a name="migrating-requires-statements"></a><span data-ttu-id="33424-150">#Requires-utasítások migrálása</span><span class="sxs-lookup"><span data-stu-id="33424-150">Migrating #Requires Statements</span></span>
<span data-ttu-id="33424-151">Amennyiben egy szkript a #Requires használatával deklarálja függőségét egy AzureRM-modultól, frissíteni kell azt az új modulnevekkel.</span><span class="sxs-lookup"><span data-stu-id="33424-151">Scripts that use #Requires to declare a dependency on AzureRM modules should be updated to use the new module names</span></span>
```powershell
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="33424-152">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="33424-152">Should be changed to</span></span>
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a><span data-ttu-id="33424-153">Import-Module-utasítások migrálása</span><span class="sxs-lookup"><span data-stu-id="33424-153">Migrating Import-Module Statements</span></span>
<span data-ttu-id="33424-154">Amennyiben egy szkript az ```Import-Module``` használatával tölt be AzureRM-modulokat, frissíteni kell azt az új modulnevekkel.</span><span class="sxs-lookup"><span data-stu-id="33424-154">Scripts that use ```Import-Module``` to load AzureRM modules will need to be updated to reflect the new module names.</span></span>
```powershell
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="33424-155">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="33424-155">Should be changed to</span></span>
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="33424-156">Teljesen minősített parancsmaghívások migrálása</span><span class="sxs-lookup"><span data-stu-id="33424-156">Migrating Fully-Qualified Cmdlet Invocations</span></span>
<span data-ttu-id="33424-157">Modulhoz minősített parancsmaghívásokat használó szkriptek, például:</span><span class="sxs-lookup"><span data-stu-id="33424-157">Scripts that use module-qualified cmdlet invocations, like</span></span>
```powershell
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="33424-158">Úgy kell módosítani, hogy az új modul- és parancsmagneveket használja</span><span class="sxs-lookup"><span data-stu-id="33424-158">Should be changed to use the new module and cmdlet names</span></span>
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="33424-159">Moduljegyzék-függőségek migrálása</span><span class="sxs-lookup"><span data-stu-id="33424-159">Migrating Module Manifest Dependencies</span></span>
<span data-ttu-id="33424-160">Amennyiben egy modul AzureRM-modultól való függését egy moduljegyzék (.psd1) fájl fejezi ki, a modul „RequiredModules” szakaszában frissíteni kell a modulok nevét.</span><span class="sxs-lookup"><span data-stu-id="33424-160">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their 'RequiredModules' section</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="33424-161">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="33424-161">Should be changed to</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="33424-162">Eltávolított modulok</span><span class="sxs-lookup"><span data-stu-id="33424-162">Removed modules</span></span>
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="33424-163">E szolgáltatások eszközállománya már nem aktívan támogatott.</span><span class="sxs-lookup"><span data-stu-id="33424-163">The tooling for these services are no longer actively supported.</span></span>  <span data-ttu-id="33424-164">Azt javasoljuk ügyfeleinknek, hogy amint lehetséges, térjenek át más szolgáltatások használatára.</span><span class="sxs-lookup"><span data-stu-id="33424-164">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="33424-165">Windows PowerShell 5.1 és .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="33424-165">Windows PowerShell 5.1 and .NET 4.7.2</span></span>
- <span data-ttu-id="33424-166">Az Az Windows PowerShell 5.1-gyel történő használatához szükséges a .NET 4.7.2 telepítése.</span><span class="sxs-lookup"><span data-stu-id="33424-166">Using Az with Windows PowerShell 5.1 requires the installation of .NET 4.7.2.</span></span> <span data-ttu-id="33424-167">Az Az PowerShell Core-ral történő használatához ugyanakkor nem szükséges a .NET 4.7.2 megléte.</span><span class="sxs-lookup"><span data-stu-id="33424-167">However, using Az with PowerShell Core does not require .NET 4.7.2.</span></span> 

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="33424-168">A felhasználói bejelentkezés ideiglenes eltávolítása a PSCredential használatával</span><span class="sxs-lookup"><span data-stu-id="33424-168">Temporary removal of User login using PSCredential</span></span>
- <span data-ttu-id="33424-169">A .NET Standard hitelesítési folyamatának változásai miatt ideiglenesen eltávolítjuk a PSCredential használatával történő felhasználói bejelentkezés lehetőségét.</span><span class="sxs-lookup"><span data-stu-id="33424-169">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="33424-170">A funkció a Windows PowerShell 5.1 2019. január 15-én megjelenő verziójában válik ismét elérhetővé.</span><span class="sxs-lookup"><span data-stu-id="33424-170">This capability will be re-introduced in the 1/15/2019 release for Windows PowerShell 5.1.</span></span> <span data-ttu-id="33424-171">Erről részletesen [ebben a cikkben](https://github.com/Azure/azure-powershell/issues/7430) írtunk.</span><span class="sxs-lookup"><span data-stu-id="33424-171">This is duscussed in detail in [this issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="33424-172">Bejelentkezés alapértelmezett eszközkóddal a webböngészőben megjelenő kérdés helyett</span><span class="sxs-lookup"><span data-stu-id="33424-172">Default Device Code login instead of Web Browser prompt</span></span>
- <span data-ttu-id="33424-173">A .NET Standard hitelesítési folyamatának változásai miatt az interaktív bejelentkezések során az eszközről történő bejelentkezés lesz az alapértelmezett bejelentkezési folyamat.</span><span class="sxs-lookup"><span data-stu-id="33424-173">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="33424-174">A webböngésző-alapú bejelentkezés a Windows PowerShell 5.1 2019. január 15-én megjelenő verziójában válik ismét elérhetővé.</span><span class="sxs-lookup"><span data-stu-id="33424-174">Web browser based login will be re-introduced for Windows PowerShell 5.1 as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="33424-175">Ezt követően a felhasználók a Switch paramétert használva választhatják az eszközről történő bejelentkezést.</span><span class="sxs-lookup"><span data-stu-id="33424-175">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="33424-176">A modul kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="33424-176">Module breaking changes</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="33424-177">Az.ApiManagement (korábban AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="33424-177">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>
- <span data-ttu-id="33424-178">A következő parancsmagok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="33424-178">Removing the following cmdlets:</span></span>
  - <span data-ttu-id="33424-179">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="33424-179">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="33424-180">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="33424-180">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="33424-181">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="33424-181">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="33424-182">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="33424-182">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="33424-183">Ezeket a tulajdonságokat mostantól a **Set-AzApiManagement** parancsmaggal kell beállítani.</span><span class="sxs-lookup"><span data-stu-id="33424-183">Use **Set-AzApiManagement** cmdlet to set these properites instead</span></span>
- <span data-ttu-id="33424-184">A következő tulajdonságok el lettek távolítva</span><span class="sxs-lookup"><span data-stu-id="33424-184">Following properties were removed</span></span>
  - <span data-ttu-id="33424-185">A `PsApiManagementHostnameConfiguration` típus `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` és `ScmHostnameConfiguration` tulajdonsága el lett távolítva a `PsApiManagementContext`ből.</span><span class="sxs-lookup"><span data-stu-id="33424-185">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="33424-186">Ezek helyett a `PsApiManagementCustomHostNameConfiguration` típus `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` és `ScmCustomHostnameConfiguration` tulajdonságát használja.</span><span class="sxs-lookup"><span data-stu-id="33424-186">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="33424-187">A `StaticIPs` tulajdonság el lett távolítva a PsApiManagementContextből.</span><span class="sxs-lookup"><span data-stu-id="33424-187">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="33424-188">Két új tulajdonságra lett osztva: ez a `PublicIPAddresses` és a `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="33424-188">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="33424-189">A kötelező `Location` tulajdonság el lett távolítva a New-AzureApiManagementVirtualNetwork parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="33424-189">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="33424-190">Az.Billing (korábban AzureRM.Billing, AzureRM.Consumption és AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="33424-190">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>
- <span data-ttu-id="33424-191">A `Get-AzConsumptionUsageDetail` parancsmag `InvoiceName` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-191">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="33424-192">A szkripteknek a számlák készítéséhez más identitásparamétereket kell használniuk.</span><span class="sxs-lookup"><span data-stu-id="33424-192">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="33424-193">Az.CognitiveServices (korábban AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="33424-193">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>
- <span data-ttu-id="33424-194">A `Get-AzCognitiveServicesAccountSkus` parancsmag `GetSkusWithAccountParamSetName` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-194">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="33424-195">A termékváltozatokat a fiók típusa és helye alapján lehet lekérdezni a ResourceGroupName és a fiók nevének használata helyett.</span><span class="sxs-lookup"><span data-stu-id="33424-195">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="33424-196">Az.Compute (korábban AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="33424-196">Az.Compute (previously AzureRM.Compute)</span></span>
- <span data-ttu-id="33424-197">A `PSVirtualMachine` és `PSVirtualMachineScaleSet` objektum `Identity` tulajdonsága mostantól nem tartalmazza az `IdentityIds` azonosítókat. A szkriptek a jövőben nem veszik figyelembe a mező értékét a feldolgozási döntések során.</span><span class="sxs-lookup"><span data-stu-id="33424-197">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="33424-198">A `PSVirtualMachineScaleSetVM` objektum `InstanceView` tulajdonságának típusa `VirtualMachineInstanceView` helyett `VirtualMachineScaleSetVMInstanceView` lett.</span><span class="sxs-lookup"><span data-stu-id="33424-198">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="33424-199">Az `UpgradePolicy` tulajdonság `AutoOSUpgradePolicy` és `AutomaticOSUpgrade` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-199">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="33424-200">A `PSSnapshotUpdate` objektum `Sku` tulajdonságának típusa `DiskSku` helyett `SnapshotSku` lett.</span><span class="sxs-lookup"><span data-stu-id="33424-200">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="33424-201">Az `Add-AzVMDataDisk` parancsmagból el lett távolítva a `VmScaleSetVMParameterSet`. Mostantól nem lehet önálló adatlemezt hozzáadni egy ScaleSet-virtuálisgéphez.</span><span class="sxs-lookup"><span data-stu-id="33424-201">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="33424-202">Az.DataFactory (korábban AzureRM.DataFactories és AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="33424-202">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>
- <span data-ttu-id="33424-203">A `New-AzDataFactoryEncryptValue` parancsmagban kötelezővé vált a `GatewayName` paraméter használata.</span><span class="sxs-lookup"><span data-stu-id="33424-203">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="33424-204">A `New-AzDataFactoryGatewayKey` parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-204">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="33424-205">A `Get-AzDataFactoryV2ActivityRun` parancsmag `LinkedServiceName` paramétere el lett távolítva. A szkriptek a jövőben nem veszik figyelembe a mező értékét a feldolgozási döntések során.</span><span class="sxs-lookup"><span data-stu-id="33424-205">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="33424-206">Az.DataLakeAnalytics (korábban AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="33424-206">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>
- <span data-ttu-id="33424-207">El lettek távolítva a következő elavult parancsmagok: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, és `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="33424-207">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="33424-208">Az.DataLakeStore (korábban AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="33424-208">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>
- <span data-ttu-id="33424-209">A következő parancsmagok `Encoding` paraméterének típusa `FileSystemCmdletProviderEncoding` helyett `System.Text.Encoding` lett.</span><span class="sxs-lookup"><span data-stu-id="33424-209">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="33424-210">Ez a módosítás eltávolítja a `String` és `Oem` kódolási értéket.</span><span class="sxs-lookup"><span data-stu-id="33424-210">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="33424-211">Az összes egyéb korábbi kódolási érték elérhető marad.</span><span class="sxs-lookup"><span data-stu-id="33424-211">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="33424-212">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="33424-212">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="33424-213">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="33424-213">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="33424-214">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="33424-214">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="33424-215">A `New-AzDataLakeStoreAccount` és `Set-AzDataLakeStoreAccount` parancsmag elavult `Tags` tulajdonságaliasa el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-215">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="33424-216">A következőt használó szkripteket:</span><span class="sxs-lookup"><span data-stu-id="33424-216">Scripts using</span></span>
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="33424-217">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="33424-217">Should be changed to</span></span>
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="33424-218">A ```PSDataLakeStoreAccountBasic``` objektum elavult tulajdonságai el lettek távolítva: ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier``` és ```FirewallAllowAzureIps```.</span><span class="sxs-lookup"><span data-stu-id="33424-218">Removed deprecated properties ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` from ```PSDataLakeStoreAccountBasic``` object.</span></span>  <span data-ttu-id="33424-219">A ```Get-AzDataLakeStoreAccount``` által visszaadott ```PSDatalakeStoreAccount``` értéket használó szkriptek nem hivatkozhatnak ezekre a tulajdonságokra.</span><span class="sxs-lookup"><span data-stu-id="33424-219">Any script that uses the ```PSDatalakeStoreAccount``` returned from ```Get-AzDataLakeStoreAccount``` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="33424-220">Az.KeyVault (korábban AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="33424-220">Az.KeyVault (previously AzureRM.KeyVault)</span></span>
- <span data-ttu-id="33424-221">A `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` és `PSKeyVaultSecretAttributes` objektum `PurgeDisabled` tulajdonsága el lett távolítva. A szkriptek a jövőben nem hivatkozhatnak a ```PurgeDisabled``` tulajdonságra a feldolgozási döntések során.</span><span class="sxs-lookup"><span data-stu-id="33424-221">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts shoudl no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="33424-222">Az.Media (korábban AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="33424-222">Az.Media (previously AzureRM.Media)</span></span>
- <span data-ttu-id="33424-223">A `New-AzMediaService` parancsmag elavult `Tags` tulajdonságaliasa el lett távolítva. A következőt használó szkripteket:</span><span class="sxs-lookup"><span data-stu-id="33424-223">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="33424-224">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="33424-224">Should be changed to</span></span>
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="33424-225">Az.Monitor (korábban AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="33424-225">Az.Monitor (previously AzureRM.Insights)</span></span>
- <span data-ttu-id="33424-226">A `Categories` és a `Timegrains` többes számú paraméternév el lett távolítva. Ezek helyett a `Set-AzDiagnosticSetting` parancsmag egyes számú paraméterneveit kell használni. A következőt használó szkripteket:</span><span class="sxs-lookup"><span data-stu-id="33424-226">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="33424-227">A következőre kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="33424-227">Should be changed to</span></span>
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="33424-228">Az.Network (korábban AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="33424-228">Az.Network (previously AzureRM.Network)</span></span>
- <span data-ttu-id="33424-229">A `Get-AzServiceEndpointPolicyDefinition` parancsmag elavult `ResourceId` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-229">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="33424-230">A `PSVirtualNetwork` objektum elavult `EnableVmProtection` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-230">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="33424-231">Az elavult `Set-AzVirtualNetworkGatewayVpnClientConfig` parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-231">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="33424-232">A szkriptek a jövőben nem hozhatnak feldolgozási döntéseket e mezők értéke alapján.</span><span class="sxs-lookup"><span data-stu-id="33424-232">Scripts shoudl no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="33424-233">Az.OperationalInsights (korábban AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="33424-233">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>
- <span data-ttu-id="33424-234">A `Get-AzOperationalInsightsDataSource` alapértelmezett paraméterkészlete el lett távolítva. Mostantól a `ByWorkspaceNameByKind` az alapértelmezett paraméterkészlet.</span><span class="sxs-lookup"><span data-stu-id="33424-234">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="33424-235">Azokat a szkripteket, amelyek a következő használatával listázták az adatforrásokat:</span><span class="sxs-lookup"><span data-stu-id="33424-235">Scripts that listed data sources using</span></span>
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="33424-236">Úgy kell módosítani, hogy megadjanak egy altípust:</span><span class="sxs-lookup"><span data-stu-id="33424-236">Should be changed to specify a Kind</span></span>
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="33424-237">Az.RecoveryServices (korábban AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup és AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="33424-237">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>
- <span data-ttu-id="33424-238">A `New/Set-AzRecoveryServicesAsrPolicy` parancsmag `Encryption` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-238">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="33424-239">A `TargetStorageAccountName` paraméter megadása mostantól kötelező a `Restore-AzRecoveryServicesBackupItem` parancsmag felügyeltlemez-visszaállítási műveleteihez.</span><span class="sxs-lookup"><span data-stu-id="33424-239">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="33424-240">A `Restore-AzRecoveryServicesBackupItem` parancsmag `StorageAccountName` és `StorageAccountResourceGroupName` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-240">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="33424-241">A `Get-AzRecoveryServicesBackupContainer` parancsmag `Name` paramétere el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="33424-241">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="33424-242">Az.Resources (korábban AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="33424-242">Az.Resources (previously AzureRM.Resources)</span></span>
- <span data-ttu-id="33424-243">A `New/Set-AzPolicyAssignment` parancsmag `Sku` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-243">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="33424-244">A `New-AzADServicePrincipal` és `New-AzADSpCredential` parancsmag `Password` paramétere el lett távolítva. A jelszavak létrehozása automatikusan történik, a korábban jelszót biztosító szkripteket:</span><span class="sxs-lookup"><span data-stu-id="33424-244">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="33424-245">Úgy kell módosítani, hogy a jelszót a kimenetből kérjék le:</span><span class="sxs-lookup"><span data-stu-id="33424-245">Should be changed to retriedve the password from the output:</span></span>
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="33424-246">Az.ServiceFabric (korábban AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="33424-246">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>
- <span data-ttu-id="33424-247">Módosítottuk a következő parancsmag visszatérési típusait:</span><span class="sxs-lookup"><span data-stu-id="33424-247">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="33424-248">Az `ApplicationHealthPolicy` típus `SerivceTypeHealthPolicies` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-248">The property `SerivceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="33424-249">A `ClusterUpgradeDeltaHealthPolicy` típus `ApplicationHealthPolicies` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-249">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="33424-250">A `ClusterUpgradePolicy` típus `OverrideUserUpgradePolicy` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-250">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="33424-251">Ezek a módosítások a következő parancsmagokat érintik:</span><span class="sxs-lookup"><span data-stu-id="33424-251">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="33424-252">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="33424-252">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="33424-253">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="33424-253">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="33424-254">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="33424-254">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="33424-255">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="33424-255">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="33424-256">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="33424-256">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="33424-257">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="33424-257">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="33424-258">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="33424-258">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="33424-259">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="33424-259">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="33424-260">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="33424-260">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="33424-261">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="33424-261">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="33424-262">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="33424-262">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="33424-263">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="33424-263">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="33424-264">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="33424-264">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="33424-265">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="33424-265">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="33424-266">Az.Sql (korábban AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="33424-266">Az.Sql (previously AzureRM.Sql)</span></span>
- <span data-ttu-id="33424-267">A `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` parancsmag `State` és `ResourceId` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-267">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="33424-268">A következő, elavult parancsmagok el lettek távolítva: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing` és `Remove-AzSqlServerAuditing`.</span><span class="sxs-lookup"><span data-stu-id="33424-268">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="33424-269">A `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` parancsmag elavult `Current` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-269">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="33424-270">A `Get-AzSqlServerServiceObjective` parancsmag elavult `DatabaseName` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-270">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="33424-271">A `Set-AzSqlDatabaseDataMaskingPolicy` parancsmag elavult `PrivilegedLogin` paramétere el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-271">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="33424-272">Az.Storage (korábban Azure.Storage és AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="33424-272">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>
- <span data-ttu-id="33424-273">Annak érdekében, hogy létre lehessen hozni egy Oauth Storage-környezetet pusztán a tárfiók nevét használva, az új alapértelmezett paraméterkészlet a következő: `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="33424-273">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="33424-274">Például: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="33424-274">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="33424-275">A `Get-AzStorageUsage` parancsmagban kötelezővé vált a `Location` paraméter használata.</span><span class="sxs-lookup"><span data-stu-id="33424-275">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="33424-276">A Storage API-metódusok mostantól feladatalapú aszinkron mintát (TAP) használnak az egyidejű API-hívások helyett.</span><span class="sxs-lookup"><span data-stu-id="33424-276">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span>
#### <a name="1-blob-snapshot"></a><span data-ttu-id="33424-277">1. Blob-pillanatképek</span><span class="sxs-lookup"><span data-stu-id="33424-277">1. Blob Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="33424-278">Előtte:</span><span class="sxs-lookup"><span data-stu-id="33424-278">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a><span data-ttu-id="33424-279">Utána:</span><span class="sxs-lookup"><span data-stu-id="33424-279">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a><span data-ttu-id="33424-280">2. Megosztási pillanatképek</span><span class="sxs-lookup"><span data-stu-id="33424-280">2. Share Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="33424-281">Előtte:</span><span class="sxs-lookup"><span data-stu-id="33424-281">Before:</span></span>
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a><span data-ttu-id="33424-282">Utána:</span><span class="sxs-lookup"><span data-stu-id="33424-282">After:</span></span>
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a><span data-ttu-id="33424-283">3. Blob helyreállítható törlésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="33424-283">3. Undelete a soft delete blob</span></span>
##### <a name="before"></a><span data-ttu-id="33424-284">Előtte:</span><span class="sxs-lookup"><span data-stu-id="33424-284">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a><span data-ttu-id="33424-285">Utána:</span><span class="sxs-lookup"><span data-stu-id="33424-285">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a><span data-ttu-id="33424-286">4. Blobszint beállítása</span><span class="sxs-lookup"><span data-stu-id="33424-286">4. Set Blob Tier</span></span>
##### <a name="before"></a><span data-ttu-id="33424-287">Előtte:</span><span class="sxs-lookup"><span data-stu-id="33424-287">Before:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a><span data-ttu-id="33424-288">Utána:</span><span class="sxs-lookup"><span data-stu-id="33424-288">After:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="33424-289">Az.Websites (korábban AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="33424-289">Az.Websites (previously AzureRM.Websites)</span></span>
- <span data-ttu-id="33424-290">A `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` és `PSSite` objektum elavult tulajdonságai el lettek távolítva.</span><span class="sxs-lookup"><span data-stu-id="33424-290">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>