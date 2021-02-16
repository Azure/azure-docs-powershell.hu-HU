---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 39e388fbdb809f136942749a0d0585189155e32b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203193"
---
# <span data-ttu-id="3ee21-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3ee21-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="3ee21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee21-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee21-103">Háttércímkészlet-konfigurációt ad hozzá a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="3ee21-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="3ee21-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3ee21-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ee21-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3ee21-105">DESCRIPTION</span></span>
<span data-ttu-id="3ee21-106">Az **Add-AzLoadBalancerBackend** parancsmag hozzáad egy háttércímkészletet egy Azure load balancerhez.</span><span class="sxs-lookup"><span data-stu-id="3ee21-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="3ee21-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3ee21-107">EXAMPLES</span></span>

### <span data-ttu-id="3ee21-108">1. példa: Háttércímkészlet-konfiguráció hozzáadása terheléselosztáshoz</span><span class="sxs-lookup"><span data-stu-id="3ee21-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="3ee21-109">Ez a parancs leküldi a MyLoadBalancer nevű terheléselosztási készletet, hozzáadja a BackendAddressPool02 nevű háttércímkészletet a MyLoadBalancer programhoz, majd a **Set-AzLoadBalancer** parancsmagot használja a MyLoadBalancer frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="3ee21-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="3ee21-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ee21-110">PARAMETERS</span></span>

### <span data-ttu-id="3ee21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee21-111">-DefaultProfile</span></span>
<span data-ttu-id="3ee21-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ee21-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ee21-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3ee21-113">-LoadBalancer</span></span>
<span data-ttu-id="3ee21-114">Egy **LoadBalancer-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="3ee21-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="3ee21-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3ee21-115">-Name</span></span>
<span data-ttu-id="3ee21-116">A hozzáadható háttércímkészlet-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ee21-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee21-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ee21-117">-Confirm</span></span>
<span data-ttu-id="3ee21-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3ee21-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ee21-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ee21-119">-WhatIf</span></span>
<span data-ttu-id="3ee21-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3ee21-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ee21-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ee21-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ee21-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee21-122">CommonParameters</span></span>
<span data-ttu-id="3ee21-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee21-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee21-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee21-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee21-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ee21-125">INPUTS</span></span>

### <span data-ttu-id="3ee21-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3ee21-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3ee21-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ee21-127">OUTPUTS</span></span>

### <span data-ttu-id="3ee21-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3ee21-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3ee21-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3ee21-129">NOTES</span></span>

## <span data-ttu-id="3ee21-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ee21-130">RELATED LINKS</span></span>

[<span data-ttu-id="3ee21-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3ee21-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="3ee21-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3ee21-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="3ee21-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3ee21-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3ee21-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3ee21-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3ee21-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3ee21-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


