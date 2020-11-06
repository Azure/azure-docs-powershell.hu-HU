---
Module Name: AzureRM.Profile
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
ms.openlocfilehash: bc3ccc2c2b0574eee40357fb0079fe22124ea3e6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490600"
---
# <span data-ttu-id="8e259-101">AzureRM. profil modul</span><span class="sxs-lookup"><span data-stu-id="8e259-101">AzureRM.Profile Module</span></span>
## <span data-ttu-id="8e259-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e259-102">Description</span></span>
<span data-ttu-id="8e259-103">Minden Azure-modul hitelesítő adatait és általános konfigurációját kezeli.</span><span class="sxs-lookup"><span data-stu-id="8e259-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="8e259-104">AzureRM. profil parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8e259-104">AzureRM.Profile Cmdlets</span></span>
### [<span data-ttu-id="8e259-105">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="8e259-105">Add-AzureRmAccount</span></span>](Add-AzureRmAccount.md)
<span data-ttu-id="8e259-106">Az Azure Resource Manager parancsmag-kérésekhez használható hitelesített fiók hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="8e259-106">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

### [<span data-ttu-id="8e259-107">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="8e259-107">Add-AzureRmEnvironment</span></span>](Add-AzureRmEnvironment.md)
<span data-ttu-id="8e259-108">Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="8e259-108">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="8e259-109">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8e259-109">Clear-AzureRmContext</span></span>](Clear-AzureRmContext.md)
<span data-ttu-id="8e259-110">Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8e259-110">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="8e259-111">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="8e259-111">Disable-AzureRmContextAutosave</span></span>](Disable-AzureRmContextAutosave.md)
<span data-ttu-id="8e259-112">Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="8e259-112">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="8e259-113">A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait</span><span class="sxs-lookup"><span data-stu-id="8e259-113">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="8e259-114">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="8e259-114">Disable-AzureRmDataCollection</span></span>](Disable-AzureRmDataCollection.md)
<span data-ttu-id="8e259-115">A AzurePowerShell-parancsmagok fejlesztéséhez kimarad az adatok gyűjtése.</span><span class="sxs-lookup"><span data-stu-id="8e259-115">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="8e259-116">Az adatokat csak akkor gyűjti össze, ha kifejezetten bejelöli.</span><span class="sxs-lookup"><span data-stu-id="8e259-116">Data is not collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="8e259-117">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="8e259-117">Enable-AzureRmContextAutosave</span></span>](Enable-AzureRmContextAutosave.md)
<span data-ttu-id="8e259-118">A PowerShell-ablak megnyitásakor az Azure-hitelesítő adatok, a fiók és az előfizetési adatok menthetők és automatikusan betölthetők.</span><span class="sxs-lookup"><span data-stu-id="8e259-118">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="8e259-119">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="8e259-119">Enable-AzureRmDataCollection</span></span>](Enable-AzureRmDataCollection.md)
<span data-ttu-id="8e259-120">Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az AzurePowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="8e259-120">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="8e259-121">A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható.</span><span class="sxs-lookup"><span data-stu-id="8e259-121">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="8e259-122">Csak akkor gyűjtünk adatokat, ha kifejezetten bekapcsolta.</span><span class="sxs-lookup"><span data-stu-id="8e259-122">No data is collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="8e259-123">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8e259-123">Get-AzureRmContext</span></span>](Get-AzureRmContext.md)
<span data-ttu-id="8e259-124">Az Azure Resource Manager-kérések hitelesítéséhez használt metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8e259-124">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="8e259-125">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="8e259-125">Get-AzureRmContextAutosaveSetting</span></span>](Get-AzureRmContextAutosaveSetting.md)
<span data-ttu-id="8e259-126">Metaadatok megjelenítése a környezeti mentés funkcióról (például a környezet automatikus mentésének whterh), valamint a mentett környezet-és hitelesítőadat-adatok helyének megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="8e259-126">Display metadata about the context autosave feature, including whterh the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="8e259-127">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="8e259-127">Get-AzureRmEnvironment</span></span>](Get-AzureRmEnvironment.md)
<span data-ttu-id="8e259-128">Az Azure Services egy példányának végpontját és metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8e259-128">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="8e259-129">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="8e259-129">Get-AzureRmSubscription</span></span>](Get-AzureRmSubscription.md)
<span data-ttu-id="8e259-130">Az aktuális fiók által elérhető előfizetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="8e259-130">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="8e259-131">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="8e259-131">Get-AzureRmTenant</span></span>](Get-AzureRmTenant.md)
<span data-ttu-id="8e259-132">Az aktuális felhasználótól kapott bérlői fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="8e259-132">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="8e259-133">Importálás – AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8e259-133">Import-AzureRmContext</span></span>](Import-AzureRmContext.md)
<span data-ttu-id="8e259-134">Azure-hitelesítési adatok betöltése egy fájlból.</span><span class="sxs-lookup"><span data-stu-id="8e259-134">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="8e259-135">Remove-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="8e259-135">Remove-AzureRmAccount</span></span>](Remove-AzureRmAccount.md)
<span data-ttu-id="8e259-136">Eltávolíthatja az ezzel a fiókkal társított összes hitelesítő adatot és kontextust.</span><span class="sxs-lookup"><span data-stu-id="8e259-136">Remove all credentials and contexts associated with this account.</span></span>

### [<span data-ttu-id="8e259-137">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8e259-137">Remove-AzureRmContext</span></span>](Remove-AzureRmContext.md)
<span data-ttu-id="8e259-138">Környezet eltávolítása az elérhető környezetek halmazból</span><span class="sxs-lookup"><span data-stu-id="8e259-138">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="8e259-139">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="8e259-139">Remove-AzureRmEnvironment</span></span>](Remove-AzureRmEnvironment.md)
<span data-ttu-id="8e259-140">Eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="8e259-140">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="8e259-141">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8e259-141">Rename-AzureRmContext</span></span>](Rename-AzureRmContext.md)
<span data-ttu-id="8e259-142">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="8e259-142">Rename an Azure context.</span></span>  <span data-ttu-id="8e259-143">Alapértelmezés szerint a kontextusokat felhasználói fiók és előfizetés szerint nevezi el a program.</span><span class="sxs-lookup"><span data-stu-id="8e259-143">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="8e259-144">Feloldás – AzureRmError</span><span class="sxs-lookup"><span data-stu-id="8e259-144">Resolve-AzureRmError</span></span>](Resolve-AzureRmError.md)
<span data-ttu-id="8e259-145">Részletes információk megjelenítése a PowerShell-hibákról, az Azure PowerShell hibáinak meghosszabbításával.</span><span class="sxs-lookup"><span data-stu-id="8e259-145">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="8e259-146">Mentés-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8e259-146">Save-AzureRmContext</span></span>](Save-AzureRmContext.md)
<span data-ttu-id="8e259-147">Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="8e259-147">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="8e259-148">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8e259-148">Select-AzureRmContext</span></span>](Select-AzureRmContext.md)
<span data-ttu-id="8e259-149">Az Azure PowerShell-parancsmagok cél (vagy fiók, bérlő) előfizetésének kiválasztása</span><span class="sxs-lookup"><span data-stu-id="8e259-149">Select a subscription to target (or account, tenant) in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="8e259-150">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="8e259-150">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="8e259-151">Visszajelzést küld az Azure PowerShell-csoportnak egy sor interaktív utasítással.</span><span class="sxs-lookup"><span data-stu-id="8e259-151">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="8e259-152">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8e259-152">Set-AzureRmContext</span></span>](Set-AzureRmContext.md)
<span data-ttu-id="8e259-153">A bérlői fiók, az előfizetés és a környezet beállítása az aktuális munkamenetben használható parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="8e259-153">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="8e259-154">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="8e259-154">Set-AzureRmEnvironment</span></span>](Set-AzureRmEnvironment.md)
<span data-ttu-id="8e259-155">Az Azure-környezet tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="8e259-155">Sets properties for an Azure environment.</span></span>

