---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: 30989d3b9c71821c2eae3cdfd97f9e4e5fc0cb15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850726"
---
# <span data-ttu-id="b567e-101">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b567e-101">Get-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="b567e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b567e-102">SYNOPSIS</span></span>
<span data-ttu-id="b567e-103">Kinyeri a szonda konfigurációját a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="b567e-103">Gets a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b567e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b567e-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b567e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b567e-105">DESCRIPTION</span></span>
<span data-ttu-id="b567e-106">A **Get-AzureRmLoadBalancerProbeConfig** parancsmag egy vagy több szonda-konfigurációt kap a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="b567e-106">The **Get-AzureRmLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="b567e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b567e-107">EXAMPLES</span></span>

### <span data-ttu-id="b567e-108">1. példa: a terheléselosztó szonda-konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b567e-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="b567e-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="b567e-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="b567e-110">A második parancs beolvassa a MyProbe nevű társított szonda-konfigurációt a $slb terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="b567e-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="b567e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b567e-111">PARAMETERS</span></span>

### <span data-ttu-id="b567e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b567e-112">-DefaultProfile</span></span>
<span data-ttu-id="b567e-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b567e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b567e-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b567e-114">-LoadBalancer</span></span>
<span data-ttu-id="b567e-115">A szonda konfigurációjának megfelelő terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="b567e-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="b567e-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b567e-116">-Name</span></span>
<span data-ttu-id="b567e-117">A beszerzéshez használandó szonda-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b567e-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="b567e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b567e-118">CommonParameters</span></span>
<span data-ttu-id="b567e-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b567e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b567e-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b567e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b567e-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b567e-121">INPUTS</span></span>

### <span data-ttu-id="b567e-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b567e-122">PSLoadBalancer</span></span>
<span data-ttu-id="b567e-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b567e-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b567e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b567e-124">OUTPUTS</span></span>

### <span data-ttu-id="b567e-125">Microsoft. Azure. commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="b567e-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="b567e-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b567e-126">NOTES</span></span>

## <span data-ttu-id="b567e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b567e-127">RELATED LINKS</span></span>

[<span data-ttu-id="b567e-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b567e-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="b567e-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b567e-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b567e-130">Új – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b567e-130">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="b567e-131">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b567e-131">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="b567e-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b567e-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


