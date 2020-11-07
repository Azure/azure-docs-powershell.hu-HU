---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 9e353eb6682e4985ff278ddc8c0207bf0f1ab45b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837674"
---
# <span data-ttu-id="cf975-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="cf975-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="cf975-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf975-102">SYNOPSIS</span></span>
<span data-ttu-id="cf975-103">Felveszi a backend-címkészlet konfigurációját a terheléselosztó értékre.</span><span class="sxs-lookup"><span data-stu-id="cf975-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="cf975-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf975-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf975-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf975-105">DESCRIPTION</span></span>
<span data-ttu-id="cf975-106">Az **Add-AzLoadBalancerBackend** parancsmag egy backend-címkészletet ad hozzá az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="cf975-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="cf975-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cf975-107">EXAMPLES</span></span>

### <span data-ttu-id="cf975-108">Példa 1 a backend-címkészlet konfigurációjának hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="cf975-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="cf975-109">Ez a parancs beolvassa a MyLoadBalancer nevű terheléselosztást, hozzáadja a BackendAddressPool02 a MyLoadBalancer nevű backend-címkészletet, majd a **set-AzLoadBalancer** parancsmagot használja a MyLoadBalancer frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="cf975-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="cf975-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf975-110">PARAMETERS</span></span>

### <span data-ttu-id="cf975-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf975-111">-DefaultProfile</span></span>
<span data-ttu-id="cf975-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf975-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf975-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf975-113">-LoadBalancer</span></span>
<span data-ttu-id="cf975-114">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="cf975-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="cf975-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf975-115">-Name</span></span>
<span data-ttu-id="cf975-116">Adja meg a hozzáadni kívánt backend-címkészlet konfigurációjának nevét.</span><span class="sxs-lookup"><span data-stu-id="cf975-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="cf975-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf975-117">-Confirm</span></span>
<span data-ttu-id="cf975-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf975-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf975-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf975-119">-WhatIf</span></span>
<span data-ttu-id="cf975-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf975-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf975-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf975-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf975-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf975-122">CommonParameters</span></span>
<span data-ttu-id="cf975-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf975-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf975-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf975-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf975-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf975-125">INPUTS</span></span>

### <span data-ttu-id="cf975-126">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf975-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cf975-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf975-127">OUTPUTS</span></span>

### <span data-ttu-id="cf975-128">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf975-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cf975-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf975-129">NOTES</span></span>

## <span data-ttu-id="cf975-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf975-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf975-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf975-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="cf975-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cf975-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="cf975-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="cf975-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="cf975-134">Új – AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="cf975-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="cf975-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="cf975-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


