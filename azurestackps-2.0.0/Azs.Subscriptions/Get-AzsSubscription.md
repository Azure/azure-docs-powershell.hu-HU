---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azssubscription
schema: 2.0.0
ms.openlocfilehash: 7dce95be9a936d341e0f063fd6d89701b18c2ce7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844749"
---
# <span data-ttu-id="9b0cc-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="9b0cc-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="9b0cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="9b0cc-103">Részletes információkat kap az adott előfizetésről.</span><span class="sxs-lookup"><span data-stu-id="9b0cc-103">Gets details about particular subscription.</span></span>

## <span data-ttu-id="9b0cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b0cc-104">SYNTAX</span></span>

### <span data-ttu-id="9b0cc-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b0cc-105">List (Default)</span></span>
```
Get-AzsSubscription [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9b0cc-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="9b0cc-106">Get</span></span>
```
Get-AzsSubscription -SubscriptionId <String[]> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9b0cc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9b0cc-107">GetViaIdentity</span></span>
```
Get-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9b0cc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b0cc-108">DESCRIPTION</span></span>
<span data-ttu-id="9b0cc-109">Részletes információkat kap az adott előfizetésről.</span><span class="sxs-lookup"><span data-stu-id="9b0cc-109">Gets details about particular subscription.</span></span>

## <span data-ttu-id="9b0cc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9b0cc-110">EXAMPLES</span></span>

### <span data-ttu-id="9b0cc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9b0cc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsSubscription | fl *

DisplayName    : Test User
Id             : /subscriptions/97d84f7a-bef7-4f2d-b651-c553be472311
OfferId        : /delegatedProviders/default/offers/TestOffer-590376ac-c8dd-4b3d-9674-b5b8fcde095b
State          : Enabled
SubscriptionId : 97d84f7a-bef7-4f2d-b651-c553be472311
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb

DisplayName    : cnur
Id             : /subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId        : /delegatedProviders/default/offers/cnur4866tenantsubsvcoffer843
State          : Enabled
SubscriptionId : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="9b0cc-112">Az előfizetések listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="9b0cc-112">Get the list of subscriptions.</span></span>

## <span data-ttu-id="9b0cc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b0cc-113">PARAMETERS</span></span>

### <span data-ttu-id="9b0cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b0cc-114">-DefaultProfile</span></span>
<span data-ttu-id="9b0cc-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b0cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9b0cc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b0cc-116">-InputObject</span></span>
<span data-ttu-id="9b0cc-117">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9b0cc-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9b0cc-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b0cc-118">-SubscriptionId</span></span>
<span data-ttu-id="9b0cc-119">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9b0cc-119">Id of the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9b0cc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b0cc-120">CommonParameters</span></span>
<span data-ttu-id="9b0cc-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b0cc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b0cc-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9b0cc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b0cc-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b0cc-123">INPUTS</span></span>

### <span data-ttu-id="9b0cc-124">Microsoft. Azure. PowerShell. parancsmagok. előfizetés. models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="9b0cc-124">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="9b0cc-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b0cc-125">OUTPUTS</span></span>

### <span data-ttu-id="9b0cc-126">Microsoft. Azure. PowerShell. parancsmagok. előfizetés. models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="9b0cc-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="9b0cc-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b0cc-127">NOTES</span></span>

<span data-ttu-id="9b0cc-128">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9b0cc-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b0cc-129">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="9b0cc-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9b0cc-130">INPUTOBJECT <ISubscriptionIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="9b0cc-130">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b0cc-131">`[DelegatedProviderId <String>]`: A delegált szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9b0cc-131">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="9b0cc-132">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9b0cc-132">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b0cc-133">`[OfferName <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="9b0cc-133">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="9b0cc-134">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9b0cc-134">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="9b0cc-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b0cc-135">RELATED LINKS</span></span>

