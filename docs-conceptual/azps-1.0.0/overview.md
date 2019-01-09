---
title: Az Azure PowerShell áttekintése
description: Az Azure PowerShell Az modul áttekintése, valamint a telepítéssel és az első lépésekkel kapcsolatos információk.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736460"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="3b7ec-103">Az Azure PowerShell áttekintése</span><span class="sxs-lookup"><span data-stu-id="3b7ec-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="3b7ec-104">Az Azure PowerShell olyan parancsmagok készletét kínálja, amelyek az [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modellt használják az Azure-erőforrások kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="3b7ec-105">Az Azure PowerShell a .NET Standardet használja, így Windows, macOS és Linux rendszereken is elérhető.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="3b7ec-106">Az Azure PowerShell az Azure Cloud Shellből is elérhető.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-106">Azure PowerShell is also available from Azure Cloud Shell.</span></span>

<span data-ttu-id="3b7ec-107">Az [Azure Cloud Shell-lel](/azure/cloud-shell/overview) futtassa az Azure PowerShellt a böngészőben, vagy [telepítse helyileg](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="3b7ec-107">Use [Azure Cloud Shell](/azure/cloud-shell/overview) to run Azure PowerShell in your browser, or [install locally](install-az-ps.md).</span></span> <span data-ttu-id="3b7ec-108">Az Azure PowerShell alapjainak megismeréséhez és az Azure használatának megkezdéséhez olvassa el az [első lépésekről](get-started-azureps.md) szóló cikket.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-108">Check out the [Get Started](get-started-azureps.md) article to learn the Azure PowerShell basics and get started with Azure.</span></span>

<span data-ttu-id="3b7ec-109">A legújabb Azure PowerShell-kiadással kapcsolatos információkért tekintse meg a [kiadási megjegyzéseket](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="3b7ec-109">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="3b7ec-110">Az új Az modul bemutatása</span><span class="sxs-lookup"><span data-stu-id="3b7ec-110">About the new Az module</span></span>

<span data-ttu-id="3b7ec-111">Ez a dokumentáció az Azure PowerShell új Az modulját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-111">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="3b7ec-112">Ez az új modul a .NET Standardre épül.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-112">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="3b7ec-113">A .NET Standard lehetővé teszi, hogy az Azure PowerShell Windows rendszeren a PowerShell 5.x, más platformon a PowerShell 6 verziójával fusson.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-113">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.x on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="3b7ec-114">Mostantól az Az modul az elsődleges módja Azure-ral való kommunikációnak a PowerShellen keresztül.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-114">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="3b7ec-115">Az AzureRM-hez továbbra is elérhetőek lesznek hibajavítások, azonban nem bővül a továbbiakban új funkciókkal.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-115">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="3b7ec-116">[Az Azure PowerShell Az modul bemutatása](new-azureps-module-az.md) című cikkben találja az új modul összes részletét, beleértve a parancsok új nevét és az AzureRM karbantartási terveit.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-116">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="3b7ec-117">Ha azonnal meg szeretné kezdeni az új modul használatát, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-117">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="3b7ec-118">Emellett az [AzureRM dokumentációja](/powershell/azure/azurerm) is elérhető.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-118">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="3b7ec-119">Bár az Azure-dokumentációban az új modul parancsmagneveinek frissítése folyamatban van, előfordulhat, hogy a cikkek még az AzureRM-parancsokat használják.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-119">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="3b7ec-120">Az Az modul telepítése után ajánlott engedélyezni az AzureRM-parancsmagaliasokat az `Enable-AzureRmAlias` paranccsal.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-120">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="3b7ec-121">További részleteket [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető cikkben talál.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-121">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="common-scenarios"></a><span data-ttu-id="3b7ec-122">Gyakori forgatókönyvek</span><span class="sxs-lookup"><span data-stu-id="3b7ec-122">Common scenarios</span></span>

<span data-ttu-id="3b7ec-123">A következő példák segítenek megismerkedni az Azure PowerShell általános forgatókönyveinek végrehajtásával:</span><span class="sxs-lookup"><span data-stu-id="3b7ec-123">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="3b7ec-124">Linux rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="3b7ec-124">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3b7ec-125">Windows rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="3b7ec-125">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3b7ec-126">Web Apps</span><span class="sxs-lookup"><span data-stu-id="3b7ec-126">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3b7ec-127">SQL Database-adatbázisok</span><span class="sxs-lookup"><span data-stu-id="3b7ec-127">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="3b7ec-128">A PowerShell alapjai</span><span class="sxs-lookup"><span data-stu-id="3b7ec-128">Learn PowerShell basics</span></span>

<span data-ttu-id="3b7ec-129">Ha még nem ismeri a PowerShellt, érdemes lehet megtekintenie a bemutatóját.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-129">If you're unfamiliar with PowerShell, an introduction may be helpful.</span></span>

* [<span data-ttu-id="3b7ec-130">A PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="3b7ec-130">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="3b7ec-131">Parancsprogram-kezelés a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="3b7ec-131">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="3b7ec-132">Az alábbi videót is megtekintheti: [A PowerShell alapjai: (1. rész) Ismerkedés a PowerShell-lel](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="3b7ec-132">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="3b7ec-133">Vagy részt vehet a Microsoft Virtual Academy a [PowerShell első lépéseit](https://mva.microsoft.com/liveevents/powershell-jumpstart) ismertető képzésén.</span><span class="sxs-lookup"><span data-stu-id="3b7ec-133">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="3b7ec-134">Fejlessze a készségeit a Microsoft Learnnel</span><span class="sxs-lookup"><span data-stu-id="3b7ec-134">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="3b7ec-135">Azure-feladatok automatizálása szkriptek használatával a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="3b7ec-135">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="3b7ec-136">További interaktív oktatóanyagok...</span><span class="sxs-lookup"><span data-stu-id="3b7ec-136">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="3b7ec-137">Egyéb Azure PowerShell-modulok</span><span class="sxs-lookup"><span data-stu-id="3b7ec-137">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="3b7ec-138">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3b7ec-138">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="3b7ec-139">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="3b7ec-139">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="3b7ec-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="3b7ec-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="3b7ec-141">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="3b7ec-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
