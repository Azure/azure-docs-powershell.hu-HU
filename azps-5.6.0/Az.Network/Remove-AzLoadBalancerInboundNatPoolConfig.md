---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9e266ad824d5637137649c73d4e3b427af2f176b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941610"
---
# <span data-ttu-id="6dcda-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6dcda-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="6dcda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dcda-102">SYNOPSIS</span></span>
<span data-ttu-id="6dcda-103">Eltávolítja a bejövő NAT-készlet konfigurációját a terheléselosztásról.</span><span class="sxs-lookup"><span data-stu-id="6dcda-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="6dcda-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6dcda-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dcda-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6dcda-105">DESCRIPTION</span></span>
<span data-ttu-id="6dcda-106">A **Remove-AzLoadBalancerInboundNatPoolConfig** parancsmag eltávolítja a bejövő NAT-készlet konfigurációját a terheléselegyenlőből.</span><span class="sxs-lookup"><span data-stu-id="6dcda-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="6dcda-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6dcda-107">EXAMPLES</span></span>

### <span data-ttu-id="6dcda-108">1: Eltávolítás</span><span class="sxs-lookup"><span data-stu-id="6dcda-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="6dcda-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dcda-109">PARAMETERS</span></span>

### <span data-ttu-id="6dcda-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dcda-110">-DefaultProfile</span></span>
<span data-ttu-id="6dcda-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6dcda-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dcda-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6dcda-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="6dcda-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6dcda-113">-Name</span></span>
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

### <span data-ttu-id="6dcda-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dcda-114">-Confirm</span></span>
<span data-ttu-id="6dcda-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6dcda-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dcda-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dcda-116">-WhatIf</span></span>
<span data-ttu-id="6dcda-117">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6dcda-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dcda-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6dcda-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dcda-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dcda-119">CommonParameters</span></span>
<span data-ttu-id="6dcda-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dcda-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dcda-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dcda-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dcda-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6dcda-122">INPUTS</span></span>

### <span data-ttu-id="6dcda-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6dcda-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6dcda-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6dcda-124">OUTPUTS</span></span>

### <span data-ttu-id="6dcda-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6dcda-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6dcda-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6dcda-126">NOTES</span></span>

## <span data-ttu-id="6dcda-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6dcda-127">RELATED LINKS</span></span>

[<span data-ttu-id="6dcda-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6dcda-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="6dcda-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6dcda-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="6dcda-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6dcda-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="6dcda-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6dcda-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
