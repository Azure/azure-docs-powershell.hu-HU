---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: f1f95866721eb5b96e4673ad24a5452b0acdaeb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012498"
---
# <span data-ttu-id="c11a3-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c11a3-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="c11a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c11a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c11a3-103">Betöltőhöz tartozó szonda-konfiguráció frissítése</span><span class="sxs-lookup"><span data-stu-id="c11a3-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="c11a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c11a3-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c11a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c11a3-105">DESCRIPTION</span></span>
<span data-ttu-id="c11a3-106">A **set-AzLoadBalancerProbeConfig** parancsmag a terheléselosztási Szondák konfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="c11a3-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="c11a3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c11a3-107">EXAMPLES</span></span>

### <span data-ttu-id="c11a3-108">Példa 1: a szonda konfigurációjának módosítása a terheléselosztó eszközön</span><span class="sxs-lookup"><span data-stu-id="c11a3-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="c11a3-109">Az első parancs megkapja a MyLoadBalancer nevű loadbalancer, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c11a3-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c11a3-110">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzLoadBalancerProbeConfig, amely új szonda-konfigurációt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="c11a3-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="c11a3-111">A harmadik parancs átadja a terheléselosztó **beállítást a set-AzLoadBalancerProbeConfig** , amely az új konfigurációt állítja be.</span><span class="sxs-lookup"><span data-stu-id="c11a3-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="c11a3-112">Felhívjuk a figyelmét arra, hogy az előző parancsban megadott paraméterek közül többet kell megadnia, mert az aktuális parancsmagnak meg kell adnia őket.</span><span class="sxs-lookup"><span data-stu-id="c11a3-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="c11a3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c11a3-113">PARAMETERS</span></span>

### <span data-ttu-id="c11a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c11a3-114">-DefaultProfile</span></span>
<span data-ttu-id="c11a3-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c11a3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11a3-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c11a3-116">-IntervalInSeconds</span></span>
<span data-ttu-id="c11a3-117">A szondáknak a terheléselosztási szolgáltatás egyes példányaihoz való előfordulási gyakoriságát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c11a3-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11a3-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c11a3-118">-LoadBalancer</span></span>
<span data-ttu-id="c11a3-119">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="c11a3-119">Specifies a load balancer.</span></span>
<span data-ttu-id="c11a3-120">Ez a parancsmag frissíti a paraméter által megadott terheléselosztó szonda-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c11a3-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c11a3-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c11a3-121">-Name</span></span>
<span data-ttu-id="c11a3-122">Annak a szonda-konfigurációnak a nevét adja meg, amelyet a parancsmag állít be.</span><span class="sxs-lookup"><span data-stu-id="c11a3-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="c11a3-123">-Port</span><span class="sxs-lookup"><span data-stu-id="c11a3-123">-Port</span></span>
<span data-ttu-id="c11a3-124">Azt a portot adja meg, amelyen a szondáknak terheléselosztást biztosító szolgáltatáshoz kell csatlakozniuk.</span><span class="sxs-lookup"><span data-stu-id="c11a3-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11a3-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="c11a3-125">-ProbeCount</span></span>
<span data-ttu-id="c11a3-126">Itt adhatja meg, hogy egy példánynál hány egymást követő hiba esetén legyenek egészségtelenek.</span><span class="sxs-lookup"><span data-stu-id="c11a3-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11a3-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c11a3-127">-Protocol</span></span>
<span data-ttu-id="c11a3-128">A szondázás számára használandó protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="c11a3-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="c11a3-129">A paraméter elfogadható értékei a következők: TCP vagy http.</span><span class="sxs-lookup"><span data-stu-id="c11a3-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11a3-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="c11a3-130">-RequestPath</span></span>
<span data-ttu-id="c11a3-131">A terheléselosztási szolgáltatás elérési útját adja meg az állapot meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="c11a3-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11a3-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c11a3-132">-Confirm</span></span>
<span data-ttu-id="c11a3-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c11a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c11a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c11a3-134">-WhatIf</span></span>
<span data-ttu-id="c11a3-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c11a3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c11a3-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c11a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c11a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11a3-137">CommonParameters</span></span>
<span data-ttu-id="c11a3-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c11a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11a3-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c11a3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11a3-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c11a3-140">INPUTS</span></span>

### <span data-ttu-id="c11a3-141">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c11a3-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c11a3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c11a3-142">System.String</span></span>

### <span data-ttu-id="c11a3-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c11a3-143">System.Int32</span></span>

## <span data-ttu-id="c11a3-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c11a3-144">OUTPUTS</span></span>

### <span data-ttu-id="c11a3-145">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c11a3-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c11a3-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c11a3-146">NOTES</span></span>

## <span data-ttu-id="c11a3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c11a3-147">RELATED LINKS</span></span>

[<span data-ttu-id="c11a3-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c11a3-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c11a3-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c11a3-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c11a3-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c11a3-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c11a3-151">Új – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c11a3-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c11a3-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c11a3-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


