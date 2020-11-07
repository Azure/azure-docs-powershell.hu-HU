---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 32e22416a6e624af293ffcc0597203d8b24351a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670550"
---
# <span data-ttu-id="ddd2a-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddd2a-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="ddd2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ddd2a-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd2a-103">Kimenő szabály konfigurációjának beolvasása a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="ddd2a-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="ddd2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ddd2a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddd2a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ddd2a-105">DESCRIPTION</span></span>
<span data-ttu-id="ddd2a-106">A **Get-AzLoadBalancerOutboundRuleConfig** parancsmag Kimenő szabály-konfigurációt vagy kimenő szabály konfigurációjának listáját adja meg a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="ddd2a-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="ddd2a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ddd2a-107">EXAMPLES</span></span>

### <span data-ttu-id="ddd2a-108">Példa 1: Kimenő szabály konfigurációjának beszerzése a terheléselosztó bővítményben</span><span class="sxs-lookup"><span data-stu-id="ddd2a-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="ddd2a-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="ddd2a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="ddd2a-110">A második parancs a kiegyenlítőhöz társított MyRule nevű Kimenő szabály konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd2a-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="ddd2a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ddd2a-111">PARAMETERS</span></span>

### <span data-ttu-id="ddd2a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd2a-112">-DefaultProfile</span></span>
<span data-ttu-id="ddd2a-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddd2a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddd2a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ddd2a-114">-LoadBalancer</span></span>
<span data-ttu-id="ddd2a-115">A terheléselosztó erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="ddd2a-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="ddd2a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ddd2a-116">-Name</span></span>
<span data-ttu-id="ddd2a-117">A Kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="ddd2a-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="ddd2a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd2a-118">CommonParameters</span></span>
<span data-ttu-id="ddd2a-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ddd2a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd2a-120">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ddd2a-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd2a-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddd2a-121">INPUTS</span></span>

### <span data-ttu-id="ddd2a-122">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ddd2a-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ddd2a-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddd2a-123">OUTPUTS</span></span>

### <span data-ttu-id="ddd2a-124">Microsoft. Azure. commands. Network. models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="ddd2a-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="ddd2a-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ddd2a-125">NOTES</span></span>

## <span data-ttu-id="ddd2a-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddd2a-126">RELATED LINKS</span></span>

[<span data-ttu-id="ddd2a-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddd2a-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ddd2a-128">Új – AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddd2a-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ddd2a-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddd2a-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ddd2a-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddd2a-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
