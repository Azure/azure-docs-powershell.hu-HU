---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 071a6db22f6788f76a6c4323c26247c070f164b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837666"
---
# <span data-ttu-id="a4e43-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a4e43-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a4e43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4e43-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e43-103">A szonda konfigurációját hozzáadja a terheléselosztó beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="a4e43-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="a4e43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4e43-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4e43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4e43-105">DESCRIPTION</span></span>
<span data-ttu-id="a4e43-106">Az **Add-AzLoadBalancerProbeConfig** parancsmag a Szondák konfigurációját az Azure terheléselosztó szolgáltatáshoz adja.</span><span class="sxs-lookup"><span data-stu-id="a4e43-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="a4e43-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4e43-107">EXAMPLES</span></span>

### <span data-ttu-id="a4e43-108">Példa 1 a szonda-konfiguráció hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="a4e43-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="a4e43-109">Ez a parancs beolvassa a myLb nevű terheléselosztást, hozzáadja a megadott szonda-konfigurációt, majd a **set-AzLoadBalancer** parancsmagot használja a terheléselosztó frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="a4e43-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="a4e43-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4e43-110">PARAMETERS</span></span>

### <span data-ttu-id="a4e43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e43-111">-DefaultProfile</span></span>
<span data-ttu-id="a4e43-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4e43-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4e43-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a4e43-113">-IntervalInSeconds</span></span>
<span data-ttu-id="a4e43-114">A szondáknak a terheléselosztási szolgáltatás egyes példányaihoz való előfordulási gyakoriságát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="a4e43-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="a4e43-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a4e43-115">-LoadBalancer</span></span>
<span data-ttu-id="a4e43-116">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a4e43-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="a4e43-117">Ez a parancsmag felveszi a szonda konfigurációját a paraméter által megadott terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="a4e43-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a4e43-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4e43-118">-Name</span></span>
<span data-ttu-id="a4e43-119">A felvenni kívánt szonda-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e43-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="a4e43-120">-Port</span><span class="sxs-lookup"><span data-stu-id="a4e43-120">-Port</span></span>
<span data-ttu-id="a4e43-121">Azt a portot adja meg, amelyen a szondáknak terheléselosztást biztosító szolgáltatáshoz kell csatlakozniuk.</span><span class="sxs-lookup"><span data-stu-id="a4e43-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="a4e43-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="a4e43-122">-ProbeCount</span></span>
<span data-ttu-id="a4e43-123">Itt adhatja meg, hogy egy példánynál hány egymást követő hiba esetén legyenek egészségtelenek.</span><span class="sxs-lookup"><span data-stu-id="a4e43-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="a4e43-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a4e43-124">-Protocol</span></span>
<span data-ttu-id="a4e43-125">A szondához használandó protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e43-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="a4e43-126">A paraméter elfogadható értékei a következők: TCP vagy http.</span><span class="sxs-lookup"><span data-stu-id="a4e43-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="a4e43-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="a4e43-127">-RequestPath</span></span>
<span data-ttu-id="a4e43-128">A terheléselosztási szolgáltatás elérési útját adja meg az állapot meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="a4e43-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="a4e43-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4e43-129">-Confirm</span></span>
<span data-ttu-id="a4e43-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4e43-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4e43-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4e43-131">-WhatIf</span></span>
<span data-ttu-id="a4e43-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4e43-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4e43-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4e43-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4e43-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e43-134">CommonParameters</span></span>
<span data-ttu-id="a4e43-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4e43-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e43-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4e43-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e43-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4e43-137">INPUTS</span></span>

### <span data-ttu-id="a4e43-138">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a4e43-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="a4e43-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a4e43-139">System.String</span></span>

### <span data-ttu-id="a4e43-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a4e43-140">System.Int32</span></span>

## <span data-ttu-id="a4e43-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4e43-141">OUTPUTS</span></span>

### <span data-ttu-id="a4e43-142">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a4e43-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a4e43-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4e43-143">NOTES</span></span>

## <span data-ttu-id="a4e43-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4e43-144">RELATED LINKS</span></span>

[<span data-ttu-id="a4e43-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a4e43-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a4e43-146">Új – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a4e43-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a4e43-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a4e43-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a4e43-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a4e43-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="a4e43-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a4e43-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


