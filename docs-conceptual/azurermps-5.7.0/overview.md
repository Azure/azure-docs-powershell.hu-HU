---
title: Az Azure PowerShell áttekintése | Microsoft Docs
description: Az Azure PowerShell áttekintése telepítési és konfigurációs hivatkozásokkal.
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: cd6b57ff6234895ec4f7a4200f9df0852b2280c2
ms.sourcegitcommit: 5f0013981fcea1d689649b9a2b2ffe84ae842e56
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2018
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="1f394-103">Az Azure PowerShell áttekintése</span><span class="sxs-lookup"><span data-stu-id="1f394-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="1f394-104">Az Azure PowerShell olyan parancsmagok készletét kínálja, amelyek az [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modellt használják az Azure-erőforrások kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="1f394-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="1f394-105">Használhatja a böngészőjében az [Azure Cloud Shell-lel](/azure/cloud-shell/overview), vagy telepítheti a helyi gépen, és használhatja bármely PowerShell-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="1f394-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="1f394-106">A [Cloud Shell-lel](/azure/cloud-shell/overview) futtassa az Azure PowerShellt a böngészőben, vagy [telepítse](install-azurerm-ps.md) saját számítógépére.</span><span class="sxs-lookup"><span data-stu-id="1f394-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="1f394-107">Ezután olvassa el az [Első lépések](get-started-azureps.md) című cikket, mielőtt használatba venné.</span><span class="sxs-lookup"><span data-stu-id="1f394-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="1f394-108">A legújabb kiadással kapcsolatos információkért lásd a [kibocsátási megjegyzéseket](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1f394-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="1f394-109">A következő példák segítenek megismerkedni az Azure PowerShell általános forgatókönyveinek végrehajtásával:</span><span class="sxs-lookup"><span data-stu-id="1f394-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="1f394-110">Linux rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="1f394-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="1f394-111">Windows rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="1f394-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="1f394-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="1f394-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="1f394-113">SQL Database-adatbázisok</span><span class="sxs-lookup"><span data-stu-id="1f394-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="1f394-114">Ha van olyan üzemelő példánya, amely a klasszikus telepítési modellt használja, és nem alakítható át, akkor az Azure PowerShell Service Management verzióját telepítheti.</span><span class="sxs-lookup"><span data-stu-id="1f394-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="1f394-115">További információ: [Az Azure PowerShell Service Management moduljának telepítése](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="1f394-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>


### <a name="need-help-with-powershell"></a><span data-ttu-id="1f394-116">Segítségre van szüksége a PowerShell-lel kapcsolatban?</span><span class="sxs-lookup"><span data-stu-id="1f394-116">Need help with PowerShell?</span></span>

<span data-ttu-id="1f394-117">Ha nem ismeri a PowerShellt, érdemes lehet elolvasni a PowerShellt bemutató anyagot.</span><span class="sxs-lookup"><span data-stu-id="1f394-117">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="1f394-118">A PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="1f394-118">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="1f394-119">Parancsprogram-kezelés a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="1f394-119">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="1f394-120">Megtekintheti a következő videót is: [A PowerShell alapjai: (1. rész) Ismerkedés a PowerShell-lel](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="1f394-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="1f394-121">Vagy részt vehet a Microsoft Virtual Academy a [PowerShell első lépéseit](https://mva.microsoft.com/liveevents/powershell-jumpstart) ismertető képzésén.</span><span class="sxs-lookup"><span data-stu-id="1f394-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="1f394-122">Egyéb Azure PowerShell-modulok</span><span class="sxs-lookup"><span data-stu-id="1f394-122">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="1f394-123">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="1f394-123">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="1f394-124">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="1f394-124">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="1f394-125">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="1f394-125">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="1f394-126">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="1f394-126">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
