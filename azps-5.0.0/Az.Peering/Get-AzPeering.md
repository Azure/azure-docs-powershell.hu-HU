---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: 58ba131ab0bebc65d8fd5259d24b2846da229721
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194901"
---
# <span data-ttu-id="4c575-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="4c575-101">Get-AzPeering</span></span>

## <span data-ttu-id="4c575-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c575-102">SYNOPSIS</span></span>
<span data-ttu-id="4c575-103">Kinyeri az előfizetéshez tartozó társközi erőforrásokat</span><span class="sxs-lookup"><span data-stu-id="4c575-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="4c575-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c575-104">SYNTAX</span></span>

### <span data-ttu-id="4c575-105">BySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c575-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c575-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="4c575-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c575-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4c575-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c575-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c575-108">DESCRIPTION</span></span>
<span data-ttu-id="4c575-109">Az előfizetésből, erőforráscsoporthoz vagy név alapján kapja meg a munkatársait.</span><span class="sxs-lookup"><span data-stu-id="4c575-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="4c575-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4c575-110">EXAMPLES</span></span>

### <span data-ttu-id="4c575-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4c575-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeering

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}

Name                 : ContosoSeattlePeering
Sku                  : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringSku
Kind                 : Direct
Connections          : {99999}
UseForPeeringService : False
PeerAsn              : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSSubResource
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions/resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="4c575-112">Megkapja az előfizetéshez tartozó összes erőforrást.</span><span class="sxs-lookup"><span data-stu-id="4c575-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="4c575-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4c575-113">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceGroupName test -Name myExchangePeering1

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="4c575-114">Beolvassa az Exchange társközi nevű `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="4c575-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="4c575-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="4c575-115">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceId $resourceId

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="4c575-116">Megkapja az erőforrás-azonosító alapján megnevezett Exchange-társat `myExchangePeering1` .</span><span class="sxs-lookup"><span data-stu-id="4c575-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="4c575-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c575-117">PARAMETERS</span></span>

### <span data-ttu-id="4c575-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c575-118">-DefaultProfile</span></span>
<span data-ttu-id="4c575-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c575-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c575-120">-Kind</span><span class="sxs-lookup"><span data-stu-id="4c575-120">-Kind</span></span>
<span data-ttu-id="4c575-121">A teljes egyenrangú erőforrást jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="4c575-121">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c575-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c575-122">-Name</span></span>
<span data-ttu-id="4c575-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="4c575-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c575-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c575-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c575-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4c575-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c575-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c575-126">-ResourceId</span></span>
<span data-ttu-id="4c575-127">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="4c575-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c575-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c575-128">CommonParameters</span></span>
<span data-ttu-id="4c575-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c575-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c575-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4c575-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c575-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c575-131">INPUTS</span></span>

### <span data-ttu-id="4c575-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4c575-132">System.String</span></span>

## <span data-ttu-id="4c575-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c575-133">OUTPUTS</span></span>

### <span data-ttu-id="4c575-134">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="4c575-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="4c575-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c575-135">NOTES</span></span>

## <span data-ttu-id="4c575-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c575-136">RELATED LINKS</span></span>
