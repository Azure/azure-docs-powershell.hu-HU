---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 82775229bc368f80c03a886b10a631a4482341df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496452"
---
# <span data-ttu-id="42d6f-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="42d6f-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="42d6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="42d6f-103">Felveszi a backend-címkészlet konfigurációját a terheléselosztó értékre.</span><span class="sxs-lookup"><span data-stu-id="42d6f-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42d6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42d6f-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d6f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="42d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="42d6f-106">Az **Add-AzureRmLoadBalancerBackend** parancsmag egy backend-címkészletet ad hozzá az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="42d6f-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="42d6f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="42d6f-107">EXAMPLES</span></span>

### <span data-ttu-id="42d6f-108">Példa 1 a backend-címkészlet konfigurációjának hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="42d6f-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="42d6f-109">Ez a parancs beolvassa a MyLoadBalancer nevű terheléselosztást, hozzáadja a BackendAddressPool02 a MyLoadBalancer nevű backend-címkészletet, majd a **set-AzureRmLoadBalancer** parancsmagot használja a MyLoadBalancer frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="42d6f-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="42d6f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42d6f-110">PARAMETERS</span></span>

### <span data-ttu-id="42d6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d6f-111">-DefaultProfile</span></span>
<span data-ttu-id="42d6f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42d6f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d6f-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42d6f-113">-LoadBalancer</span></span>
<span data-ttu-id="42d6f-114">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="42d6f-114">Specifies a **LoadBalancer** object.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42d6f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="42d6f-115">-Name</span></span>
<span data-ttu-id="42d6f-116">Adja meg a hozzáadni kívánt backend-címkészlet konfigurációjának nevét.</span><span class="sxs-lookup"><span data-stu-id="42d6f-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d6f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d6f-117">CommonParameters</span></span>
<span data-ttu-id="42d6f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42d6f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d6f-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d6f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d6f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42d6f-120">INPUTS</span></span>

### <span data-ttu-id="42d6f-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42d6f-121">PSLoadBalancer</span></span>
<span data-ttu-id="42d6f-122">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="42d6f-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="42d6f-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42d6f-123">OUTPUTS</span></span>

### <span data-ttu-id="42d6f-124">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42d6f-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="42d6f-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42d6f-125">NOTES</span></span>

## <span data-ttu-id="42d6f-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42d6f-126">RELATED LINKS</span></span>

[<span data-ttu-id="42d6f-127">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42d6f-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="42d6f-128">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="42d6f-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="42d6f-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="42d6f-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="42d6f-130">Új – AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="42d6f-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="42d6f-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="42d6f-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


