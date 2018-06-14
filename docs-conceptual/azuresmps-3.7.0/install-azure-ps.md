---
title: Az Azure PowerShell Service Management moduljának telepítése és konfigurálása | Microsoft Docs
description: Az Azure PowerShell telepítése és konfigurálása az első használathoz.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 5f59e5e5fec4fb721ac7548c12c906c7c8d5733e
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853763"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="668ec-103">Az Azure PowerShell Service Management moduljának telepítése</span><span class="sxs-lookup"><span data-stu-id="668ec-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="668ec-104">Az Azure PowerShell telepítésének előnyben részesített módszere a [PowerShell-galériából](https://www.powershellgallery.com/) történő telepítés.</span><span class="sxs-lookup"><span data-stu-id="668ec-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="668ec-105">1. lépés: A PowerShellGet telepítése</span><span class="sxs-lookup"><span data-stu-id="668ec-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="668ec-106">Ahhoz, hogy elemeket telepíthessen a PowerShell-galériából, szükség van a PowerShellGet modulra.</span><span class="sxs-lookup"><span data-stu-id="668ec-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="668ec-107">Győződjön meg arról, hogy rendelkezik a PowerShellGet megfelelő verziójával, és az egyéb rendszerkövetelmények is teljesülnek.</span><span class="sxs-lookup"><span data-stu-id="668ec-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="668ec-108">A következő parancs futtatásával ellenőrizze, hogy telepítve van-e a PowerShellGet a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="668ec-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="668ec-109">Az alábbihoz hasonló kimenetnek kell megjelennie:</span><span class="sxs-lookup"><span data-stu-id="668ec-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="668ec-110">Ha a PowerShellGet nincs telepítve, akkor tekintse meg [A PowerShellGet beszerzése](#how-to-get-powershellget) című szakaszt.</span><span class="sxs-lookup"><span data-stu-id="668ec-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="668ec-111">2. lépés: Az Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="668ec-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="668ec-112">Futtassa az alábbi parancsot rendszergazdaként a Windows PowerShell-konzolból:</span><span class="sxs-lookup"><span data-stu-id="668ec-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="668ec-113">Az Azure-modul az Azure Resource Manager-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="668ec-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="668ec-114">Az AzureRM-modul telepítésekor a rendszer minden olyan Azure-modult letölt és telepít a PowerShell-galériából, amely előzőleg nem volt telepítve.</span><span class="sxs-lookup"><span data-stu-id="668ec-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="668ec-115">Az Azure PowerShell Service Management modulnak vannak az Azure PowerShell Resource Manager-modulokkal közös függőségei.</span><span class="sxs-lookup"><span data-stu-id="668ec-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="668ec-116">Ha már telepítette az Azure PowerShell Resource Manager-modulokat, hozzá kell adnia az `-AllowClobber` paramétert a telepítési parancshoz.</span><span class="sxs-lookup"><span data-stu-id="668ec-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="668ec-117">Ez lehetővé teszi a meglévő közös függőségek frissítését.</span><span class="sxs-lookup"><span data-stu-id="668ec-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="668ec-118">A paraméter nélkül a modul telepítése sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="668ec-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="668ec-119">A modul telepítése után a modult az alábbi parancs futtatásával importálhatja:</span><span class="sxs-lookup"><span data-stu-id="668ec-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="668ec-120">A parancsmagok használata</span><span class="sxs-lookup"><span data-stu-id="668ec-120">To use the cmdlets</span></span>

<span data-ttu-id="668ec-121">Az Azure Service Management-parancsmagok használatának megkezdéséhez jelentkezzen be az Azure-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="668ec-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="668ec-122">A fiókba való bejelentkezéshez futtassa a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="668ec-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="668ec-123">Az Azure-ba való bejelentkezés után az Azure PowerShell létrehoz egy környezetet az adott munkamenethez.</span><span class="sxs-lookup"><span data-stu-id="668ec-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="668ec-124">Ez a környezet tartalmazza az adott munkamenet összes parancsmagjához használt Azure PowerShell-környezetet, -fiókot, -bérlőt és -előfizetést.</span><span class="sxs-lookup"><span data-stu-id="668ec-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="668ec-125">Most már készen áll az alábbi modulok használatára.</span><span class="sxs-lookup"><span data-stu-id="668ec-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="668ec-126">Azure Service Management-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="668ec-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="668ec-127">Az Azure PowerShell-modulok rendszeresen frissülnek.</span><span class="sxs-lookup"><span data-stu-id="668ec-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="668ec-128">Ha a parancsmagokat tárgyaló online súgóban olyan parancsmagokról vagy paraméterekről olvas, amelyek az Ön moduljában nem szerepelnek, töltse le és telepítse a modul legújabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="668ec-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="668ec-129">A saját modulverziójának az azonosításához írja be a következőt: `(Get-Module Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="668ec-129">To find the version of your module, type: `(Get-Module Azure).Version`.</span></span>

<span data-ttu-id="668ec-130">Az Azure-ban gyakran előforduló feladatok némelyikének automatizálását segítő mintaszkripteket lásd a [Microsoft Azure Script Centerben](http://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="668ec-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="668ec-131">Általános információk a Windows PowerShell telepítéséről, megismeréséről, használatáról és testreszabásáról: [Szkriptek használata a Windows PowerShell-lel](http://go.microsoft.com/fwlink/p/?linkid=320210).</span><span class="sxs-lookup"><span data-stu-id="668ec-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="668ec-132">A PowerShellGet beszerzése</span><span class="sxs-lookup"><span data-stu-id="668ec-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="668ec-133">Operációs rendszer verziója</span><span class="sxs-lookup"><span data-stu-id="668ec-133">OS Version</span></span>|<span data-ttu-id="668ec-134">Telepítési utasítások</span><span class="sxs-lookup"><span data-stu-id="668ec-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="668ec-135">Windows 10 vagy Windows Server 2016 rendszert használok</span><span class="sxs-lookup"><span data-stu-id="668ec-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="668ec-136">Az operációs rendszer részét képező Windows Management Framework (WMF) 5.0 beépített eleme</span><span class="sxs-lookup"><span data-stu-id="668ec-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="668ec-137">Frissíteni szeretnék a PowerShell 5-ös verziójára</span><span class="sxs-lookup"><span data-stu-id="668ec-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="668ec-138">A WMF legújabb verziójának telepítése</span><span class="sxs-lookup"><span data-stu-id="668ec-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="668ec-139">A PowerShell 3-as vagy 4-es verziójával rendelkező Windows-verziót használok</span><span class="sxs-lookup"><span data-stu-id="668ec-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="668ec-140">A PackageManagement-modulok beszerzése</span><span class="sxs-lookup"><span data-stu-id="668ec-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="668ec-141">Az Azure PowerShell verziószámának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="668ec-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="668ec-142">Habár javasoljuk, hogy a lehető leghamarabb frissítsen a legújabb verzióra, az Azure PowerShell számos verziója támogatott.</span><span class="sxs-lookup"><span data-stu-id="668ec-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="668ec-143">Az Azure PowerShell telepített verziójának megállapításához futtassa a következő parancsot a parancssorban: `Get-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="668ec-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
