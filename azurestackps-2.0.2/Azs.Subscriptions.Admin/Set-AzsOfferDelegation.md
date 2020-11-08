---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 59afc363d040724bbd525afc6e1f599a995cfdcb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017159"
---
# <span data-ttu-id="46e2f-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="46e2f-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="46e2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="46e2f-103">Hozza létre vagy frissítse az ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="46e2f-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="46e2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46e2f-104">SYNTAX</span></span>

### <span data-ttu-id="46e2f-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46e2f-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-PropertiesSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="46e2f-106">Frissítés</span><span class="sxs-lookup"><span data-stu-id="46e2f-106">Update</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46e2f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="46e2f-107">DESCRIPTION</span></span>
<span data-ttu-id="46e2f-108">Hozza létre vagy frissítse az ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="46e2f-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="46e2f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="46e2f-109">EXAMPLES</span></span>

### <span data-ttu-id="46e2f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="46e2f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"

{{ Add output here }}
```

<span data-ttu-id="46e2f-111">Frissíti az ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="46e2f-111">Updates the offer delegation.</span></span>

## <span data-ttu-id="46e2f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46e2f-112">PARAMETERS</span></span>

### <span data-ttu-id="46e2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e2f-113">-DefaultProfile</span></span>
<span data-ttu-id="46e2f-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46e2f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46e2f-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="46e2f-115">-Location</span></span>
<span data-ttu-id="46e2f-116">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="46e2f-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46e2f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46e2f-117">-Name</span></span>
<span data-ttu-id="46e2f-118">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="46e2f-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46e2f-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="46e2f-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="46e2f-120">Delegált ajánlat</span><span class="sxs-lookup"><span data-stu-id="46e2f-120">Offer delegation.</span></span>
<span data-ttu-id="46e2f-121">A kivitelezéshez tekintse meg a OFFERDELEGATIONDEFINITION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="46e2f-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="46e2f-122">-OfferName</span><span class="sxs-lookup"><span data-stu-id="46e2f-122">-OfferName</span></span>
<span data-ttu-id="46e2f-123">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="46e2f-123">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46e2f-124">-PropertiesSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46e2f-124">-PropertiesSubscriptionId</span></span>
<span data-ttu-id="46e2f-125">A delegált ajánlatot kapó előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="46e2f-125">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46e2f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e2f-126">-ResourceGroupName</span></span>
<span data-ttu-id="46e2f-127">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="46e2f-127">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46e2f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46e2f-128">-SubscriptionId</span></span>
<span data-ttu-id="46e2f-129">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="46e2f-129">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46e2f-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46e2f-130">-Confirm</span></span>
<span data-ttu-id="46e2f-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46e2f-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46e2f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e2f-132">-WhatIf</span></span>
<span data-ttu-id="46e2f-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46e2f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46e2f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46e2f-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46e2f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e2f-135">CommonParameters</span></span>
<span data-ttu-id="46e2f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46e2f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e2f-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="46e2f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e2f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46e2f-138">INPUTS</span></span>

### <span data-ttu-id="46e2f-139">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="46e2f-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="46e2f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46e2f-140">OUTPUTS</span></span>

### <span data-ttu-id="46e2f-141">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="46e2f-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="46e2f-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="46e2f-142">ALIASES</span></span>

## <span data-ttu-id="46e2f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46e2f-143">NOTES</span></span>

<span data-ttu-id="46e2f-144">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="46e2f-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46e2f-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="46e2f-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="46e2f-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : delegált ajánlat</span><span class="sxs-lookup"><span data-stu-id="46e2f-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="46e2f-147">`[Location <String>]`: Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="46e2f-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="46e2f-148">`[SubscriptionId <String>]`: A delegált ajánlatot kapó előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="46e2f-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="46e2f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46e2f-149">RELATED LINKS</span></span>

