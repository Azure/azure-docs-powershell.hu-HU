---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 74815c263435860f9281f476babc80574b63b161
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921930"
---
# <span data-ttu-id="8ee13-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ee13-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="8ee13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ee13-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee13-103">Egy vagy több bejövő NAT-készlet-konfigurációt kap egy terheléselosztási eszköztől.</span><span class="sxs-lookup"><span data-stu-id="8ee13-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="8ee13-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ee13-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ee13-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ee13-105">DESCRIPTION</span></span>
<span data-ttu-id="8ee13-106">A **Get-AzLoadBalancerInboundNatPoolConfig** parancsmag egy vagy több bejövő NAT-készlet-konfigurációt kap egy terheléselegyenlőtől.</span><span class="sxs-lookup"><span data-stu-id="8ee13-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="8ee13-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ee13-107">EXAMPLES</span></span>

### <span data-ttu-id="8ee13-108">1: Get</span><span class="sxs-lookup"><span data-stu-id="8ee13-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="8ee13-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ee13-109">PARAMETERS</span></span>

### <span data-ttu-id="8ee13-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee13-110">-DefaultProfile</span></span>
<span data-ttu-id="8ee13-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ee13-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ee13-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8ee13-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="8ee13-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8ee13-113">-Name</span></span>
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

### <span data-ttu-id="8ee13-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee13-114">CommonParameters</span></span>
<span data-ttu-id="8ee13-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee13-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee13-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ee13-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee13-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ee13-117">INPUTS</span></span>

### <span data-ttu-id="8ee13-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8ee13-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8ee13-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ee13-119">OUTPUTS</span></span>

### <span data-ttu-id="8ee13-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="8ee13-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="8ee13-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ee13-121">NOTES</span></span>

## <span data-ttu-id="8ee13-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ee13-122">RELATED LINKS</span></span>

[<span data-ttu-id="8ee13-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ee13-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8ee13-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ee13-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8ee13-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ee13-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8ee13-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ee13-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
