---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6bcf0957d389f45bb0e010446381303c6124146b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837942"
---
# <span data-ttu-id="cd706-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cd706-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="cd706-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd706-102">SYNOPSIS</span></span>
<span data-ttu-id="cd706-103">A terheléselosztó beállításához létrehoz egy szonda-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="cd706-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="cd706-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd706-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd706-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd706-105">DESCRIPTION</span></span>
<span data-ttu-id="cd706-106">A **New-AzLoadBalancerProbeConfig** parancsmag létrehoz egy, az Azure-terheléselosztáshoz használható szonda-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="cd706-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="cd706-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd706-107">EXAMPLES</span></span>

### <span data-ttu-id="cd706-108">Példa 1: Probe-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="cd706-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="cd706-109">A parancs létrehoz egy MyProbe nevű szonda-konfigurációt a HTTP protokoll használatával.</span><span class="sxs-lookup"><span data-stu-id="cd706-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="cd706-110">Az új szonda egy terheléselosztásos szolgáltatáshoz csatlakozik a 80-on.</span><span class="sxs-lookup"><span data-stu-id="cd706-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="cd706-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd706-111">PARAMETERS</span></span>

### <span data-ttu-id="cd706-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd706-112">-DefaultProfile</span></span>
<span data-ttu-id="cd706-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd706-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd706-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="cd706-114">-IntervalInSeconds</span></span>
<span data-ttu-id="cd706-115">A szondáknak a terheléselosztási szolgáltatás egyes példányaihoz való előfordulási gyakoriságát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="cd706-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="cd706-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd706-116">-Name</span></span>
<span data-ttu-id="cd706-117">A létrehozandó szonda-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd706-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="cd706-118">-Port</span><span class="sxs-lookup"><span data-stu-id="cd706-118">-Port</span></span>
<span data-ttu-id="cd706-119">Azt a portot adja meg, amelyen az új szonda a terheléselosztási szolgáltatáshoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="cd706-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="cd706-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="cd706-120">-ProbeCount</span></span>
<span data-ttu-id="cd706-121">Itt adhatja meg, hogy egy példánynál hány egymást követő hiba esetén legyenek egészségtelenek.</span><span class="sxs-lookup"><span data-stu-id="cd706-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="cd706-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="cd706-122">-Protocol</span></span>
<span data-ttu-id="cd706-123">A Probe beállításához használandó protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd706-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="cd706-124">A paraméter elfogadható értékei a következők: TCP vagy http.</span><span class="sxs-lookup"><span data-stu-id="cd706-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="cd706-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="cd706-125">-RequestPath</span></span>
<span data-ttu-id="cd706-126">Annak az elérési útját adja meg egy terheléselosztásos szolgáltatásban, amellyel meghatározhatja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="cd706-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="cd706-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd706-127">-Confirm</span></span>
<span data-ttu-id="cd706-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd706-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd706-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd706-129">-WhatIf</span></span>
<span data-ttu-id="cd706-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd706-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd706-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd706-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd706-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd706-132">CommonParameters</span></span>
<span data-ttu-id="cd706-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd706-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd706-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd706-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd706-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd706-135">INPUTS</span></span>

### <span data-ttu-id="cd706-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cd706-136">System.String</span></span>

### <span data-ttu-id="cd706-137">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cd706-137">System.Int32</span></span>

## <span data-ttu-id="cd706-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd706-138">OUTPUTS</span></span>

### <span data-ttu-id="cd706-139">Microsoft. Azure. commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="cd706-139">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="cd706-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd706-140">NOTES</span></span>

## <span data-ttu-id="cd706-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd706-141">RELATED LINKS</span></span>

[<span data-ttu-id="cd706-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cd706-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cd706-143">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cd706-143">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cd706-144">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cd706-144">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cd706-145">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cd706-145">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


