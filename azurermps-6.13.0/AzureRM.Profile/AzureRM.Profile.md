---
Module Name: AzureRM.Profile
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
ms.openlocfilehash: b9aa5f188d2c4c0167068d304487a0a7d4c7ea2d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490559"
---
# <span data-ttu-id="a667e-101">AzureRM. profil modul</span><span class="sxs-lookup"><span data-stu-id="a667e-101">AzureRM.Profile Module</span></span>
## <span data-ttu-id="a667e-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="a667e-102">Description</span></span>
<span data-ttu-id="a667e-103">Minden Azure-modul hitelesítő adatait és általános konfigurációját kezeli.</span><span class="sxs-lookup"><span data-stu-id="a667e-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="a667e-104">AzureRM. profil parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a667e-104">AzureRM.Profile Cmdlets</span></span>
### [<span data-ttu-id="a667e-105">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="a667e-105">Add-AzureRmEnvironment</span></span>](Add-AzureRmEnvironment.md)
<span data-ttu-id="a667e-106">Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="a667e-106">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="a667e-107">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a667e-107">Clear-AzureRmContext</span></span>](Clear-AzureRmContext.md)
<span data-ttu-id="a667e-108">Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a667e-108">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="a667e-109">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="a667e-109">Clear-AzureRmDefault</span></span>](Clear-AzureRmDefault.md)
<span data-ttu-id="a667e-110">Törli a felhasználó által az aktuális környezetben beállított alapértékeket.</span><span class="sxs-lookup"><span data-stu-id="a667e-110">Clears the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="a667e-111">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="a667e-111">Connect-AzureRmAccount</span></span>](Connect-AzureRmAccount.md)
<span data-ttu-id="a667e-112">Csatlakozás az Azure-hoz hitelesített fiókkal az Azure Resource Manager parancsmag-kérésekkel való használathoz.</span><span class="sxs-lookup"><span data-stu-id="a667e-112">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

### [<span data-ttu-id="a667e-113">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="a667e-113">Disable-AzureRmContextAutosave</span></span>](Disable-AzureRmContextAutosave.md)
<span data-ttu-id="a667e-114">Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="a667e-114">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="a667e-115">A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait</span><span class="sxs-lookup"><span data-stu-id="a667e-115">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="a667e-116">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="a667e-116">Disable-AzureRmDataCollection</span></span>](Disable-AzureRmDataCollection.md)
<span data-ttu-id="a667e-117">A AzurePowerShell-parancsmagok fejlesztéséhez kimarad az adatok gyűjtése.</span><span class="sxs-lookup"><span data-stu-id="a667e-117">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="a667e-118">Az adatokat csak akkor gyűjti össze, ha kifejezetten bejelöli.</span><span class="sxs-lookup"><span data-stu-id="a667e-118">Data is not collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="a667e-119">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="a667e-119">Disconnect-AzureRmAccount</span></span>](Disconnect-AzureRmAccount.md)
<span data-ttu-id="a667e-120">Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókkal társított összes hitelesítő adatot és kontextust.</span><span class="sxs-lookup"><span data-stu-id="a667e-120">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

### [<span data-ttu-id="a667e-121">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="a667e-121">Enable-AzureRmContextAutosave</span></span>](Enable-AzureRmContextAutosave.md)
<span data-ttu-id="a667e-122">A PowerShell-ablak megnyitásakor az Azure-hitelesítő adatok, a fiók és az előfizetési adatok menthetők és automatikusan betölthetők.</span><span class="sxs-lookup"><span data-stu-id="a667e-122">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="a667e-123">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="a667e-123">Enable-AzureRmDataCollection</span></span>](Enable-AzureRmDataCollection.md)
<span data-ttu-id="a667e-124">Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az AzurePowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="a667e-124">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="a667e-125">A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható.</span><span class="sxs-lookup"><span data-stu-id="a667e-125">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="a667e-126">Csak akkor gyűjtünk adatokat, ha kifejezetten bekapcsolta.</span><span class="sxs-lookup"><span data-stu-id="a667e-126">No data is collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="a667e-127">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a667e-127">Get-AzureRmContext</span></span>](Get-AzureRmContext.md)
<span data-ttu-id="a667e-128">Az Azure Resource Manager-kérések hitelesítéséhez használt metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a667e-128">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="a667e-129">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="a667e-129">Get-AzureRmContextAutosaveSetting</span></span>](Get-AzureRmContextAutosaveSetting.md)
<span data-ttu-id="a667e-130">Metaadatok megjelenítése a környezeti mentés funkcióról, például hogy a környezet automatikusan mentve van-e, illetve hogy hol találhatók a mentett környezet-és hitelesítőadat-adatok.</span><span class="sxs-lookup"><span data-stu-id="a667e-130">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="a667e-131">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="a667e-131">Get-AzureRmDefault</span></span>](Get-AzureRmDefault.md)
<span data-ttu-id="a667e-132">A felhasználó által az aktuális környezetben beállított alapértékek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="a667e-132">Get the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="a667e-133">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="a667e-133">Get-AzureRmEnvironment</span></span>](Get-AzureRmEnvironment.md)
<span data-ttu-id="a667e-134">Az Azure Services egy példányának végpontját és metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a667e-134">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="a667e-135">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="a667e-135">Get-AzureRmSubscription</span></span>](Get-AzureRmSubscription.md)
<span data-ttu-id="a667e-136">Az aktuális fiók által elérhető előfizetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="a667e-136">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="a667e-137">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="a667e-137">Get-AzureRmTenant</span></span>](Get-AzureRmTenant.md)
<span data-ttu-id="a667e-138">Az aktuális felhasználótól kapott bérlői fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="a667e-138">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="a667e-139">Importálás – AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a667e-139">Import-AzureRmContext</span></span>](Import-AzureRmContext.md)
<span data-ttu-id="a667e-140">Azure-hitelesítési adatok betöltése egy fájlból.</span><span class="sxs-lookup"><span data-stu-id="a667e-140">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="a667e-141">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a667e-141">Remove-AzureRmContext</span></span>](Remove-AzureRmContext.md)
<span data-ttu-id="a667e-142">Környezet eltávolítása az elérhető környezetek halmazból</span><span class="sxs-lookup"><span data-stu-id="a667e-142">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="a667e-143">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="a667e-143">Remove-AzureRmEnvironment</span></span>](Remove-AzureRmEnvironment.md)
<span data-ttu-id="a667e-144">Eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="a667e-144">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="a667e-145">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a667e-145">Rename-AzureRmContext</span></span>](Rename-AzureRmContext.md)
<span data-ttu-id="a667e-146">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="a667e-146">Rename an Azure context.</span></span>  <span data-ttu-id="a667e-147">Alapértelmezés szerint a kontextusokat felhasználói fiók és előfizetés szerint nevezi el a program.</span><span class="sxs-lookup"><span data-stu-id="a667e-147">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="a667e-148">Feloldás – AzureRmError</span><span class="sxs-lookup"><span data-stu-id="a667e-148">Resolve-AzureRmError</span></span>](Resolve-AzureRmError.md)
<span data-ttu-id="a667e-149">Részletes információk megjelenítése a PowerShell-hibákról, az Azure PowerShell hibáinak meghosszabbításával.</span><span class="sxs-lookup"><span data-stu-id="a667e-149">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="a667e-150">Mentés-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a667e-150">Save-AzureRmContext</span></span>](Save-AzureRmContext.md)
<span data-ttu-id="a667e-151">Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="a667e-151">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="a667e-152">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a667e-152">Select-AzureRmContext</span></span>](Select-AzureRmContext.md)
<span data-ttu-id="a667e-153">Előfizetés és fiók kiválasztása az Azure PowerShell-parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="a667e-153">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="a667e-154">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="a667e-154">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="a667e-155">Visszajelzést küld az Azure PowerShell-csoportnak egy sor interaktív utasítással.</span><span class="sxs-lookup"><span data-stu-id="a667e-155">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="a667e-156">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a667e-156">Set-AzureRmContext</span></span>](Set-AzureRmContext.md)
<span data-ttu-id="a667e-157">A bérlői fiók, az előfizetés és a környezet beállítása az aktuális munkamenetben használható parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="a667e-157">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="a667e-158">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="a667e-158">Set-AzureRmDefault</span></span>](Set-AzureRmDefault.md)
<span data-ttu-id="a667e-159">Alapértelmezett érték beállítása az aktuális környezetben</span><span class="sxs-lookup"><span data-stu-id="a667e-159">Sets a default in the current context</span></span>

### [<span data-ttu-id="a667e-160">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="a667e-160">Set-AzureRmEnvironment</span></span>](Set-AzureRmEnvironment.md)
<span data-ttu-id="a667e-161">Az Azure-környezet tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="a667e-161">Sets properties for an Azure environment.</span></span>

