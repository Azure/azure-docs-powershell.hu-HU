---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: cc9a79b424d6ad81804aaed0d941ca017463abba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498296"
---
# <span data-ttu-id="8f3fe-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8f3fe-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="8f3fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="8f3fe-103">Kimenő szabály konfigurációjának eltávolítása a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="8f3fe-103">Removes an outbound rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f3fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f3fe-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f3fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f3fe-105">DESCRIPTION</span></span>
<span data-ttu-id="8f3fe-106">A **Remove-AzureRmLoadBalancerOutboundRuleConfig** parancsmag egy kimenő szabály konfigurációját az Azure terheléselosztó szolgáltatásból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="8f3fe-106">The **Remove-AzureRmLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="8f3fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8f3fe-107">EXAMPLES</span></span>

### <span data-ttu-id="8f3fe-108">1. példa: egy kimenő szabály törlése Azure terheléselosztó szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="8f3fe-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzureRmLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzureRmLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="8f3fe-109">Az első parancs megkapja az eltávolítani kívánt Kimenő szabály konfigurációjának megfelelő terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8f3fe-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="8f3fe-110">A második parancs eltávolítja a kapcsolódó Kimenő szabály konfigurációját a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="8f3fe-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="8f3fe-111">A harmadik parancs frissíti a terheléselosztó bővítményt.</span><span class="sxs-lookup"><span data-stu-id="8f3fe-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="8f3fe-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f3fe-112">PARAMETERS</span></span>

### <span data-ttu-id="8f3fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f3fe-113">-DefaultProfile</span></span>
<span data-ttu-id="8f3fe-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f3fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f3fe-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8f3fe-115">-LoadBalancer</span></span>
<span data-ttu-id="8f3fe-116">A terheléselosztó erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="8f3fe-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="8f3fe-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8f3fe-117">-Name</span></span>
<span data-ttu-id="8f3fe-118">A Kimenő szabály neve</span><span class="sxs-lookup"><span data-stu-id="8f3fe-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3fe-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f3fe-119">-Confirm</span></span>
<span data-ttu-id="8f3fe-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f3fe-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3fe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f3fe-121">-WhatIf</span></span>
<span data-ttu-id="8f3fe-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f3fe-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f3fe-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f3fe-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f3fe-124">CommonParameters</span></span>
<span data-ttu-id="8f3fe-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f3fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f3fe-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f3fe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f3fe-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f3fe-127">INPUTS</span></span>

### <span data-ttu-id="8f3fe-128">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8f3fe-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8f3fe-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f3fe-129">OUTPUTS</span></span>

### <span data-ttu-id="8f3fe-130">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8f3fe-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8f3fe-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f3fe-131">NOTES</span></span>

## <span data-ttu-id="8f3fe-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f3fe-132">RELATED LINKS</span></span>
