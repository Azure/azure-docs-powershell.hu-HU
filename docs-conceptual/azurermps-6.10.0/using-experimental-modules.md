---
title: Kísérleti Azure PowerShell-modulok használata
description: A kísérleti Azure PowerShell-modulok filozófiájának és használatának ismertetése.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: cb1c49682ea1bfd5fa43baafe4cb0f7fc0c46020
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/11/2018
ms.locfileid: "48889201"
---
# <a name="use-experimental-azure-powershell-modules"></a><span data-ttu-id="a6092-103">Kísérleti Azure PowerShell-modulok használata</span><span class="sxs-lookup"><span data-stu-id="a6092-103">Use experimental Azure PowerShell modules</span></span>

<span data-ttu-id="a6092-104">Mivel az Azure a fejlesztői eszközökre (különösen a parancssori felületekre) helyezi a hangsúlyt, az Azure PowerShell csapata az Azure PowerShell felhasználói felületének számos fejlesztésével kísérletezik.</span><span class="sxs-lookup"><span data-stu-id="a6092-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="a6092-105">Kísérleti módszertan</span><span class="sxs-lookup"><span data-stu-id="a6092-105">Experimentation methodology</span></span>

<span data-ttu-id="a6092-106">A kísérletezés érdekében új Azure PowerShell-modulokat hozunk létre, amelyek az Azure SDK meglévő funkcióit új, könnyebben használható módon kezelik.</span><span class="sxs-lookup"><span data-stu-id="a6092-106">To facilitate experimentation, we're creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="a6092-107">A parancsmagok a legtöbb esetben pontosan megegyeznek a meglévő parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="a6092-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="a6092-108">A kísérleti parancsmagok azonban olyan egyszerűsített jelölésrendszert és intelligensebb alapértelmezett értékeket kínálnak, amelyekkel könnyebben hozhatók létre és kezelhetők az Azure-erőforrások.</span><span class="sxs-lookup"><span data-stu-id="a6092-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="a6092-109">Ezek a modulok a meglévő Azure PowerShell-modulok mellett telepíthetők.</span><span class="sxs-lookup"><span data-stu-id="a6092-109">These modules can be installed side by side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="a6092-110">A parancsmagneveket lerövidítettük, hogy rövidebb neveket kelljen megadni, illetve hogy elkerüljük a névütközést a meglévő, nem kísérleti parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="a6092-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="a6092-111">A kísérleti modulok az alábbi elnevezési szabályt követik: `AzureRM.*.Experiments`.</span><span class="sxs-lookup"><span data-stu-id="a6092-111">The experimental modules use the following naming convention: `AzureRM.*.Experiments`.</span></span> <span data-ttu-id="a6092-112">Ez a elnevezési szabály az előzetes verziójú modulok elnevezéséhez hasonló: `AzureRM.*.Preview`.</span><span class="sxs-lookup"><span data-stu-id="a6092-112">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="a6092-113">Az előzetes verziójú modulok nem azonosak a kísérleti modulokkal.</span><span class="sxs-lookup"><span data-stu-id="a6092-113">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="a6092-114">Az előzetes modulok az Azure-szolgáltatások olyan új funkcióit valósítják meg, amelyek csak előzetes ajánlatként érhetők el.</span><span class="sxs-lookup"><span data-stu-id="a6092-114">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="a6092-115">Az előzetes verziójú modulok a meglévő Azure PowerShell-modulokat váltják fel, és ugyanazokat a parancsmag- és paraméterneveket használják.</span><span class="sxs-lookup"><span data-stu-id="a6092-115">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="a6092-116">A kísérleti modulok telepítése</span><span class="sxs-lookup"><span data-stu-id="a6092-116">How to install an experimental module</span></span>

<span data-ttu-id="a6092-117">A kísérleti modulok a meglévő Azure PowerShell-modulokhoz hasonlóan a PowerShell-galériában vannak közzétéve.</span><span class="sxs-lookup"><span data-stu-id="a6092-117">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="a6092-118">A kísérleti modulok listájának megtekintéséhez futtassa a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="a6092-118">To see a list of experimental modules, run the following command:</span></span>

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

<span data-ttu-id="a6092-119">A kísérleti modulok telepítéséhez használja a következő parancsokat egy emelt szintű PowerShell-munkamenetből:</span><span class="sxs-lookup"><span data-stu-id="a6092-119">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="a6092-120">Dokumentáció és támogatás</span><span class="sxs-lookup"><span data-stu-id="a6092-120">Documentation and support</span></span>

<span data-ttu-id="a6092-121">A dokumentációt a telepítőcsomag tartalmazza, és a `Get-Help` parancsmaggal érhető el.</span><span class="sxs-lookup"><span data-stu-id="a6092-121">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="a6092-122">A kísérleti modulokhoz nem jelenik meg hivatalos dokumentáció.</span><span class="sxs-lookup"><span data-stu-id="a6092-122">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="a6092-123">Javasoljuk, hogy tesztelje ezeket a modulokat.</span><span class="sxs-lookup"><span data-stu-id="a6092-123">We encourage you to test these modules.</span></span> <span data-ttu-id="a6092-124">A visszajelzések segítenek nekünk a modulok használhatóságának fejlesztésében és a felhasználói igények kielégítésében.</span><span class="sxs-lookup"><span data-stu-id="a6092-124">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="a6092-125">Mivel azonban ezek kísérleti modulok, csak korlátozott támogatás érhető el hozzájuk.</span><span class="sxs-lookup"><span data-stu-id="a6092-125">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="a6092-126">Kérdéseit és a hibajelentéseket egy [hibajegy](https://github.com/Azure/azure-powershell/issues) létrehozásával küldheti be a GitHub-adattárban.</span><span class="sxs-lookup"><span data-stu-id="a6092-126">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="a6092-127">Kísérletek és fejlesztési területek</span><span class="sxs-lookup"><span data-stu-id="a6092-127">Experiments and areas of improvement</span></span>

<span data-ttu-id="a6092-128">Ezeket a fejlesztéseket a versenytársaink termékeinek főbb előnyei alapján választottuk ki.</span><span class="sxs-lookup"><span data-stu-id="a6092-128">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="a6092-129">Például az Azure CLI 2.0 egyik fontos eleme, hogy a parancsok _forgatókönyveken_, és nem _API felületeken_ alapulnak.</span><span class="sxs-lookup"><span data-stu-id="a6092-129">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="a6092-130">Az Azure CLI 2.0 számos intelligens alapértelmezett értéket alkalmaz, amelyekkel az „első lépések” forgatókönyvek könnyebben használhatók a végfelhasználók számára.</span><span class="sxs-lookup"><span data-stu-id="a6092-130">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="a6092-131">Központi fejlesztések</span><span class="sxs-lookup"><span data-stu-id="a6092-131">Core improvements</span></span>

<span data-ttu-id="a6092-132">A központi fejlesztések a „józan megfontoláson” alapulnak, és az ilyen frissítések bevezetéséhez nem sok kísérletezés szükséges.</span><span class="sxs-lookup"><span data-stu-id="a6092-132">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="a6092-133">Forgatókönyv-alapú parancsmagok – \**Minden* parancsmagot forgatókönyvek, és nem az Azure REST-szolgáltatás köré kell építeni.</span><span class="sxs-lookup"><span data-stu-id="a6092-133">Scenario-based Cmdlets - \**All*- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="a6092-134">Rövidebb nevek – Ez a parancsmagok (például: `New-AzureRmVM` => `New-AzVm`) és a paraméterek (például: `-ResourceGroupName` => `-Rg`) nevére is vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="a6092-134">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="a6092-135">A „régi” parancsmagokkal való kompatibilitás érdekében aliasok használhatók.</span><span class="sxs-lookup"><span data-stu-id="a6092-135">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="a6092-136">Biztosítson _visszafelé kompatibilis_ paraméterkészleteket.</span><span class="sxs-lookup"><span data-stu-id="a6092-136">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="a6092-137">Intelligens alapértékek – Adja meg a „szükséges” információkat intelligens alapértelmezett értékekkel.</span><span class="sxs-lookup"><span data-stu-id="a6092-137">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="a6092-138">Például:</span><span class="sxs-lookup"><span data-stu-id="a6092-138">For example:</span></span>
  - <span data-ttu-id="a6092-139">Erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="a6092-139">Resource Group</span></span>
  - <span data-ttu-id="a6092-140">Hely</span><span class="sxs-lookup"><span data-stu-id="a6092-140">Location</span></span>
  - <span data-ttu-id="a6092-141">Függő erőforrások</span><span class="sxs-lookup"><span data-stu-id="a6092-141">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="a6092-142">Kísérleti fejlesztések</span><span class="sxs-lookup"><span data-stu-id="a6092-142">Experimental improvements</span></span>

<span data-ttu-id="a6092-143">A kísérleti fejlesztések segítségével a csoport kísérletezéssel tesztelheti a jelentős változásokat.</span><span class="sxs-lookup"><span data-stu-id="a6092-143">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="a6092-144">Egyszerű típusok – A létrehozási forgatókönyveknek távol kell esniük az összetett típusoktól és a konfigurációs objektumoktól.</span><span class="sxs-lookup"><span data-stu-id="a6092-144">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="a6092-145">Egyszerűsítse a konfigurációt egy vagy két paraméterre.</span><span class="sxs-lookup"><span data-stu-id="a6092-145">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="a6092-146">„Intelligens létrehozás” – Az „intelligens létrehozást” megvalósító egyik létrehozási forgatókönyvhöz _sincs_ kötelező paraméter: az összes szükséges információt az Azure PowerShell választja ki a saját belátása szerint.</span><span class="sxs-lookup"><span data-stu-id="a6092-146">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="a6092-147">Szürke paraméterek – Sok esetben néhány paraméter „szürke” vagy félig választható.</span><span class="sxs-lookup"><span data-stu-id="a6092-147">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="a6092-148">Ha a paraméter nincs megadva, a rendszer megkérdezi a felhasználót, hogy létrejöjjön-e a paraméter.</span><span class="sxs-lookup"><span data-stu-id="a6092-148">If the parameter isn't specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="a6092-149">Szintén célszerű, ha a szürke paraméterek a környezet alapján következtetnek ki egy értéket a felhasználó beleegyezésével.</span><span class="sxs-lookup"><span data-stu-id="a6092-149">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="a6092-150">Hasznos lehet például, ha a szürke paraméter a legutóbb használt értéket javasolja.</span><span class="sxs-lookup"><span data-stu-id="a6092-150">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="a6092-151">`-Auto` kapcsoló – Az `-Auto` kapcsoló „felhasználó által aktiválható” módon biztosítja a felhasználóknak _az összes beállítás alapértelmezett értékre való állítását_, ugyanakkor fenntartja a kötelező paraméterek integritását a fő útvonalon.</span><span class="sxs-lookup"><span data-stu-id="a6092-151">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="a6092-152">Szolgáltatásspecifikus kapcsolók</span><span class="sxs-lookup"><span data-stu-id="a6092-152">Feature-specific switches</span></span>

<span data-ttu-id="a6092-153">A „Webalkalmazás létrehozása” forgatókönyv például egy `-Git` vagy `-AddRemote` kapcsolóval rendelkezhet, amely automatikusan egy távoli „azure” mappát ad hozzá egy meglévő Git-adattárhoz.</span><span class="sxs-lookup"><span data-stu-id="a6092-153">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="a6092-154">Beállítható alapértelmezett értékek – A felhasználóknak képesnek kell lenniük arra, hogy alapértelmezett értékeket állítsanak be bizonyos általános paraméterekhez (például `-ResourceGroupName` és `-Location`).</span><span class="sxs-lookup"><span data-stu-id="a6092-154">Settable Defaults - Users should be able to set defaults for common parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="a6092-155">Alapértelmezett méretek – Az erőforrások „méretei” megtéveszthetik a felhasználókat, mert sok erőforrás-szolgáltató különböző neveket használ (például „\_DS1\_v2 szabvány” vagy „S1”).</span><span class="sxs-lookup"><span data-stu-id="a6092-155">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="a6092-156">A legtöbb felhasználót azonban jobban érdeklik a költségek.</span><span class="sxs-lookup"><span data-stu-id="a6092-156">However, most users care more about cost.</span></span> <span data-ttu-id="a6092-157">Ezért logikus „univerzális” méreteket meghatározni egy díjszabási ütemezés alapján.</span><span class="sxs-lookup"><span data-stu-id="a6092-157">So it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="a6092-158">A felhasználók adott méretet választhatnak vagy hagyhatják, hogy az Azure PowerShell kiválassza a _legjobb lehetőséget_ az erőforrás és a költségvetés alapján.</span><span class="sxs-lookup"><span data-stu-id="a6092-158">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="a6092-159">Kimeneti formátum – Az Azure PowerShell jelenleg `PSObject` elemeket ad vissza, és kevés konzolkimenet van.</span><span class="sxs-lookup"><span data-stu-id="a6092-159">Output Format - Azure PowerShell currently returns `PSObject`s and there's little console output.</span></span> <span data-ttu-id="a6092-160">Lehetséges, hogy az Azure PowerShellnek információt kell megjelenítenie a felhasználónak a használt „intelligens alapértékekről”.</span><span class="sxs-lookup"><span data-stu-id="a6092-160">Azure PowerShell may need to display some information to the user about the "smart defaults" used.</span></span>
