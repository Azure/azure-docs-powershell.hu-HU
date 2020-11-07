---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e97e8f3ed5769e4f81175b29f097aa4946d28881
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841834"
---
# <span data-ttu-id="2e62b-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2e62b-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="2e62b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e62b-102">SYNOPSIS</span></span>
<span data-ttu-id="2e62b-103">Felveszi a backend-címkészlet konfigurációját a terheléselosztó értékre.</span><span class="sxs-lookup"><span data-stu-id="2e62b-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="2e62b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e62b-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e62b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e62b-105">DESCRIPTION</span></span>
<span data-ttu-id="2e62b-106">Az **Add-AzLoadBalancerBackend** parancsmag egy backend-címkészletet ad hozzá az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="2e62b-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="2e62b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2e62b-107">EXAMPLES</span></span>

### <span data-ttu-id="2e62b-108">Példa 1 a backend-címkészlet konfigurációjának hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="2e62b-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="2e62b-109">Ez a parancs beolvassa a MyLoadBalancer nevű terheléselosztást, hozzáadja a BackendAddressPool02 a MyLoadBalancer nevű backend-címkészletet, majd a **set-AzLoadBalancer** parancsmagot használja a MyLoadBalancer frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="2e62b-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="2e62b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e62b-110">PARAMETERS</span></span>

### <span data-ttu-id="2e62b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e62b-111">-DefaultProfile</span></span>
<span data-ttu-id="2e62b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e62b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e62b-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2e62b-113">-LoadBalancer</span></span>
<span data-ttu-id="2e62b-114">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2e62b-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="2e62b-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e62b-115">-Name</span></span>
<span data-ttu-id="2e62b-116">Adja meg a hozzáadni kívánt backend-címkészlet konfigurációjának nevét.</span><span class="sxs-lookup"><span data-stu-id="2e62b-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="2e62b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e62b-117">CommonParameters</span></span>
<span data-ttu-id="2e62b-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e62b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e62b-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e62b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e62b-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e62b-120">INPUTS</span></span>

### <span data-ttu-id="2e62b-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2e62b-121">PSLoadBalancer</span></span>
<span data-ttu-id="2e62b-122">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2e62b-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="2e62b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e62b-123">OUTPUTS</span></span>

### <span data-ttu-id="2e62b-124">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2e62b-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2e62b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e62b-125">NOTES</span></span>

## <span data-ttu-id="2e62b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e62b-126">RELATED LINKS</span></span>

[<span data-ttu-id="2e62b-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2e62b-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2e62b-128">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2e62b-128">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="2e62b-129">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2e62b-129">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="2e62b-130">Új – AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2e62b-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="2e62b-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2e62b-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


