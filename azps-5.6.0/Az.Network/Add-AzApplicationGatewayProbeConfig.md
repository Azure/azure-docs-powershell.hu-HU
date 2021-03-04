---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 385a77c2b7b11d20b3ffb8d3728720b46c431d4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933881"
---
# <span data-ttu-id="bd41a-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bd41a-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="bd41a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd41a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd41a-103">Hozzáad egy állapotkezelőt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="bd41a-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="bd41a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd41a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd41a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd41a-105">DESCRIPTION</span></span>
<span data-ttu-id="bd41a-106">A Add-AzApplicationGatewayProbeConfig parancsmag hozzáadja az állapot állapotát egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="bd41a-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="bd41a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd41a-107">EXAMPLES</span></span>

### <span data-ttu-id="bd41a-108">1. példa: Állapotkezelő szolgáltatás hozzáadása egy alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="bd41a-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="bd41a-109">Ez a parancs hozzáadja az Átjáró nevű alkalmazás-átjáróhoz az 11. állapot nevét.</span><span class="sxs-lookup"><span data-stu-id="bd41a-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="bd41a-110">A parancs a nem megfelelő küszöbértéket is 8-ra állítja, és 120 másodperc elteltével időkorrektra állítja.</span><span class="sxs-lookup"><span data-stu-id="bd41a-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="bd41a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd41a-111">PARAMETERS</span></span>

### <span data-ttu-id="bd41a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bd41a-112">-ApplicationGateway</span></span>
<span data-ttu-id="bd41a-113">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag hozzáad egy átjárót.</span><span class="sxs-lookup"><span data-stu-id="bd41a-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd41a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd41a-114">-DefaultProfile</span></span>
<span data-ttu-id="bd41a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd41a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd41a-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="bd41a-116">-HostName</span></span>
<span data-ttu-id="bd41a-117">Azt a gazdanevet adja meg, amelybe a parancsmag elküldi a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bd41a-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="bd41a-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="bd41a-118">-Interval</span></span>
<span data-ttu-id="bd41a-119">Másodpercben megadja az intervallumot.</span><span class="sxs-lookup"><span data-stu-id="bd41a-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="bd41a-120">Ez két egymást követő sorozat között eltelt időintervallum.</span><span class="sxs-lookup"><span data-stu-id="bd41a-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="bd41a-121">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="bd41a-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="bd41a-122">-Match</span><span class="sxs-lookup"><span data-stu-id="bd41a-122">-Match</span></span>
<span data-ttu-id="bd41a-123">Az állapotra adott válaszban szereplő törzs.</span><span class="sxs-lookup"><span data-stu-id="bd41a-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="bd41a-124">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="bd41a-124">Default value is empty</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd41a-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="bd41a-125">-MinServers</span></span>
<span data-ttu-id="bd41a-126">Azon kiszolgálók minimális száma, amelyek mindig kifogástalan állapotúként vannak megjelölve.</span><span class="sxs-lookup"><span data-stu-id="bd41a-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="bd41a-127">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="bd41a-127">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd41a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="bd41a-128">-Name</span></span>
<span data-ttu-id="bd41a-129">A vizsgálat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd41a-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="bd41a-130">-Path</span><span class="sxs-lookup"><span data-stu-id="bd41a-130">-Path</span></span>
<span data-ttu-id="bd41a-131">A vizsgálat relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd41a-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="bd41a-132">Az érvényes elérési út a perjellel (/) kezdődik.</span><span class="sxs-lookup"><span data-stu-id="bd41a-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="bd41a-133">A teszt a következőnek \<Protocol\> lesz elküldve: : \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="bd41a-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="bd41a-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bd41a-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="bd41a-135">Hogy az állomásfejlécet a háttér-http-beállítások között kell-e kivetni.</span><span class="sxs-lookup"><span data-stu-id="bd41a-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="bd41a-136">Az alapértelmezett érték hamis</span><span class="sxs-lookup"><span data-stu-id="bd41a-136">Default value is false</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd41a-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="bd41a-137">-Protocol</span></span>
<span data-ttu-id="bd41a-138">A tamaksz küldését protokollja határozza meg.</span><span class="sxs-lookup"><span data-stu-id="bd41a-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="bd41a-139">Ez a parancsmag csak a HTTP protokollt támogatja.</span><span class="sxs-lookup"><span data-stu-id="bd41a-139">This cmdlet supports HTTP only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd41a-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="bd41a-140">-Timeout</span></span>
<span data-ttu-id="bd41a-141">A időkorlát másodpercben megadott időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="bd41a-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="bd41a-142">Ez a parancsmag hibásnak jelöli a sérültet, ha nem érkezik érvényes válasz ebben az időkorlátban.</span><span class="sxs-lookup"><span data-stu-id="bd41a-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="bd41a-143">Az érvényes értékek 1 másodperc és 86400 másodperc között vannak.</span><span class="sxs-lookup"><span data-stu-id="bd41a-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="bd41a-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="bd41a-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="bd41a-145">Az újrapróbálkozás számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd41a-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="bd41a-146">A háttérkiszolgáló le van jelölve, miután egymást követő sikertelen sikertelenségek száma elérte a nem megfelelő küszöbértéket.</span><span class="sxs-lookup"><span data-stu-id="bd41a-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="bd41a-147">Az érvényes értékek 1 másodperc és 20 másodperc között vannak.</span><span class="sxs-lookup"><span data-stu-id="bd41a-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="bd41a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd41a-148">CommonParameters</span></span>
<span data-ttu-id="bd41a-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd41a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd41a-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd41a-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd41a-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd41a-151">INPUTS</span></span>

### <span data-ttu-id="bd41a-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bd41a-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bd41a-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd41a-153">OUTPUTS</span></span>

### <span data-ttu-id="bd41a-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bd41a-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bd41a-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd41a-155">NOTES</span></span>

## <span data-ttu-id="bd41a-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd41a-156">RELATED LINKS</span></span>

[<span data-ttu-id="bd41a-157">Bővítmény hozzáadása meglévő alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="bd41a-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="bd41a-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bd41a-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="bd41a-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bd41a-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="bd41a-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bd41a-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="bd41a-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bd41a-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

