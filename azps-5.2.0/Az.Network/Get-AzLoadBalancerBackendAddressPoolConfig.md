---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f6acd469c49df7e67e8aa9bf00faf4952a33eb79
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365524"
---
# <span data-ttu-id="70575-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="70575-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="70575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70575-102">SYNOPSIS</span></span>
<span data-ttu-id="70575-103">Háttércímkészlet-konfigurációt kap a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="70575-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="70575-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="70575-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70575-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="70575-105">DESCRIPTION</span></span>
<span data-ttu-id="70575-106">A **Get-AzLoadBalancerBackendAddressPoolConfig** parancsmag egyetlen háttércímkészletet vagy a háttércímkészletek listáját kapja egy terheléselegyenítőn belül.</span><span class="sxs-lookup"><span data-stu-id="70575-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="70575-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="70575-107">EXAMPLES</span></span>

### <span data-ttu-id="70575-108">1. példa: A háttércímkészlet lekérte</span><span class="sxs-lookup"><span data-stu-id="70575-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="70575-109">Az első parancs egy MyLoadBalancer nevű meglévő terhelésegyenleg-kezelőt kap a MyResourceGroup nevű erőforráscsoportban, majd tárolja azt a $loadbalancer változóban.</span><span class="sxs-lookup"><span data-stu-id="70575-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="70575-110">A második parancs a backend-címkészlet BackendAddressPool02 nevű konfigurációját kapja meg a $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="70575-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="70575-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70575-111">PARAMETERS</span></span>

### <span data-ttu-id="70575-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70575-112">-DefaultProfile</span></span>
<span data-ttu-id="70575-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70575-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70575-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70575-114">-LoadBalancer</span></span>
<span data-ttu-id="70575-115">A háttércímkészlethez tartozó terheléskiegyenlítőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="70575-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70575-116">-Name</span><span class="sxs-lookup"><span data-stu-id="70575-116">-Name</span></span>
<span data-ttu-id="70575-117">Annak a terheléskiegyenlítőnek a nevét adja meg, amely a háttércímkészletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="70575-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70575-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70575-118">CommonParameters</span></span>
<span data-ttu-id="70575-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70575-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70575-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70575-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70575-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70575-121">INPUTS</span></span>

### <span data-ttu-id="70575-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70575-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="70575-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70575-123">OUTPUTS</span></span>

### <span data-ttu-id="70575-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="70575-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="70575-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="70575-125">NOTES</span></span>

## <span data-ttu-id="70575-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70575-126">RELATED LINKS</span></span>

[<span data-ttu-id="70575-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="70575-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="70575-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70575-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="70575-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="70575-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="70575-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="70575-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


