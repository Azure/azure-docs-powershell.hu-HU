---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: b320d8d938264700fdde320cad5844325f66b938
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837587"
---
# <span data-ttu-id="3b710-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3b710-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="3b710-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b710-102">SYNOPSIS</span></span>
<span data-ttu-id="3b710-103">Beilleszti a backend-címkészlet konfigurációját a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="3b710-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="3b710-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b710-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b710-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b710-105">DESCRIPTION</span></span>
<span data-ttu-id="3b710-106">A **Get-AzLoadBalancerBackendAddressPoolConfig** parancsmag egyetlen backend-címkészletet vagy a backend-címeket tartalmazó listák listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="3b710-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="3b710-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b710-107">EXAMPLES</span></span>

### <span data-ttu-id="3b710-108">Példa 1: a backend-címkészlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="3b710-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="3b710-109">Az első parancs a MyResourceGroup nevű erőforráscsoport MyLoadBalancer nevű meglévő terheléselosztó elemét kapja, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3b710-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="3b710-110">A második parancs beolvassa a BackendAddressPool02 nevű társított backend-cím alkalmazáskészletének konfigurációját a $loadbalancer betöltőhöz.</span><span class="sxs-lookup"><span data-stu-id="3b710-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="3b710-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b710-111">PARAMETERS</span></span>

### <span data-ttu-id="3b710-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b710-112">-DefaultProfile</span></span>
<span data-ttu-id="3b710-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b710-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b710-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3b710-114">-LoadBalancer</span></span>
<span data-ttu-id="3b710-115">A backend-címkészlet eléréséhez társított terheléselosztó.</span><span class="sxs-lookup"><span data-stu-id="3b710-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="3b710-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3b710-116">-Name</span></span>
<span data-ttu-id="3b710-117">Itt adhatja meg annak a terheléselosztásnak a nevét, amely a backend-címkészletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3b710-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="3b710-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b710-118">CommonParameters</span></span>
<span data-ttu-id="3b710-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b710-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b710-120">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3b710-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b710-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b710-121">INPUTS</span></span>

### <span data-ttu-id="3b710-122">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3b710-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3b710-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b710-123">OUTPUTS</span></span>

### <span data-ttu-id="3b710-124">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3b710-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="3b710-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b710-125">NOTES</span></span>

## <span data-ttu-id="3b710-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b710-126">RELATED LINKS</span></span>

[<span data-ttu-id="3b710-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3b710-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3b710-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3b710-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="3b710-129">Új – AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3b710-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3b710-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3b710-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


