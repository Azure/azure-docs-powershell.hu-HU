---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93657832"
---
# Az. MarketplaceOrdering modul
## Leírás
Az ebben a szakaszban szereplő témakörök az Azure MarketplaceOrdering-hoz szükséges Azure PowerShell-parancsmagokat az Azure Resource Manager (ARM) keretrendszerben dokumentálják. A parancsmagok a Microsoft. Azure. commands. MarketplaceOrdering névtérben találhatók. Ezek a parancsmagok lehetővé teszik az Azure-felhasználóknak, hogy fogadjanak el egy piactér jogi feltételeit, amelyek további lehetőségeket kínálnak az ilyen megoldások programozott bevezetéséhez. A felhasználók eltagadhatják a már elfogadott jogi fogalmakat is.

## Az. MarketplaceOrdering parancsmagok
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Az adott közzétevői azonosító (közzétevő), ajánlati azonosító (PRODUCT) és Plan azonosító (név) szerződési feltételeinek beszerzése. Az e parancs által visszaadott kitételeket a program átadja Set-AzMarketplaceTerms a jogi fogalmak elfogadásához.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Az adott közzétevői azonosító (közzétevő), az ajánlat azonosítója (szorzat) és a terv azonosítója (név) feltételeinek elfogadása vagy elvetése. Kérjük, hogy a szerződési feltételeknek megfelelő Get-AzMarketplaceTerms használatával töltse le a szerződési szabályokat.

