---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 6be8097fb649b6ebdec1c6dc5f28f2a06c572d35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327847"
---
# <span data-ttu-id="5af9c-101">Az.Accounts modul</span><span class="sxs-lookup"><span data-stu-id="5af9c-101">Az.Accounts Module</span></span>
## <span data-ttu-id="5af9c-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="5af9c-102">Description</span></span>
<span data-ttu-id="5af9c-103">Kezeli az összes Azure-modul hitelesítő adatait és közös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5af9c-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="5af9c-104">Az.Accounts parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5af9c-104">Az.Accounts Cmdlets</span></span>
### [<span data-ttu-id="5af9c-105">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="5af9c-105">Add-AzEnvironment</span></span>](Add-AzEnvironment.md)
<span data-ttu-id="5af9c-106">Végpontokat és metaadatokat ad hozzá az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="5af9c-106">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="5af9c-107">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="5af9c-107">Clear-AzContext</span></span>](Clear-AzContext.md)
<span data-ttu-id="5af9c-108">Távolítsa el az Azure-beli hitelesítő adatokat, fiókadatokat és előfizetési adatokat.</span><span class="sxs-lookup"><span data-stu-id="5af9c-108">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="5af9c-109">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="5af9c-109">Clear-AzDefault</span></span>](Clear-AzDefault.md)
<span data-ttu-id="5af9c-110">Törli a felhasználó által az aktuális környezetben beállított alapértelmezett értékeket.</span><span class="sxs-lookup"><span data-stu-id="5af9c-110">Clears the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="5af9c-111">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="5af9c-111">Connect-AzAccount</span></span>](Connect-AzAccount.md)
<span data-ttu-id="5af9c-112">Csatlakozzon az Azure-hoz egy hitelesített fiókkal az Az PowerShell-modulok parancsmagjaival való használathoz.</span><span class="sxs-lookup"><span data-stu-id="5af9c-112">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

### [<span data-ttu-id="5af9c-113">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="5af9c-113">Disable-AzContextAutosave</span></span>](Disable-AzContextAutosave.md)
<span data-ttu-id="5af9c-114">Kapcsolja ki az Azure-beli hitelesítő adatok automatikus mentését.</span><span class="sxs-lookup"><span data-stu-id="5af9c-114">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="5af9c-115">A bejelentkezési adatok a PowerShell-ablak következő megnyitásakor elfelejtkednek</span><span class="sxs-lookup"><span data-stu-id="5af9c-115">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="5af9c-116">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="5af9c-116">Disable-AzDataCollection</span></span>](Disable-AzDataCollection.md)
<span data-ttu-id="5af9c-117">Az Azure PowerShell-parancsmagok fejlesztése érdekében leiratkozás az adatgyűjtésről.</span><span class="sxs-lookup"><span data-stu-id="5af9c-117">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5af9c-118">Az adatokat alapértelmezés szerint gyűjtjük, hacsak Ön kifejezetten le nem tiltja.</span><span class="sxs-lookup"><span data-stu-id="5af9c-118">Data is collected by default unless you explicitly opt out.</span></span>

### [<span data-ttu-id="5af9c-119">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="5af9c-119">Disable-AzureRmAlias</span></span>](Disable-AzureRmAlias.md)
<span data-ttu-id="5af9c-120">Letiltja az AzureRm előtag-aliasokat az Az modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="5af9c-120">Disables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="5af9c-121">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="5af9c-121">Disconnect-AzAccount</span></span>](Disconnect-AzAccount.md)
<span data-ttu-id="5af9c-122">Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja a fiókkal társított összes hitelesítő adatokat és kontextust.</span><span class="sxs-lookup"><span data-stu-id="5af9c-122">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

### [<span data-ttu-id="5af9c-123">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="5af9c-123">Enable-AzContextAutosave</span></span>](Enable-AzContextAutosave.md)
<span data-ttu-id="5af9c-124">A PowerShell-ablak megnyitásakor a rendszer menti és automatikusan betölti az Azure-beli hitelesítő adatokat, fiók- és előfizetésadatokat.</span><span class="sxs-lookup"><span data-stu-id="5af9c-124">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="5af9c-125">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="5af9c-125">Enable-AzDataCollection</span></span>](Enable-AzDataCollection.md)
<span data-ttu-id="5af9c-126">Lehetővé teszi, hogy az Azure PowerShell adatokat gyűjtsön az Azure PowerShell-parancsmagok felhasználói élményének javításához.</span><span class="sxs-lookup"><span data-stu-id="5af9c-126">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5af9c-127">A parancsmag végrehajtása az aktuális gép aktuális felhasználója számára is be fog jelentkezni az adatgyűjtésbe.</span><span class="sxs-lookup"><span data-stu-id="5af9c-127">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="5af9c-128">Az adatokat alapértelmezés szerint gyűjtjük, hacsak Ön kifejezetten nem tiltja le.</span><span class="sxs-lookup"><span data-stu-id="5af9c-128">Data is collected by default unless you explicitly opt out.</span></span>

### [<span data-ttu-id="5af9c-129">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="5af9c-129">Enable-AzureRmAlias</span></span>](Enable-AzureRmAlias.md)
<span data-ttu-id="5af9c-130">Engedélyezi az AzureRm előtag-aliasokat az Az-modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="5af9c-130">Enables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="5af9c-131">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="5af9c-131">Get-AzAccessToken</span></span>](Get-AzAccessToken.md)
<span data-ttu-id="5af9c-132">Nyers hozzáférési jogkivonat beszerzése.</span><span class="sxs-lookup"><span data-stu-id="5af9c-132">Get raw access token.</span></span>

### [<span data-ttu-id="5af9c-133">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="5af9c-133">Get-AzContext</span></span>](Get-AzContext.md)
<span data-ttu-id="5af9c-134">Az Azure Resource Manager-kérelmek hitelesítéséhez használt metaadatok bekérése.</span><span class="sxs-lookup"><span data-stu-id="5af9c-134">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="5af9c-135">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="5af9c-135">Get-AzContextAutosaveSetting</span></span>](Get-AzContextAutosaveSetting.md)
<span data-ttu-id="5af9c-136">A környezet automatikus mentésének funkciójának metaadatainak megjelenítése, beleértve a környezet automatikus mentésének és a mentett környezet és hitelesítő adatok helyének megjelenítését.</span><span class="sxs-lookup"><span data-stu-id="5af9c-136">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="5af9c-137">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="5af9c-137">Get-AzDefault</span></span>](Get-AzDefault.md)
<span data-ttu-id="5af9c-138">Szerezze be a felhasználó által az aktuális környezetben beállított alapértelmezett értékeket.</span><span class="sxs-lookup"><span data-stu-id="5af9c-138">Get the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="5af9c-139">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="5af9c-139">Get-AzEnvironment</span></span>](Get-AzEnvironment.md)
<span data-ttu-id="5af9c-140">Végpontok és metaadatok lekérte az Azure-szolgáltatások egy példányát.</span><span class="sxs-lookup"><span data-stu-id="5af9c-140">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="5af9c-141">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="5af9c-141">Get-AzSubscription</span></span>](Get-AzSubscription.md)
<span data-ttu-id="5af9c-142">Szerezze be az aktuális fiók által elérhető előfizetéseket.</span><span class="sxs-lookup"><span data-stu-id="5af9c-142">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="5af9c-143">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="5af9c-143">Get-AzTenant</span></span>](Get-AzTenant.md)
<span data-ttu-id="5af9c-144">Az aktuális felhasználóhoz engedélyezett bérlőket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5af9c-144">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="5af9c-145">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="5af9c-145">Import-AzContext</span></span>](Import-AzContext.md)
<span data-ttu-id="5af9c-146">Egy fájlból betölti az Azure-hitelesítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="5af9c-146">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="5af9c-147">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="5af9c-147">Invoke-AzRestMethod</span></span>](Invoke-AzRestMethod.md)
<span data-ttu-id="5af9c-148">Kizárólag Azure-erőforrás-kezelési végpontra vonatkozó HTTP-kérések építése és végrehajtása</span><span class="sxs-lookup"><span data-stu-id="5af9c-148">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

### [<span data-ttu-id="5af9c-149">Register-AzModule</span><span class="sxs-lookup"><span data-stu-id="5af9c-149">Register-AzModule</span></span>](Register-AzModule.md)
<span data-ttu-id="5af9c-150">CSAK BELSŐ HASZNÁLAT ESETÉN – Futásidejű támogatás az AutoRest által létrehozott parancsmagok számára</span><span class="sxs-lookup"><span data-stu-id="5af9c-150">FOR INTERNAL USE ONLY - Provide Runtime Support for AutoRest Generated cmdlets</span></span>

### [<span data-ttu-id="5af9c-151">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="5af9c-151">Remove-AzContext</span></span>](Remove-AzContext.md)
<span data-ttu-id="5af9c-152">Környezet eltávolítása az elérhető környezetek készletből</span><span class="sxs-lookup"><span data-stu-id="5af9c-152">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="5af9c-153">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="5af9c-153">Remove-AzEnvironment</span></span>](Remove-AzEnvironment.md)
<span data-ttu-id="5af9c-154">Eltávolítja az adott Azure-példányhoz való csatlakozás végpontját és metaadatait.</span><span class="sxs-lookup"><span data-stu-id="5af9c-154">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="5af9c-155">Átnevezés-AzContext</span><span class="sxs-lookup"><span data-stu-id="5af9c-155">Rename-AzContext</span></span>](Rename-AzContext.md)
<span data-ttu-id="5af9c-156">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="5af9c-156">Rename an Azure context.</span></span>  <span data-ttu-id="5af9c-157">Az alapértelmezett környezetek neve felhasználói fiók és előfizetés szerint van elnevezve.</span><span class="sxs-lookup"><span data-stu-id="5af9c-157">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="5af9c-158">Resolve-AzError</span><span class="sxs-lookup"><span data-stu-id="5af9c-158">Resolve-AzError</span></span>](Resolve-AzError.md)
<span data-ttu-id="5af9c-159">Részletes információkat jelenít meg a PowerShell-hibákról, az Azure PowerShell-hibák részletes adataival együtt.</span><span class="sxs-lookup"><span data-stu-id="5af9c-159">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="5af9c-160">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="5af9c-160">Save-AzContext</span></span>](Save-AzContext.md)
<span data-ttu-id="5af9c-161">Menti az aktuális hitelesítési adatokat más PowerShell-munkamenetekben való használatra.</span><span class="sxs-lookup"><span data-stu-id="5af9c-161">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="5af9c-162">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="5af9c-162">Select-AzContext</span></span>](Select-AzContext.md)
<span data-ttu-id="5af9c-163">Válassza ki a célként kijelölni kívánt előfizetést és fiókot az Azure PowerShell-parancsmagokkal</span><span class="sxs-lookup"><span data-stu-id="5af9c-163">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="5af9c-164">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="5af9c-164">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="5af9c-165">Visszajelzést küld az Azure PowerShell-csapatnak egy interaktív üzenetcsoporton keresztül.</span><span class="sxs-lookup"><span data-stu-id="5af9c-165">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="5af9c-166">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="5af9c-166">Set-AzContext</span></span>](Set-AzContext.md)
<span data-ttu-id="5af9c-167">Beállítja a parancsmagok aktuális munkamenetben használt bérlői, előfizetési és környezetét.</span><span class="sxs-lookup"><span data-stu-id="5af9c-167">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="5af9c-168">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="5af9c-168">Set-AzDefault</span></span>](Set-AzDefault.md)
<span data-ttu-id="5af9c-169">Alapértelmezett beállítás az aktuális környezetben</span><span class="sxs-lookup"><span data-stu-id="5af9c-169">Sets a default in the current context</span></span>

### [<span data-ttu-id="5af9c-170">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="5af9c-170">Set-AzEnvironment</span></span>](Set-AzEnvironment.md)
<span data-ttu-id="5af9c-171">Beállítja egy Azure-környezet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="5af9c-171">Sets properties for an Azure environment.</span></span>

### [<span data-ttu-id="5af9c-172">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="5af9c-172">Uninstall-AzureRm</span></span>](Uninstall-AzureRm.md)
<span data-ttu-id="5af9c-173">Eltávolítja az összes AzureRm-modult egy gépről.</span><span class="sxs-lookup"><span data-stu-id="5af9c-173">Removes all AzureRm modules from a machine.</span></span>

