---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: 902fa7e266583fe52c516ac3704bdc394215e2c7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850326"
---
# <span data-ttu-id="09cd5-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="09cd5-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="09cd5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="09cd5-103">A szonda konfigurációjának cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="09cd5-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09cd5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09cd5-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09cd5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09cd5-105">DESCRIPTION</span></span>
<span data-ttu-id="09cd5-106">A **set-AzureRmLoadBalancerProbeConfig** parancsmag a szonda-konfiguráció céljának állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="09cd5-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="09cd5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="09cd5-107">EXAMPLES</span></span>

### <span data-ttu-id="09cd5-108">Példa 1: a szonda konfigurációjának módosítása a terheléselosztó eszközön</span><span class="sxs-lookup"><span data-stu-id="09cd5-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="09cd5-109">Az első parancs megkapja a MyLoadBalancer nevű loadbalancer, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09cd5-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="09cd5-110">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzureRmLoadBalancerProbeConfig, amely új szonda-konfigurációt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="09cd5-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="09cd5-111">A harmadik parancs átadja a terheléselosztó **beállítást a set-AzureRmLoadBalancerProbeConfig** , amely az új konfigurációt állítja be.</span><span class="sxs-lookup"><span data-stu-id="09cd5-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="09cd5-112">Felhívjuk a figyelmét arra, hogy az előző parancsban megadott paraméterek közül többet kell megadnia, mert az aktuális parancsmagnak meg kell adnia őket.</span><span class="sxs-lookup"><span data-stu-id="09cd5-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="09cd5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09cd5-113">PARAMETERS</span></span>

### <span data-ttu-id="09cd5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09cd5-114">-DefaultProfile</span></span>
<span data-ttu-id="09cd5-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09cd5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09cd5-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="09cd5-116">-IntervalInSeconds</span></span>
<span data-ttu-id="09cd5-117">A szondáknak a terheléselosztási szolgáltatás egyes példányaihoz való előfordulási gyakoriságát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="09cd5-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09cd5-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="09cd5-118">-LoadBalancer</span></span>
<span data-ttu-id="09cd5-119">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="09cd5-119">Specifies a load balancer.</span></span>
<span data-ttu-id="09cd5-120">Ez a parancsmag a paraméter által megadott terheléselosztó beállításának a cél állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="09cd5-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="09cd5-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="09cd5-121">-Name</span></span>
<span data-ttu-id="09cd5-122">Annak a szonda-konfigurációnak a nevét adja meg, amelyet a parancsmag állít be.</span><span class="sxs-lookup"><span data-stu-id="09cd5-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="09cd5-123">-Port</span><span class="sxs-lookup"><span data-stu-id="09cd5-123">-Port</span></span>
<span data-ttu-id="09cd5-124">Azt a portot adja meg, amelyen a szondáknak terheléselosztást biztosító szolgáltatáshoz kell csatlakozniuk.</span><span class="sxs-lookup"><span data-stu-id="09cd5-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09cd5-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="09cd5-125">-ProbeCount</span></span>
<span data-ttu-id="09cd5-126">Itt adhatja meg, hogy egy példánynál hány egymást követő hiba esetén legyenek egészségtelenek.</span><span class="sxs-lookup"><span data-stu-id="09cd5-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09cd5-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="09cd5-127">-Protocol</span></span>
<span data-ttu-id="09cd5-128">A szondázás számára használandó protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="09cd5-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="09cd5-129">A paraméter elfogadható értékei a következők: TCP vagy http.</span><span class="sxs-lookup"><span data-stu-id="09cd5-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09cd5-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="09cd5-130">-RequestPath</span></span>
<span data-ttu-id="09cd5-131">A terheléselosztási szolgáltatás elérési útját adja meg az állapot meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="09cd5-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="09cd5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09cd5-132">CommonParameters</span></span>
<span data-ttu-id="09cd5-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09cd5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09cd5-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09cd5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09cd5-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09cd5-135">INPUTS</span></span>

### <span data-ttu-id="09cd5-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="09cd5-136">PSLoadBalancer</span></span>
<span data-ttu-id="09cd5-137">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="09cd5-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="09cd5-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09cd5-138">OUTPUTS</span></span>

### <span data-ttu-id="09cd5-139">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="09cd5-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="09cd5-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09cd5-140">NOTES</span></span>

## <span data-ttu-id="09cd5-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09cd5-141">RELATED LINKS</span></span>

[<span data-ttu-id="09cd5-142">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="09cd5-142">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="09cd5-143">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="09cd5-143">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="09cd5-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="09cd5-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="09cd5-145">Új – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="09cd5-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="09cd5-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="09cd5-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


