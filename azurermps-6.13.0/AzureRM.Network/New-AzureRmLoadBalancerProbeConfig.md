---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a4889190e58edd896d1a93222a35688dd5884c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495903"
---
# <span data-ttu-id="8a647-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8a647-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="8a647-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a647-102">SYNOPSIS</span></span>
<span data-ttu-id="8a647-103">A terheléselosztó beállításához létrehoz egy szonda-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="8a647-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a647-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a647-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a647-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a647-105">DESCRIPTION</span></span>
<span data-ttu-id="8a647-106">A **New-AzureRmLoadBalancerProbeConfig** parancsmag létrehoz egy, az Azure-terheléselosztáshoz használható szonda-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="8a647-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8a647-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8a647-107">EXAMPLES</span></span>

### <span data-ttu-id="8a647-108">Példa 1: Probe-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="8a647-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="8a647-109">A parancs létrehoz egy MyProbe nevű szonda-konfigurációt a HTTP protokoll használatával.</span><span class="sxs-lookup"><span data-stu-id="8a647-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="8a647-110">Az új szonda egy terheléselosztásos szolgáltatáshoz csatlakozik a 80-on.</span><span class="sxs-lookup"><span data-stu-id="8a647-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="8a647-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a647-111">PARAMETERS</span></span>

### <span data-ttu-id="8a647-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a647-112">-DefaultProfile</span></span>
<span data-ttu-id="8a647-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a647-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a647-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8a647-114">-IntervalInSeconds</span></span>
<span data-ttu-id="8a647-115">A szondáknak a terheléselosztási szolgáltatás egyes példányaihoz való előfordulási gyakoriságát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="8a647-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="8a647-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8a647-116">-Name</span></span>
<span data-ttu-id="8a647-117">A létrehozandó szonda-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a647-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="8a647-118">-Port</span><span class="sxs-lookup"><span data-stu-id="8a647-118">-Port</span></span>
<span data-ttu-id="8a647-119">Azt a portot adja meg, amelyen az új szonda a terheléselosztási szolgáltatáshoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="8a647-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="8a647-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="8a647-120">-ProbeCount</span></span>
<span data-ttu-id="8a647-121">Itt adhatja meg, hogy egy példánynál hány egymást követő hiba esetén legyenek egészségtelenek.</span><span class="sxs-lookup"><span data-stu-id="8a647-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="8a647-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8a647-122">-Protocol</span></span>
<span data-ttu-id="8a647-123">A Probe beállításához használandó protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a647-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="8a647-124">A paraméter elfogadható értékei a következők: TCP vagy http.</span><span class="sxs-lookup"><span data-stu-id="8a647-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="8a647-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="8a647-125">-RequestPath</span></span>
<span data-ttu-id="8a647-126">Annak az elérési útját adja meg egy terheléselosztásos szolgáltatásban, amellyel meghatározhatja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="8a647-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="8a647-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8a647-127">-Confirm</span></span>
<span data-ttu-id="8a647-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8a647-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a647-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a647-129">-WhatIf</span></span>
<span data-ttu-id="8a647-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8a647-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a647-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8a647-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a647-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a647-132">CommonParameters</span></span>
<span data-ttu-id="8a647-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a647-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a647-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a647-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a647-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a647-135">INPUTS</span></span>

### <span data-ttu-id="8a647-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a647-136">None</span></span>

## <span data-ttu-id="8a647-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a647-137">OUTPUTS</span></span>

### <span data-ttu-id="8a647-138">Microsoft. Azure. commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="8a647-138">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="8a647-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a647-139">NOTES</span></span>

## <span data-ttu-id="8a647-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a647-140">RELATED LINKS</span></span>

[<span data-ttu-id="8a647-141">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8a647-141">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="8a647-142">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8a647-142">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="8a647-143">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8a647-143">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="8a647-144">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8a647-144">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


