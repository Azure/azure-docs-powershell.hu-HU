---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 08644bd8b9846b0eb7d647b3df9c12008070c059
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940122"
---
# <span data-ttu-id="956d5-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="956d5-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="956d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="956d5-102">SYNOPSIS</span></span>
<span data-ttu-id="956d5-103">A háttércímkészlet konfigurációjának eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="956d5-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="956d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="956d5-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="956d5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="956d5-105">DESCRIPTION</span></span>
<span data-ttu-id="956d5-106">A **Remove-AzLoadBalancerBackendAddressPoolConfig** parancsmag eltávolítja a háttércímkészletet a terheléselegyenítőből.</span><span class="sxs-lookup"><span data-stu-id="956d5-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="956d5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="956d5-107">EXAMPLES</span></span>

### <span data-ttu-id="956d5-108">1. példa: Háttércímkészlet-konfiguráció eltávolítása terheléselosztásból</span><span class="sxs-lookup"><span data-stu-id="956d5-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="956d5-109">Ez a parancs megkapja a MyLoadBalancer nevű terheléselegyenítőt, és átadja a **Remove-AzLoadBalancerBackendAddressPoolConfig** fájlnak, amely eltávolítja a BackendAddressPool02 konfigurációt a MyLoadBalancerből.</span><span class="sxs-lookup"><span data-stu-id="956d5-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig**, which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="956d5-110">Végül a Set-AzLoadBalancer a MyLoadBalancer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="956d5-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="956d5-111">Ne feledje, hogy a törlés előtt a háttércímkészletnek konfigurálva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="956d5-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="956d5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="956d5-112">PARAMETERS</span></span>

### <span data-ttu-id="956d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956d5-113">-DefaultProfile</span></span>
<span data-ttu-id="956d5-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="956d5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="956d5-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="956d5-115">-LoadBalancer</span></span>
<span data-ttu-id="956d5-116">Azt a terheléskiegyenlítőt adja meg, amely az eltávolítható háttércímkészletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="956d5-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="956d5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="956d5-117">-Name</span></span>
<span data-ttu-id="956d5-118">Annak a háttércímkészletnek a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="956d5-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="956d5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="956d5-119">-Confirm</span></span>
<span data-ttu-id="956d5-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="956d5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="956d5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="956d5-121">-WhatIf</span></span>
<span data-ttu-id="956d5-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="956d5-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="956d5-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="956d5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="956d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956d5-124">CommonParameters</span></span>
<span data-ttu-id="956d5-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="956d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956d5-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="956d5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956d5-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="956d5-127">INPUTS</span></span>

### <span data-ttu-id="956d5-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="956d5-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="956d5-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="956d5-129">OUTPUTS</span></span>

### <span data-ttu-id="956d5-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="956d5-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="956d5-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="956d5-131">NOTES</span></span>

## <span data-ttu-id="956d5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="956d5-132">RELATED LINKS</span></span>

[<span data-ttu-id="956d5-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="956d5-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="956d5-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="956d5-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="956d5-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="956d5-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="956d5-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="956d5-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


