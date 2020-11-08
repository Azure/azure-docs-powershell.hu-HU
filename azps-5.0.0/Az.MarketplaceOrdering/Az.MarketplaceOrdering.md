---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194603"
---
# <span data-ttu-id="776f2-101">Az. MarketplaceOrdering modul</span><span class="sxs-lookup"><span data-stu-id="776f2-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="776f2-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="776f2-102">Description</span></span>
<span data-ttu-id="776f2-103">Az ebben a szakaszban szereplő témakörök az Azure MarketplaceOrdering-hoz szükséges Azure PowerShell-parancsmagokat az Azure Resource Manager (ARM) keretrendszerben dokumentálják.</span><span class="sxs-lookup"><span data-stu-id="776f2-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="776f2-104">A parancsmagok a Microsoft. Azure. commands. MarketplaceOrdering névtérben találhatók.</span><span class="sxs-lookup"><span data-stu-id="776f2-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="776f2-105">Ezek a parancsmagok lehetővé teszik az Azure-felhasználóknak, hogy fogadjanak el egy piactér jogi feltételeit, amelyek további lehetőségeket kínálnak az ilyen megoldások programozott bevezetéséhez.</span><span class="sxs-lookup"><span data-stu-id="776f2-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="776f2-106">A felhasználók eltagadhatják a már elfogadott jogi fogalmakat is.</span><span class="sxs-lookup"><span data-stu-id="776f2-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="776f2-107">Az. MarketplaceOrdering parancsmagok</span><span class="sxs-lookup"><span data-stu-id="776f2-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="776f2-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="776f2-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="776f2-109">Az adott közzétevői azonosító (közzétevő), ajánlati azonosító (PRODUCT) és Plan azonosító (név) szerződési feltételeinek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="776f2-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="776f2-110">Az e parancs által visszaadott kitételeket a program átadja Set-AzMarketplaceTerms a jogi fogalmak elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="776f2-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="776f2-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="776f2-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="776f2-112">Az adott közzétevői azonosító (közzétevő), az ajánlat azonosítója (szorzat) és a terv azonosítója (név) feltételeinek elfogadása vagy elvetése.</span><span class="sxs-lookup"><span data-stu-id="776f2-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="776f2-113">Kérjük, hogy a szerződési feltételeknek megfelelő Get-AzMarketplaceTerms használatával töltse le a szerződési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="776f2-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>
