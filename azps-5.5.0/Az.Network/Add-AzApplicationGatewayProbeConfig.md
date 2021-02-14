---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cea6f92ba15e43d5977af03dfee1054240f5ecad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157210"
---
# <span data-ttu-id="00be4-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00be4-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="00be4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00be4-102">SYNOPSIS</span></span>
<span data-ttu-id="00be4-103">Hozzáad egy állapotkezelőt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="00be4-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="00be4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00be4-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00be4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00be4-105">DESCRIPTION</span></span>
<span data-ttu-id="00be4-106">A Add-AzApplicationGatewayProbeConfig parancsmag hozzáadja az állapot állapotát egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="00be4-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="00be4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00be4-107">EXAMPLES</span></span>

### <span data-ttu-id="00be4-108">1. példa: Állapot állapotának hozzáadása egy alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="00be4-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="00be4-109">Ez a parancs hozzáadja az Átjáró nevű alkalmazás-átjáróhoz az 11. állapot nevét.</span><span class="sxs-lookup"><span data-stu-id="00be4-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="00be4-110">A parancs a nem megfelelő küszöbértéket is 8-ra állítja, és 120 másodperc elteltével időkorrektra állítja.</span><span class="sxs-lookup"><span data-stu-id="00be4-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="00be4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00be4-111">PARAMETERS</span></span>

### <span data-ttu-id="00be4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00be4-112">-ApplicationGateway</span></span>
<span data-ttu-id="00be4-113">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag hozzáad egy átjárót.</span><span class="sxs-lookup"><span data-stu-id="00be4-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="00be4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00be4-114">-DefaultProfile</span></span>
<span data-ttu-id="00be4-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00be4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00be4-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="00be4-116">-HostName</span></span>
<span data-ttu-id="00be4-117">Azt a gazdanevet adja meg, amelybe a parancsmag elküldi a gazdatárat.</span><span class="sxs-lookup"><span data-stu-id="00be4-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="00be4-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="00be4-118">-Interval</span></span>
<span data-ttu-id="00be4-119">Másodpercben megadja az intervallumot.</span><span class="sxs-lookup"><span data-stu-id="00be4-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="00be4-120">Ez a két egymást követő időszak közötti időintervallum.</span><span class="sxs-lookup"><span data-stu-id="00be4-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="00be4-121">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="00be4-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="00be4-122">-Match</span><span class="sxs-lookup"><span data-stu-id="00be4-122">-Match</span></span>
<span data-ttu-id="00be4-123">Az állapotra adott válaszban szereplő törzs.</span><span class="sxs-lookup"><span data-stu-id="00be4-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="00be4-124">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="00be4-124">Default value is empty</span></span>

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

### <span data-ttu-id="00be4-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="00be4-125">-MinServers</span></span>
<span data-ttu-id="00be4-126">Azon kiszolgálók minimális száma, amelyek mindig kifogástalan állapotúként vannak megjelölve.</span><span class="sxs-lookup"><span data-stu-id="00be4-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="00be4-127">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="00be4-127">Default value is 0</span></span>

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

### <span data-ttu-id="00be4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="00be4-128">-Name</span></span>
<span data-ttu-id="00be4-129">A vizsgálat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00be4-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="00be4-130">-Path</span><span class="sxs-lookup"><span data-stu-id="00be4-130">-Path</span></span>
<span data-ttu-id="00be4-131">A vizsgálat relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="00be4-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="00be4-132">Az érvényes elérési út a perjellel (/) kezdődik.</span><span class="sxs-lookup"><span data-stu-id="00be4-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="00be4-133">A teszt a következőnek \<Protocol\> lesz \<host\> elküldve: : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="00be4-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="00be4-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00be4-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="00be4-135">Hogy az állomásfejlécet a háttér-http-beállítások között kell-e kivetni.</span><span class="sxs-lookup"><span data-stu-id="00be4-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="00be4-136">Az alapértelmezett érték hamis</span><span class="sxs-lookup"><span data-stu-id="00be4-136">Default value is false</span></span>

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

### <span data-ttu-id="00be4-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="00be4-137">-Protocol</span></span>
<span data-ttu-id="00be4-138">A protokoll, amely a küldéshez használatos.</span><span class="sxs-lookup"><span data-stu-id="00be4-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="00be4-139">Ez a parancsmag csak a HTTP protokollt támogatja.</span><span class="sxs-lookup"><span data-stu-id="00be4-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="00be4-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="00be4-140">-Timeout</span></span>
<span data-ttu-id="00be4-141">A időkorlát másodpercben megadott időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="00be4-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="00be4-142">Ez a parancsmag hibásnak jelöli a sérültet, ha nem érkezik érvényes válasz ebben az időkorlátban.</span><span class="sxs-lookup"><span data-stu-id="00be4-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="00be4-143">Az érvényes értékek 1 másodperc és 86400 másodperc között vannak.</span><span class="sxs-lookup"><span data-stu-id="00be4-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="00be4-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="00be4-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="00be4-145">Az újrapróbálkozás számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="00be4-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="00be4-146">A háttérkiszolgáló le van jelölve, miután az egymást követő sikertelen sikertelen hibák száma elérte a nem megfelelő küszöbértéket.</span><span class="sxs-lookup"><span data-stu-id="00be4-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="00be4-147">Az érvényes értékek 1 másodperc és 20 másodperc között vannak.</span><span class="sxs-lookup"><span data-stu-id="00be4-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="00be4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00be4-148">CommonParameters</span></span>
<span data-ttu-id="00be4-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00be4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00be4-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00be4-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00be4-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00be4-151">INPUTS</span></span>

### <span data-ttu-id="00be4-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00be4-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00be4-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00be4-153">OUTPUTS</span></span>

### <span data-ttu-id="00be4-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00be4-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00be4-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00be4-155">NOTES</span></span>

## <span data-ttu-id="00be4-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00be4-156">RELATED LINKS</span></span>

[<span data-ttu-id="00be4-157">Adatbázis hozzáadása meglévő alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="00be4-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="00be4-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00be4-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="00be4-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00be4-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="00be4-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00be4-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="00be4-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00be4-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

