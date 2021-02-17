---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: dd887874540a216cc826f807059e6534b99e28f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147114"
---
# <span data-ttu-id="f50ba-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f50ba-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="f50ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f50ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f50ba-103">Terheléselosztást kap.</span><span class="sxs-lookup"><span data-stu-id="f50ba-103">Gets a load balancer.</span></span>

## <span data-ttu-id="f50ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f50ba-104">SYNTAX</span></span>

### <span data-ttu-id="f50ba-105">NoExpand (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f50ba-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f50ba-106">Kibontás</span><span class="sxs-lookup"><span data-stu-id="f50ba-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f50ba-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f50ba-107">DESCRIPTION</span></span>
<span data-ttu-id="f50ba-108">A **Get-AzLoadBalancer** parancsmag egy vagy több Olyan Azure terhelésegyenleg-kezelőt kap, amely egy erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="f50ba-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="f50ba-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f50ba-109">EXAMPLES</span></span>

### <span data-ttu-id="f50ba-110">1. példa: Terheléselosztást kell lehozni</span><span class="sxs-lookup"><span data-stu-id="f50ba-110">Example 1: Get a load balancer</span></span>
```
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer1" -ResourceGroupName "MyResourceGroup"

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="f50ba-111">Ez a parancs a MyLoadBalancer nevű terheléselosztást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f50ba-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="f50ba-112">A parancsmag futtatásához terheléselegyenlőnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f50ba-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="f50ba-113">2. példa: Terheléselosztási lista szűréssel</span><span class="sxs-lookup"><span data-stu-id="f50ba-113">Example 2: List load balancers using filtering</span></span>
```
PS C:\> Get-AzLoadBalancer -Name MyLoadBalancer*

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }

Name                     : MyLoadBalancer2
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="f50ba-114">Ez a parancs a "MyLoadBalancer" névvel kezdődik minden terhelésegyensúlyzóhoz</span><span class="sxs-lookup"><span data-stu-id="f50ba-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="f50ba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f50ba-115">PARAMETERS</span></span>

### <span data-ttu-id="f50ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f50ba-116">-DefaultProfile</span></span>
<span data-ttu-id="f50ba-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f50ba-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f50ba-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f50ba-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50ba-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f50ba-119">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f50ba-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f50ba-120">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f50ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f50ba-121">CommonParameters</span></span>
<span data-ttu-id="f50ba-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f50ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f50ba-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f50ba-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f50ba-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f50ba-124">INPUTS</span></span>

### <span data-ttu-id="f50ba-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f50ba-125">System.String</span></span>

## <span data-ttu-id="f50ba-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f50ba-126">OUTPUTS</span></span>

### <span data-ttu-id="f50ba-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f50ba-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f50ba-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f50ba-128">NOTES</span></span>

## <span data-ttu-id="f50ba-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f50ba-129">RELATED LINKS</span></span>

[<span data-ttu-id="f50ba-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f50ba-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="f50ba-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f50ba-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="f50ba-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f50ba-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


