---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 9304471b12f33d677f493a3ee6803a1219d9f977
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302036"
---
# <span data-ttu-id="ed4db-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed4db-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ed4db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed4db-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4db-103">Bejövő hálózati címfordítási szabály konfigurációjának beolvasása a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="ed4db-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ed4db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed4db-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed4db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed4db-105">DESCRIPTION</span></span>
<span data-ttu-id="ed4db-106">A **Get-AzLoadBalancerInboundNatRuleConfig** parancsmag egy vagy több bejövő hálózati címfordítási (NAT-) szabályt kap az Azure-terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="ed4db-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="ed4db-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ed4db-107">EXAMPLES</span></span>

### <span data-ttu-id="ed4db-108">1. példa: bejövő CÍMFORDÍTÁSi szabály konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ed4db-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="ed4db-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, és a változóban tárolja a $slb.</span><span class="sxs-lookup"><span data-stu-id="ed4db-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="ed4db-110">A második parancs beolvassa a MyInboundNatRule1 nevű társított NAT-szabályt a $slb.</span><span class="sxs-lookup"><span data-stu-id="ed4db-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="ed4db-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed4db-111">PARAMETERS</span></span>

### <span data-ttu-id="ed4db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4db-112">-DefaultProfile</span></span>
<span data-ttu-id="ed4db-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed4db-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed4db-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ed4db-114">-LoadBalancer</span></span>
<span data-ttu-id="ed4db-115">A beszerzéshez a bejövő NAT-szabályok konfigurációjának megfelelő terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed4db-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="ed4db-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed4db-116">-Name</span></span>
<span data-ttu-id="ed4db-117">A beszerzéshez a bejövő NAT-szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed4db-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="ed4db-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4db-118">CommonParameters</span></span>
<span data-ttu-id="ed4db-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed4db-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4db-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ed4db-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4db-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed4db-121">INPUTS</span></span>

### <span data-ttu-id="ed4db-122">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ed4db-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ed4db-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed4db-123">OUTPUTS</span></span>

### <span data-ttu-id="ed4db-124">Microsoft. Azure. commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="ed4db-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="ed4db-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed4db-125">NOTES</span></span>

## <span data-ttu-id="ed4db-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed4db-126">RELATED LINKS</span></span>

[<span data-ttu-id="ed4db-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ed4db-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ed4db-128">Új – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed4db-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ed4db-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed4db-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ed4db-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed4db-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


