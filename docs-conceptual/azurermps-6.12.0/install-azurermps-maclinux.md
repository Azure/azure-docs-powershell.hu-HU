---
title: Az Azure PowerShell telepítése macOS vagy Linux rendszeren
description: Az Azure PowerShell telepítése macOS vagy Linux rendszeren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2018
ms.locfileid: "51576419"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="2ffe6-103">Az Azure PowerShell telepítése macOS vagy Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="2ffe6-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="2ffe6-104">Nem Windows rendszerű platformokon az Azure PowerShell futtatható a PowerShell Core 6-os verziójában.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="2ffe6-105">A PowerShell e verziója bármely, .NET Core-t támogató platformon történő használatra készült.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="2ffe6-106">Ezen platformokon történő használatra elérhető az Azure PowerShell egy .NET Standard-verziója.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="2ffe6-107">Jelenleg a .NET Standardhez készült Azure PowerShell csak bétaverzióban érhető el.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-107">At this time, Azure PowerShell for .NET Standard is still in beta.</span></span>
> <span data-ttu-id="2ffe6-108">Ha problémákba ütközik vagy hibát észlel, jelentse be a problémát a GitHubon.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="2ffe6-109">Az Azure PowerShell problémái</span><span class="sxs-lookup"><span data-stu-id="2ffe6-109">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="2ffe6-110">A PowerShell Core telepítése</span><span class="sxs-lookup"><span data-stu-id="2ffe6-110">Install PowerShell Core</span></span>

<span data-ttu-id="2ffe6-111">A PowerShell Core telepítési útmutatása eltér a macOS- és a Linux-disztribúciók esetében.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-111">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="2ffe6-112">Részletes útmutatásokat a következő cikkekben talál:</span><span class="sxs-lookup"><span data-stu-id="2ffe6-112">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="2ffe6-113">A PowerShell Core telepítése macOS rendszeren</span><span class="sxs-lookup"><span data-stu-id="2ffe6-113">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="2ffe6-114">A PowerShell Core telepítése Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="2ffe6-114">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="2ffe6-115">A .NET Standardhez készült Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="2ffe6-115">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ffe6-116">A más cikkekben ismertetett `AzureRM` modul nem működik a PowerShell Core-ral.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-116">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="2ffe6-117">Telepítenie kell az `Az` modult, ha az Azure PowerShell minden funkcióját használni szeretné a PowerShell Core-ban.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-117">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="2ffe6-118">A PowerShell Core tartalmazza az előre telepített PowerShellGet modult.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="2ffe6-119">Indítsa el a PowerShellt a következő paranccsal:</span><span class="sxs-lookup"><span data-stu-id="2ffe6-119">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="2ffe6-120">Az Azure PowerShell telepítéséhez futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="2ffe6-120">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="2ffe6-121">Ha egy engedélyekkel kapcsolatos problémája akad, amikor megpróbálja telepíteni a modult, elképzelhető, hogy superuser-módban kell futtatnia a PowerShellt modulok telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-121">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="2ffe6-122">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="2ffe6-123">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="2ffe6-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="2ffe6-124">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="2ffe6-125">Aliasok engedélyezése</span><span class="sxs-lookup"><span data-stu-id="2ffe6-125">Enable aliases</span></span>

<span data-ttu-id="2ffe6-126">A meglévő `AzureRM` modullal való kompatibilitás érdekében az új `Az` modul képes visszamenőlegesen kompatibilis aliasokat létrehozni az `AzureRM` parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-126">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="2ffe6-127">A modul első használata előtt állítsa be az aliasokat a következő paranccsal:</span><span class="sxs-lookup"><span data-stu-id="2ffe6-127">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="2ffe6-128">Ez csak a jelenlegi felhasználó aliasait állítja be.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-128">This sets up aliases for the current user only.</span></span> <span data-ttu-id="2ffe6-129">A parancsmagsúgóból megtudhatja, hogy milyen egyéb értékeket lehet megadni a `-Scope`-hoz az aliasok beállításának céljából.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-129">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="2ffe6-130">Ha egy elérési úttal kapcsolatos problémája akad, bizonyosodjon meg róla, hogy az elérési út megtalálható a helyi rendszeren.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-130">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="2ffe6-131">A `CurrentUser` hatókör esetében ez a probléma a következő parancs `bash`-ban való futtatásával oldható meg:</span><span class="sxs-lookup"><span data-stu-id="2ffe6-131">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="2ffe6-132">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="2ffe6-132">Sign in</span></span>

<span data-ttu-id="2ffe6-133">Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `Az` modult a PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-133">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="2ffe6-134">A modul importálásához __nincs__ szükség megemelt jogosultsági szintre.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-134">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="2ffe6-135">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-135">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="2ffe6-136">Az `Az` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-136">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="2ffe6-137">macOS és Linux rendszeren a `$Profile` környezeti változó segítségével használja a profilját.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-137">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="2ffe6-138">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című részt.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-138">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="2ffe6-139">További lépések</span><span class="sxs-lookup"><span data-stu-id="2ffe6-139">Next Steps</span></span>

<span data-ttu-id="2ffe6-140">Az Azure PowerShell használatával kapcsolatos további információkért tekintse meg az [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="2ffe6-140">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
