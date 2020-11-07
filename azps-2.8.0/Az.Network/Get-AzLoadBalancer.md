---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: 38a8083b96915ad40aafcb4437b88d9266cae1bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837328"
---
# <span data-ttu-id="070f6-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="070f6-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="070f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="070f6-102">SYNOPSIS</span></span>
<span data-ttu-id="070f6-103">Terheléselosztást kap.</span><span class="sxs-lookup"><span data-stu-id="070f6-103">Gets a load balancer.</span></span>

## <span data-ttu-id="070f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="070f6-104">SYNTAX</span></span>

### <span data-ttu-id="070f6-105">Kibontott (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="070f6-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="070f6-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="070f6-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="070f6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="070f6-107">DESCRIPTION</span></span>
<span data-ttu-id="070f6-108">A **Get-AzLoadBalancer** parancsmag egy vagy több, az erőforráscsoport által tartalmazott, az Azure rendszerhez tartozó terheléselosztást kap.</span><span class="sxs-lookup"><span data-stu-id="070f6-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="070f6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="070f6-109">EXAMPLES</span></span>

### <span data-ttu-id="070f6-110">Példa 1: terheléselosztó beszerzése</span><span class="sxs-lookup"><span data-stu-id="070f6-110">Example 1: Get a load balancer</span></span>
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
                             "Name": "Basic"
                           }
```

<span data-ttu-id="070f6-111">Ez a parancs a MyLoadBalancer nevű terheléselosztó parancsot kapja.</span><span class="sxs-lookup"><span data-stu-id="070f6-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="070f6-112">A parancsmag futtatásához a terheléselosztásnak léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="070f6-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="070f6-113">2. példa: a lista betöltői a szűréssel</span><span class="sxs-lookup"><span data-stu-id="070f6-113">Example 2: List load balancers using filtering</span></span>
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
                             "Name": "Basic"
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
                             "Name": "Basic"
                           }
```

<span data-ttu-id="070f6-114">Ez a parancs a "MyLoadBalancer" kezdetű névvel beilleszti az összes terheléselosztó nevet.</span><span class="sxs-lookup"><span data-stu-id="070f6-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="070f6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="070f6-115">PARAMETERS</span></span>

### <span data-ttu-id="070f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="070f6-116">-DefaultProfile</span></span>
<span data-ttu-id="070f6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="070f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="070f6-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="070f6-118">-ExpandResource</span></span>
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

### <span data-ttu-id="070f6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="070f6-119">-Name</span></span>
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

### <span data-ttu-id="070f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="070f6-120">-ResourceGroupName</span></span>
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

### <span data-ttu-id="070f6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="070f6-121">CommonParameters</span></span>
<span data-ttu-id="070f6-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="070f6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="070f6-123">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="070f6-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="070f6-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="070f6-124">INPUTS</span></span>

### <span data-ttu-id="070f6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="070f6-125">System.String</span></span>

## <span data-ttu-id="070f6-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="070f6-126">OUTPUTS</span></span>

### <span data-ttu-id="070f6-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="070f6-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="070f6-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="070f6-128">NOTES</span></span>

## <span data-ttu-id="070f6-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="070f6-129">RELATED LINKS</span></span>

[<span data-ttu-id="070f6-130">Új – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="070f6-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="070f6-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="070f6-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="070f6-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="070f6-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


