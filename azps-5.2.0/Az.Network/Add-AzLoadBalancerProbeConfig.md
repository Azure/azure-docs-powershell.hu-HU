---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4da0085e3ee0b7e023d93f5b1d54bf500512e5d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365594"
---
# <span data-ttu-id="706d1-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="706d1-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="706d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="706d1-102">SYNOPSIS</span></span>
<span data-ttu-id="706d1-103">Konfigurációt ad a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="706d1-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="706d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="706d1-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="706d1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="706d1-105">DESCRIPTION</span></span>
<span data-ttu-id="706d1-106">Az **Add-AzLoadBalancerProbeConfig** parancsmag konfigurációt ad az Azure terheléselegyenlőjébe.</span><span class="sxs-lookup"><span data-stu-id="706d1-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="706d1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="706d1-107">EXAMPLES</span></span>

### <span data-ttu-id="706d1-108">1. példa: Konfiguráció konfigurációjának hozzáadása terheléselosztáshoz</span><span class="sxs-lookup"><span data-stu-id="706d1-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="706d1-109">Ez a parancs lekérte a myLb nevű terheléselosztást, hozzáadja a megadott konfigurációt a konfigurációhoz, majd a **Set-AzLoadBalancer** parancsmagot használja a terheléselosztás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="706d1-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="706d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="706d1-110">PARAMETERS</span></span>

### <span data-ttu-id="706d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="706d1-111">-DefaultProfile</span></span>
<span data-ttu-id="706d1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="706d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="706d1-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="706d1-113">-IntervalInSeconds</span></span>
<span data-ttu-id="706d1-114">A terheléselosztási szolgáltatás egyes példányai közötti intervallumot adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="706d1-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="706d1-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="706d1-115">-LoadBalancer</span></span>
<span data-ttu-id="706d1-116">Egy **LoadBalancer-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="706d1-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="706d1-117">Ez a parancsmag hozzáad egy konfigurációs konfigurációt a paraméter által megadott terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="706d1-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="706d1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="706d1-118">-Name</span></span>
<span data-ttu-id="706d1-119">Megadja a hozzáadni szükséges konfigurációs konfiguráció nevét.</span><span class="sxs-lookup"><span data-stu-id="706d1-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="706d1-120">-Port</span><span class="sxs-lookup"><span data-stu-id="706d1-120">-Port</span></span>
<span data-ttu-id="706d1-121">Azt a portot adja meg, amelyen a terheléselosztású szolgáltatáshoz csatlakoznia kell.</span><span class="sxs-lookup"><span data-stu-id="706d1-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="706d1-122">-CountCount</span><span class="sxs-lookup"><span data-stu-id="706d1-122">-ProbeCount</span></span>
<span data-ttu-id="706d1-123">Az egy példányon egymást követő sikertelen példányok számát adja meg, amelyek nem megfelelőnek minősülnek.</span><span class="sxs-lookup"><span data-stu-id="706d1-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="706d1-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="706d1-124">-Protocol</span></span>
<span data-ttu-id="706d1-125">A vizsgálathoz használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="706d1-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="706d1-126">A paraméter elfogadható értékei: Tcp vagy Http.</span><span class="sxs-lookup"><span data-stu-id="706d1-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="706d1-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="706d1-127">-RequestPath</span></span>
<span data-ttu-id="706d1-128">A terheléselosztási szolgáltatásban meghatározza az állapot megállapításához használni megfelelő elérési utat.</span><span class="sxs-lookup"><span data-stu-id="706d1-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="706d1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="706d1-129">-Confirm</span></span>
<span data-ttu-id="706d1-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="706d1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="706d1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="706d1-131">-WhatIf</span></span>
<span data-ttu-id="706d1-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="706d1-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="706d1-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="706d1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="706d1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="706d1-134">CommonParameters</span></span>
<span data-ttu-id="706d1-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="706d1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="706d1-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="706d1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="706d1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="706d1-137">INPUTS</span></span>

### <span data-ttu-id="706d1-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="706d1-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="706d1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="706d1-139">System.String</span></span>

### <span data-ttu-id="706d1-140">System.Int32</span><span class="sxs-lookup"><span data-stu-id="706d1-140">System.Int32</span></span>

## <span data-ttu-id="706d1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="706d1-141">OUTPUTS</span></span>

### <span data-ttu-id="706d1-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="706d1-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="706d1-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="706d1-143">NOTES</span></span>

## <span data-ttu-id="706d1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="706d1-144">RELATED LINKS</span></span>

[<span data-ttu-id="706d1-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="706d1-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="706d1-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="706d1-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="706d1-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="706d1-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="706d1-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="706d1-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="706d1-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="706d1-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


