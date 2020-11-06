---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: bbbdd28f0ea3916581c20cf8f078eca1cb2ddca6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490283"
---
# <span data-ttu-id="f628f-101">AzureRM. MarketplaceOrdering modul</span><span class="sxs-lookup"><span data-stu-id="f628f-101">AzureRM.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="f628f-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="f628f-102">Description</span></span>
<span data-ttu-id="f628f-103">Az ebben a szakaszban szereplő témakörök az Azure MarketplaceOrdering-hoz szükséges Azure PowerShell-parancsmagokat az Azure Resource Manager (ARM) keretrendszerben dokumentálják.</span><span class="sxs-lookup"><span data-stu-id="f628f-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="f628f-104">A parancsmagok a Microsoft. Azure. commands. MarketplaceOrdering névtérben találhatók.</span><span class="sxs-lookup"><span data-stu-id="f628f-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="f628f-105">Ezek a parancsmagok lehetővé teszik az Azure-felhasználóknak, hogy fogadjanak el egy piactér jogi feltételeit, amelyek további lehetőségeket kínálnak az ilyen megoldások programozott bevezetéséhez.</span><span class="sxs-lookup"><span data-stu-id="f628f-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="f628f-106">A felhasználók eltagadhatják a már elfogadott jogi fogalmakat is.</span><span class="sxs-lookup"><span data-stu-id="f628f-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="f628f-107">AzureRM. MarketplaceOrdering parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f628f-107">AzureRM.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="f628f-108">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="f628f-108">Get-AzureRmMarketplaceTerms</span></span>](Get-AzureRmMarketplaceTerms.md)
<span data-ttu-id="f628f-109">Az adott közzétevői azonosító (közzétevő), ajánlati azonosító (PRODUCT) és Plan azonosító (név) szerződési feltételeinek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="f628f-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="f628f-110">Az e parancs által visszaadott kitételeket a program átadja Set-AzureRmMarketplaceTerms a jogi fogalmak elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="f628f-110">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="f628f-111">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="f628f-111">Set-AzureRmMarketplaceTerms</span></span>](Set-AzureRmMarketplaceTerms.md)
<span data-ttu-id="f628f-112">Az adott közzétevői azonosító (közzétevő), az ajánlat azonosítója (szorzat) és a terv azonosítója (név) feltételeinek elfogadása vagy elvetése.</span><span class="sxs-lookup"><span data-stu-id="f628f-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="f628f-113">Kérjük, hogy a szerződési feltételeknek megfelelő Get-AzureRmMarketplaceTerms használatával töltse le a szerződési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="f628f-113">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

