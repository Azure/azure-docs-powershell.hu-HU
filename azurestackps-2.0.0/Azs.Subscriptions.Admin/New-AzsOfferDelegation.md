---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 8a3797006bb5006b1b4e715b45c5e12763c49f32
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94015097"
---
# <span data-ttu-id="e92c3-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e92c3-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="e92c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e92c3-102">SYNOPSIS</span></span>
<span data-ttu-id="e92c3-103">Hozza létre vagy frissítse az ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="e92c3-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="e92c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e92c3-104">SYNTAX</span></span>

### <span data-ttu-id="e92c3-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e92c3-105">CreateExpanded (Default)</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-TargetSubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e92c3-106">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="e92c3-106">Create</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e92c3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e92c3-107">DESCRIPTION</span></span>
<span data-ttu-id="e92c3-108">Hozza létre vagy frissítse az ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="e92c3-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="e92c3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e92c3-109">EXAMPLES</span></span>

### <span data-ttu-id="e92c3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e92c3-110">Example 1</span></span>
```powershell
PS C:\> New-AzsOfferDelegation -Name "testofferdelegation" -OfferName "testoffer" -ResourceGroupName "testrg" -TargetSubscriptionId "dbc27112-f67a-4690-ba12-730f71cba018"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer/offerDelegations/testofferdel
                 egation
Location       : redmond
Name           : testoffer/testofferdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cba018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="e92c3-111">Hozzon létre egy új ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="e92c3-111">Create a new offer delegation.</span></span>

## <span data-ttu-id="e92c3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e92c3-112">PARAMETERS</span></span>

### <span data-ttu-id="e92c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e92c3-113">-DefaultProfile</span></span>
<span data-ttu-id="e92c3-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e92c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e92c3-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="e92c3-115">-Location</span></span>
<span data-ttu-id="e92c3-116">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="e92c3-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e92c3-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e92c3-117">-Name</span></span>
<span data-ttu-id="e92c3-118">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="e92c3-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="e92c3-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="e92c3-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="e92c3-120">Delegált ajánlat</span><span class="sxs-lookup"><span data-stu-id="e92c3-120">Offer delegation.</span></span>
<span data-ttu-id="e92c3-121">A kivitelezéshez tekintse meg a OFFERDELEGATIONDEFINITION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e92c3-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e92c3-122">-OfferName</span><span class="sxs-lookup"><span data-stu-id="e92c3-122">-OfferName</span></span>
<span data-ttu-id="e92c3-123">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="e92c3-123">Name of an offer.</span></span>

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

### <span data-ttu-id="e92c3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e92c3-124">-ResourceGroupName</span></span>
<span data-ttu-id="e92c3-125">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="e92c3-125">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e92c3-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e92c3-126">-SubscriptionId</span></span>
<span data-ttu-id="e92c3-127">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e92c3-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e92c3-128">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e92c3-128">-TargetSubscriptionId</span></span>
<span data-ttu-id="e92c3-129">A delegált ajánlatot kapó előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e92c3-129">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e92c3-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e92c3-130">-Confirm</span></span>
<span data-ttu-id="e92c3-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e92c3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e92c3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e92c3-132">-WhatIf</span></span>
<span data-ttu-id="e92c3-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e92c3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e92c3-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e92c3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e92c3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e92c3-135">CommonParameters</span></span>
<span data-ttu-id="e92c3-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e92c3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e92c3-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e92c3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e92c3-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e92c3-138">INPUTS</span></span>

### <span data-ttu-id="e92c3-139">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e92c3-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="e92c3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e92c3-140">OUTPUTS</span></span>

### <span data-ttu-id="e92c3-141">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e92c3-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="e92c3-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e92c3-142">ALIASES</span></span>

## <span data-ttu-id="e92c3-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e92c3-143">NOTES</span></span>

<span data-ttu-id="e92c3-144">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e92c3-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e92c3-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e92c3-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e92c3-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : delegált ajánlat</span><span class="sxs-lookup"><span data-stu-id="e92c3-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="e92c3-147">`[Location <String>]`: Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="e92c3-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="e92c3-148">`[SubscriptionId <String>]`: A delegált ajánlatot kapó előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e92c3-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="e92c3-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e92c3-149">RELATED LINKS</span></span>

