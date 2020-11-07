---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: a9a76af9eaee36913fd22c8003d6f4b9ba8c7b77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670161"
---
# <span data-ttu-id="b4f73-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b4f73-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="b4f73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4f73-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f73-103">A bejövő NAT-készlet konfigurációjának eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="b4f73-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="b4f73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4f73-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4f73-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4f73-105">DESCRIPTION</span></span>
<span data-ttu-id="b4f73-106">A **Remove-AzLoadBalancerInboundNatPoolConfig** parancsmag eltávolítja a bejövő NAT-készlet konfigurációját a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="b4f73-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="b4f73-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b4f73-107">EXAMPLES</span></span>

### <span data-ttu-id="b4f73-108">1: eltávolítás</span><span class="sxs-lookup"><span data-stu-id="b4f73-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="b4f73-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4f73-109">PARAMETERS</span></span>

### <span data-ttu-id="b4f73-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f73-110">-DefaultProfile</span></span>
<span data-ttu-id="b4f73-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4f73-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4f73-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4f73-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="b4f73-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4f73-113">-Name</span></span>
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

### <span data-ttu-id="b4f73-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4f73-114">-Confirm</span></span>
<span data-ttu-id="b4f73-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4f73-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4f73-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4f73-116">-WhatIf</span></span>
<span data-ttu-id="b4f73-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4f73-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4f73-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4f73-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4f73-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f73-119">CommonParameters</span></span>
<span data-ttu-id="b4f73-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4f73-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f73-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f73-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f73-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4f73-122">INPUTS</span></span>

### <span data-ttu-id="b4f73-123">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4f73-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b4f73-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4f73-124">OUTPUTS</span></span>

### <span data-ttu-id="b4f73-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4f73-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b4f73-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4f73-126">NOTES</span></span>

## <span data-ttu-id="b4f73-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4f73-127">RELATED LINKS</span></span>

[<span data-ttu-id="b4f73-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b4f73-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b4f73-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b4f73-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b4f73-130">Új – AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b4f73-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b4f73-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b4f73-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
