---
title: Az Azure PowerShell áttekintése
description: Az Azure PowerShell Az modul áttekintése, valamint a telepítéssel és az első lépésekkel kapcsolatos információk.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 1978ba5415a27349ac68175144cca0d89fa26d96
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052617"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="32f29-103">Az Azure PowerShell áttekintése</span><span class="sxs-lookup"><span data-stu-id="32f29-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="32f29-104">Az Azure PowerShell olyan parancsmagok készletét kínálja, amelyek az [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modellt használják az Azure-erőforrások kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="32f29-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="32f29-105">Az Azure PowerShell a .NET Standardet használja, így Windows, macOS és Linux rendszereken is elérhető.</span><span class="sxs-lookup"><span data-stu-id="32f29-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="32f29-106">Az Azure PowerShell az Azure Cloud Shellben is elérhető.</span><span class="sxs-lookup"><span data-stu-id="32f29-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="32f29-107">Az új Az modul bemutatása</span><span class="sxs-lookup"><span data-stu-id="32f29-107">About the new Az module</span></span>

<span data-ttu-id="32f29-108">Ez a dokumentáció az Azure PowerShell új Az modulját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="32f29-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="32f29-109">Ez az új modul a .NET Standardre épül.</span><span class="sxs-lookup"><span data-stu-id="32f29-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="32f29-110">A .NET Standard lehetővé teszi, hogy az Azure PowerShell a Windows rendszeren a PowerShell 5.1-es, más platformon pedig a PowerShell Core 6.x vagy újabb verziójával fusson.</span><span class="sxs-lookup"><span data-stu-id="32f29-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.1 on Windows or PowerShell Core 6.x and later on any platform.</span></span> <span data-ttu-id="32f29-111">Mostantól az Az modul az elsődleges módja Azure-ral való kommunikációnak a PowerShellen keresztül.</span><span class="sxs-lookup"><span data-stu-id="32f29-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="32f29-112">Az AzureRM-hez továbbra is elérhetőek lesznek hibajavítások, azonban nem bővül a továbbiakban új funkciókkal.</span><span class="sxs-lookup"><span data-stu-id="32f29-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="32f29-113">[Az Azure PowerShell Az modul bemutatása](new-azureps-module-az.md) című cikkben találja az új modul összes részletét, beleértve a parancsok új nevét és az AzureRM karbantartási terveit.</span><span class="sxs-lookup"><span data-stu-id="32f29-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="32f29-114">Ha azonnal meg szeretné kezdeni az új modul használatát, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="32f29-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="32f29-115">Emellett az [AzureRM dokumentációja](/powershell/azure/azurerm) is elérhető.</span><span class="sxs-lookup"><span data-stu-id="32f29-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="32f29-116">Bár az Azure-dokumentációban az új modul parancsmagneveinek frissítése folyamatban van, előfordulhat, hogy a cikkek még az AzureRM-parancsokat használják.</span><span class="sxs-lookup"><span data-stu-id="32f29-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="32f29-117">Az Az modul telepítése után ajánlott engedélyezni az AzureRM-parancsmagaliasokat az `Enable-AzureRmAlias` paranccsal.</span><span class="sxs-lookup"><span data-stu-id="32f29-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="32f29-118">További részleteket [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető cikkben talál.</span><span class="sxs-lookup"><span data-stu-id="32f29-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="32f29-119">Futtatás vagy telepítés</span><span class="sxs-lookup"><span data-stu-id="32f29-119">Run or install</span></span>

<span data-ttu-id="32f29-120">Az Azure PowerShell telepíthető a PowerShell 5.1-es vagy újabb verzióján a Windows rendszeren, a PowerShell Core 6.x vagy újabb verzióján bármely platformon, vagy az Azure Cloud Shellben is futtatható.</span><span class="sxs-lookup"><span data-stu-id="32f29-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell Core 6.x and later on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="32f29-121">Ha böngészőben szeretné futtatni az Azure Cloud Shell használatával, tekintse meg a [PowerShell Azure Cloud Shellben való használatát bemutató rövid útmutatót](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="32f29-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="32f29-122">Ha szeretné a rendszerére telepíteni az Azure PowerShellt, tekintse meg az[ Azure PowerShell telepítése](install-az-ps.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="32f29-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="32f29-123">A legújabb Azure PowerShell-kiadással kapcsolatos információkért tekintse meg a [kiadási megjegyzéseket](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="32f29-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="32f29-124">Első lépések</span><span class="sxs-lookup"><span data-stu-id="32f29-124">Get Started</span></span>

<span data-ttu-id="32f29-125">Az Azure PowerShell alapjainak megismeréséhez olvassa el az [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="32f29-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="32f29-126">Ha még nem ismeri a PowerShellt, érdemes lehet megtekintenie a bemutatókat:</span><span class="sxs-lookup"><span data-stu-id="32f29-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="32f29-127">A PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="32f29-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* [<span data-ttu-id="32f29-128">Parancsprogram-kezelés a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="32f29-128">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)
* [<span data-ttu-id="32f29-129">A PowerShell alapjai: (1. rész) Ismerkedés a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="32f29-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span></span>](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)

<span data-ttu-id="32f29-130">A következő példák segítségével megismerheti az Azure néhány gyakori használati esetét:</span><span class="sxs-lookup"><span data-stu-id="32f29-130">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="32f29-131">Linux rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="32f29-131">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="32f29-132">Windows rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="32f29-132">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="32f29-133">Web Apps</span><span class="sxs-lookup"><span data-stu-id="32f29-133">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="32f29-134">SQL Database-adatbázisok</span><span class="sxs-lookup"><span data-stu-id="32f29-134">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="32f29-135">Fejlessze a készségeit a Microsoft Learnnel</span><span class="sxs-lookup"><span data-stu-id="32f29-135">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="32f29-136">Azure-feladatok automatizálása szkriptek használatával a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="32f29-136">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="32f29-137">További interaktív oktatóanyagok...</span><span class="sxs-lookup"><span data-stu-id="32f29-137">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="32f29-138">Egyéb Azure PowerShell-modulok</span><span class="sxs-lookup"><span data-stu-id="32f29-138">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="32f29-139">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="32f29-139">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="32f29-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="32f29-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="32f29-141">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="32f29-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
