---
title: Az Azure PowerShell áttekintése | Microsoft Docs
description: Az Azure PowerShell áttekintése telepítési és konfigurációs hivatkozásokkal.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/20/2018
ms.openlocfilehash: 9d1b9c35829facc34cd7c252cb450fcce18685b2
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/28/2020
ms.locfileid: "84122231"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="0e824-103">Az Azure PowerShell áttekintése</span><span class="sxs-lookup"><span data-stu-id="0e824-103">Overview of Azure PowerShell</span></span>

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

<span data-ttu-id="0e824-104">Az Azure PowerShell olyan parancsmagok készletét kínálja, amelyek az [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modellt használják az Azure-erőforrások kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="0e824-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="0e824-105">Használhatja a böngészőjében az [Azure Cloud Shell-lel](/azure/cloud-shell/overview), vagy telepítheti a helyi gépen, és használhatja bármely PowerShell-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="0e824-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="0e824-106">A [Cloud Shell-lel](/azure/cloud-shell/overview) futtassa az Azure PowerShellt a böngészőben, vagy [telepítse](install-azurerm-ps.md) saját számítógépére.</span><span class="sxs-lookup"><span data-stu-id="0e824-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="0e824-107">Ezután olvassa el az [Első lépések](get-started-azureps.md) című cikket, mielőtt használatba venné.</span><span class="sxs-lookup"><span data-stu-id="0e824-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="0e824-108">A legújabb kiadással kapcsolatos információkért lásd a [kibocsátási megjegyzéseket](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0e824-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="0e824-109">A következő példák segítenek megismerkedni az Azure PowerShell általános forgatókönyveinek végrehajtásával:</span><span class="sxs-lookup"><span data-stu-id="0e824-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

- [<span data-ttu-id="0e824-110">Linux rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="0e824-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="0e824-111">Windows rendszerű virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="0e824-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="0e824-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="0e824-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="0e824-113">SQL Database-adatbázisok</span><span class="sxs-lookup"><span data-stu-id="0e824-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="0e824-114">A PowerShell alapjai</span><span class="sxs-lookup"><span data-stu-id="0e824-114">Learn PowerShell basics</span></span>

<span data-ttu-id="0e824-115">Ha nem ismeri a PowerShellt, érdemes lehet elolvasni a PowerShellt bemutató anyagot.</span><span class="sxs-lookup"><span data-stu-id="0e824-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

- [<span data-ttu-id="0e824-116">A PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="0e824-116">Installing PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
- [<span data-ttu-id="0e824-117">PowerShell – tanulási források</span><span class="sxs-lookup"><span data-stu-id="0e824-117">PowerShell learning resources</span></span>](/powershell/scripting/learn/more-powershell-learning)

<span data-ttu-id="0e824-118">Az alábbi videót is megtekintheti: [A PowerShell alapjai: (1. rész) Ismerkedés a PowerShell-lel](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="0e824-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="0e824-119">Fejlessze a készségeit a Microsoft Learnnel</span><span class="sxs-lookup"><span data-stu-id="0e824-119">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="0e824-120">Azure-feladatok automatizálása szkriptek használatával a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="0e824-120">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="0e824-121">További interaktív oktatóanyagok...</span><span class="sxs-lookup"><span data-stu-id="0e824-121">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="0e824-122">Egyéb Azure PowerShell-modulok</span><span class="sxs-lookup"><span data-stu-id="0e824-122">Other Azure PowerShell modules</span></span>

- [<span data-ttu-id="0e824-123">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="0e824-123">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
- [<span data-ttu-id="0e824-124">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="0e824-124">Azure Information Protection</span></span>](/powershell/azure/aip/)
- [<span data-ttu-id="0e824-125">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0e824-125">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
- [<span data-ttu-id="0e824-126">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="0e824-126">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
