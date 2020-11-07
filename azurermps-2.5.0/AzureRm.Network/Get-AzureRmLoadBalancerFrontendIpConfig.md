---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: a80fa84beaaea0307447f25767d665c465e8c2aa
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848170"
---
# <span data-ttu-id="dafa6-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dafa6-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="dafa6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dafa6-102">SYNOPSIS</span></span>
<span data-ttu-id="dafa6-103">Beilleszti az előtér IP-konfigurációját egy terheléselosztó nézetben.</span><span class="sxs-lookup"><span data-stu-id="dafa6-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dafa6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dafa6-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dafa6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dafa6-105">DESCRIPTION</span></span>
<span data-ttu-id="dafa6-106">A **Get-AzureRmLoadBalancerFrontendIpConfig** parancsmag az előtér IP-konfigurációját, illetve az előtér IP-konfigurációinak listáját a terheléselosztásban kapja.</span><span class="sxs-lookup"><span data-stu-id="dafa6-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="dafa6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dafa6-107">EXAMPLES</span></span>

### <span data-ttu-id="dafa6-108">1. példa: az előtér IP-konfigurációjának beszerzése a terheléselosztó bővítményben</span><span class="sxs-lookup"><span data-stu-id="dafa6-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="dafa6-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="dafa6-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="dafa6-110">A második parancs beilleszti az előtér-végponthoz társított IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="dafa6-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="dafa6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dafa6-111">PARAMETERS</span></span>

### <span data-ttu-id="dafa6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafa6-112">-DefaultProfile</span></span>
<span data-ttu-id="dafa6-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dafa6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dafa6-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dafa6-114">-LoadBalancer</span></span>
<span data-ttu-id="dafa6-115">Annak az IP-konfigurációnak a terheléselosztását adja meg, amely az előtér IP-konfigurációjához van társítva.</span><span class="sxs-lookup"><span data-stu-id="dafa6-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="dafa6-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dafa6-116">-Name</span></span>
<span data-ttu-id="dafa6-117">Annak az IP-konfigurációnak a neve, amely az előtér IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dafa6-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="dafa6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafa6-118">CommonParameters</span></span>
<span data-ttu-id="dafa6-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dafa6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafa6-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dafa6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafa6-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dafa6-121">INPUTS</span></span>

### <span data-ttu-id="dafa6-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dafa6-122">PSLoadBalancer</span></span>
<span data-ttu-id="dafa6-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dafa6-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="dafa6-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dafa6-124">OUTPUTS</span></span>

### <span data-ttu-id="dafa6-125">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dafa6-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="dafa6-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dafa6-126">NOTES</span></span>

## <span data-ttu-id="dafa6-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dafa6-127">RELATED LINKS</span></span>

[<span data-ttu-id="dafa6-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dafa6-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dafa6-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dafa6-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="dafa6-130">Új – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dafa6-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dafa6-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dafa6-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dafa6-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dafa6-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


