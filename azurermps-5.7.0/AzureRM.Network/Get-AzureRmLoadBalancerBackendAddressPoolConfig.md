---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 5dbb8953559ee9b28673bb1fae1b857e540f298b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496436"
---
# <span data-ttu-id="43107-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="43107-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="43107-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43107-102">SYNOPSIS</span></span>
<span data-ttu-id="43107-103">Beilleszti a backend-címkészlet konfigurációját a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="43107-103">Gets a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43107-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43107-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43107-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="43107-105">DESCRIPTION</span></span>
<span data-ttu-id="43107-106">A **Get-AzureRmLoadBalancerBackendAddressPoolConfig** parancsmag egyetlen backend-címkészletet vagy a backend-címeket tartalmazó listák listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="43107-106">The **Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="43107-107">Példák</span><span class="sxs-lookup"><span data-stu-id="43107-107">EXAMPLES</span></span>

### <span data-ttu-id="43107-108">Példa 1: a backend-címkészlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="43107-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="43107-109">Az első parancs a MyResourceGroup nevű erőforráscsoport MyLoadBalancer nevű meglévő terheléselosztó elemét kapja, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="43107-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="43107-110">A második parancs beolvassa a BackendAddressPool02 nevű társított backend-cím alkalmazáskészletének konfigurációját a $loadbalancer betöltőhöz.</span><span class="sxs-lookup"><span data-stu-id="43107-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="43107-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43107-111">PARAMETERS</span></span>

### <span data-ttu-id="43107-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43107-112">-DefaultProfile</span></span>
<span data-ttu-id="43107-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43107-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43107-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43107-114">-LoadBalancer</span></span>
<span data-ttu-id="43107-115">A backend-címkészlet eléréséhez társított terheléselosztó.</span><span class="sxs-lookup"><span data-stu-id="43107-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43107-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43107-116">-Name</span></span>
<span data-ttu-id="43107-117">Itt adhatja meg annak a terheléselosztásnak a nevét, amely a backend-címkészletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="43107-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43107-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43107-118">CommonParameters</span></span>
<span data-ttu-id="43107-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43107-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43107-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43107-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43107-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43107-121">INPUTS</span></span>

### <span data-ttu-id="43107-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43107-122">PSLoadBalancer</span></span>
<span data-ttu-id="43107-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="43107-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="43107-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43107-124">OUTPUTS</span></span>

### <span data-ttu-id="43107-125">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="43107-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="43107-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43107-126">NOTES</span></span>

## <span data-ttu-id="43107-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43107-127">RELATED LINKS</span></span>

[<span data-ttu-id="43107-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="43107-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="43107-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43107-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="43107-130">Új – AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="43107-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="43107-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="43107-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


