---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186226"
---
# <span data-ttu-id="c106b-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c106b-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c106b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c106b-102">SYNOPSIS</span></span>
<span data-ttu-id="c106b-103">Egy vagy több bejövő NAT-készletet kap a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="c106b-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="c106b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c106b-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c106b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c106b-105">DESCRIPTION</span></span>
<span data-ttu-id="c106b-106">A **Get-AzLoadBalancerInboundNatPoolConfig** parancsmag egy vagy több bejövő NAT-gyűjtői konfigurációt kap a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="c106b-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="c106b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c106b-107">EXAMPLES</span></span>

### <span data-ttu-id="c106b-108">1: Get</span><span class="sxs-lookup"><span data-stu-id="c106b-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="c106b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c106b-109">PARAMETERS</span></span>

### <span data-ttu-id="c106b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c106b-110">-DefaultProfile</span></span>
<span data-ttu-id="c106b-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c106b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c106b-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c106b-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="c106b-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c106b-113">-Name</span></span>
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

### <span data-ttu-id="c106b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c106b-114">CommonParameters</span></span>
<span data-ttu-id="c106b-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c106b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c106b-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c106b-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c106b-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c106b-117">INPUTS</span></span>

### <span data-ttu-id="c106b-118">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c106b-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c106b-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c106b-119">OUTPUTS</span></span>

### <span data-ttu-id="c106b-120">Microsoft. Azure. commands. Network. models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="c106b-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="c106b-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c106b-121">NOTES</span></span>

## <span data-ttu-id="c106b-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c106b-122">RELATED LINKS</span></span>

[<span data-ttu-id="c106b-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c106b-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c106b-124">Új – AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c106b-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c106b-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c106b-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c106b-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c106b-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
