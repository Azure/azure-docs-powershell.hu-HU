---
title: Azure-előfizetések kezelése az Azure PowerShell-lel
description: Azure-előfizetések kezelése az Azure PowerShell-lel
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 778fdb463a42b609d3a94c910a2c0f9553ef4eb9
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "72370328"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="99877-103">Több Azure-előfizetés használata</span><span class="sxs-lookup"><span data-stu-id="99877-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="99877-104">A legtöbb Azure-felhasználó egész életében egy előfizetést használ.</span><span class="sxs-lookup"><span data-stu-id="99877-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="99877-105">Azonban több vállalat tagjaként, vagy ha a vállalat különböző csoportokra osztotta a hozzáférést bizonyos erőforrásokhoz, több előfizetéssel is rendelkezhet az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="99877-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="99877-106">A CLI az előfizetések globális és parancsonkénti kiválasztását is támogatja.</span><span class="sxs-lookup"><span data-stu-id="99877-106">The CLI supports selecting a subscription both globally and per command.</span></span>

<span data-ttu-id="99877-107">Az előfizetésekkel, számlázással és költségkezeléssel kapcsolatos további információkért lásd [a számlázás és költségkezelés dokumentációját](/azure/billing/).</span><span class="sxs-lookup"><span data-stu-id="99877-107">For detailed information on subscriptions, billing, and cost management, see the [billing and cost management documentation](/azure/billing/).</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="99877-108">Bérlők, felhasználók, és előfizetések</span><span class="sxs-lookup"><span data-stu-id="99877-108">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="99877-109">Előfordulhat, hogy nem egyértelműek a bérlők, a felhasználók és az előfizetések közötti különbségek az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="99877-109">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="99877-110">A _bérlő_ az Azure Active Directory azon entitása, amely az egész vállalatot magában foglalja.</span><span class="sxs-lookup"><span data-stu-id="99877-110">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="99877-111">A bérlőnek legalább egy _előfizetése_ és egy _felhasználója_ van.</span><span class="sxs-lookup"><span data-stu-id="99877-111">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="99877-112">A felhasználó egy egyén, aki kizárólag egy bérlővel van társítva: a vállalattal, amelyikhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="99877-112">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="99877-113">A felhasználók azok a fiókok, amelyekkel be lehet jelentkezni az Azure-ba az erőforrások létrehozásához, kezeléséhez és használatához.</span><span class="sxs-lookup"><span data-stu-id="99877-113">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="99877-114">A felhasználó több _előfizetéshez_ is hozzáférhet, amelyek a felhőszolgáltatások, köztük az Azure használatára vonatkozó, Microsofttal kötött megállapodások.</span><span class="sxs-lookup"><span data-stu-id="99877-114">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="99877-115">Minden erőforrás egy előfizetéshez van társítva.</span><span class="sxs-lookup"><span data-stu-id="99877-115">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="99877-116">A bérlők, felhasználók és előfizetések közötti különbségekről további információt az [Azure felhőszolgáltatásokkal kapcsolatos terminológiai szótárában](/azure/azure-glossary-cloud-terminology) talál.</span><span class="sxs-lookup"><span data-stu-id="99877-116">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="99877-117">Ha szeretné megtudni, hogyan adhat hozzá új előfizetést Azure Active Directory-bérlőjéhez, tekintse meg az [Azure-előfizetés hozzáadása az Azure Active Directoryhoz](/azure/active-directory/active-directory-how-subscriptions-associated-directory) című részt.</span><span class="sxs-lookup"><span data-stu-id="99877-117">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="99877-118">Egy adott bérlőbe való bejelentkezés módjának megismeréséhez tekintse meg [az Azure PowerShell-lel történő bejelentkezést](/powershell/azure/authenticate-azureps) ismertető cikket.</span><span class="sxs-lookup"><span data-stu-id="99877-118">To learn how to sign in to a specific tenant, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="99877-119">Az aktív előfizetés módosítása</span><span class="sxs-lookup"><span data-stu-id="99877-119">Change the active subscription</span></span>

<span data-ttu-id="99877-120">Az Azure PowerShellben az előfizetések erőforrásaihoz való hozzáféréshez az aktuális Azure-munkamenethez társított előfizetés módosítására van szükség.</span><span class="sxs-lookup"><span data-stu-id="99877-120">In Azure PowerShell, accessing the resources for a subscription requires changing the subscription associated with your current Azure session.</span></span>
<span data-ttu-id="99877-121">Ennek módja az aktív munkamenet módosítása, annak tekintetében, hogy mely bérlőn, előfizetésen és felhasználón futtassa a parancsmagokat.</span><span class="sxs-lookup"><span data-stu-id="99877-121">This is done by modifying the active session context, the information about which tenant, subscription, and user cmdlets should be run against.</span></span>
<span data-ttu-id="99877-122">Az előfizetések módosításához először Azure PowerShell-környezetobjektum lekérésére van szükség a [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) segítségével, majd az aktuális környezet módosítására a [Set-AzContext](/powershell/module/az.accounts/set-azcontext) használatával.</span><span class="sxs-lookup"><span data-stu-id="99877-122">In order to change subscriptions, an Azure PowerShell Context object first needs to be retrieved with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and then the current context changed with [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span></span>

<span data-ttu-id="99877-123">A következő példa bemutatja, hogyan lehet lekérni egy előfizetést a jelenleg aktív bérlőn, és aktív munkamenetként beállítani:</span><span class="sxs-lookup"><span data-stu-id="99877-123">The next example shows how to get a subscription in the currently active tenant, and set it as the active session:</span></span>

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

<span data-ttu-id="99877-124">Az Azure PowerShell-környezetekre vonatkozó további információért – beleértve azok mentését és a közöttük való gyors váltást a több előfizetés könnyű használata érdekében – tekintse meg a [hitelesítő adatok az Azure PowerShell-környezetekben való megőrzéséről](context-persistence.md) szóló szakaszt.</span><span class="sxs-lookup"><span data-stu-id="99877-124">To learn more about Azure PowerShell contexts, including how to save them and quickly switch between them for working with multiple subscriptions easily, see [Persist credentials with Azure PowerShell contexts](context-persistence.md).</span></span>
