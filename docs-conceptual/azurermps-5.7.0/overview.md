---
title: Az Azure PowerShell áttekintése | Microsoft Docs
description: Az Azure PowerShell áttekintése telepítési és konfigurációs hivatkozásokkal.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: b260abb91de26dadac31340f17f97ff378813fac
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "67863206"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="89f0e-103">Az Azure PowerShell áttekintése</span><span class="sxs-lookup"><span data-stu-id="89f0e-103">Overview of Azure PowerShell</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

<span data-ttu-id="89f0e-104">Az Azure PowerShell olyan parancsmagok készletét kínálja, amelyek az [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modellt használják az Azure-erőforrások kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="89f0e-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="89f0e-105">Használhatja a böngészőjében az [Azure Cloud Shell-lel](/azure/cloud-shell/overview), vagy telepítheti a helyi gépen, és használhatja bármely PowerShell-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="89f0e-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="89f0e-106">A [Cloud Shell-lel](/azure/cloud-shell/overview) futtassa az Azure PowerShellt a böngészőben, vagy [telepítse](install-azurerm-ps.md) saját számítógépére.</span><span class="sxs-lookup"><span data-stu-id="89f0e-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="89f0e-107">Ezután olvassa el az [Első lépések](get-started-azureps.md) című cikket a használat megkezdéséhez.</span><span class="sxs-lookup"><span data-stu-id="89f0e-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="89f0e-108">A legújabb kiadással kapcsolatos információkért tekintse meg a [kibocsátási megjegyzéseket](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="89f0e-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="89f0e-109">A következő példák segítenek megismerkedni az Azure PowerShell általános forgatókönyveinek végrehajtásával:</span><span class="sxs-lookup"><span data-stu-id="89f0e-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="89f0e-110">Linux rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="89f0e-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="89f0e-111">Windows rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="89f0e-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="89f0e-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="89f0e-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="89f0e-113">SQL Database-adatbázisok</span><span class="sxs-lookup"><span data-stu-id="89f0e-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="89f0e-114">A PowerShell alapjai</span><span class="sxs-lookup"><span data-stu-id="89f0e-114">Learn PowerShell basics</span></span>

<span data-ttu-id="89f0e-115">Ha nem ismeri a PowerShellt, érdemes lehet elolvasni a PowerShellt bemutató anyagot.</span><span class="sxs-lookup"><span data-stu-id="89f0e-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="89f0e-116">A PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="89f0e-116">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="89f0e-117">Parancsprogram-kezelés a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="89f0e-117">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="89f0e-118">Megtekintheti a következő videót is: [A PowerShell alapjai: (1. rész) Ismerkedés a PowerShell-lel](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="89f0e-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="89f0e-119">Egyéb Azure PowerShell-modulok</span><span class="sxs-lookup"><span data-stu-id="89f0e-119">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="89f0e-120">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="89f0e-120">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="89f0e-121">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="89f0e-121">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="89f0e-122">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="89f0e-122">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="89f0e-123">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="89f0e-123">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
