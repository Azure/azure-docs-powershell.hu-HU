---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1bcaab526ac2fbb82d696db7197bbc8d69c0078f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680810"
---
# <span data-ttu-id="55c9b-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55c9b-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="55c9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="55c9b-103">Kimenő szabály konfigurációjának beolvasása a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="55c9b-103">Gets an outbound rule configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55c9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55c9b-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55c9b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55c9b-105">DESCRIPTION</span></span>
<span data-ttu-id="55c9b-106">A **Get-AzureRmLoadBalancerOutboundRuleConfig** parancsmag Kimenő szabály-konfigurációt vagy kimenő szabály konfigurációjának listáját adja meg a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="55c9b-106">The **Get-AzureRmLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="55c9b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="55c9b-107">EXAMPLES</span></span>

### <span data-ttu-id="55c9b-108">Példa 1: Kimenő szabály konfigurációjának beszerzése a terheléselosztó bővítményben</span><span class="sxs-lookup"><span data-stu-id="55c9b-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="55c9b-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="55c9b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="55c9b-110">A második parancs a kiegyenlítőhöz társított MyRule nevű Kimenő szabály konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="55c9b-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="55c9b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55c9b-111">PARAMETERS</span></span>

### <span data-ttu-id="55c9b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c9b-112">-DefaultProfile</span></span>
<span data-ttu-id="55c9b-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55c9b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55c9b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55c9b-114">-LoadBalancer</span></span>
<span data-ttu-id="55c9b-115">A terheléselosztó erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="55c9b-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="55c9b-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="55c9b-116">-Name</span></span>
<span data-ttu-id="55c9b-117">A Kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="55c9b-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="55c9b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c9b-118">CommonParameters</span></span>
<span data-ttu-id="55c9b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55c9b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c9b-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c9b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c9b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55c9b-121">INPUTS</span></span>

### <span data-ttu-id="55c9b-122">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55c9b-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="55c9b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55c9b-123">OUTPUTS</span></span>

### <span data-ttu-id="55c9b-124">Microsoft. Azure. commands. Network. models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="55c9b-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="55c9b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55c9b-125">NOTES</span></span>

## <span data-ttu-id="55c9b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55c9b-126">RELATED LINKS</span></span>
