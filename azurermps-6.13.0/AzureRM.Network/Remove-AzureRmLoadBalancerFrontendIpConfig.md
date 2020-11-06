---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 1a71b48387948d65ba0db24fdb2c236a11a9a44d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505300"
---
# <span data-ttu-id="a99f4-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a99f4-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="a99f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a99f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a99f4-103">Az előtér IP-konfigurációjának eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="a99f4-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a99f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a99f4-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a99f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a99f4-105">DESCRIPTION</span></span>
<span data-ttu-id="a99f4-106">A **Remove-AzureRmLoadBalancerFrontendIpConfig** parancsmag az Azure Loader-ből eltávolítja az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a99f4-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="a99f4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a99f4-107">EXAMPLES</span></span>

### <span data-ttu-id="a99f4-108">1. példa: az előtér IP-konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="a99f4-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a99f4-109">Az első parancs megkapja az eltávolítani kívánt előtér-IP-konfigurációhoz társított terheléselosztó bővítményt, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a99f4-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="a99f4-110">A második parancs eltávolítja a kapcsolódó felületet az IP-konfigurációból $loadbalancer a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="a99f4-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a99f4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a99f4-111">PARAMETERS</span></span>

### <span data-ttu-id="a99f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99f4-112">-DefaultProfile</span></span>
<span data-ttu-id="a99f4-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a99f4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a99f4-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a99f4-114">-LoadBalancer</span></span>
<span data-ttu-id="a99f4-115">Megadja az eltávolítandó előtér IP-konfigurációját tartalmazó terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="a99f4-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="a99f4-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a99f4-116">-Name</span></span>
<span data-ttu-id="a99f4-117">Az eltávolítandó IP-cím konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a99f4-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="a99f4-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a99f4-118">-Confirm</span></span>
<span data-ttu-id="a99f4-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a99f4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a99f4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a99f4-120">-WhatIf</span></span>
<span data-ttu-id="a99f4-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a99f4-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a99f4-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a99f4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a99f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99f4-123">CommonParameters</span></span>
<span data-ttu-id="a99f4-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a99f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99f4-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99f4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99f4-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a99f4-126">INPUTS</span></span>

### <span data-ttu-id="a99f4-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a99f4-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="a99f4-128">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a99f4-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="a99f4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a99f4-129">OUTPUTS</span></span>

### <span data-ttu-id="a99f4-130">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a99f4-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a99f4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a99f4-131">NOTES</span></span>

## <span data-ttu-id="a99f4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a99f4-132">RELATED LINKS</span></span>

[<span data-ttu-id="a99f4-133">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a99f4-133">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a99f4-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a99f4-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a99f4-135">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a99f4-135">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a99f4-136">Új – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a99f4-136">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a99f4-137">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a99f4-137">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


