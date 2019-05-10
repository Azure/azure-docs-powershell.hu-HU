---
title: Azure-előfizetések kezelése az Azure PowerShell-lel
description: Azure-előfizetések kezelése az Azure PowerShell-lel
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 29d7c84d0ca9ae8d3e4e22f407b007d2d582f8bc
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048767"
---
# <a name="use-multiple-azure-subscriptions"></a>Több Azure-előfizetés használata

A legtöbb Azure-felhasználó egész életében egy előfizetést használ. Azonban több vállalat tagjaként, vagy ha a vállalat különböző csoportokra osztotta a hozzáférést bizonyos erőforrásokhoz, több előfizetéssel is rendelkezhet az Azure-ban. A CLI az előfizetések globális és parancsonkénti kiválasztását is támogatja.

## <a name="tenants-users-and-subscriptions"></a>Bérlők, felhasználók, és előfizetések

Előfordulhat, hogy nem egyértelműek a bérlők, a felhasználók és az előfizetések közötti különbségek az Azure-ban. A _bérlő_ az Azure Active Directory azon entitása, amely az egész vállalatot magában foglalja. A bérlőnek legalább egy _előfizetése_ és egy _felhasználója_ van. A felhasználó egy egyén, aki kizárólag egy bérlővel van társítva: a vállalattal, amelyikhez tartozik. A felhasználók azok a fiókok, amelyekkel be lehet jelentkezni az Azure-ba az erőforrások létrehozásához, kezeléséhez és használatához.
A felhasználó több _előfizetéshez_ is hozzáférhet, amelyek a felhőszolgáltatások, köztük az Azure használatára vonatkozó, Microsofttal kötött megállapodások. Minden erőforrás egy előfizetéshez van társítva.

A bérlők, felhasználók és előfizetések közötti különbségekről további információt az [Azure felhőszolgáltatásokkal kapcsolatos terminológiai szótárában](/azure/azure-glossary-cloud-terminology) talál.  Ha szeretné megtudni, hogyan adhat hozzá új előfizetést Azure Active Directory-bérlőjéhez, tekintse meg az [Azure-előfizetés hozzáadása az Azure Active Directoryhoz](/azure/active-directory/active-directory-how-subscriptions-associated-directory) című részt.
Egy adott bérlőbe való bejelentkezés módjának megismeréséhez tekintse meg [az Azure PowerShell-lel történő bejelentkezést](/powershell/azure/authenticate-azureps) ismertető cikket.

## <a name="change-the-active-subscription"></a>Az aktív előfizetés módosítása

Az Azure PowerShellben az előfizetések erőforrásaihoz való hozzáféréshez az aktuális Azure-munkamenethez társított előfizetés módosítására van szükség.
Ennek módja az aktív munkamenet módosítása, annak tekintetében, hogy mely bérlőn, előfizetésen és felhasználón futtassa a parancsmagokat.
Az előfizetések módosításához először Azure PowerShell-környezetobjektum lekérésére van szükség a [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) segítségével, majd az aktuális környezet módosítására a [Set-AzContext](/powershell/module/az.accounts/set-azcontext) használatával.

A következő példa bemutatja, hogyan lehet lekérni egy előfizetést a jelenleg aktív bérlőn, és aktív munkamenetként beállítani:

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

Az Azure PowerShell-környezetekre vonatkozó további információért – beleértve azok mentését és a közöttük való gyors váltást a több előfizetés könnyű használata érdekében – tekintse meg a [hitelesítő adatok az Azure PowerShell-környezetekben való megőrzéséről](context-persistence.md) szóló szakaszt.
