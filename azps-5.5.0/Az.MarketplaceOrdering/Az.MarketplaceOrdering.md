---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147498"
---
# <span data-ttu-id="ac9ba-101">Az.MarketplaceOrdering Module</span><span class="sxs-lookup"><span data-stu-id="ac9ba-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="ac9ba-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac9ba-102">Description</span></span>
<span data-ttu-id="ac9ba-103">A szakasz témakörei az Azure Resource Manager (ARM) keretrendszer Azure PowerShell-parancsmagokat tartalmaznak az Azure MarketplaceOrdering szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="ac9ba-104">A parancsmagok a Microsoft.Azure.Commands.MarketplaceOrdering namespace webhelyen létezik.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="ac9ba-105">Ezek a parancsmagok lehetővé teszik az Azure-felhasználóknak, hogy elfogadják a jogi feltételeket egy olyan piactéren, amely további programok telepítését teszi lehetővé ezen megoldásokhoz.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="ac9ba-106">A felhasználók a már elfogadott jogi feltételeket is elutasíthatnak.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="ac9ba-107">Az.MarketplaceOrdering parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ac9ba-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="ac9ba-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ac9ba-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="ac9ba-109">Szerezze be egy adott közzétevő-azonosító (Publisher), az ajánlatazonosító(Termék) és a tervazonosító(Név) szerződési feltételeit.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ac9ba-110">A jelen parancs által visszaadott kifejezésobjektumot át kell Set-AzMarketplaceTerms a jogi feltételek elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="ac9ba-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ac9ba-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="ac9ba-112">Elfogadhatja vagy elutasíthatja egy adott közzétevő-azonosító(Publisher), az ajánlatazonosító(Termék) és a tervazonosító(Név) feltételeit.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ac9ba-113">Kérjük, Get-AzMarketplaceTerms fel a szerződési feltételeket.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

