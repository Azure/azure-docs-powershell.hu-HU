---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203083"
---
# <span data-ttu-id="19bdd-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="19bdd-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="19bdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="19bdd-103">Egy vagy több bejövő NAT-készlet-konfigurációt kap egy terheléselosztási eszköztől.</span><span class="sxs-lookup"><span data-stu-id="19bdd-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="19bdd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19bdd-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19bdd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="19bdd-106">A **Get-AzLoadBalancerInboundNatPoolConfig** parancsmag egy vagy több bejövő NAT-készlet-konfigurációt kap egy terheléselegyenlőtől.</span><span class="sxs-lookup"><span data-stu-id="19bdd-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="19bdd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19bdd-107">EXAMPLES</span></span>

### <span data-ttu-id="19bdd-108">1: Get</span><span class="sxs-lookup"><span data-stu-id="19bdd-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="19bdd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19bdd-109">PARAMETERS</span></span>

### <span data-ttu-id="19bdd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19bdd-110">-DefaultProfile</span></span>
<span data-ttu-id="19bdd-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19bdd-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19bdd-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19bdd-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="19bdd-113">-Name</span><span class="sxs-lookup"><span data-stu-id="19bdd-113">-Name</span></span>
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

### <span data-ttu-id="19bdd-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19bdd-114">CommonParameters</span></span>
<span data-ttu-id="19bdd-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19bdd-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19bdd-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19bdd-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19bdd-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19bdd-117">INPUTS</span></span>

### <span data-ttu-id="19bdd-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19bdd-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="19bdd-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19bdd-119">OUTPUTS</span></span>

### <span data-ttu-id="19bdd-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="19bdd-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="19bdd-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19bdd-121">NOTES</span></span>

## <span data-ttu-id="19bdd-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19bdd-122">RELATED LINKS</span></span>

[<span data-ttu-id="19bdd-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="19bdd-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="19bdd-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="19bdd-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="19bdd-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="19bdd-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="19bdd-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="19bdd-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
