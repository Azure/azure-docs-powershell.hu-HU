---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: eb7f7b85286d491d4168e08ef94c1a46ff9076ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492473"
---
# <span data-ttu-id="f8372-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8372-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="f8372-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8372-102">SYNOPSIS</span></span>
<span data-ttu-id="f8372-103">A backend-címkészlet konfigurációjának eltávolítása a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="f8372-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8372-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8372-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8372-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8372-105">DESCRIPTION</span></span>
<span data-ttu-id="f8372-106">A **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** parancsmag a backend-címkészlet eltávolítását a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="f8372-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="f8372-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f8372-107">EXAMPLES</span></span>

### <span data-ttu-id="f8372-108">1. példa: a backend-címkészlet konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="f8372-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="f8372-109">Ez a parancs beolvassa a MyLoadBalancer nevű terheléselosztást, és átadja a **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , amely eltávolítja a BackendAddressPool02 konfigurációt a MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="f8372-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="f8372-110">Végül az Set-AzureRmLoadBalancer parancsmag frissíti a MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="f8372-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="f8372-111">Felhívjuk a figyelmét arra, hogy a backend-címkészlet konfigurációjának csak a törlése előtt kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f8372-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="f8372-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8372-112">PARAMETERS</span></span>

### <span data-ttu-id="f8372-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8372-113">-LoadBalancer</span></span>
<span data-ttu-id="f8372-114">Itt adhatja meg az eltávolítandó backend-címkészletet tartalmazó terheléselosztót.</span><span class="sxs-lookup"><span data-stu-id="f8372-114">Specifies the load balancer that contains the backend address pool to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8372-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f8372-115">-Name</span></span>
<span data-ttu-id="f8372-116">Annak a backend-címkészlet a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="f8372-116">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f8372-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8372-117">-DefaultProfile</span></span>
<span data-ttu-id="f8372-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8372-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8372-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8372-119">CommonParameters</span></span>
<span data-ttu-id="f8372-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8372-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8372-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8372-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8372-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8372-122">INPUTS</span></span>

### <span data-ttu-id="f8372-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8372-123">PSLoadBalancer</span></span>
<span data-ttu-id="f8372-124">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f8372-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f8372-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8372-125">OUTPUTS</span></span>

### <span data-ttu-id="f8372-126">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8372-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f8372-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8372-127">NOTES</span></span>

## <span data-ttu-id="f8372-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8372-128">RELATED LINKS</span></span>

[<span data-ttu-id="f8372-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8372-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f8372-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8372-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f8372-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8372-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f8372-132">Új – AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8372-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


