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
ms.openlocfilehash: 710decaf8fcc0ba57e1e978a665474047393adc7
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/29/2019
ms.locfileid: "66375719"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="7932c-103">Az Azure PowerShell áttekintése</span><span class="sxs-lookup"><span data-stu-id="7932c-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="7932c-104">Az Azure PowerShell olyan parancsmagok készletét kínálja, amelyek az [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modellt használják az Azure-erőforrások kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="7932c-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="7932c-105">Az Azure PowerShell a .NET Standardet használja, így Windows, macOS és Linux rendszereken is elérhető.</span><span class="sxs-lookup"><span data-stu-id="7932c-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="7932c-106">Az Azure PowerShell az Azure Cloud Shellben is elérhető.</span><span class="sxs-lookup"><span data-stu-id="7932c-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="7932c-107">Az új Az modul bemutatása</span><span class="sxs-lookup"><span data-stu-id="7932c-107">About the new Az module</span></span>

<span data-ttu-id="7932c-108">Ez a dokumentáció az Azure PowerShell új Az modulját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="7932c-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="7932c-109">Ez az új modul a .NET Standardre épül.</span><span class="sxs-lookup"><span data-stu-id="7932c-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="7932c-110">A .NET Standard lehetővé teszi, hogy az Azure PowerShell a Windows rendszeren a PowerShell 5.1-es, más platformon pedig a PowerShell Core 6.x vagy újabb verziójával fusson.</span><span class="sxs-lookup"><span data-stu-id="7932c-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.1 on Windows or PowerShell Core 6.x and later on any platform.</span></span> <span data-ttu-id="7932c-111">Mostantól az Az modul az elsődleges módja Azure-ral való kommunikációnak a PowerShellen keresztül.</span><span class="sxs-lookup"><span data-stu-id="7932c-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="7932c-112">Az AzureRM-hez továbbra is elérhetőek lesznek hibajavítások, azonban nem bővül a továbbiakban új funkciókkal.</span><span class="sxs-lookup"><span data-stu-id="7932c-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="7932c-113">[Az Azure PowerShell Az modul bemutatása](new-azureps-module-az.md) című cikkben találja az új modul összes részletét, beleértve a parancsok új nevét és az AzureRM karbantartási terveit.</span><span class="sxs-lookup"><span data-stu-id="7932c-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="7932c-114">Ha azonnal meg szeretné kezdeni az új modul használatát, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="7932c-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="7932c-115">Emellett az [AzureRM dokumentációja](/powershell/azure/azurerm) is elérhető.</span><span class="sxs-lookup"><span data-stu-id="7932c-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="7932c-116">Bár az Azure-dokumentációban az új modul parancsmagneveinek frissítése folyamatban van, előfordulhat, hogy a cikkek még az AzureRM-parancsokat használják.</span><span class="sxs-lookup"><span data-stu-id="7932c-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="7932c-117">Az Az modul telepítése után ajánlott engedélyezni az AzureRM-parancsmagaliasokat az `Enable-AzureRmAlias` paranccsal.</span><span class="sxs-lookup"><span data-stu-id="7932c-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="7932c-118">További részleteket [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető cikkben talál.</span><span class="sxs-lookup"><span data-stu-id="7932c-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="7932c-119">Futtatás vagy telepítés</span><span class="sxs-lookup"><span data-stu-id="7932c-119">Run or install</span></span>

<span data-ttu-id="7932c-120">Az Azure PowerShell telepíthető a PowerShell 5.1-es vagy újabb verzióján a Windows rendszeren, a PowerShell Core 6.x vagy újabb verzióján bármely platformon, vagy az Azure Cloud Shellben is futtatható.</span><span class="sxs-lookup"><span data-stu-id="7932c-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell Core 6.x and later on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="7932c-121">Ha böngészőben szeretné futtatni az Azure Cloud Shell használatával, tekintse meg a [PowerShell Azure Cloud Shellben való használatát bemutató rövid útmutatót](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="7932c-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="7932c-122">Ha szeretné a rendszerére telepíteni az Azure PowerShellt, tekintse meg az[ Azure PowerShell telepítése](install-az-ps.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="7932c-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="7932c-123">A legújabb Azure PowerShell-kiadással kapcsolatos információkért tekintse meg a [kiadási megjegyzéseket](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="7932c-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="7932c-124">Első lépések</span><span class="sxs-lookup"><span data-stu-id="7932c-124">Get Started</span></span>

<span data-ttu-id="7932c-125">Az Azure PowerShell alapjainak megismeréséhez olvassa el az [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="7932c-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="7932c-126">Ha még nem ismeri a PowerShellt, érdemes lehet megtekintenie a bemutatókat:</span><span class="sxs-lookup"><span data-stu-id="7932c-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="7932c-127">A PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="7932c-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* [<span data-ttu-id="7932c-128">Parancsprogram-kezelés a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="7932c-128">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)
* [<span data-ttu-id="7932c-129">A PowerShell alapjai: (1. rész) Ismerkedés a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="7932c-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span></span>](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)
* <span data-ttu-id="7932c-130">Microsoft Virtual Academy – [A PowerShell első lépéseit bemutató rövid ismertető](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span><span class="sxs-lookup"><span data-stu-id="7932c-130">Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span></span>

<span data-ttu-id="7932c-131">A következő példák segítségével megismerheti az Azure néhány gyakori használati esetét:</span><span class="sxs-lookup"><span data-stu-id="7932c-131">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="7932c-132">Linux rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="7932c-132">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="7932c-133">Windows rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="7932c-133">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="7932c-134">Web Apps</span><span class="sxs-lookup"><span data-stu-id="7932c-134">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="7932c-135">SQL Database-adatbázisok</span><span class="sxs-lookup"><span data-stu-id="7932c-135">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="7932c-136">Fejlessze a készségeit a Microsoft Learnnel</span><span class="sxs-lookup"><span data-stu-id="7932c-136">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="7932c-137">Azure-feladatok automatizálása szkriptek használatával a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="7932c-137">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="7932c-138">További interaktív oktatóanyagok...</span><span class="sxs-lookup"><span data-stu-id="7932c-138">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="7932c-139">Egyéb Azure PowerShell-modulok</span><span class="sxs-lookup"><span data-stu-id="7932c-139">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="7932c-140">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="7932c-140">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="7932c-141">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7932c-141">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="7932c-142">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="7932c-142">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
