---
title: Az Azure PowerShell telepítésének egyéb módjai | Microsoft Docs
description: Az Azure PowerShell telepítése az MSI-csomag vagy a Webplatform-telepítő használatával.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: fd5263a327fa8e4b70418bf6fa7702d8c5383733
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/08/2018
ms.locfileid: "33911952"
---
# <a name="other-installation-methods"></a><span data-ttu-id="c8316-103">Egyéb telepítési módszerek</span><span class="sxs-lookup"><span data-stu-id="c8316-103">Other installation methods</span></span>

<span data-ttu-id="c8316-104">Az Azure PowerShell többféle módszerrel telepíthető.</span><span class="sxs-lookup"><span data-stu-id="c8316-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="c8316-105">Az előnyben részesített módszer a PowerShellGet használata a PowerShell-galériával.</span><span class="sxs-lookup"><span data-stu-id="c8316-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="c8316-106">Az Azure PowerShell a Windows rendszeren a Webplatform-telepítő (WebPI) vagy a GitHubról elérhető MSI-fájl használatával telepíthető.</span><span class="sxs-lookup"><span data-stu-id="c8316-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span> <span data-ttu-id="c8316-107">Az Azure PowerShell Docker-tárolóban is telepíthető.</span><span class="sxs-lookup"><span data-stu-id="c8316-107">Azure PowerShell can also be installed in a Docker container.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="c8316-108">Telepítés Windows rendszeren a Webplatform-telepítővel</span><span class="sxs-lookup"><span data-stu-id="c8316-108">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="c8316-109">A legújabb Azure PowerShell ugyanúgy telepíthető a WebPI-ről, ahogy a korábbi verziók.</span><span class="sxs-lookup"><span data-stu-id="c8316-109">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="c8316-110">Töltse le az [Azure PowerShell WebPI csomagot](http://aka.ms/webpi-azps), és indítsa el a telepítést.</span><span class="sxs-lookup"><span data-stu-id="c8316-110">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="c8316-111">Ha korábban már telepített Azure-modulokat a PowerShell-galériából, a telepítő automatikusan eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="c8316-111">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="c8316-112">Ez egyszerűbbé teszi a környezetet, mivel így biztosítható, hogy csak egy Azure PowerShell-verzió lesz telepítve.</span><span class="sxs-lookup"><span data-stu-id="c8316-112">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="c8316-113">Léteznek azonban olyan forgatókönyvek, amikor több telepített verzióra lehet szüksége egy időben.</span><span class="sxs-lookup"><span data-stu-id="c8316-113">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="c8316-114">A PowerShell-galéria moduljai a következő helyen települnek: `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="c8316-114">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="c8316-115">A WebPI telepítője ezzel szemben a következő helyen telepíti az Azure-modulokat: `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="c8316-115">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="c8316-116">Ha hiba merül fel a telepítés során, törölje manuálisan az Azure\* mappákat a `$env:ProgramFiles\WindowsPowerShell\Modules` mappából, és próbálkozzon újra a telepítéssel.</span><span class="sxs-lookup"><span data-stu-id="c8316-116">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="c8316-117">A telepítés befejeztével a `$env:PSModulePath` beállításnak tartalmaznia kell az Azure PowerShell-parancsmagokat tartalmazó könyvtárakat.</span><span class="sxs-lookup"><span data-stu-id="c8316-117">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="c8316-118">A következő paranccsal ellenőrizheti, hogy az Azure PowerShell megfelelően van-e telepítve.</span><span class="sxs-lookup"><span data-stu-id="c8316-118">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="c8316-119">Létezik egy ismert hiba, amely a WebPI telepítésekor léphet fel.</span><span class="sxs-lookup"><span data-stu-id="c8316-119">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="c8316-120">Ha a számítógépet a rendszerfrissítések és egyéb telepítések miatt újra kell indítani, előfordulhat, hogy az `$env:PSModulePath` frissítései nem tartalmazzák az Azure PowerShell telepítési útvonalát.</span><span class="sxs-lookup"><span data-stu-id="c8316-120">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="c8316-121">A parancsmagok telepítés utáni betöltése vagy végrehajtása során a következő hibaüzenet jelenhet meg:</span><span class="sxs-lookup"><span data-stu-id="c8316-121">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="c8316-122">Ez a hiba a gép újraindításával vagy a modul teljes útvonallal való importálásával javítható.</span><span class="sxs-lookup"><span data-stu-id="c8316-122">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="c8316-123">Például:</span><span class="sxs-lookup"><span data-stu-id="c8316-123">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="c8316-124">Telepítés Windows rendszeren az MSI-csomaggal</span><span class="sxs-lookup"><span data-stu-id="c8316-124">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="c8316-125">Az Azure PowerShell telepíthető a [GitHubról](https://aka.ms/azps-release) elérhető MSI-fájllal is.</span><span class="sxs-lookup"><span data-stu-id="c8316-125">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="c8316-126">Ha az Azure-modulok korábbi verziói már telepítve vannak, a telepítő automatikusan eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="c8316-126">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="c8316-127">Az MSI-csomag a(z) `$env:ProgramFiles\WindowsPowerShell\Modules` helyre telepíti a modulokat, azonban nem hoz létre verzióspecifikus mappákat.</span><span class="sxs-lookup"><span data-stu-id="c8316-127">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="install-in-a-docker-container"></a><span data-ttu-id="c8316-128">Telepítés Docker-tárolóban</span><span class="sxs-lookup"><span data-stu-id="c8316-128">Install in a Docker container</span></span>

<span data-ttu-id="c8316-129">Elérhető az Azure PowerShell-hez előre konfigurált Docker-rendszerkép.</span><span class="sxs-lookup"><span data-stu-id="c8316-129">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="c8316-130">A tárolót a következő paranccsal futtathatja: `docker run`.</span><span class="sxs-lookup"><span data-stu-id="c8316-130">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="c8316-131">Emellett elérhető a parancsmagok egy részhalmaza PowerShell Core-tároló formájában.</span><span class="sxs-lookup"><span data-stu-id="c8316-131">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="c8316-132">Mac és Linux rendszereken a `latest` rendszerképet használhatja.</span><span class="sxs-lookup"><span data-stu-id="c8316-132">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="c8316-133">Windowson a `nanoserver` rendszerképet használhatja.</span><span class="sxs-lookup"><span data-stu-id="c8316-133">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="c8316-134">Az Azure PowerShell az `Install-Module` parancsmaggal van telepítve a [PowerShell-galériából](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="c8316-134">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>
