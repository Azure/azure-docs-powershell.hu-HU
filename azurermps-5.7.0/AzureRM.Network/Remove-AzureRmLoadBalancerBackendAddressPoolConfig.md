---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e0131701764fd912e5583bae6add3e43265faade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494465"
---
# <span data-ttu-id="770ac-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="770ac-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="770ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="770ac-102">SYNOPSIS</span></span>
<span data-ttu-id="770ac-103">A backend-címkészlet konfigurációjának eltávolítása a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="770ac-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="770ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="770ac-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="770ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="770ac-105">DESCRIPTION</span></span>
<span data-ttu-id="770ac-106">A **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** parancsmag a backend-címkészlet eltávolítását a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="770ac-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="770ac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="770ac-107">EXAMPLES</span></span>

### <span data-ttu-id="770ac-108">1. példa: a backend-címkészlet konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="770ac-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="770ac-109">Ez a parancs beolvassa a MyLoadBalancer nevű terheléselosztást, és átadja a **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , amely eltávolítja a BackendAddressPool02 konfigurációt a MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="770ac-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="770ac-110">Végül az Set-AzureRmLoadBalancer parancsmag frissíti a MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="770ac-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="770ac-111">Felhívjuk a figyelmét arra, hogy a backend-címkészlet konfigurációjának csak a törlése előtt kell lennie.</span><span class="sxs-lookup"><span data-stu-id="770ac-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="770ac-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="770ac-112">PARAMETERS</span></span>

### <span data-ttu-id="770ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770ac-113">-DefaultProfile</span></span>
<span data-ttu-id="770ac-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="770ac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="770ac-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="770ac-115">-LoadBalancer</span></span>
<span data-ttu-id="770ac-116">Itt adhatja meg az eltávolítandó backend-címkészletet tartalmazó terheléselosztót.</span><span class="sxs-lookup"><span data-stu-id="770ac-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="770ac-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="770ac-117">-Name</span></span>
<span data-ttu-id="770ac-118">Annak a backend-címkészlet a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="770ac-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770ac-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770ac-119">CommonParameters</span></span>
<span data-ttu-id="770ac-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="770ac-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770ac-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="770ac-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770ac-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="770ac-122">INPUTS</span></span>

### <span data-ttu-id="770ac-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="770ac-123">PSLoadBalancer</span></span>
<span data-ttu-id="770ac-124">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="770ac-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="770ac-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="770ac-125">OUTPUTS</span></span>

### <span data-ttu-id="770ac-126">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="770ac-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="770ac-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="770ac-127">NOTES</span></span>

## <span data-ttu-id="770ac-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="770ac-128">RELATED LINKS</span></span>

[<span data-ttu-id="770ac-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="770ac-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="770ac-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="770ac-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="770ac-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="770ac-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="770ac-132">Új – AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="770ac-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


