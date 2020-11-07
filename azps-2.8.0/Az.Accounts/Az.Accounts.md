---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 7eb19dfc45a954a9e23a3cc6c04190c3a1388547
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93665500"
---
# <span data-ttu-id="af98e-101">Az Accounts (fiókok) modul</span><span class="sxs-lookup"><span data-stu-id="af98e-101">Az.Accounts Module</span></span>
## <span data-ttu-id="af98e-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="af98e-102">Description</span></span>
<span data-ttu-id="af98e-103">Minden Azure-modul hitelesítő adatait és általános konfigurációját kezeli.</span><span class="sxs-lookup"><span data-stu-id="af98e-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="af98e-104">Az. accounts parancsmagok</span><span class="sxs-lookup"><span data-stu-id="af98e-104">Az.Accounts Cmdlets</span></span>
### [<span data-ttu-id="af98e-105">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="af98e-105">Add-AzEnvironment</span></span>](Add-AzEnvironment.md)
<span data-ttu-id="af98e-106">Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="af98e-106">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="af98e-107">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="af98e-107">Clear-AzContext</span></span>](Clear-AzContext.md)
<span data-ttu-id="af98e-108">Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="af98e-108">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="af98e-109">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="af98e-109">Clear-AzDefault</span></span>](Clear-AzDefault.md)
<span data-ttu-id="af98e-110">Törli a felhasználó által az aktuális környezetben beállított alapértékeket.</span><span class="sxs-lookup"><span data-stu-id="af98e-110">Clears the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="af98e-111">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="af98e-111">Connect-AzAccount</span></span>](Connect-AzAccount.md)
<span data-ttu-id="af98e-112">Csatlakozás az Azure-hoz hitelesített fiókkal az Azure Resource Manager parancsmag-kérésekkel való használathoz.</span><span class="sxs-lookup"><span data-stu-id="af98e-112">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

### [<span data-ttu-id="af98e-113">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="af98e-113">Disable-AzContextAutosave</span></span>](Disable-AzContextAutosave.md)
<span data-ttu-id="af98e-114">Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="af98e-114">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="af98e-115">A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait</span><span class="sxs-lookup"><span data-stu-id="af98e-115">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="af98e-116">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="af98e-116">Disable-AzDataCollection</span></span>](Disable-AzDataCollection.md)
<span data-ttu-id="af98e-117">A AzurePowerShell-parancsmagok fejlesztéséhez kimarad az adatok gyűjtése.</span><span class="sxs-lookup"><span data-stu-id="af98e-117">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="af98e-118">Az adatokat csak akkor gyűjti össze, ha kifejezetten bejelöli.</span><span class="sxs-lookup"><span data-stu-id="af98e-118">Data is not collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="af98e-119">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="af98e-119">Disable-AzureRmAlias</span></span>](Disable-AzureRmAlias.md)
<span data-ttu-id="af98e-120">Letiltja a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="af98e-120">Disables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="af98e-121">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="af98e-121">Disconnect-AzAccount</span></span>](Disconnect-AzAccount.md)
<span data-ttu-id="af98e-122">Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókkal társított összes hitelesítő adatot és kontextust.</span><span class="sxs-lookup"><span data-stu-id="af98e-122">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

### [<span data-ttu-id="af98e-123">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="af98e-123">Enable-AzContextAutosave</span></span>](Enable-AzContextAutosave.md)
<span data-ttu-id="af98e-124">A PowerShell-ablak megnyitásakor az Azure-hitelesítő adatok, a fiók és az előfizetési adatok menthetők és automatikusan betölthetők.</span><span class="sxs-lookup"><span data-stu-id="af98e-124">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="af98e-125">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="af98e-125">Enable-AzDataCollection</span></span>](Enable-AzDataCollection.md)
<span data-ttu-id="af98e-126">Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az AzurePowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="af98e-126">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="af98e-127">A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható.</span><span class="sxs-lookup"><span data-stu-id="af98e-127">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="af98e-128">Csak akkor gyűjtünk adatokat, ha kifejezetten bekapcsolta.</span><span class="sxs-lookup"><span data-stu-id="af98e-128">No data is collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="af98e-129">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="af98e-129">Enable-AzureRmAlias</span></span>](Enable-AzureRmAlias.md)
<span data-ttu-id="af98e-130">Engedélyezi a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="af98e-130">Enables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="af98e-131">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="af98e-131">Get-AzContext</span></span>](Get-AzContext.md)
<span data-ttu-id="af98e-132">Az Azure Resource Manager-kérések hitelesítéséhez használt metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="af98e-132">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="af98e-133">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="af98e-133">Get-AzContextAutosaveSetting</span></span>](Get-AzContextAutosaveSetting.md)
<span data-ttu-id="af98e-134">Metaadatok megjelenítése a környezeti mentés funkcióról, például hogy a környezet automatikusan mentve van-e, illetve hogy hol találhatók a mentett környezet-és hitelesítőadat-adatok.</span><span class="sxs-lookup"><span data-stu-id="af98e-134">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="af98e-135">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="af98e-135">Get-AzDefault</span></span>](Get-AzDefault.md)
<span data-ttu-id="af98e-136">A felhasználó által az aktuális környezetben beállított alapértékek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="af98e-136">Get the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="af98e-137">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="af98e-137">Get-AzEnvironment</span></span>](Get-AzEnvironment.md)
<span data-ttu-id="af98e-138">Az Azure Services egy példányának végpontját és metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="af98e-138">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="af98e-139">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="af98e-139">Get-AzProfile</span></span>](Get-AzProfile.md)
<span data-ttu-id="af98e-140">A telepített modulok által támogatott szolgáltatásprofilok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="af98e-140">Get the service profiles supported by installed modules.</span></span>

### [<span data-ttu-id="af98e-141">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="af98e-141">Get-AzSubscription</span></span>](Get-AzSubscription.md)
<span data-ttu-id="af98e-142">Az aktuális fiók által elérhető előfizetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="af98e-142">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="af98e-143">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="af98e-143">Get-AzTenant</span></span>](Get-AzTenant.md)
<span data-ttu-id="af98e-144">Az aktuális felhasználótól kapott bérlői fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="af98e-144">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="af98e-145">Importálás – AzContext</span><span class="sxs-lookup"><span data-stu-id="af98e-145">Import-AzContext</span></span>](Import-AzContext.md)
<span data-ttu-id="af98e-146">Azure-hitelesítési adatok betöltése egy fájlból.</span><span class="sxs-lookup"><span data-stu-id="af98e-146">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="af98e-147">Register-AzModule</span><span class="sxs-lookup"><span data-stu-id="af98e-147">Register-AzModule</span></span>](Register-AzModule.md)
<span data-ttu-id="af98e-148">CSAK belső használatra – futásidejű támogatás nyújtása az autorest bővítmények által generált parancsmagok számára.</span><span class="sxs-lookup"><span data-stu-id="af98e-148">FOR INTERNAL USE ONLY - Provide Runtime Support for AutoRest Generated cmdlets.</span></span>

### [<span data-ttu-id="af98e-149">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="af98e-149">Remove-AzContext</span></span>](Remove-AzContext.md)
<span data-ttu-id="af98e-150">Környezet eltávolítása az elérhető környezetek halmazból</span><span class="sxs-lookup"><span data-stu-id="af98e-150">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="af98e-151">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="af98e-151">Remove-AzEnvironment</span></span>](Remove-AzEnvironment.md)
<span data-ttu-id="af98e-152">Eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="af98e-152">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="af98e-153">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="af98e-153">Rename-AzContext</span></span>](Rename-AzContext.md)
<span data-ttu-id="af98e-154">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="af98e-154">Rename an Azure context.</span></span>  <span data-ttu-id="af98e-155">Alapértelmezés szerint a kontextusokat felhasználói fiók és előfizetés szerint nevezi el a program.</span><span class="sxs-lookup"><span data-stu-id="af98e-155">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="af98e-156">Feloldás – AzError</span><span class="sxs-lookup"><span data-stu-id="af98e-156">Resolve-AzError</span></span>](Resolve-AzError.md)
<span data-ttu-id="af98e-157">Részletes információk megjelenítése a PowerShell-hibákról, az Azure PowerShell hibáinak meghosszabbításával.</span><span class="sxs-lookup"><span data-stu-id="af98e-157">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="af98e-158">Mentés-AzContext</span><span class="sxs-lookup"><span data-stu-id="af98e-158">Save-AzContext</span></span>](Save-AzContext.md)
<span data-ttu-id="af98e-159">Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="af98e-159">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="af98e-160">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="af98e-160">Select-AzContext</span></span>](Select-AzContext.md)
<span data-ttu-id="af98e-161">Előfizetés és fiók kiválasztása az Azure PowerShell-parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="af98e-161">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="af98e-162">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="af98e-162">Select-AzProfile</span></span>](Select-AzProfile.md)
<span data-ttu-id="af98e-163">Több szolgáltatásprofilt támogató modulok esetén – a megadott szolgáltatásprofil megfelelő parancsmagok behelyezése.</span><span class="sxs-lookup"><span data-stu-id="af98e-163">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

### [<span data-ttu-id="af98e-164">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="af98e-164">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="af98e-165">Visszajelzést küld az Azure PowerShell-csoportnak egy sor interaktív utasítással.</span><span class="sxs-lookup"><span data-stu-id="af98e-165">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="af98e-166">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="af98e-166">Set-AzContext</span></span>](Set-AzContext.md)
<span data-ttu-id="af98e-167">A bérlői fiók, az előfizetés és a környezet beállítása az aktuális munkamenetben használható parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="af98e-167">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="af98e-168">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="af98e-168">Set-AzDefault</span></span>](Set-AzDefault.md)
<span data-ttu-id="af98e-169">Alapértelmezett érték beállítása az aktuális környezetben</span><span class="sxs-lookup"><span data-stu-id="af98e-169">Sets a default in the current context</span></span>

### [<span data-ttu-id="af98e-170">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="af98e-170">Set-AzEnvironment</span></span>](Set-AzEnvironment.md)
<span data-ttu-id="af98e-171">Az Azure-környezet tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="af98e-171">Sets properties for an Azure environment.</span></span>

### [<span data-ttu-id="af98e-172">Eltávolítás – AzureRm</span><span class="sxs-lookup"><span data-stu-id="af98e-172">Uninstall-AzureRm</span></span>](Uninstall-AzureRm.md)
<span data-ttu-id="af98e-173">Eltávolítja az összes AzureRm-modult egy gépről.</span><span class="sxs-lookup"><span data-stu-id="af98e-173">Removes all AzureRm modules from a machine.</span></span>

