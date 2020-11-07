---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b135f9a54c084eb7bc5dc4562e16c67e316f8736
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841142"
---
# <span data-ttu-id="d6ebe-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6ebe-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d6ebe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ebe-103">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjának eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="d6ebe-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="d6ebe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6ebe-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6ebe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6ebe-105">DESCRIPTION</span></span>
<span data-ttu-id="d6ebe-106">A **Remove-AzLoadBalancerInboundNatRuleConfig** parancsmag egy bejövő hálózati címfordítási (NAT) szabály-konfigurációt távolít el az Azure terheléselosztó szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="d6ebe-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="d6ebe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d6ebe-107">EXAMPLES</span></span>

### <span data-ttu-id="d6ebe-108">1: a bejövő NAT-szabályok törlése Azure-terheléselosztásból</span><span class="sxs-lookup"><span data-stu-id="d6ebe-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="d6ebe-109">Az első parancs betölti a már meglévő terheléselosztó nevű "mylb" nevű kiegyenlítőt, és a változót a $load kiegyensúlyozó változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d6ebe-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="d6ebe-110">A második parancs eltávolítja a betöltőhöz társított bejövő NAT-szabályt.</span><span class="sxs-lookup"><span data-stu-id="d6ebe-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="d6ebe-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6ebe-111">PARAMETERS</span></span>

### <span data-ttu-id="d6ebe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ebe-112">-DefaultProfile</span></span>
<span data-ttu-id="d6ebe-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6ebe-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6ebe-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d6ebe-114">-LoadBalancer</span></span>
<span data-ttu-id="d6ebe-115">Azt a **LoadBalancer** -objektumot adja meg, amely a parancsmag által eltávolított bejövő címfordítási szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d6ebe-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d6ebe-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6ebe-116">-Name</span></span>
<span data-ttu-id="d6ebe-117">Annak a bejövő CÍMFORDÍTÁSi szabály konfigurációjának a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="d6ebe-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d6ebe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ebe-118">CommonParameters</span></span>
<span data-ttu-id="d6ebe-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6ebe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ebe-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6ebe-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ebe-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6ebe-121">INPUTS</span></span>

### <span data-ttu-id="d6ebe-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d6ebe-122">PSLoadBalancer</span></span>
<span data-ttu-id="d6ebe-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d6ebe-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d6ebe-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6ebe-124">OUTPUTS</span></span>

### <span data-ttu-id="d6ebe-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d6ebe-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d6ebe-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6ebe-126">NOTES</span></span>

## <span data-ttu-id="d6ebe-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6ebe-127">RELATED LINKS</span></span>

[<span data-ttu-id="d6ebe-128">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6ebe-128">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d6ebe-129">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6ebe-129">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d6ebe-130">Új – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6ebe-130">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d6ebe-131">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6ebe-131">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


