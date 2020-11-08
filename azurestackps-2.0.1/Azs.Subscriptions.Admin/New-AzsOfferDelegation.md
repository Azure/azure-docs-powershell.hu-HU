---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 8a3797006bb5006b1b4e715b45c5e12763c49f32
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015185"
---
# <span data-ttu-id="55f9d-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="55f9d-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="55f9d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="55f9d-103">Hozza létre vagy frissítse az ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="55f9d-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="55f9d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55f9d-104">SYNTAX</span></span>

### <span data-ttu-id="55f9d-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55f9d-105">CreateExpanded (Default)</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-TargetSubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="55f9d-106">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="55f9d-106">Create</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55f9d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="55f9d-107">DESCRIPTION</span></span>
<span data-ttu-id="55f9d-108">Hozza létre vagy frissítse az ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="55f9d-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="55f9d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="55f9d-109">EXAMPLES</span></span>

### <span data-ttu-id="55f9d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="55f9d-110">Example 1</span></span>
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

<span data-ttu-id="55f9d-111">Hozzon létre egy új ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="55f9d-111">Create a new offer delegation.</span></span>

## <span data-ttu-id="55f9d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55f9d-112">PARAMETERS</span></span>

### <span data-ttu-id="55f9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f9d-113">-DefaultProfile</span></span>
<span data-ttu-id="55f9d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55f9d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55f9d-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="55f9d-115">-Location</span></span>
<span data-ttu-id="55f9d-116">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="55f9d-116">Location of the resource</span></span>

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

### <span data-ttu-id="55f9d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="55f9d-117">-Name</span></span>
<span data-ttu-id="55f9d-118">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="55f9d-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="55f9d-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="55f9d-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="55f9d-120">Delegált ajánlat</span><span class="sxs-lookup"><span data-stu-id="55f9d-120">Offer delegation.</span></span>
<span data-ttu-id="55f9d-121">A kivitelezéshez tekintse meg a OFFERDELEGATIONDEFINITION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="55f9d-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

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

### <span data-ttu-id="55f9d-122">-OfferName</span><span class="sxs-lookup"><span data-stu-id="55f9d-122">-OfferName</span></span>
<span data-ttu-id="55f9d-123">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="55f9d-123">Name of an offer.</span></span>

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

### <span data-ttu-id="55f9d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f9d-124">-ResourceGroupName</span></span>
<span data-ttu-id="55f9d-125">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="55f9d-125">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="55f9d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55f9d-126">-SubscriptionId</span></span>
<span data-ttu-id="55f9d-127">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="55f9d-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="55f9d-128">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55f9d-128">-TargetSubscriptionId</span></span>
<span data-ttu-id="55f9d-129">A delegált ajánlatot kapó előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="55f9d-129">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="55f9d-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="55f9d-130">-Confirm</span></span>
<span data-ttu-id="55f9d-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="55f9d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55f9d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f9d-132">-WhatIf</span></span>
<span data-ttu-id="55f9d-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="55f9d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55f9d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55f9d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55f9d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f9d-135">CommonParameters</span></span>
<span data-ttu-id="55f9d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55f9d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f9d-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="55f9d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f9d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55f9d-138">INPUTS</span></span>

### <span data-ttu-id="55f9d-139">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="55f9d-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="55f9d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55f9d-140">OUTPUTS</span></span>

### <span data-ttu-id="55f9d-141">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="55f9d-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="55f9d-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="55f9d-142">ALIASES</span></span>

## <span data-ttu-id="55f9d-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55f9d-143">NOTES</span></span>

<span data-ttu-id="55f9d-144">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="55f9d-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55f9d-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="55f9d-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="55f9d-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : delegált ajánlat</span><span class="sxs-lookup"><span data-stu-id="55f9d-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="55f9d-147">`[Location <String>]`: Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="55f9d-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="55f9d-148">`[SubscriptionId <String>]`: A delegált ajánlatot kapó előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="55f9d-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="55f9d-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55f9d-149">RELATED LINKS</span></span>

