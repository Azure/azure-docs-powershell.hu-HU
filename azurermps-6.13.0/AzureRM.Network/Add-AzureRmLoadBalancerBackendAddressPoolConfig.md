---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 0cc210563046a0ff8ee0554eb479e5eb822157fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680061"
---
# <span data-ttu-id="772f4-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="772f4-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="772f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="772f4-102">SYNOPSIS</span></span>
<span data-ttu-id="772f4-103">Felveszi a backend-címkészlet konfigurációját a terheléselosztó értékre.</span><span class="sxs-lookup"><span data-stu-id="772f4-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="772f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="772f4-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="772f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="772f4-105">DESCRIPTION</span></span>
<span data-ttu-id="772f4-106">Az **Add-AzureRmLoadBalancerBackend** parancsmag egy backend-címkészletet ad hozzá az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="772f4-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="772f4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="772f4-107">EXAMPLES</span></span>

### <span data-ttu-id="772f4-108">Példa 1 a backend-címkészlet konfigurációjának hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="772f4-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="772f4-109">Ez a parancs beolvassa a MyLoadBalancer nevű terheléselosztást, hozzáadja a BackendAddressPool02 a MyLoadBalancer nevű backend-címkészletet, majd a **set-AzureRmLoadBalancer** parancsmagot használja a MyLoadBalancer frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="772f4-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="772f4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="772f4-110">PARAMETERS</span></span>

### <span data-ttu-id="772f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="772f4-111">-DefaultProfile</span></span>
<span data-ttu-id="772f4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="772f4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="772f4-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="772f4-113">-LoadBalancer</span></span>
<span data-ttu-id="772f4-114">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="772f4-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="772f4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="772f4-115">-Name</span></span>
<span data-ttu-id="772f4-116">Adja meg a hozzáadni kívánt backend-címkészlet konfigurációjának nevét.</span><span class="sxs-lookup"><span data-stu-id="772f4-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="772f4-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="772f4-117">-Confirm</span></span>
<span data-ttu-id="772f4-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="772f4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="772f4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="772f4-119">-WhatIf</span></span>
<span data-ttu-id="772f4-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="772f4-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="772f4-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="772f4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="772f4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="772f4-122">CommonParameters</span></span>
<span data-ttu-id="772f4-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="772f4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="772f4-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="772f4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="772f4-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="772f4-125">INPUTS</span></span>

### <span data-ttu-id="772f4-126">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="772f4-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="772f4-127">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="772f4-127">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="772f4-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="772f4-128">OUTPUTS</span></span>

### <span data-ttu-id="772f4-129">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="772f4-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="772f4-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="772f4-130">NOTES</span></span>

## <span data-ttu-id="772f4-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="772f4-131">RELATED LINKS</span></span>

[<span data-ttu-id="772f4-132">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="772f4-132">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="772f4-133">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="772f4-133">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="772f4-134">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="772f4-134">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="772f4-135">Új – AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="772f4-135">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="772f4-136">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="772f4-136">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


