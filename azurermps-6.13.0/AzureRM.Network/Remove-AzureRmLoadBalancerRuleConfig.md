---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b51c7300296644ffeda75d1fb9e4cf695ff61def
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493625"
---
# <span data-ttu-id="a59da-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a59da-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a59da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a59da-102">SYNOPSIS</span></span>
<span data-ttu-id="a59da-103">Új szabály konfigurációjának eltávolítása a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="a59da-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a59da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a59da-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a59da-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a59da-105">DESCRIPTION</span></span>
<span data-ttu-id="a59da-106">A **Remove-AzureRmLoadBalancerRuleConfig** parancsmag eltávolítja az Azure-terheléselosztási szabályok konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a59da-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a59da-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a59da-107">EXAMPLES</span></span>

### <span data-ttu-id="a59da-108">1. példa: szabály-konfiguráció eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="a59da-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a59da-109">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a59da-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="a59da-110">A második parancs eltávolítja a MyLBruleName nevű szabály-konfigurációt a $loadbalancer terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="a59da-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a59da-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a59da-111">PARAMETERS</span></span>

### <span data-ttu-id="a59da-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a59da-112">-DefaultProfile</span></span>
<span data-ttu-id="a59da-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a59da-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a59da-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a59da-114">-LoadBalancer</span></span>
<span data-ttu-id="a59da-115">Azt a **LoadBalancer** objektumot adja meg, amely a parancsmag által eltávolított szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a59da-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a59da-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a59da-116">-Name</span></span>
<span data-ttu-id="a59da-117">Annak a terheléselosztó szabály-konfigurációnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="a59da-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a59da-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a59da-118">-Confirm</span></span>
<span data-ttu-id="a59da-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a59da-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a59da-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a59da-120">-WhatIf</span></span>
<span data-ttu-id="a59da-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a59da-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a59da-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a59da-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a59da-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a59da-123">CommonParameters</span></span>
<span data-ttu-id="a59da-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a59da-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a59da-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a59da-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a59da-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a59da-126">INPUTS</span></span>

### <span data-ttu-id="a59da-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a59da-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="a59da-128">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a59da-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="a59da-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a59da-129">OUTPUTS</span></span>

### <span data-ttu-id="a59da-130">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a59da-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a59da-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a59da-131">NOTES</span></span>

## <span data-ttu-id="a59da-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a59da-132">RELATED LINKS</span></span>

[<span data-ttu-id="a59da-133">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a59da-133">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a59da-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a59da-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a59da-135">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a59da-135">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a59da-136">Új – AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a59da-136">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a59da-137">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a59da-137">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


