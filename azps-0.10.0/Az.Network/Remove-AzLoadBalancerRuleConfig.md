---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 9c50452acd832c7ac7ca0c4bc2827b8f320115b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841129"
---
# <span data-ttu-id="0c0a7-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c0a7-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="0c0a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="0c0a7-103">Új szabály konfigurációjának eltávolítása a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="0c0a7-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="0c0a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c0a7-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c0a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c0a7-105">DESCRIPTION</span></span>
<span data-ttu-id="0c0a7-106">A **Remove-AzLoadBalancerRuleConfig** parancsmag eltávolítja az Azure-terheléselosztási szabályok konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="0c0a7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0c0a7-107">EXAMPLES</span></span>

### <span data-ttu-id="0c0a7-108">1. példa: szabály-konfiguráció eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="0c0a7-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="0c0a7-109">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="0c0a7-110">A második parancs eltávolítja a MyLBruleName nevű szabály-konfigurációt a $loadbalancer terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="0c0a7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c0a7-111">PARAMETERS</span></span>

### <span data-ttu-id="0c0a7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c0a7-112">-DefaultProfile</span></span>
<span data-ttu-id="0c0a7-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c0a7-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c0a7-114">-LoadBalancer</span></span>
<span data-ttu-id="0c0a7-115">Azt a **LoadBalancer** objektumot adja meg, amely a parancsmag által eltávolított szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0c0a7-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c0a7-116">-Name</span></span>
<span data-ttu-id="0c0a7-117">Annak a terheléselosztó szabály-konfigurációnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0c0a7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0a7-118">CommonParameters</span></span>
<span data-ttu-id="0c0a7-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c0a7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c0a7-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c0a7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0a7-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c0a7-121">INPUTS</span></span>

### <span data-ttu-id="0c0a7-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c0a7-122">PSLoadBalancer</span></span>
<span data-ttu-id="0c0a7-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0c0a7-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0c0a7-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c0a7-124">OUTPUTS</span></span>

### <span data-ttu-id="0c0a7-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c0a7-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0c0a7-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c0a7-126">NOTES</span></span>

## <span data-ttu-id="0c0a7-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c0a7-127">RELATED LINKS</span></span>

[<span data-ttu-id="0c0a7-128">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c0a7-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0c0a7-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c0a7-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0c0a7-130">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c0a7-130">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0c0a7-131">Új – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c0a7-131">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0c0a7-132">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c0a7-132">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


