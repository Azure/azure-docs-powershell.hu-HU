---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 134ce4c55d29d5f0dc6c46a1d0495f392694386f
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93657825"
---
# <span data-ttu-id="402a0-101">Az Accounts (fiókok) modul</span><span class="sxs-lookup"><span data-stu-id="402a0-101">Az.Accounts Module</span></span>
## <span data-ttu-id="402a0-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="402a0-102">Description</span></span>
<span data-ttu-id="402a0-103">Minden Azure-modul hitelesítő adatait és általános konfigurációját kezeli.</span><span class="sxs-lookup"><span data-stu-id="402a0-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="402a0-104">Az. accounts parancsmagok</span><span class="sxs-lookup"><span data-stu-id="402a0-104">Az.Accounts Cmdlets</span></span>
### [<span data-ttu-id="402a0-105">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="402a0-105">Add-AzEnvironment</span></span>](Add-AzEnvironment.md)
<span data-ttu-id="402a0-106">Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="402a0-106">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="402a0-107">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="402a0-107">Clear-AzContext</span></span>](Clear-AzContext.md)
<span data-ttu-id="402a0-108">Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="402a0-108">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="402a0-109">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="402a0-109">Clear-AzDefault</span></span>](Clear-AzDefault.md)
<span data-ttu-id="402a0-110">Törli a felhasználó által az aktuális környezetben beállított alapértékeket.</span><span class="sxs-lookup"><span data-stu-id="402a0-110">Clears the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="402a0-111">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="402a0-111">Connect-AzAccount</span></span>](Connect-AzAccount.md)
<span data-ttu-id="402a0-112">Csatlakozás az Azure-hoz hitelesített fiókkal az Azure Resource Manager parancsmag-kérésekkel való használathoz.</span><span class="sxs-lookup"><span data-stu-id="402a0-112">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

### [<span data-ttu-id="402a0-113">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="402a0-113">Disable-AzContextAutosave</span></span>](Disable-AzContextAutosave.md)
<span data-ttu-id="402a0-114">Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="402a0-114">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="402a0-115">A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait</span><span class="sxs-lookup"><span data-stu-id="402a0-115">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="402a0-116">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="402a0-116">Disable-AzDataCollection</span></span>](Disable-AzDataCollection.md)
<span data-ttu-id="402a0-117">A AzurePowerShell-parancsmagok fejlesztéséhez kimarad az adatok gyűjtése.</span><span class="sxs-lookup"><span data-stu-id="402a0-117">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="402a0-118">Az adatokat csak akkor gyűjti össze, ha kifejezetten bejelöli.</span><span class="sxs-lookup"><span data-stu-id="402a0-118">Data is not collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="402a0-119">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="402a0-119">Disable-AzureRmAlias</span></span>](Disable-AzureRmAlias.md)
<span data-ttu-id="402a0-120">Letiltja a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="402a0-120">Disables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="402a0-121">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="402a0-121">Disconnect-AzAccount</span></span>](Disconnect-AzAccount.md)
<span data-ttu-id="402a0-122">Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókkal társított összes hitelesítő adatot és kontextust.</span><span class="sxs-lookup"><span data-stu-id="402a0-122">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

### [<span data-ttu-id="402a0-123">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="402a0-123">Enable-AzContextAutosave</span></span>](Enable-AzContextAutosave.md)
<span data-ttu-id="402a0-124">A PowerShell-ablak megnyitásakor az Azure-hitelesítő adatok, a fiók és az előfizetési adatok menthetők és automatikusan betölthetők.</span><span class="sxs-lookup"><span data-stu-id="402a0-124">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="402a0-125">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="402a0-125">Enable-AzDataCollection</span></span>](Enable-AzDataCollection.md)
<span data-ttu-id="402a0-126">Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az AzurePowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="402a0-126">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="402a0-127">A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható.</span><span class="sxs-lookup"><span data-stu-id="402a0-127">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="402a0-128">Csak akkor gyűjtünk adatokat, ha kifejezetten bekapcsolta.</span><span class="sxs-lookup"><span data-stu-id="402a0-128">No data is collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="402a0-129">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="402a0-129">Enable-AzureRmAlias</span></span>](Enable-AzureRmAlias.md)
<span data-ttu-id="402a0-130">Engedélyezi a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="402a0-130">Enables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="402a0-131">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="402a0-131">Get-AzContext</span></span>](Get-AzContext.md)
<span data-ttu-id="402a0-132">Az Azure Resource Manager-kérések hitelesítéséhez használt metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="402a0-132">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="402a0-133">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="402a0-133">Get-AzContextAutosaveSetting</span></span>](Get-AzContextAutosaveSetting.md)
<span data-ttu-id="402a0-134">Metaadatok megjelenítése a környezeti mentés funkcióról, például hogy a környezet automatikusan mentve van-e, illetve hogy hol találhatók a mentett környezet-és hitelesítőadat-adatok.</span><span class="sxs-lookup"><span data-stu-id="402a0-134">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="402a0-135">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="402a0-135">Get-AzDefault</span></span>](Get-AzDefault.md)
<span data-ttu-id="402a0-136">A felhasználó által az aktuális környezetben beállított alapértékek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="402a0-136">Get the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="402a0-137">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="402a0-137">Get-AzEnvironment</span></span>](Get-AzEnvironment.md)
<span data-ttu-id="402a0-138">Az Azure Services egy példányának végpontját és metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="402a0-138">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="402a0-139">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="402a0-139">Get-AzSubscription</span></span>](Get-AzSubscription.md)
<span data-ttu-id="402a0-140">Az aktuális fiók által elérhető előfizetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="402a0-140">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="402a0-141">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="402a0-141">Get-AzTenant</span></span>](Get-AzTenant.md)
<span data-ttu-id="402a0-142">Az aktuális felhasználótól kapott bérlői fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="402a0-142">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="402a0-143">Importálás – AzContext</span><span class="sxs-lookup"><span data-stu-id="402a0-143">Import-AzContext</span></span>](Import-AzContext.md)
<span data-ttu-id="402a0-144">Azure-hitelesítési adatok betöltése egy fájlból.</span><span class="sxs-lookup"><span data-stu-id="402a0-144">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="402a0-145">Register-AzModule</span><span class="sxs-lookup"><span data-stu-id="402a0-145">Register-AzModule</span></span>](Register-AzModule.md)
<span data-ttu-id="402a0-146">Csak belső parancsmag támogatása az autorest bővítmények által generált parancsmagok futtatásához.</span><span class="sxs-lookup"><span data-stu-id="402a0-146">Internal-only cmdlet that provides runtime support for AUtoRest generated cmdlets.</span></span>

### [<span data-ttu-id="402a0-147">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="402a0-147">Remove-AzContext</span></span>](Remove-AzContext.md)
<span data-ttu-id="402a0-148">Környezet eltávolítása az elérhető környezetek halmazból</span><span class="sxs-lookup"><span data-stu-id="402a0-148">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="402a0-149">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="402a0-149">Remove-AzEnvironment</span></span>](Remove-AzEnvironment.md)
<span data-ttu-id="402a0-150">Eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="402a0-150">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="402a0-151">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="402a0-151">Rename-AzContext</span></span>](Rename-AzContext.md)
<span data-ttu-id="402a0-152">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="402a0-152">Rename an Azure context.</span></span>  <span data-ttu-id="402a0-153">Alapértelmezés szerint a kontextusokat felhasználói fiók és előfizetés szerint nevezi el a program.</span><span class="sxs-lookup"><span data-stu-id="402a0-153">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="402a0-154">Feloldás – AzError</span><span class="sxs-lookup"><span data-stu-id="402a0-154">Resolve-AzError</span></span>](Resolve-AzError.md)
<span data-ttu-id="402a0-155">Részletes információk megjelenítése a PowerShell-hibákról, az Azure PowerShell hibáinak meghosszabbításával.</span><span class="sxs-lookup"><span data-stu-id="402a0-155">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="402a0-156">Mentés-AzContext</span><span class="sxs-lookup"><span data-stu-id="402a0-156">Save-AzContext</span></span>](Save-AzContext.md)
<span data-ttu-id="402a0-157">Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="402a0-157">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="402a0-158">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="402a0-158">Select-AzContext</span></span>](Select-AzContext.md)
<span data-ttu-id="402a0-159">Előfizetés és fiók kiválasztása az Azure PowerShell-parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="402a0-159">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="402a0-160">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="402a0-160">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="402a0-161">Visszajelzést küld az Azure PowerShell-csoportnak egy sor interaktív utasítással.</span><span class="sxs-lookup"><span data-stu-id="402a0-161">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="402a0-162">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="402a0-162">Set-AzContext</span></span>](Set-AzContext.md)
<span data-ttu-id="402a0-163">A bérlői fiók, az előfizetés és a környezet beállítása az aktuális munkamenetben használható parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="402a0-163">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="402a0-164">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="402a0-164">Set-AzDefault</span></span>](Set-AzDefault.md)
<span data-ttu-id="402a0-165">Alapértelmezett érték beállítása az aktuális környezetben</span><span class="sxs-lookup"><span data-stu-id="402a0-165">Sets a default in the current context</span></span>

### [<span data-ttu-id="402a0-166">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="402a0-166">Set-AzEnvironment</span></span>](Set-AzEnvironment.md)
<span data-ttu-id="402a0-167">Az Azure-környezet tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="402a0-167">Sets properties for an Azure environment.</span></span>

### [<span data-ttu-id="402a0-168">Eltávolítás – AzureRm</span><span class="sxs-lookup"><span data-stu-id="402a0-168">Uninstall-AzureRm</span></span>](Uninstall-AzureRm.md)
<span data-ttu-id="402a0-169">Eltávolítja az összes AzureRm-modult egy gépről.</span><span class="sxs-lookup"><span data-stu-id="402a0-169">Removes all AzureRm modules from a machine.</span></span>

