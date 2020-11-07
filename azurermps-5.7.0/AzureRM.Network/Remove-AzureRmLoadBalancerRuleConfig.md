---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 25340322c7d5f74eb8f277db9f7693c938007840
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680408"
---
# <span data-ttu-id="c088b-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c088b-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="c088b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c088b-102">SYNOPSIS</span></span>
<span data-ttu-id="c088b-103">Új szabály konfigurációjának eltávolítása a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="c088b-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c088b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c088b-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c088b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c088b-105">DESCRIPTION</span></span>
<span data-ttu-id="c088b-106">A **Remove-AzureRmLoadBalancerRuleConfig** parancsmag eltávolítja az Azure-terheléselosztási szabályok konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c088b-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c088b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c088b-107">EXAMPLES</span></span>

### <span data-ttu-id="c088b-108">1. példa: szabály-konfiguráció eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="c088b-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="c088b-109">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c088b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="c088b-110">A második parancs eltávolítja a MyLBruleName nevű szabály-konfigurációt a $loadbalancer terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="c088b-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="c088b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c088b-111">PARAMETERS</span></span>

### <span data-ttu-id="c088b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c088b-112">-DefaultProfile</span></span>
<span data-ttu-id="c088b-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c088b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c088b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c088b-114">-LoadBalancer</span></span>
<span data-ttu-id="c088b-115">Azt a **LoadBalancer** objektumot adja meg, amely a parancsmag által eltávolított szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c088b-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c088b-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c088b-116">-Name</span></span>
<span data-ttu-id="c088b-117">Annak a terheléselosztó szabály-konfigurációnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="c088b-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c088b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c088b-118">CommonParameters</span></span>
<span data-ttu-id="c088b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c088b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c088b-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c088b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c088b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c088b-121">INPUTS</span></span>

### <span data-ttu-id="c088b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c088b-122">PSLoadBalancer</span></span>
<span data-ttu-id="c088b-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c088b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c088b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c088b-124">OUTPUTS</span></span>

### <span data-ttu-id="c088b-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c088b-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c088b-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c088b-126">NOTES</span></span>

## <span data-ttu-id="c088b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c088b-127">RELATED LINKS</span></span>

[<span data-ttu-id="c088b-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c088b-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c088b-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c088b-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c088b-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c088b-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c088b-131">Új – AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c088b-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c088b-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c088b-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


