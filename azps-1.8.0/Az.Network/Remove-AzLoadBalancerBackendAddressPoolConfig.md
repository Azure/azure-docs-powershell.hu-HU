---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: ba4251615bd732526ca88f085cf2c7f2d2bf284d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670167"
---
# <span data-ttu-id="d16b1-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d16b1-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="d16b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d16b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d16b1-103">A backend-címkészlet konfigurációjának eltávolítása a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="d16b1-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="d16b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d16b1-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d16b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d16b1-105">DESCRIPTION</span></span>
<span data-ttu-id="d16b1-106">A **Remove-AzLoadBalancerBackendAddressPoolConfig** parancsmag a backend-címkészlet eltávolítását a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="d16b1-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="d16b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d16b1-107">EXAMPLES</span></span>

### <span data-ttu-id="d16b1-108">1. példa: a backend-címkészlet konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="d16b1-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="d16b1-109">Ez a parancs beolvassa a MyLoadBalancer nevű terheléselosztást, és átadja a **Remove-AzLoadBalancerBackendAddressPoolConfig** , amely eltávolítja a BackendAddressPool02 konfigurációt a MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d16b1-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="d16b1-110">Végül az Set-AzLoadBalancer parancsmag frissíti a MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d16b1-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="d16b1-111">Felhívjuk a figyelmét arra, hogy a backend-címkészlet konfigurációjának csak a törlése előtt kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d16b1-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="d16b1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d16b1-112">PARAMETERS</span></span>

### <span data-ttu-id="d16b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d16b1-113">-DefaultProfile</span></span>
<span data-ttu-id="d16b1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d16b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d16b1-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d16b1-115">-LoadBalancer</span></span>
<span data-ttu-id="d16b1-116">Itt adhatja meg az eltávolítandó backend-címkészletet tartalmazó terheléselosztót.</span><span class="sxs-lookup"><span data-stu-id="d16b1-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="d16b1-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d16b1-117">-Name</span></span>
<span data-ttu-id="d16b1-118">Annak a backend-címkészlet a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="d16b1-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d16b1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d16b1-119">-Confirm</span></span>
<span data-ttu-id="d16b1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d16b1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d16b1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d16b1-121">-WhatIf</span></span>
<span data-ttu-id="d16b1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d16b1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d16b1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d16b1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d16b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d16b1-124">CommonParameters</span></span>
<span data-ttu-id="d16b1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d16b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d16b1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d16b1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d16b1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d16b1-127">INPUTS</span></span>

### <span data-ttu-id="d16b1-128">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d16b1-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d16b1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d16b1-129">OUTPUTS</span></span>

### <span data-ttu-id="d16b1-130">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d16b1-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d16b1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d16b1-131">NOTES</span></span>

## <span data-ttu-id="d16b1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d16b1-132">RELATED LINKS</span></span>

[<span data-ttu-id="d16b1-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d16b1-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="d16b1-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d16b1-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d16b1-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d16b1-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="d16b1-136">Új – AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d16b1-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


