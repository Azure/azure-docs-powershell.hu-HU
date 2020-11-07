---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6b866dc04975c2cde17509182e21936a2d6c9363
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841617"
---
# <span data-ttu-id="92d57-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92d57-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="92d57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92d57-102">SYNOPSIS</span></span>
<span data-ttu-id="92d57-103">Bejövő hálózati címfordítási szabály konfigurációjának beolvasása a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="92d57-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="92d57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92d57-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92d57-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="92d57-105">DESCRIPTION</span></span>
<span data-ttu-id="92d57-106">A **Get-AzLoadBalancerInboundNatRuleConfig** parancsmag egy vagy több bejövő hálózati címfordítási (NAT-) szabályt kap az Azure-terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="92d57-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="92d57-107">Példák</span><span class="sxs-lookup"><span data-stu-id="92d57-107">EXAMPLES</span></span>

### <span data-ttu-id="92d57-108">1. példa: bejövő CÍMFORDÍTÁSi szabály konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="92d57-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="92d57-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, és a változóban tárolja a $slb.</span><span class="sxs-lookup"><span data-stu-id="92d57-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="92d57-110">A második parancs beolvassa a MyInboundNatRule1 nevű társított NAT-szabályt a $slb.</span><span class="sxs-lookup"><span data-stu-id="92d57-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="92d57-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92d57-111">PARAMETERS</span></span>

### <span data-ttu-id="92d57-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d57-112">-DefaultProfile</span></span>
<span data-ttu-id="92d57-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92d57-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92d57-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92d57-114">-LoadBalancer</span></span>
<span data-ttu-id="92d57-115">A beszerzéshez a bejövő NAT-szabályok konfigurációjának megfelelő terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="92d57-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="92d57-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="92d57-116">-Name</span></span>
<span data-ttu-id="92d57-117">A beszerzéshez a bejövő NAT-szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="92d57-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="92d57-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d57-118">CommonParameters</span></span>
<span data-ttu-id="92d57-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92d57-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d57-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92d57-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d57-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92d57-121">INPUTS</span></span>

### <span data-ttu-id="92d57-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92d57-122">PSLoadBalancer</span></span>
<span data-ttu-id="92d57-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="92d57-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="92d57-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92d57-124">OUTPUTS</span></span>

### <span data-ttu-id="92d57-125">Microsoft. Azure. commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="92d57-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="92d57-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92d57-126">NOTES</span></span>

## <span data-ttu-id="92d57-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92d57-127">RELATED LINKS</span></span>

[<span data-ttu-id="92d57-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92d57-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="92d57-129">Új – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92d57-129">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="92d57-130">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92d57-130">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="92d57-131">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92d57-131">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


