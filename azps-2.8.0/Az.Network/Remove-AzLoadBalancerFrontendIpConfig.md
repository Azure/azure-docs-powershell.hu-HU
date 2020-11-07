---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 75a12ab9543eb19301cc8e17e4ebff6e4db80c00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837097"
---
# <span data-ttu-id="b7d30-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7d30-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b7d30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7d30-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d30-103">Az előtér IP-konfigurációjának eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="b7d30-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="b7d30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7d30-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7d30-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7d30-105">DESCRIPTION</span></span>
<span data-ttu-id="b7d30-106">A **Remove-AzLoadBalancerFrontendIpConfig** parancsmag az Azure Loader-ből eltávolítja az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b7d30-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="b7d30-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b7d30-107">EXAMPLES</span></span>

### <span data-ttu-id="b7d30-108">1. példa: az előtér IP-konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="b7d30-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="b7d30-109">Az első parancs megkapja az eltávolítani kívánt előtér-IP-konfigurációhoz társított terheléselosztó bővítményt, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b7d30-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="b7d30-110">A második parancs eltávolítja a kapcsolódó felületet az IP-konfigurációból $loadbalancer a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="b7d30-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="b7d30-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7d30-111">PARAMETERS</span></span>

### <span data-ttu-id="b7d30-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d30-112">-DefaultProfile</span></span>
<span data-ttu-id="b7d30-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7d30-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7d30-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7d30-114">-LoadBalancer</span></span>
<span data-ttu-id="b7d30-115">Megadja az eltávolítandó előtér IP-konfigurációját tartalmazó terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="b7d30-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="b7d30-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b7d30-116">-Name</span></span>
<span data-ttu-id="b7d30-117">Az eltávolítandó IP-cím konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7d30-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="b7d30-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7d30-118">-Confirm</span></span>
<span data-ttu-id="b7d30-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7d30-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7d30-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7d30-120">-WhatIf</span></span>
<span data-ttu-id="b7d30-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7d30-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7d30-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7d30-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7d30-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d30-123">CommonParameters</span></span>
<span data-ttu-id="b7d30-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7d30-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d30-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7d30-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d30-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7d30-126">INPUTS</span></span>

### <span data-ttu-id="b7d30-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7d30-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b7d30-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7d30-128">OUTPUTS</span></span>

### <span data-ttu-id="b7d30-129">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7d30-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b7d30-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7d30-130">NOTES</span></span>

## <span data-ttu-id="b7d30-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7d30-131">RELATED LINKS</span></span>

[<span data-ttu-id="b7d30-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7d30-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b7d30-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7d30-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b7d30-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7d30-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b7d30-135">Új – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7d30-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b7d30-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7d30-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


