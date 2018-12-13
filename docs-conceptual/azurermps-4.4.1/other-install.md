---
title: Az Azure PowerShell telepítésének egyéb módjai | Microsoft Docs
description: Az Azure PowerShell telepítése az MSI-csomag vagy a Webplatform-telepítő használatával.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 5016c7e768aba94308d0e78785481fafbac36c74
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/13/2018
ms.locfileid: "53216347"
---
# <a name="other-installation-methods"></a><span data-ttu-id="c21d0-103">Egyéb telepítési módszerek</span><span class="sxs-lookup"><span data-stu-id="c21d0-103">Other installation methods</span></span>

<span data-ttu-id="c21d0-104">Az Azure PowerShell többféle módszerrel telepíthető.</span><span class="sxs-lookup"><span data-stu-id="c21d0-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="c21d0-105">Az előnyben részesített módszer a PowerShellGet használata a PowerShell-galériával.</span><span class="sxs-lookup"><span data-stu-id="c21d0-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="c21d0-106">Az Azure PowerShell a Windows rendszeren a Webplatform-telepítő (WebPI) vagy a GitHubról elérhető MSI-fájl használatával telepíthető.</span><span class="sxs-lookup"><span data-stu-id="c21d0-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="c21d0-107">Telepítés Windows rendszeren a Webplatform-telepítővel</span><span class="sxs-lookup"><span data-stu-id="c21d0-107">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="c21d0-108">A legújabb Azure PowerShell ugyanúgy telepíthető a WebPI-ről, ahogy a korábbi verziók.</span><span class="sxs-lookup"><span data-stu-id="c21d0-108">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="c21d0-109">Töltse le az [Azure PowerShell WebPI csomagot](http://aka.ms/webpi-azps), és indítsa el a telepítést.</span><span class="sxs-lookup"><span data-stu-id="c21d0-109">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="c21d0-110">Ha korábban már telepített Azure-modulokat a PowerShell-galériából, a telepítő automatikusan eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="c21d0-110">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="c21d0-111">Ez egyszerűbbé teszi a környezetet, mivel így biztosítható, hogy csak egy Azure PowerShell-verzió lesz telepítve.</span><span class="sxs-lookup"><span data-stu-id="c21d0-111">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="c21d0-112">Léteznek azonban olyan forgatókönyvek, amikor több telepített verzióra lehet szüksége egy időben.</span><span class="sxs-lookup"><span data-stu-id="c21d0-112">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="c21d0-113">A PowerShell-galéria moduljai a következő helyen települnek: `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="c21d0-113">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="c21d0-114">A WebPI telepítője ezzel szemben a következő helyen telepíti az Azure-modulokat: `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="c21d0-114">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="c21d0-115">Ha hiba merül fel a telepítés során, törölje manuálisan az Azure\* mappákat a `$env:ProgramFiles\WindowsPowerShell\Modules` mappából, és próbálkozzon újra a telepítéssel.</span><span class="sxs-lookup"><span data-stu-id="c21d0-115">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="c21d0-116">A telepítés befejeztével a `$env:PSModulePath` beállításnak tartalmaznia kell az Azure PowerShell-parancsmagokat tartalmazó könyvtárakat.</span><span class="sxs-lookup"><span data-stu-id="c21d0-116">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="c21d0-117">A következő paranccsal ellenőrizheti, hogy az Azure PowerShell megfelelően van-e telepítve.</span><span class="sxs-lookup"><span data-stu-id="c21d0-117">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="c21d0-118">Létezik egy ismert hiba, amely a WebPI telepítésekor léphet fel.</span><span class="sxs-lookup"><span data-stu-id="c21d0-118">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="c21d0-119">Ha a számítógépet a rendszerfrissítések és egyéb telepítések miatt újra kell indítani, előfordulhat, hogy az `$env:PSModulePath` frissítései nem tartalmazzák az Azure PowerShell telepítési útvonalát.</span><span class="sxs-lookup"><span data-stu-id="c21d0-119">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="c21d0-120">A parancsmagok telepítés utáni betöltése vagy végrehajtása során a következő hibaüzenet jelenhet meg:</span><span class="sxs-lookup"><span data-stu-id="c21d0-120">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="c21d0-121">Ez a hiba a gép újraindításával vagy a modul teljes útvonallal való importálásával javítható.</span><span class="sxs-lookup"><span data-stu-id="c21d0-121">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="c21d0-122">Például:</span><span class="sxs-lookup"><span data-stu-id="c21d0-122">For example:</span></span>

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="c21d0-123">Telepítés Windows rendszeren az MSI-csomaggal</span><span class="sxs-lookup"><span data-stu-id="c21d0-123">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="c21d0-124">Az Azure PowerShell telepíthető a [GitHubról](https://github.com/Azure/azure-powershell/releases/latest) elérhető MSI-fájllal is.</span><span class="sxs-lookup"><span data-stu-id="c21d0-124">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="c21d0-125">Ha az Azure-modulok korábbi verziói már telepítve vannak, a telepítő automatikusan eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="c21d0-125">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="c21d0-126">Az MSI-csomag a(z) `$env:ProgramFiles\WindowsPowerShell\Modules` helyre telepíti a modulokat, azonban nem hoz létre verzióspecifikus mappákat.</span><span class="sxs-lookup"><span data-stu-id="c21d0-126">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

