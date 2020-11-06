---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 169a63248ebc499f577a635821131e0153e64433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501768"
---
# <span data-ttu-id="673f2-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="673f2-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="673f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="673f2-102">SYNOPSIS</span></span>
<span data-ttu-id="673f2-103">Egy adatszondát ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="673f2-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="673f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="673f2-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="673f2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="673f2-105">DESCRIPTION</span></span>
<span data-ttu-id="673f2-106">A Add-AzureRmApplicationGatewayProbeConfig parancsmag az alkalmazás-átjáróhoz ad hozzá egy állapottanúsítvány-adatszondát.</span><span class="sxs-lookup"><span data-stu-id="673f2-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="673f2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="673f2-107">EXAMPLES</span></span>

### <span data-ttu-id="673f2-108">1. példa: biztonságiállapot-szonda felvétele az alkalmazás-átjáróba</span><span class="sxs-lookup"><span data-stu-id="673f2-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="673f2-109">Ez a parancs hozzáadja az átjáró nevű Probe01 nevű állapot-szonda nevű állapotot.</span><span class="sxs-lookup"><span data-stu-id="673f2-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="673f2-110">A parancs azt is megadhatja, hogy az egészségtelen küszöböt 8 próbálkozásra és időpontra állítja az 120 másodperc elteltével.</span><span class="sxs-lookup"><span data-stu-id="673f2-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="673f2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="673f2-111">PARAMETERS</span></span>

### <span data-ttu-id="673f2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="673f2-112">-ApplicationGateway</span></span>
<span data-ttu-id="673f2-113">Annak az alkalmazásnak az átjáróját adja meg, amelyre ez a parancsmag felveszi a szondát.</span><span class="sxs-lookup"><span data-stu-id="673f2-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="673f2-114">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="673f2-114">-HostName</span></span>
<span data-ttu-id="673f2-115">Azt az állomásnevet adja meg, amelyre a parancsmag elküldi a szondát.</span><span class="sxs-lookup"><span data-stu-id="673f2-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="673f2-116">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="673f2-116">-Interval</span></span>
<span data-ttu-id="673f2-117">A szonda intervallumát másodpercben kifejezve adja meg.</span><span class="sxs-lookup"><span data-stu-id="673f2-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="673f2-118">Ez a két egymást követő szonda közötti időtartam.</span><span class="sxs-lookup"><span data-stu-id="673f2-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="673f2-119">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="673f2-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="673f2-120">-Hol. van</span><span class="sxs-lookup"><span data-stu-id="673f2-120">-Match</span></span>
<span data-ttu-id="673f2-121">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="673f2-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="673f2-122">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="673f2-122">Default value is empty</span></span>

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

### <span data-ttu-id="673f2-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="673f2-123">-MinServers</span></span>
<span data-ttu-id="673f2-124">A mindig egészségesként megjelölt kiszolgálók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="673f2-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="673f2-125">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="673f2-125">Default value is 0</span></span>

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

### <span data-ttu-id="673f2-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="673f2-126">-Name</span></span>
<span data-ttu-id="673f2-127">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="673f2-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="673f2-128">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="673f2-128">-Path</span></span>
<span data-ttu-id="673f2-129">A szonda relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="673f2-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="673f2-130">Az érvényes elérési út a perjel (/) karakterrel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="673f2-130">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="673f2-131">A szondát a program a \<Protocol\> ://: értékre küldi \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="673f2-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="673f2-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="673f2-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="673f2-133">Azt, hogy az állomásfejléc a backend http-beállításai között legyen-e kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="673f2-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="673f2-134">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="673f2-134">Default value is false</span></span>

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

### <span data-ttu-id="673f2-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="673f2-135">-Protocol</span></span>
<span data-ttu-id="673f2-136">A szonda küldéséhez használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="673f2-136">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="673f2-137">Ez a parancsmag csak a HTTP-t támogatja.</span><span class="sxs-lookup"><span data-stu-id="673f2-137">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="673f2-138">-Timeout</span><span class="sxs-lookup"><span data-stu-id="673f2-138">-Timeout</span></span>
<span data-ttu-id="673f2-139">A szonda időkorlátját adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="673f2-139">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="673f2-140">Ez a parancsmag a szondát hibásnak minősíti, ha az időtúllépési időszakmal nem érkezik érvényes válasz.</span><span class="sxs-lookup"><span data-stu-id="673f2-140">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="673f2-141">Az érvényes értékek 1 másodperc és 86400 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="673f2-141">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="673f2-142">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="673f2-142">-UnhealthyThreshold</span></span>
<span data-ttu-id="673f2-143">A szonda ismételt ismételt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="673f2-143">Specifies the probe retry count.</span></span>
<span data-ttu-id="673f2-144">A backend-kiszolgáló az egymást követő Szondák meghibásodása után nem éri el az egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="673f2-144">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="673f2-145">Az érvényes értékek 1 másodperc és 20 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="673f2-145">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="673f2-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="673f2-146">-DefaultProfile</span></span>
<span data-ttu-id="673f2-147">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="673f2-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="673f2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="673f2-148">CommonParameters</span></span>
<span data-ttu-id="673f2-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="673f2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="673f2-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="673f2-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="673f2-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="673f2-151">INPUTS</span></span>

### <span data-ttu-id="673f2-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="673f2-152">PSApplicationGateway</span></span>
<span data-ttu-id="673f2-153">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="673f2-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="673f2-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="673f2-154">OUTPUTS</span></span>

### <span data-ttu-id="673f2-155">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="673f2-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="673f2-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="673f2-156">NOTES</span></span>

## <span data-ttu-id="673f2-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="673f2-157">RELATED LINKS</span></span>

[<span data-ttu-id="673f2-158">Szonda hozzáadása meglévő alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="673f2-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="673f2-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="673f2-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="673f2-160">Új – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="673f2-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="673f2-161">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="673f2-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="673f2-162">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="673f2-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

