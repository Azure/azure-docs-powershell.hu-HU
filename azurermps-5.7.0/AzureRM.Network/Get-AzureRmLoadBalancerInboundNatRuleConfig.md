---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6464b1a7794278bf8bf350add937ac49f23431f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680148"
---
# <span data-ttu-id="d55d4-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d55d4-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d55d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d55d4-102">SYNOPSIS</span></span>
<span data-ttu-id="d55d4-103">Bejövő hálózati címfordítási szabály konfigurációjának beolvasása a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="d55d4-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d55d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d55d4-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d55d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d55d4-105">DESCRIPTION</span></span>
<span data-ttu-id="d55d4-106">A **Get-AzureRmLoadBalancerInboundNatRuleConfig** parancsmag egy vagy több bejövő hálózati címfordítási (NAT-) szabályt kap az Azure-terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="d55d4-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="d55d4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d55d4-107">EXAMPLES</span></span>

### <span data-ttu-id="d55d4-108">1. példa: bejövő CÍMFORDÍTÁSi szabály konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d55d4-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="d55d4-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, és a változóban tárolja a $slb.</span><span class="sxs-lookup"><span data-stu-id="d55d4-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="d55d4-110">A második parancs beolvassa a MyInboundNatRule1 nevű társított NAT-szabályt a $slb.</span><span class="sxs-lookup"><span data-stu-id="d55d4-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="d55d4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d55d4-111">PARAMETERS</span></span>

### <span data-ttu-id="d55d4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d55d4-112">-DefaultProfile</span></span>
<span data-ttu-id="d55d4-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d55d4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d55d4-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d55d4-114">-LoadBalancer</span></span>
<span data-ttu-id="d55d4-115">A beszerzéshez a bejövő NAT-szabályok konfigurációjának megfelelő terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="d55d4-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="d55d4-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d55d4-116">-Name</span></span>
<span data-ttu-id="d55d4-117">A beszerzéshez a bejövő NAT-szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d55d4-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="d55d4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55d4-118">CommonParameters</span></span>
<span data-ttu-id="d55d4-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d55d4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55d4-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d55d4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55d4-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d55d4-121">INPUTS</span></span>

### <span data-ttu-id="d55d4-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d55d4-122">PSLoadBalancer</span></span>
<span data-ttu-id="d55d4-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d55d4-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d55d4-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d55d4-124">OUTPUTS</span></span>

### <span data-ttu-id="d55d4-125">Microsoft. Azure. commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="d55d4-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="d55d4-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d55d4-126">NOTES</span></span>

## <span data-ttu-id="d55d4-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d55d4-127">RELATED LINKS</span></span>

[<span data-ttu-id="d55d4-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d55d4-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d55d4-129">Új – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d55d4-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d55d4-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d55d4-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d55d4-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d55d4-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


