---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160722"
---
# <span data-ttu-id="9faf4-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9faf4-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="9faf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9faf4-102">SYNOPSIS</span></span>
<span data-ttu-id="9faf4-103">Eltávolítja az előlapi IP-konfigurációt a terheléselosztásról.</span><span class="sxs-lookup"><span data-stu-id="9faf4-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="9faf4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9faf4-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9faf4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9faf4-105">DESCRIPTION</span></span>
<span data-ttu-id="9faf4-106">A **Remove-AzLoadBalancerFrontendIpConfig** parancsmag eltávolítja az előtér-IP-konfigurációt az Azure terheléselegyenítőből.</span><span class="sxs-lookup"><span data-stu-id="9faf4-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="9faf4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9faf4-107">EXAMPLES</span></span>

### <span data-ttu-id="9faf4-108">1. példa: Előlapi IP-konfiguráció eltávolítása terheléselosztásról</span><span class="sxs-lookup"><span data-stu-id="9faf4-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="9faf4-109">Az első parancs lehozza az eltávolítani kívánt előlapi IP-konfigurációhoz társított terhelésegyenleg-elegyet, majd tárolja azt a $loadbalancer változóban.</span><span class="sxs-lookup"><span data-stu-id="9faf4-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="9faf4-110">A második parancs eltávolítja a társított előlapi IP-konfigurációt a $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="9faf4-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="9faf4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9faf4-111">PARAMETERS</span></span>

### <span data-ttu-id="9faf4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9faf4-112">-DefaultProfile</span></span>
<span data-ttu-id="9faf4-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9faf4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9faf4-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9faf4-114">-LoadBalancer</span></span>
<span data-ttu-id="9faf4-115">Megadja az eltávolítható előlapi IP-konfigurációt tartalmazó terheléskiegyenlenlőt.</span><span class="sxs-lookup"><span data-stu-id="9faf4-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="9faf4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9faf4-116">-Name</span></span>
<span data-ttu-id="9faf4-117">Az eltávolítható előlapi IP-címkonfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9faf4-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="9faf4-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9faf4-118">-Confirm</span></span>
<span data-ttu-id="9faf4-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9faf4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9faf4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9faf4-120">-WhatIf</span></span>
<span data-ttu-id="9faf4-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9faf4-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9faf4-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9faf4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9faf4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9faf4-123">CommonParameters</span></span>
<span data-ttu-id="9faf4-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9faf4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9faf4-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9faf4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9faf4-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9faf4-126">INPUTS</span></span>

### <span data-ttu-id="9faf4-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9faf4-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9faf4-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9faf4-128">OUTPUTS</span></span>

### <span data-ttu-id="9faf4-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9faf4-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9faf4-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9faf4-130">NOTES</span></span>

## <span data-ttu-id="9faf4-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9faf4-131">RELATED LINKS</span></span>

[<span data-ttu-id="9faf4-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9faf4-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9faf4-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9faf4-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="9faf4-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9faf4-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9faf4-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9faf4-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9faf4-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9faf4-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


