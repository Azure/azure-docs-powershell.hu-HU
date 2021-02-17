---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156707"
---
# <span data-ttu-id="c7581-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c7581-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="c7581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7581-102">SYNOPSIS</span></span>
<span data-ttu-id="c7581-103">Egy terheléselosztás konfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="c7581-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="c7581-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7581-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7581-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7581-105">DESCRIPTION</span></span>
<span data-ttu-id="c7581-106">A **Set-AzLoadBalancerProbeConfig** parancsmag frissíti a terheléselegyenlő konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c7581-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="c7581-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7581-107">EXAMPLES</span></span>

### <span data-ttu-id="c7581-108">1. példa: A terheléselosztás konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="c7581-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="c7581-109">Az első parancs lekérte a MyLoadBalancer nevű loadbalancer nevet, majd a $slb tárolja.</span><span class="sxs-lookup"><span data-stu-id="c7581-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c7581-110">A második parancs a folyamat műveleti jelével adja át a $slb terheléselegyenlőt az Add-AzLoadBalancerProbeConfig fájlnak, amely egy új konfigurációt ad a konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="c7581-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="c7581-111">A harmadik parancs átadja a terheléselegyenlőt a **Set-AzLoadBalancerProbeConfig** eszköznek, amely beállítja az új konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="c7581-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="c7581-112">Felhívjuk a figyelmét arra, hogy az előző parancsban megadott paraméterek közül többnek is meg kell adnia, mert az aktuális parancsmag kötelező.</span><span class="sxs-lookup"><span data-stu-id="c7581-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="c7581-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7581-113">PARAMETERS</span></span>

### <span data-ttu-id="c7581-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7581-114">-DefaultProfile</span></span>
<span data-ttu-id="c7581-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7581-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7581-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c7581-116">-IntervalInSeconds</span></span>
<span data-ttu-id="c7581-117">A terheléselosztási szolgáltatás egyes példányai közötti intervallumot adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c7581-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="c7581-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7581-118">-LoadBalancer</span></span>
<span data-ttu-id="c7581-119">Terheléselosztást ad meg.</span><span class="sxs-lookup"><span data-stu-id="c7581-119">Specifies a load balancer.</span></span>
<span data-ttu-id="c7581-120">Ez a parancsmag frissíti a paraméter által megadott terheléselosztási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="c7581-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c7581-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c7581-121">-Name</span></span>
<span data-ttu-id="c7581-122">A parancsmag konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7581-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="c7581-123">-Port</span><span class="sxs-lookup"><span data-stu-id="c7581-123">-Port</span></span>
<span data-ttu-id="c7581-124">Azt a portot adja meg, amelyen a terheléselosztású szolgáltatáshoz csatlakoznia kell.</span><span class="sxs-lookup"><span data-stu-id="c7581-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="c7581-125">-Countcount</span><span class="sxs-lookup"><span data-stu-id="c7581-125">-ProbeCount</span></span>
<span data-ttu-id="c7581-126">Egy példányon egymást követő sikertelen példányok számát adja meg, amelyek nem megfelelőnek minősülnek.</span><span class="sxs-lookup"><span data-stu-id="c7581-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="c7581-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c7581-127">-Protocol</span></span>
<span data-ttu-id="c7581-128">Az eljáráshoz használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7581-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="c7581-129">A paraméter elfogadható értékei: Tcp vagy Http.</span><span class="sxs-lookup"><span data-stu-id="c7581-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="c7581-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="c7581-130">-RequestPath</span></span>
<span data-ttu-id="c7581-131">A terheléselosztási szolgáltatásban meghatározza az állapot megállapításához használni megfelelő elérési utat.</span><span class="sxs-lookup"><span data-stu-id="c7581-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="c7581-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7581-132">-Confirm</span></span>
<span data-ttu-id="c7581-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c7581-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7581-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7581-134">-WhatIf</span></span>
<span data-ttu-id="c7581-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c7581-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7581-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7581-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7581-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7581-137">CommonParameters</span></span>
<span data-ttu-id="c7581-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7581-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7581-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7581-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7581-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7581-140">INPUTS</span></span>

### <span data-ttu-id="c7581-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7581-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c7581-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c7581-142">System.String</span></span>

### <span data-ttu-id="c7581-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c7581-143">System.Int32</span></span>

## <span data-ttu-id="c7581-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7581-144">OUTPUTS</span></span>

### <span data-ttu-id="c7581-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7581-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c7581-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7581-146">NOTES</span></span>

## <span data-ttu-id="c7581-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7581-147">RELATED LINKS</span></span>

[<span data-ttu-id="c7581-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c7581-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c7581-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7581-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c7581-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c7581-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c7581-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c7581-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c7581-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c7581-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


