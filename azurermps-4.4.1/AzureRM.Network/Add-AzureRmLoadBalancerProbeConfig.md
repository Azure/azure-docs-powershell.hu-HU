---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 79e9d856825e174bc8667f99e7b25b301230dec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500812"
---
# <span data-ttu-id="d736c-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d736c-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="d736c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d736c-102">SYNOPSIS</span></span>
<span data-ttu-id="d736c-103">A szonda konfigurációját hozzáadja a terheléselosztó beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="d736c-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d736c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d736c-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d736c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d736c-105">DESCRIPTION</span></span>
<span data-ttu-id="d736c-106">Az **Add-AzureRmLoadBalancerProbeConfig** parancsmag a Szondák konfigurációját az Azure terheléselosztó szolgáltatáshoz adja.</span><span class="sxs-lookup"><span data-stu-id="d736c-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="d736c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d736c-107">EXAMPLES</span></span>

### <span data-ttu-id="d736c-108">Példa 1 a szonda-konfiguráció hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="d736c-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="d736c-109">Ez a parancs beolvassa a myLb nevű terheléselosztást, hozzáadja a megadott szonda-konfigurációt, majd a **set-AzureRmLoadBalancer** parancsmagot használja a terheléselosztó frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="d736c-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="d736c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d736c-110">PARAMETERS</span></span>

### <span data-ttu-id="d736c-111">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d736c-111">-IntervalInSeconds</span></span>
<span data-ttu-id="d736c-112">A szondáknak a terheléselosztási szolgáltatás egyes példányaihoz való előfordulási gyakoriságát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="d736c-112">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d736c-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d736c-113">-LoadBalancer</span></span>
<span data-ttu-id="d736c-114">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d736c-114">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="d736c-115">Ez a parancsmag felveszi a szonda konfigurációját a paraméter által megadott terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="d736c-115">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d736c-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d736c-116">-Name</span></span>
<span data-ttu-id="d736c-117">A felvenni kívánt szonda-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d736c-117">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="d736c-118">-Port</span><span class="sxs-lookup"><span data-stu-id="d736c-118">-Port</span></span>
<span data-ttu-id="d736c-119">Azt a portot adja meg, amelyen a szondáknak terheléselosztást biztosító szolgáltatáshoz kell csatlakozniuk.</span><span class="sxs-lookup"><span data-stu-id="d736c-119">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d736c-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="d736c-120">-ProbeCount</span></span>
<span data-ttu-id="d736c-121">Itt adhatja meg, hogy egy példánynál hány egymást követő hiba esetén legyenek egészségtelenek.</span><span class="sxs-lookup"><span data-stu-id="d736c-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d736c-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d736c-122">-Protocol</span></span>
<span data-ttu-id="d736c-123">A szondához használandó protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d736c-123">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="d736c-124">A paraméter elfogadható értékei a következők: TCP vagy http.</span><span class="sxs-lookup"><span data-stu-id="d736c-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d736c-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="d736c-125">-RequestPath</span></span>
<span data-ttu-id="d736c-126">A terheléselosztási szolgáltatás elérési útját adja meg az állapot meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="d736c-126">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d736c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d736c-127">-DefaultProfile</span></span>
<span data-ttu-id="d736c-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d736c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d736c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d736c-129">CommonParameters</span></span>
<span data-ttu-id="d736c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d736c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d736c-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d736c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d736c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d736c-132">INPUTS</span></span>

### <span data-ttu-id="d736c-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d736c-133">PSLoadBalancer</span></span>
<span data-ttu-id="d736c-134">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d736c-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d736c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d736c-135">OUTPUTS</span></span>

### <span data-ttu-id="d736c-136">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d736c-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d736c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d736c-137">NOTES</span></span>

## <span data-ttu-id="d736c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d736c-138">RELATED LINKS</span></span>

[<span data-ttu-id="d736c-139">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d736c-139">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="d736c-140">Új – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d736c-140">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="d736c-141">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d736c-141">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="d736c-142">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d736c-142">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="d736c-143">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d736c-143">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


