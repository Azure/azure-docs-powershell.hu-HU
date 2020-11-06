---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6dcd7c51a43387139de85a3a9f0c17c0b19cfe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497532"
---
# <span data-ttu-id="bbbbf-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbbbf-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="bbbbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="bbbbf-103">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjának eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="bbbbf-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbbbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbbbf-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbbbf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbbbf-105">DESCRIPTION</span></span>
<span data-ttu-id="bbbbf-106">A **Remove-AzureRmLoadBalancerInboundNatRuleConfig** parancsmag egy bejövő hálózati címfordítási (NAT) szabály-konfigurációt távolít el az Azure terheléselosztó szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="bbbbf-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="bbbbf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bbbbf-107">EXAMPLES</span></span>

### <span data-ttu-id="bbbbf-108">1: a bejövő NAT-szabályok törlése Azure-terheléselosztásból</span><span class="sxs-lookup"><span data-stu-id="bbbbf-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="bbbbf-109">Az első parancs betölti a már meglévő terheléselosztó nevű "mylb" nevű kiegyenlítőt, és a változót a $load kiegyensúlyozó változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bbbbf-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="bbbbf-110">A második parancs eltávolítja a betöltőhöz társított bejövő NAT-szabályt.</span><span class="sxs-lookup"><span data-stu-id="bbbbf-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="bbbbf-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbbbf-111">PARAMETERS</span></span>

### <span data-ttu-id="bbbbf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbbbf-112">-DefaultProfile</span></span>
<span data-ttu-id="bbbbf-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbbbf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbbbf-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbbbf-114">-LoadBalancer</span></span>
<span data-ttu-id="bbbbf-115">Azt a **LoadBalancer** -objektumot adja meg, amely a parancsmag által eltávolított bejövő címfordítási szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bbbbf-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bbbbf-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bbbbf-116">-Name</span></span>
<span data-ttu-id="bbbbf-117">Annak a bejövő CÍMFORDÍTÁSi szabály konfigurációjának a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="bbbbf-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bbbbf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbbbf-118">CommonParameters</span></span>
<span data-ttu-id="bbbbf-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbbbf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbbbf-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbbbf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbbbf-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbbbf-121">INPUTS</span></span>

### <span data-ttu-id="bbbbf-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbbbf-122">PSLoadBalancer</span></span>
<span data-ttu-id="bbbbf-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="bbbbf-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="bbbbf-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbbbf-124">OUTPUTS</span></span>

### <span data-ttu-id="bbbbf-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbbbf-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bbbbf-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbbbf-126">NOTES</span></span>

## <span data-ttu-id="bbbbf-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbbbf-127">RELATED LINKS</span></span>

[<span data-ttu-id="bbbbf-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbbbf-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bbbbf-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbbbf-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bbbbf-130">Új – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbbbf-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bbbbf-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbbbf-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


