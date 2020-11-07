---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 192eb5ebfa21c97aa7043c4d4719831def08d93e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850646"
---
# <span data-ttu-id="cf9ee-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cf9ee-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="cf9ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf9ee-102">SYNOPSIS</span></span>
<span data-ttu-id="cf9ee-103">Az előtér IP-konfigurációjának eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf9ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf9ee-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf9ee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf9ee-105">DESCRIPTION</span></span>
<span data-ttu-id="cf9ee-106">A **Remove-AzureRmLoadBalancerFrontendIpConfig** parancsmag az Azure Loader-ből eltávolítja az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="cf9ee-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cf9ee-107">EXAMPLES</span></span>

### <span data-ttu-id="cf9ee-108">1. példa: az előtér IP-konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="cf9ee-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="cf9ee-109">Az első parancs megkapja az eltávolítani kívánt előtér-IP-konfigurációhoz társított terheléselosztó bővítményt, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="cf9ee-110">A második parancs eltávolítja a kapcsolódó felületet az IP-konfigurációból $loadbalancer a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="cf9ee-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf9ee-111">PARAMETERS</span></span>

### <span data-ttu-id="cf9ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf9ee-112">-DefaultProfile</span></span>
<span data-ttu-id="cf9ee-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf9ee-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf9ee-114">-LoadBalancer</span></span>
<span data-ttu-id="cf9ee-115">Megadja az eltávolítandó előtér IP-konfigurációját tartalmazó terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="cf9ee-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf9ee-116">-Name</span></span>
<span data-ttu-id="cf9ee-117">Az eltávolítandó IP-cím konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="cf9ee-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf9ee-118">CommonParameters</span></span>
<span data-ttu-id="cf9ee-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf9ee-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf9ee-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf9ee-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf9ee-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf9ee-121">INPUTS</span></span>

### <span data-ttu-id="cf9ee-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf9ee-122">PSLoadBalancer</span></span>
<span data-ttu-id="cf9ee-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cf9ee-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="cf9ee-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf9ee-124">OUTPUTS</span></span>

### <span data-ttu-id="cf9ee-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf9ee-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cf9ee-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf9ee-126">NOTES</span></span>

## <span data-ttu-id="cf9ee-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf9ee-127">RELATED LINKS</span></span>

[<span data-ttu-id="cf9ee-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cf9ee-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cf9ee-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf9ee-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="cf9ee-130">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cf9ee-130">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cf9ee-131">Új – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cf9ee-131">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cf9ee-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cf9ee-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


