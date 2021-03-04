---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 3e7433c8c779c078ab1b264e6b724d06cd884bab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940113"
---
# <span data-ttu-id="a28fd-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a28fd-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a28fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a28fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a28fd-103">Ez a beállítás eltávolítja a konfigurációt a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="a28fd-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="a28fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a28fd-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a28fd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a28fd-105">DESCRIPTION</span></span>
<span data-ttu-id="a28fd-106">A **Remove-AzLoadBalancerProbeConfig** parancsmag eltávolítja a konfigurációt a terheléselegyenlőből.</span><span class="sxs-lookup"><span data-stu-id="a28fd-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="a28fd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a28fd-107">EXAMPLES</span></span>

### <span data-ttu-id="a28fd-108">1. példa: Konfiguráció eltávolítása terheléselosztásból</span><span class="sxs-lookup"><span data-stu-id="a28fd-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a28fd-109">Az első parancs lekérte a MyLoadBalancer nevű terheléselosztási törlőt, majd a $loadbalancer tárolja.</span><span class="sxs-lookup"><span data-stu-id="a28fd-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="a28fd-110">A második parancs törli a MyProbe nevű konfigurációt a $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a28fd-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a28fd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a28fd-111">PARAMETERS</span></span>

### <span data-ttu-id="a28fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28fd-112">-DefaultProfile</span></span>
<span data-ttu-id="a28fd-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a28fd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a28fd-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a28fd-114">-LoadBalancer</span></span>
<span data-ttu-id="a28fd-115">Megadja a parancsmag által eltávolított konfigurációs konfigurációt tartalmazó terheléskiegyenlenlőt.</span><span class="sxs-lookup"><span data-stu-id="a28fd-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a28fd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a28fd-116">-Name</span></span>
<span data-ttu-id="a28fd-117">Annak a konfigurációnak a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a28fd-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a28fd-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a28fd-118">-Confirm</span></span>
<span data-ttu-id="a28fd-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a28fd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a28fd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a28fd-120">-WhatIf</span></span>
<span data-ttu-id="a28fd-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a28fd-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a28fd-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a28fd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a28fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28fd-123">CommonParameters</span></span>
<span data-ttu-id="a28fd-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a28fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28fd-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a28fd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28fd-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a28fd-126">INPUTS</span></span>

### <span data-ttu-id="a28fd-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a28fd-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a28fd-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a28fd-128">OUTPUTS</span></span>

### <span data-ttu-id="a28fd-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a28fd-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a28fd-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a28fd-130">NOTES</span></span>

## <span data-ttu-id="a28fd-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a28fd-131">RELATED LINKS</span></span>

[<span data-ttu-id="a28fd-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a28fd-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a28fd-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a28fd-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a28fd-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a28fd-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a28fd-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a28fd-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a28fd-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a28fd-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


