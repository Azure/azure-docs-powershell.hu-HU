---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: e7da21709215b4ab185a573e32c8d15de901b33f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014826"
---
# <span data-ttu-id="a4ba0-101">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a4ba0-101">Set-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="a4ba0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ba0-103">Az állapot-szonda konfigurációjának beállítása egy meglévő alkalmazás-átjárón.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="a4ba0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4ba0-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4ba0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="a4ba0-106">A Set-AzApplicationGatewayProbeConfig parancsmag az állapot-szonda konfigurációját állítja be egy meglévő alkalmazás-átjárón.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-106">The Set-AzApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="a4ba0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4ba0-107">EXAMPLES</span></span>

### <span data-ttu-id="a4ba0-108">1. példa: egy adatszonda konfigurációjának beállítása az alkalmazás-átjárón</span><span class="sxs-lookup"><span data-stu-id="a4ba0-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="a4ba0-109">Ez a parancs a Probe05 nevű, az átjáró nevű alkalmazás-átjáróhoz tartozó állapot-szonda konfigurációját állítja be.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="a4ba0-110">A parancs azt is megadhatja, hogy az egészségtelen küszöböt 8 próbálkozásra és időpontra állítja az 120 másodperc elteltével.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="a4ba0-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4ba0-111">PARAMETERS</span></span>

### <span data-ttu-id="a4ba0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4ba0-112">-ApplicationGateway</span></span>
<span data-ttu-id="a4ba0-113">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a szondát küldi.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="a4ba0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ba0-114">-DefaultProfile</span></span>
<span data-ttu-id="a4ba0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4ba0-116">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="a4ba0-116">-HostName</span></span>
<span data-ttu-id="a4ba0-117">Azt az állomásnevet adja meg, amelyre a parancsmag elküldi a szondát.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="a4ba0-118">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="a4ba0-118">-Interval</span></span>
<span data-ttu-id="a4ba0-119">A szonda intervallumát másodpercben kifejezve adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="a4ba0-120">Ez a két egymást követő szonda közötti időtartam.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="a4ba0-121">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="a4ba0-122">-Hol. van</span><span class="sxs-lookup"><span data-stu-id="a4ba0-122">-Match</span></span>
<span data-ttu-id="a4ba0-123">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="a4ba0-124">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="a4ba0-124">Default value is empty</span></span>

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

### <span data-ttu-id="a4ba0-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="a4ba0-125">-MinServers</span></span>
<span data-ttu-id="a4ba0-126">A mindig egészségesként megjelölt kiszolgálók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="a4ba0-127">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="a4ba0-127">Default value is 0</span></span>

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

### <span data-ttu-id="a4ba0-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4ba0-128">-Name</span></span>
<span data-ttu-id="a4ba0-129">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="a4ba0-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="a4ba0-130">-Path</span></span>
<span data-ttu-id="a4ba0-131">A szonda relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="a4ba0-132">Az érvényes elérési utak a perjel karakterrel (/) kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="a4ba0-133">A szondát a rendszer elküldi a következő \< protokollnak \> ::// \< Host \> : \< port \> \< path \> .</span><span class="sxs-lookup"><span data-stu-id="a4ba0-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="a4ba0-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a4ba0-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="a4ba0-135">Azt, hogy az állomásfejléc a backend http-beállításai között legyen-e kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="a4ba0-136">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="a4ba0-136">Default value is false</span></span>

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

### <span data-ttu-id="a4ba0-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a4ba0-137">-Protocol</span></span>
<span data-ttu-id="a4ba0-138">A szonda küldéséhez használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="a4ba0-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="a4ba0-139">-Timeout</span></span>
<span data-ttu-id="a4ba0-140">A szonda időkorlátját adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="a4ba0-141">Ez a parancsmag a szondát hibásnak minősíti, ha az időtúllépési időszakmal nem érkezik érvényes válasz.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="a4ba0-142">Az érvényes értékek 1 másodperc és 86400 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="a4ba0-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="a4ba0-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="a4ba0-144">A szonda ismételt ismételt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="a4ba0-145">A backend-kiszolgáló az egymást követő Szondák meghibásodása után nem éri el az egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="a4ba0-146">Az érvényes értékek 1 másodperc és 20 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="a4ba0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ba0-147">CommonParameters</span></span>
<span data-ttu-id="a4ba0-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4ba0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ba0-149">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ba0-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ba0-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4ba0-150">INPUTS</span></span>

### <span data-ttu-id="a4ba0-151">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4ba0-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a4ba0-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4ba0-152">OUTPUTS</span></span>

### <span data-ttu-id="a4ba0-153">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4ba0-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a4ba0-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4ba0-154">NOTES</span></span>

## <span data-ttu-id="a4ba0-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4ba0-155">RELATED LINKS</span></span>

[<span data-ttu-id="a4ba0-156">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a4ba0-156">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="a4ba0-157">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a4ba0-157">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="a4ba0-158">Új – AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a4ba0-158">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="a4ba0-159">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a4ba0-159">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

