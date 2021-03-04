---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 816c94281c246762dac41f2e69e080dfec70565d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919897"
---
# <span data-ttu-id="15bba-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15bba-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="15bba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15bba-102">SYNOPSIS</span></span>
<span data-ttu-id="15bba-103">Bejövő NAT-szabálykonfigurációt kap a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="15bba-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="15bba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="15bba-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15bba-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="15bba-105">DESCRIPTION</span></span>
<span data-ttu-id="15bba-106">A **Get-AzLoadBalancerInboundNatRuleConfig** parancsmag egy vagy több bejövő hálózati címfordítási (NAT) szabályt kap egy Azure-terheléselegyenlítóben.</span><span class="sxs-lookup"><span data-stu-id="15bba-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="15bba-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="15bba-107">EXAMPLES</span></span>

### <span data-ttu-id="15bba-108">1. példa: Bejövő NAT-szabály konfigurálása</span><span class="sxs-lookup"><span data-stu-id="15bba-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="15bba-109">Az első parancs lehozza a MyLoadBalancer nevű terhelésegyenleg-eltöltőt, és tárolja azt a $slb.</span><span class="sxs-lookup"><span data-stu-id="15bba-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="15bba-110">A második parancs a myInboundNatRule1 nevű társított NAT-szabályt a rendszer terheléselosztási $slb.</span><span class="sxs-lookup"><span data-stu-id="15bba-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="15bba-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15bba-111">PARAMETERS</span></span>

### <span data-ttu-id="15bba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15bba-112">-DefaultProfile</span></span>
<span data-ttu-id="15bba-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15bba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15bba-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="15bba-114">-LoadBalancer</span></span>
<span data-ttu-id="15bba-115">A bejövő NAT-szabály konfigurációjának betöltéshez társított terheléskiegyenlító.</span><span class="sxs-lookup"><span data-stu-id="15bba-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="15bba-116">-Name</span><span class="sxs-lookup"><span data-stu-id="15bba-116">-Name</span></span>
<span data-ttu-id="15bba-117">A lekért bejövő NAT-szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15bba-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="15bba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15bba-118">CommonParameters</span></span>
<span data-ttu-id="15bba-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15bba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15bba-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15bba-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15bba-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15bba-121">INPUTS</span></span>

### <span data-ttu-id="15bba-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="15bba-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="15bba-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15bba-123">OUTPUTS</span></span>

### <span data-ttu-id="15bba-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="15bba-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="15bba-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="15bba-125">NOTES</span></span>

## <span data-ttu-id="15bba-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15bba-126">RELATED LINKS</span></span>

[<span data-ttu-id="15bba-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="15bba-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="15bba-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15bba-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="15bba-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15bba-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="15bba-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15bba-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


