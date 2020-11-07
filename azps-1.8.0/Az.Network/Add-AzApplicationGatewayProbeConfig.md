---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 25db1c941975111cdf000ce142519e90f08cd101
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670739"
---
# <span data-ttu-id="2329e-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2329e-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="2329e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2329e-102">SYNOPSIS</span></span>
<span data-ttu-id="2329e-103">Egy adatszondát ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="2329e-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="2329e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2329e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2329e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2329e-105">DESCRIPTION</span></span>
<span data-ttu-id="2329e-106">A Add-AzApplicationGatewayProbeConfig parancsmag az alkalmazás-átjáróhoz ad hozzá egy állapottanúsítvány-adatszondát.</span><span class="sxs-lookup"><span data-stu-id="2329e-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="2329e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2329e-107">EXAMPLES</span></span>

### <span data-ttu-id="2329e-108">1. példa: biztonságiállapot-szonda felvétele az alkalmazás-átjáróba</span><span class="sxs-lookup"><span data-stu-id="2329e-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="2329e-109">Ez a parancs hozzáadja az átjáró nevű Probe01 nevű állapot-szonda nevű állapotot.</span><span class="sxs-lookup"><span data-stu-id="2329e-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="2329e-110">A parancs azt is megadhatja, hogy az egészségtelen küszöböt 8 próbálkozásra és időpontra állítja az 120 másodperc elteltével.</span><span class="sxs-lookup"><span data-stu-id="2329e-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="2329e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2329e-111">PARAMETERS</span></span>

### <span data-ttu-id="2329e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2329e-112">-ApplicationGateway</span></span>
<span data-ttu-id="2329e-113">Annak az alkalmazásnak az átjáróját adja meg, amelyre ez a parancsmag felveszi a szondát.</span><span class="sxs-lookup"><span data-stu-id="2329e-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="2329e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2329e-114">-DefaultProfile</span></span>
<span data-ttu-id="2329e-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2329e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2329e-116">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="2329e-116">-HostName</span></span>
<span data-ttu-id="2329e-117">Azt az állomásnevet adja meg, amelyre a parancsmag elküldi a szondát.</span><span class="sxs-lookup"><span data-stu-id="2329e-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="2329e-118">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="2329e-118">-Interval</span></span>
<span data-ttu-id="2329e-119">A szonda intervallumát másodpercben kifejezve adja meg.</span><span class="sxs-lookup"><span data-stu-id="2329e-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="2329e-120">Ez a két egymást követő szonda közötti időtartam.</span><span class="sxs-lookup"><span data-stu-id="2329e-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="2329e-121">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="2329e-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="2329e-122">-Hol. van</span><span class="sxs-lookup"><span data-stu-id="2329e-122">-Match</span></span>
<span data-ttu-id="2329e-123">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="2329e-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="2329e-124">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="2329e-124">Default value is empty</span></span>

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

### <span data-ttu-id="2329e-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="2329e-125">-MinServers</span></span>
<span data-ttu-id="2329e-126">A mindig egészségesként megjelölt kiszolgálók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="2329e-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="2329e-127">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="2329e-127">Default value is 0</span></span>

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

### <span data-ttu-id="2329e-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2329e-128">-Name</span></span>
<span data-ttu-id="2329e-129">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2329e-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="2329e-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="2329e-130">-Path</span></span>
<span data-ttu-id="2329e-131">A szonda relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2329e-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="2329e-132">Az érvényes elérési út a perjel (/) karakterrel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="2329e-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="2329e-133">A szondát a rendszer elküldi a következő \< protokollnak \> ::// \< Host \> : \< port \> \< path \> .</span><span class="sxs-lookup"><span data-stu-id="2329e-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="2329e-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2329e-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="2329e-135">Azt, hogy az állomásfejléc a backend http-beállításai között legyen-e kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="2329e-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="2329e-136">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="2329e-136">Default value is false</span></span>

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

### <span data-ttu-id="2329e-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="2329e-137">-Protocol</span></span>
<span data-ttu-id="2329e-138">A szonda küldéséhez használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="2329e-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="2329e-139">Ez a parancsmag csak a HTTP-t támogatja.</span><span class="sxs-lookup"><span data-stu-id="2329e-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="2329e-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="2329e-140">-Timeout</span></span>
<span data-ttu-id="2329e-141">A szonda időkorlátját adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="2329e-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="2329e-142">Ez a parancsmag a szondát hibásnak minősíti, ha az időtúllépési időszakmal nem érkezik érvényes válasz.</span><span class="sxs-lookup"><span data-stu-id="2329e-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="2329e-143">Az érvényes értékek 1 másodperc és 86400 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="2329e-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="2329e-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="2329e-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="2329e-145">A szonda ismételt ismételt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2329e-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="2329e-146">A backend-kiszolgáló az egymást követő Szondák meghibásodása után nem éri el az egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="2329e-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="2329e-147">Az érvényes értékek 1 másodperc és 20 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="2329e-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="2329e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2329e-148">CommonParameters</span></span>
<span data-ttu-id="2329e-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2329e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2329e-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2329e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2329e-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2329e-151">INPUTS</span></span>

### <span data-ttu-id="2329e-152">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2329e-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2329e-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2329e-153">OUTPUTS</span></span>

### <span data-ttu-id="2329e-154">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2329e-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2329e-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2329e-155">NOTES</span></span>

## <span data-ttu-id="2329e-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2329e-156">RELATED LINKS</span></span>

[<span data-ttu-id="2329e-157">Szonda hozzáadása meglévő alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="2329e-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="2329e-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2329e-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2329e-159">Új – AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2329e-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2329e-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2329e-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2329e-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2329e-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

