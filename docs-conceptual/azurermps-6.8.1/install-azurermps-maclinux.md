---
title: Az Azure PowerShell telepítése macOS vagy Linux rendszeren
description: Az Azure PowerShell telepítése macOS vagy Linux rendszeren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: f014d62e898da195a38052db6b7e37a2cd96dfdd
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560116"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="6c9bd-103">Az Azure PowerShell telepítése macOS vagy Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="6c9bd-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="6c9bd-104">Nem Windows rendszerű platformokon az Azure PowerShell futtatható a PowerShell Core 6-os verziójában.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="6c9bd-105">A PowerShell e verziója bármely, .NET Core-t támogató platformon történő használatra készült.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="6c9bd-106">Ezen platformokon történő használatra elérhető az Azure PowerShell egy .NET Standard-verziója.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="6c9bd-107">Jelenleg a PowerShell Core 6-os verziója és a .NET Core-hoz készült Azure PowerShell csak bétaverzióban érhető el.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="6c9bd-108">A termékek korlátozott támogatással rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-108">Support for these products is limited.</span></span> <span data-ttu-id="6c9bd-109">Ha problémákba ütközik vagy hibát észlel, jelentse be a problémát a GitHubon.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="6c9bd-110">A PowerShell Core 6-os verziójának problémái</span><span class="sxs-lookup"><span data-stu-id="6c9bd-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="6c9bd-111">Az Azure PowerShell problémái</span><span class="sxs-lookup"><span data-stu-id="6c9bd-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="6c9bd-112">A PowerShell Core telepítése</span><span class="sxs-lookup"><span data-stu-id="6c9bd-112">Install PowerShell Core</span></span>

<span data-ttu-id="6c9bd-113">A PowerShell Core telepítési útmutatása eltér a macOS- és a Linux-disztribúciók esetében.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="6c9bd-114">Részletes útmutatásokat a következő cikkekben talál:</span><span class="sxs-lookup"><span data-stu-id="6c9bd-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="6c9bd-115">A PowerShell Core telepítése macOS rendszeren</span><span class="sxs-lookup"><span data-stu-id="6c9bd-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="6c9bd-116">A PowerShell Core telepítése Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="6c9bd-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="6c9bd-117">A .NET Core-hoz készült Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="6c9bd-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="6c9bd-118">A PowerShell Core tartalmazza az előre telepített PowerShellGet modult.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="6c9bd-119">Modulok a PowerShellben történő telepítéséhez megemelt jogosultsági szint szükséges, ezért a munkamenetet superuser felhasználóként kell elindítani:</span><span class="sxs-lookup"><span data-stu-id="6c9bd-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="6c9bd-120">Az Azure PowerShell telepítéséhez futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="6c9bd-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!IMPORTANT]
> <span data-ttu-id="6c9bd-121">A más cikkekben ismertetett `AzureRM` modul nem a .NET Core-hoz készült, és nem fog működni a PowerShell Core-ral.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="6c9bd-122">A(z) `Az` modulok minden `AzureRM` parancsmagra tartalmaznak parancsaliasokat, így a(z) `AzureRM` egész dokumentációja érvényes.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-122">The `Az` modules contain command aliases for all `AzureRM` cmdlets, so all of the documentation for `AzureRM` applies.</span></span>

<span data-ttu-id="6c9bd-123">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="6c9bd-124">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="6c9bd-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="6c9bd-125">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="6c9bd-126">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="6c9bd-126">Sign in</span></span>

<span data-ttu-id="6c9bd-127">Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `Az` modult a PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-127">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="6c9bd-128">A modul importálásához __nincs__ szükség megemelt jogosultsági szintre.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="6c9bd-129">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="6c9bd-130">Az `Az` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-130">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="6c9bd-131">macOS és Linux rendszeren a `$Profile` környezeti változó segítségével használja a profilját.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="6c9bd-132">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című részt.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-132">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="6c9bd-133">További lépések</span><span class="sxs-lookup"><span data-stu-id="6c9bd-133">Next Steps</span></span>

<span data-ttu-id="6c9bd-134">Az Azure PowerShell használatával kapcsolatos további információkért tekintse meg az [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="6c9bd-134">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
