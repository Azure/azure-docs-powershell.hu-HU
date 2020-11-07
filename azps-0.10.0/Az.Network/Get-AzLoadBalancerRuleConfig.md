---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: a5d21e5a34727d0bc13730503d55be6ef604a245
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841609"
---
# <span data-ttu-id="2382a-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2382a-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="2382a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2382a-102">SYNOPSIS</span></span>
<span data-ttu-id="2382a-103">Kinyeri a szabály konfigurációját a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="2382a-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="2382a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2382a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2382a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2382a-105">DESCRIPTION</span></span>
<span data-ttu-id="2382a-106">A **Get-AzLoadBalancerRuleConfig** parancsmag egy vagy több szabály-konfigurációt kap a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="2382a-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="2382a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2382a-107">EXAMPLES</span></span>

### <span data-ttu-id="2382a-108">Példa 1: terheléselosztó szabály-konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="2382a-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="2382a-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="2382a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="2382a-110">A második parancs beolvassa a MyLBrulename nevű társított szabály konfigurációját a $slb terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="2382a-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="2382a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2382a-111">PARAMETERS</span></span>

### <span data-ttu-id="2382a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2382a-112">-DefaultProfile</span></span>
<span data-ttu-id="2382a-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2382a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2382a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2382a-114">-LoadBalancer</span></span>
<span data-ttu-id="2382a-115">A beolvasás szabály konfigurációjával társított terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="2382a-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="2382a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2382a-116">-Name</span></span>
<span data-ttu-id="2382a-117">A beolvasott szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2382a-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="2382a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2382a-118">CommonParameters</span></span>
<span data-ttu-id="2382a-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2382a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2382a-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2382a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2382a-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2382a-121">INPUTS</span></span>

### <span data-ttu-id="2382a-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2382a-122">PSLoadBalancer</span></span>
<span data-ttu-id="2382a-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2382a-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="2382a-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2382a-124">OUTPUTS</span></span>

### <span data-ttu-id="2382a-125">Microsoft. Azure. commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="2382a-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="2382a-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2382a-126">NOTES</span></span>

## <span data-ttu-id="2382a-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2382a-127">RELATED LINKS</span></span>

[<span data-ttu-id="2382a-128">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2382a-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="2382a-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2382a-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2382a-130">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2382a-130">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="2382a-131">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2382a-131">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


