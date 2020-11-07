---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6e647cbc20e74c5c473fe91b2ec592177c0713ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841325"
---
# <span data-ttu-id="ea6bf-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea6bf-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ea6bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ea6bf-103">A terheléselosztó beállításához létrehoz egy szonda-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="ea6bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea6bf-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea6bf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea6bf-105">DESCRIPTION</span></span>
<span data-ttu-id="ea6bf-106">A **New-AzLoadBalancerProbeConfig** parancsmag létrehoz egy, az Azure-terheléselosztáshoz használható szonda-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ea6bf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ea6bf-107">EXAMPLES</span></span>

### <span data-ttu-id="ea6bf-108">Példa 1: Probe-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="ea6bf-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="ea6bf-109">A parancs létrehoz egy MyProbe nevű szonda-konfigurációt a HTTP protokoll használatával.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="ea6bf-110">Az új szonda egy terheléselosztásos szolgáltatáshoz csatlakozik a 80-on.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="ea6bf-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea6bf-111">PARAMETERS</span></span>

### <span data-ttu-id="ea6bf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea6bf-112">-DefaultProfile</span></span>
<span data-ttu-id="ea6bf-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea6bf-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ea6bf-114">-IntervalInSeconds</span></span>
<span data-ttu-id="ea6bf-115">A szondáknak a terheléselosztási szolgáltatás egyes példányaihoz való előfordulási gyakoriságát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="ea6bf-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ea6bf-116">-Name</span></span>
<span data-ttu-id="ea6bf-117">A létrehozandó szonda-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="ea6bf-118">-Port</span><span class="sxs-lookup"><span data-stu-id="ea6bf-118">-Port</span></span>
<span data-ttu-id="ea6bf-119">Azt a portot adja meg, amelyen az új szonda a terheléselosztási szolgáltatáshoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="ea6bf-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="ea6bf-120">-ProbeCount</span></span>
<span data-ttu-id="ea6bf-121">Itt adhatja meg, hogy egy példánynál hány egymást követő hiba esetén legyenek egészségtelenek.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="ea6bf-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ea6bf-122">-Protocol</span></span>
<span data-ttu-id="ea6bf-123">A Probe beállításához használandó protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="ea6bf-124">A paraméter elfogadható értékei a következők: TCP vagy http.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="ea6bf-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="ea6bf-125">-RequestPath</span></span>
<span data-ttu-id="ea6bf-126">Annak az elérési útját adja meg egy terheléselosztásos szolgáltatásban, amellyel meghatározhatja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="ea6bf-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="ea6bf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea6bf-127">CommonParameters</span></span>
<span data-ttu-id="ea6bf-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea6bf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea6bf-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea6bf-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea6bf-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea6bf-130">INPUTS</span></span>

## <span data-ttu-id="ea6bf-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea6bf-131">OUTPUTS</span></span>

### <span data-ttu-id="ea6bf-132">Microsoft. Azure. commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="ea6bf-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="ea6bf-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea6bf-133">NOTES</span></span>

## <span data-ttu-id="ea6bf-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea6bf-134">RELATED LINKS</span></span>

[<span data-ttu-id="ea6bf-135">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea6bf-135">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ea6bf-136">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea6bf-136">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ea6bf-137">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea6bf-137">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ea6bf-138">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea6bf-138">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


