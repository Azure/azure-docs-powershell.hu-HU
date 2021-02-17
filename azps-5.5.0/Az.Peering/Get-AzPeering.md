---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: 58ba131ab0bebc65d8fd5259d24b2846da229721
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156618"
---
# <span data-ttu-id="c646d-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c646d-101">Get-AzPeering</span></span>

## <span data-ttu-id="c646d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c646d-102">SYNOPSIS</span></span>
<span data-ttu-id="c646d-103">Társviszony-létesítő erőforrások lekérte egy előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="c646d-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="c646d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c646d-104">SYNTAX</span></span>

### <span data-ttu-id="c646d-105">BySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c646d-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c646d-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="c646d-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c646d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c646d-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c646d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c646d-108">DESCRIPTION</span></span>
<span data-ttu-id="c646d-109">A társviszonyokat egy előfizetésből, erőforráscsoportból vagy név alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c646d-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="c646d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c646d-110">EXAMPLES</span></span>

### <span data-ttu-id="c646d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c646d-111">Example 1</span></span>
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

<span data-ttu-id="c646d-112">Beveszi az előfizetés összes erőforrását.</span><span class="sxs-lookup"><span data-stu-id="c646d-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="c646d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c646d-113">Example 2</span></span>
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

<span data-ttu-id="c646d-114">Az Exchange társviszony-létesítésének neve `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="c646d-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="c646d-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="c646d-115">Example 2</span></span>
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

<span data-ttu-id="c646d-116">Az erőforrásazonosító alapján elnevezi az Exchange `myExchangePeering1` társviszony-létesítését.</span><span class="sxs-lookup"><span data-stu-id="c646d-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="c646d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c646d-117">PARAMETERS</span></span>

### <span data-ttu-id="c646d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c646d-118">-DefaultProfile</span></span>
<span data-ttu-id="c646d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c646d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c646d-120">-Kind</span><span class="sxs-lookup"><span data-stu-id="c646d-120">-Kind</span></span>
<span data-ttu-id="c646d-121">Az összes társviszony-létesítő erőforrást megjeleníti kind szerint.</span><span class="sxs-lookup"><span data-stu-id="c646d-121">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="c646d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c646d-122">-Name</span></span>
<span data-ttu-id="c646d-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="c646d-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="c646d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c646d-124">-ResourceGroupName</span></span>
<span data-ttu-id="c646d-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c646d-125">The resource group name.</span></span>

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

### <span data-ttu-id="c646d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c646d-126">-ResourceId</span></span>
<span data-ttu-id="c646d-127">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="c646d-127">The resource id string name.</span></span>

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

### <span data-ttu-id="c646d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c646d-128">CommonParameters</span></span>
<span data-ttu-id="c646d-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c646d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c646d-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c646d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c646d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c646d-131">INPUTS</span></span>

### <span data-ttu-id="c646d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c646d-132">System.String</span></span>

## <span data-ttu-id="c646d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c646d-133">OUTPUTS</span></span>

### <span data-ttu-id="c646d-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="c646d-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="c646d-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c646d-135">NOTES</span></span>

## <span data-ttu-id="c646d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c646d-136">RELATED LINKS</span></span>
