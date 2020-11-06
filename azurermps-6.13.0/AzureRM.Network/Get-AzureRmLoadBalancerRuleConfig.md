---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b09aeb7288f69d0edc678578bbcc91306f5b0c2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505768"
---
# <span data-ttu-id="929a9-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="929a9-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="929a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="929a9-102">SYNOPSIS</span></span>
<span data-ttu-id="929a9-103">Kinyeri a szabály konfigurációját a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="929a9-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="929a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="929a9-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="929a9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="929a9-105">DESCRIPTION</span></span>
<span data-ttu-id="929a9-106">A **Get-AzureRmLoadBalancerRuleConfig** parancsmag egy vagy több szabály-konfigurációt kap a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="929a9-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="929a9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="929a9-107">EXAMPLES</span></span>

### <span data-ttu-id="929a9-108">Példa 1: terheléselosztó szabály-konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="929a9-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="929a9-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="929a9-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="929a9-110">A második parancs beolvassa a MyLBrulename nevű társított szabály konfigurációját a $slb terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="929a9-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="929a9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="929a9-111">PARAMETERS</span></span>

### <span data-ttu-id="929a9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="929a9-112">-DefaultProfile</span></span>
<span data-ttu-id="929a9-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="929a9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929a9-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="929a9-114">-LoadBalancer</span></span>
<span data-ttu-id="929a9-115">A beolvasás szabály konfigurációjával társított terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="929a9-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="929a9-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="929a9-116">-Name</span></span>
<span data-ttu-id="929a9-117">A beolvasott szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="929a9-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="929a9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929a9-118">CommonParameters</span></span>
<span data-ttu-id="929a9-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="929a9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929a9-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="929a9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929a9-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="929a9-121">INPUTS</span></span>

### <span data-ttu-id="929a9-122">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="929a9-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="929a9-123">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="929a9-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="929a9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="929a9-124">OUTPUTS</span></span>

### <span data-ttu-id="929a9-125">Microsoft. Azure. commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="929a9-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="929a9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="929a9-126">NOTES</span></span>

## <span data-ttu-id="929a9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="929a9-127">RELATED LINKS</span></span>

[<span data-ttu-id="929a9-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="929a9-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="929a9-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="929a9-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="929a9-130">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="929a9-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="929a9-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="929a9-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


