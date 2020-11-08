---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsdelegatedprovideroffer
schema: 2.0.0
ms.openlocfilehash: 118834c020a198d355d3f3b9e6dc17699f88e0cc
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015197"
---
# <span data-ttu-id="1b022-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="1b022-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="1b022-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b022-102">SYNOPSIS</span></span>
<span data-ttu-id="1b022-103">A megadott ajánlat beszerzése a delegált szolgáltatónak.</span><span class="sxs-lookup"><span data-stu-id="1b022-103">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="1b022-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b022-104">SYNTAX</span></span>

### <span data-ttu-id="1b022-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1b022-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1b022-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="1b022-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> -OfferName <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b022-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1b022-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderOffer -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b022-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b022-108">DESCRIPTION</span></span>
<span data-ttu-id="1b022-109">A megadott ajánlat beszerzése a delegált szolgáltatónak.</span><span class="sxs-lookup"><span data-stu-id="1b022-109">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="1b022-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1b022-110">EXAMPLES</span></span>

### <span data-ttu-id="1b022-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1b022-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d

{{ Add output here }}
```

<span data-ttu-id="1b022-112">A megadott delegált szolgáltatóra vonatkozó ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="1b022-112">Get the list of offers for the specified delegated provider</span></span>

## <span data-ttu-id="1b022-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b022-113">PARAMETERS</span></span>

### <span data-ttu-id="1b022-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b022-114">-DefaultProfile</span></span>
<span data-ttu-id="1b022-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b022-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b022-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="1b022-116">-DelegatedProviderId</span></span>
<span data-ttu-id="1b022-117">A delegált szolgáltató azonosítója</span><span class="sxs-lookup"><span data-stu-id="1b022-117">Id of the delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b022-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b022-118">-InputObject</span></span>
<span data-ttu-id="1b022-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1b022-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1b022-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="1b022-120">-OfferName</span></span>
<span data-ttu-id="1b022-121">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="1b022-121">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b022-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b022-122">CommonParameters</span></span>
<span data-ttu-id="1b022-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b022-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b022-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1b022-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b022-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b022-125">INPUTS</span></span>

### <span data-ttu-id="1b022-126">Microsoft. Azure. PowerShell. parancsmagok. előfizetés. models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="1b022-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="1b022-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b022-127">OUTPUTS</span></span>

### <span data-ttu-id="1b022-128">Microsoft. Azure. PowerShell. parancsmagok. előfizetés. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="1b022-128">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="1b022-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b022-129">NOTES</span></span>

<span data-ttu-id="1b022-130">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1b022-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1b022-131">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1b022-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1b022-132">INPUTOBJECT <ISubscriptionIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1b022-132">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1b022-133">`[DelegatedProviderId <String>]`: A delegált szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1b022-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="1b022-134">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1b022-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1b022-135">`[OfferName <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="1b022-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="1b022-136">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1b022-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="1b022-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b022-137">RELATED LINKS</span></span>

