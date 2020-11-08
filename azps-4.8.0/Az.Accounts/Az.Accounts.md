---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: d15e053e8801c292add5a80e04726f1eeb1181fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180700"
---
# <span data-ttu-id="1cc76-101">Az Accounts (fiókok) modul</span><span class="sxs-lookup"><span data-stu-id="1cc76-101">Az.Accounts Module</span></span>
## <span data-ttu-id="1cc76-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cc76-102">Description</span></span>
<span data-ttu-id="1cc76-103">Minden Azure-modul hitelesítő adatait és általános konfigurációját kezeli.</span><span class="sxs-lookup"><span data-stu-id="1cc76-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="1cc76-104">Az. accounts parancsmagok</span><span class="sxs-lookup"><span data-stu-id="1cc76-104">Az.Accounts Cmdlets</span></span>
### [<span data-ttu-id="1cc76-105">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1cc76-105">Add-AzEnvironment</span></span>](Add-AzEnvironment.md)
<span data-ttu-id="1cc76-106">Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="1cc76-106">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="1cc76-107">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="1cc76-107">Clear-AzContext</span></span>](Clear-AzContext.md)
<span data-ttu-id="1cc76-108">Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1cc76-108">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="1cc76-109">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="1cc76-109">Clear-AzDefault</span></span>](Clear-AzDefault.md)
<span data-ttu-id="1cc76-110">Törli a felhasználó által az aktuális környezetben beállított alapértékeket.</span><span class="sxs-lookup"><span data-stu-id="1cc76-110">Clears the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="1cc76-111">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="1cc76-111">Connect-AzAccount</span></span>](Connect-AzAccount.md)
<span data-ttu-id="1cc76-112">Csatlakozás az Azure-hoz hitelesített fiókkal a PowerShell-modulokból származó parancsmagokkal való használathoz.</span><span class="sxs-lookup"><span data-stu-id="1cc76-112">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

### [<span data-ttu-id="1cc76-113">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="1cc76-113">Disable-AzContextAutosave</span></span>](Disable-AzContextAutosave.md)
<span data-ttu-id="1cc76-114">Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="1cc76-114">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="1cc76-115">A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait</span><span class="sxs-lookup"><span data-stu-id="1cc76-115">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="1cc76-116">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="1cc76-116">Disable-AzDataCollection</span></span>](Disable-AzDataCollection.md)
<span data-ttu-id="1cc76-117">Az Azure PowerShell-parancsmagok fejlesztésére az adatok gyűjtésének kijavítása.</span><span class="sxs-lookup"><span data-stu-id="1cc76-117">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="1cc76-118">Az adatokat alapértelmezés szerint gyűjtjük, hacsak nem kifejezetten kikapcsolja.</span><span class="sxs-lookup"><span data-stu-id="1cc76-118">Data is collected by default unless you explicitly opt out.</span></span>

### [<span data-ttu-id="1cc76-119">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="1cc76-119">Disable-AzureRmAlias</span></span>](Disable-AzureRmAlias.md)
<span data-ttu-id="1cc76-120">Letiltja a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="1cc76-120">Disables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="1cc76-121">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="1cc76-121">Disconnect-AzAccount</span></span>](Disconnect-AzAccount.md)
<span data-ttu-id="1cc76-122">Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókkal társított összes hitelesítő adatot és kontextust.</span><span class="sxs-lookup"><span data-stu-id="1cc76-122">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

### [<span data-ttu-id="1cc76-123">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="1cc76-123">Enable-AzContextAutosave</span></span>](Enable-AzContextAutosave.md)
<span data-ttu-id="1cc76-124">A PowerShell-ablak megnyitásakor az Azure-hitelesítő adatok, a fiók és az előfizetési adatok menthetők és automatikusan betölthetők.</span><span class="sxs-lookup"><span data-stu-id="1cc76-124">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="1cc76-125">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="1cc76-125">Enable-AzDataCollection</span></span>](Enable-AzDataCollection.md)
<span data-ttu-id="1cc76-126">Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az Azure PowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="1cc76-126">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="1cc76-127">A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható.</span><span class="sxs-lookup"><span data-stu-id="1cc76-127">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="1cc76-128">Az adatokat alapértelmezés szerint gyűjtjük, hacsak nem kifejezetten kikapcsolja.</span><span class="sxs-lookup"><span data-stu-id="1cc76-128">Data is collected by default unless you explicitly opt out.</span></span>

### [<span data-ttu-id="1cc76-129">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="1cc76-129">Enable-AzureRmAlias</span></span>](Enable-AzureRmAlias.md)
<span data-ttu-id="1cc76-130">Engedélyezi a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="1cc76-130">Enables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="1cc76-131">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="1cc76-131">Get-AzContext</span></span>](Get-AzContext.md)
<span data-ttu-id="1cc76-132">Az Azure Resource Manager-kérések hitelesítéséhez használt metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1cc76-132">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="1cc76-133">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="1cc76-133">Get-AzContextAutosaveSetting</span></span>](Get-AzContextAutosaveSetting.md)
<span data-ttu-id="1cc76-134">Metaadatok megjelenítése a környezeti mentés funkcióról, például hogy a környezet automatikusan mentve van-e, illetve hogy hol találhatók a mentett környezet-és hitelesítőadat-adatok.</span><span class="sxs-lookup"><span data-stu-id="1cc76-134">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="1cc76-135">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="1cc76-135">Get-AzDefault</span></span>](Get-AzDefault.md)
<span data-ttu-id="1cc76-136">A felhasználó által az aktuális környezetben beállított alapértékek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="1cc76-136">Get the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="1cc76-137">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1cc76-137">Get-AzEnvironment</span></span>](Get-AzEnvironment.md)
<span data-ttu-id="1cc76-138">Az Azure Services egy példányának végpontját és metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1cc76-138">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="1cc76-139">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="1cc76-139">Get-AzProfile</span></span>](Get-AzProfile.md)
<span data-ttu-id="1cc76-140">A telepített modulok által támogatott szolgáltatásprofilok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="1cc76-140">Get the service profiles supported by installed modules.</span></span>

### [<span data-ttu-id="1cc76-141">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="1cc76-141">Get-AzSubscription</span></span>](Get-AzSubscription.md)
<span data-ttu-id="1cc76-142">Az aktuális fiók által elérhető előfizetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="1cc76-142">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="1cc76-143">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="1cc76-143">Get-AzTenant</span></span>](Get-AzTenant.md)
<span data-ttu-id="1cc76-144">Az aktuális felhasználótól kapott bérlői fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="1cc76-144">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="1cc76-145">Importálás – AzContext</span><span class="sxs-lookup"><span data-stu-id="1cc76-145">Import-AzContext</span></span>](Import-AzContext.md)
<span data-ttu-id="1cc76-146">Azure-hitelesítési adatok betöltése egy fájlból.</span><span class="sxs-lookup"><span data-stu-id="1cc76-146">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="1cc76-147">Meghívó-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="1cc76-147">Invoke-AzRestMethod</span></span>](Invoke-AzRestMethod.md)
<span data-ttu-id="1cc76-148">HTTP-kérés létesítése és végrehajtása csak az Azure erőforrás-kezelési végponttal</span><span class="sxs-lookup"><span data-stu-id="1cc76-148">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

### [<span data-ttu-id="1cc76-149">Register-AzModule</span><span class="sxs-lookup"><span data-stu-id="1cc76-149">Register-AzModule</span></span>](Register-AzModule.md)
<span data-ttu-id="1cc76-150">CSAK belső használatra – futásidejű támogatás nyújtása az autorest bővítmények által generált parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="1cc76-150">FOR INTERNAL USE ONLY - Provide Runtime Support for AutoRest Generated cmdlets</span></span>

### [<span data-ttu-id="1cc76-151">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="1cc76-151">Remove-AzContext</span></span>](Remove-AzContext.md)
<span data-ttu-id="1cc76-152">Környezet eltávolítása az elérhető környezetek halmazból</span><span class="sxs-lookup"><span data-stu-id="1cc76-152">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="1cc76-153">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1cc76-153">Remove-AzEnvironment</span></span>](Remove-AzEnvironment.md)
<span data-ttu-id="1cc76-154">Eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="1cc76-154">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="1cc76-155">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="1cc76-155">Rename-AzContext</span></span>](Rename-AzContext.md)
<span data-ttu-id="1cc76-156">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="1cc76-156">Rename an Azure context.</span></span>  <span data-ttu-id="1cc76-157">Alapértelmezés szerint a kontextusokat felhasználói fiók és előfizetés szerint nevezi el a program.</span><span class="sxs-lookup"><span data-stu-id="1cc76-157">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="1cc76-158">Feloldás – AzError</span><span class="sxs-lookup"><span data-stu-id="1cc76-158">Resolve-AzError</span></span>](Resolve-AzError.md)
<span data-ttu-id="1cc76-159">Részletes információk megjelenítése a PowerShell-hibákról, az Azure PowerShell hibáinak meghosszabbításával.</span><span class="sxs-lookup"><span data-stu-id="1cc76-159">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="1cc76-160">Mentés-AzContext</span><span class="sxs-lookup"><span data-stu-id="1cc76-160">Save-AzContext</span></span>](Save-AzContext.md)
<span data-ttu-id="1cc76-161">Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="1cc76-161">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="1cc76-162">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="1cc76-162">Select-AzContext</span></span>](Select-AzContext.md)
<span data-ttu-id="1cc76-163">Előfizetés és fiók kiválasztása az Azure PowerShell-parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="1cc76-163">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="1cc76-164">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="1cc76-164">Select-AzProfile</span></span>](Select-AzProfile.md)
<span data-ttu-id="1cc76-165">Több szolgáltatásprofilt támogató modulok esetén – a megadott szolgáltatásprofil megfelelő parancsmagok behelyezése.</span><span class="sxs-lookup"><span data-stu-id="1cc76-165">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

### [<span data-ttu-id="1cc76-166">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="1cc76-166">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="1cc76-167">Visszajelzést küld az Azure PowerShell-csoportnak egy sor interaktív utasítással.</span><span class="sxs-lookup"><span data-stu-id="1cc76-167">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="1cc76-168">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="1cc76-168">Set-AzContext</span></span>](Set-AzContext.md)
<span data-ttu-id="1cc76-169">A bérlői fiók, az előfizetés és a környezet beállítása az aktuális munkamenetben használható parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="1cc76-169">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="1cc76-170">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="1cc76-170">Set-AzDefault</span></span>](Set-AzDefault.md)
<span data-ttu-id="1cc76-171">Alapértelmezett érték beállítása az aktuális környezetben</span><span class="sxs-lookup"><span data-stu-id="1cc76-171">Sets a default in the current context</span></span>

### [<span data-ttu-id="1cc76-172">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1cc76-172">Set-AzEnvironment</span></span>](Set-AzEnvironment.md)
<span data-ttu-id="1cc76-173">Az Azure-környezet tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="1cc76-173">Sets properties for an Azure environment.</span></span>

### [<span data-ttu-id="1cc76-174">Eltávolítás – AzureRm</span><span class="sxs-lookup"><span data-stu-id="1cc76-174">Uninstall-AzureRm</span></span>](Uninstall-AzureRm.md)
<span data-ttu-id="1cc76-175">Eltávolítja az összes AzureRm-modult egy gépről.</span><span class="sxs-lookup"><span data-stu-id="1cc76-175">Removes all AzureRm modules from a machine.</span></span>

