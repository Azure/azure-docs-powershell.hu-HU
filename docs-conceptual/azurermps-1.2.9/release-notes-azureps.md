---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: c57ba563b5a4d4d19944fe8eca2cb4244ee5ed9e
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819711"
---
# <a name="release-notes"></a><span data-ttu-id="ad50d-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="ad50d-103">Release notes</span></span>

<span data-ttu-id="ad50d-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="ad50d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="ad50d-105">1.2.9-es verzió</span><span class="sxs-lookup"><span data-stu-id="ad50d-105">Version 1.2.9</span></span>

<span data-ttu-id="ad50d-106">A kiadás változásai</span><span class="sxs-lookup"><span data-stu-id="ad50d-106">Changes This Release</span></span>

* <span data-ttu-id="ad50d-107">AzureRm.AzureStackAdmin-modul</span><span class="sxs-lookup"><span data-stu-id="ad50d-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="ad50d-108">Az Add-AzureRmResourceProviderRegistration parancsmag módosítása a felügyeleti és bérlői Azure Resource Manager-felosztás támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="ad50d-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="ad50d-109">Új paraméter hozzáadása: -ResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="ad50d-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="ad50d-110">Az -AdminUri, -ApiVersion, -SubscriptionId és -Token paraméterek eltávolítása minden parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="ad50d-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="ad50d-111">Többször figyelmeztettük a felhasználókat a paraméterek elavulásával kapcsolatban, most pedig eltávolítottuk őket.</span><span class="sxs-lookup"><span data-stu-id="ad50d-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="ad50d-112">AzureStackStorage-modul</span><span class="sxs-lookup"><span data-stu-id="ad50d-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="ad50d-113">Új parancsmagok hozzáadása a tárolóáttelepítési forgatókönyvek támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="ad50d-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="ad50d-114">A belső összetevőkre és az alapul szolgáló funkciókra hivatkozó parancsmagok eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ad50d-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="ad50d-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="ad50d-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="ad50d-116">Új modul létrehozása az Azure PowerShell-parancsmagok verzióinak a verzióprofilokon keresztül történő kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="ad50d-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>