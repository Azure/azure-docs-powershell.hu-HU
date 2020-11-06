---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 378d9521e309629bdb9e6ee58cfc1cd06fd9ef7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493643"
---
# <span data-ttu-id="97def-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97def-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="97def-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97def-102">SYNOPSIS</span></span>
<span data-ttu-id="97def-103">Bejövő hálózati címfordítási szabály konfigurációjának beolvasása a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="97def-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97def-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97def-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97def-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97def-105">DESCRIPTION</span></span>
<span data-ttu-id="97def-106">A **Get-AzureRmLoadBalancerInboundNatRuleConfig** parancsmag egy vagy több bejövő hálózati címfordítási (NAT-) szabályt kap az Azure-terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="97def-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="97def-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97def-107">EXAMPLES</span></span>

### <span data-ttu-id="97def-108">1. példa: bejövő CÍMFORDÍTÁSi szabály konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="97def-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="97def-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, és a változóban tárolja a $slb.</span><span class="sxs-lookup"><span data-stu-id="97def-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="97def-110">A második parancs beolvassa a MyInboundNatRule1 nevű társított NAT-szabályt a $slb.</span><span class="sxs-lookup"><span data-stu-id="97def-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="97def-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97def-111">PARAMETERS</span></span>

### <span data-ttu-id="97def-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97def-112">-DefaultProfile</span></span>
<span data-ttu-id="97def-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97def-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97def-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97def-114">-LoadBalancer</span></span>
<span data-ttu-id="97def-115">A beszerzéshez a bejövő NAT-szabályok konfigurációjának megfelelő terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="97def-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="97def-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97def-116">-Name</span></span>
<span data-ttu-id="97def-117">A beszerzéshez a bejövő NAT-szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97def-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="97def-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97def-118">CommonParameters</span></span>
<span data-ttu-id="97def-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97def-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97def-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97def-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97def-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97def-121">INPUTS</span></span>

### <span data-ttu-id="97def-122">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97def-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="97def-123">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="97def-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="97def-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97def-124">OUTPUTS</span></span>

### <span data-ttu-id="97def-125">Microsoft. Azure. commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="97def-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="97def-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97def-126">NOTES</span></span>

## <span data-ttu-id="97def-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97def-127">RELATED LINKS</span></span>

[<span data-ttu-id="97def-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97def-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="97def-129">Új – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97def-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="97def-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97def-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="97def-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97def-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


