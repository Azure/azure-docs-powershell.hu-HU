---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 30abb6f2d11eeae9749e7285a91ddeb93a1bf743
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841158"
---
# <span data-ttu-id="20836-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="20836-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="20836-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20836-102">SYNOPSIS</span></span>
<span data-ttu-id="20836-103">A backend-címkészlet konfigurációjának eltávolítása a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="20836-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="20836-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20836-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20836-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20836-105">DESCRIPTION</span></span>
<span data-ttu-id="20836-106">A **Remove-AzLoadBalancerBackendAddressPoolConfig** parancsmag a backend-címkészlet eltávolítását a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="20836-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="20836-107">Példák</span><span class="sxs-lookup"><span data-stu-id="20836-107">EXAMPLES</span></span>

### <span data-ttu-id="20836-108">1. példa: a backend-címkészlet konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="20836-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="20836-109">Ez a parancs beolvassa a MyLoadBalancer nevű terheléselosztást, és átadja a **Remove-AzLoadBalancerBackendAddressPoolConfig** , amely eltávolítja a BackendAddressPool02 konfigurációt a MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="20836-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="20836-110">Végül az Set-AzLoadBalancer parancsmag frissíti a MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="20836-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="20836-111">Felhívjuk a figyelmét arra, hogy a backend-címkészlet konfigurációjának csak a törlése előtt kell lennie.</span><span class="sxs-lookup"><span data-stu-id="20836-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="20836-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20836-112">PARAMETERS</span></span>

### <span data-ttu-id="20836-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20836-113">-DefaultProfile</span></span>
<span data-ttu-id="20836-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20836-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20836-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20836-115">-LoadBalancer</span></span>
<span data-ttu-id="20836-116">Itt adhatja meg az eltávolítandó backend-címkészletet tartalmazó terheléselosztót.</span><span class="sxs-lookup"><span data-stu-id="20836-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="20836-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="20836-117">-Name</span></span>
<span data-ttu-id="20836-118">Annak a backend-címkészlet a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="20836-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="20836-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20836-119">CommonParameters</span></span>
<span data-ttu-id="20836-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20836-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20836-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20836-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20836-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20836-122">INPUTS</span></span>

### <span data-ttu-id="20836-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20836-123">PSLoadBalancer</span></span>
<span data-ttu-id="20836-124">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="20836-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="20836-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20836-125">OUTPUTS</span></span>

### <span data-ttu-id="20836-126">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20836-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="20836-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20836-127">NOTES</span></span>

## <span data-ttu-id="20836-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20836-128">RELATED LINKS</span></span>

[<span data-ttu-id="20836-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="20836-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="20836-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20836-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="20836-131">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="20836-131">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="20836-132">Új – AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="20836-132">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


