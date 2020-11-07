---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: bb0821265f87f959523009a9277dc884498e0e0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850342"
---
# <span data-ttu-id="3bb63-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3bb63-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="3bb63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3bb63-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb63-103">Új szabály konfigurációjának eltávolítása a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="3bb63-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bb63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3bb63-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bb63-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3bb63-105">DESCRIPTION</span></span>
<span data-ttu-id="3bb63-106">A **Remove-AzureRmLoadBalancerRuleConfig** parancsmag eltávolítja az Azure-terheléselosztási szabályok konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="3bb63-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="3bb63-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3bb63-107">EXAMPLES</span></span>

### <span data-ttu-id="3bb63-108">1. példa: szabály-konfiguráció eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="3bb63-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="3bb63-109">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3bb63-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="3bb63-110">A második parancs eltávolítja a MyLBruleName nevű szabály-konfigurációt a $loadbalancer terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="3bb63-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="3bb63-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3bb63-111">PARAMETERS</span></span>

### <span data-ttu-id="3bb63-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb63-112">-DefaultProfile</span></span>
<span data-ttu-id="3bb63-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bb63-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bb63-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3bb63-114">-LoadBalancer</span></span>
<span data-ttu-id="3bb63-115">Azt a **LoadBalancer** objektumot adja meg, amely a parancsmag által eltávolított szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3bb63-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3bb63-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3bb63-116">-Name</span></span>
<span data-ttu-id="3bb63-117">Annak a terheléselosztó szabály-konfigurációnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="3bb63-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3bb63-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb63-118">CommonParameters</span></span>
<span data-ttu-id="3bb63-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3bb63-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb63-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bb63-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb63-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bb63-121">INPUTS</span></span>

### <span data-ttu-id="3bb63-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3bb63-122">PSLoadBalancer</span></span>
<span data-ttu-id="3bb63-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3bb63-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="3bb63-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bb63-124">OUTPUTS</span></span>

### <span data-ttu-id="3bb63-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3bb63-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3bb63-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3bb63-126">NOTES</span></span>

## <span data-ttu-id="3bb63-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bb63-127">RELATED LINKS</span></span>

[<span data-ttu-id="3bb63-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3bb63-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="3bb63-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3bb63-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="3bb63-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3bb63-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="3bb63-131">Új – AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3bb63-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="3bb63-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3bb63-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


