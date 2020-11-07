---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 87c064cbd3672a5e8d8f198432de87c0facf29cd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849977"
---
# <span data-ttu-id="fd67c-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fd67c-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="fd67c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd67c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd67c-103">Egy adatszondát ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="fd67c-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd67c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd67c-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd67c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd67c-105">DESCRIPTION</span></span>
<span data-ttu-id="fd67c-106">A Add-AzureRmApplicationGatewayProbeConfig parancsmag az alkalmazás-átjáróhoz ad hozzá egy állapottanúsítvány-adatszondát.</span><span class="sxs-lookup"><span data-stu-id="fd67c-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="fd67c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fd67c-107">EXAMPLES</span></span>

### <span data-ttu-id="fd67c-108">1. példa: biztonságiállapot-szonda felvétele az alkalmazás-átjáróba</span><span class="sxs-lookup"><span data-stu-id="fd67c-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="fd67c-109">Ez a parancs hozzáadja az átjáró nevű Probe01 nevű állapot-szonda nevű állapotot.</span><span class="sxs-lookup"><span data-stu-id="fd67c-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="fd67c-110">A parancs azt is megadhatja, hogy az egészségtelen küszöböt 8 próbálkozásra és időpontra állítja az 120 másodperc elteltével.</span><span class="sxs-lookup"><span data-stu-id="fd67c-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="fd67c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd67c-111">PARAMETERS</span></span>

### <span data-ttu-id="fd67c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd67c-112">-ApplicationGateway</span></span>
<span data-ttu-id="fd67c-113">Annak az alkalmazásnak az átjáróját adja meg, amelyre ez a parancsmag felveszi a szondát.</span><span class="sxs-lookup"><span data-stu-id="fd67c-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd67c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd67c-114">-DefaultProfile</span></span>
<span data-ttu-id="fd67c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd67c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd67c-116">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="fd67c-116">-HostName</span></span>
<span data-ttu-id="fd67c-117">Azt az állomásnevet adja meg, amelyre a parancsmag elküldi a szondát.</span><span class="sxs-lookup"><span data-stu-id="fd67c-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="fd67c-118">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="fd67c-118">-Interval</span></span>
<span data-ttu-id="fd67c-119">A szonda intervallumát másodpercben kifejezve adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd67c-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="fd67c-120">Ez a két egymást követő szonda közötti időtartam.</span><span class="sxs-lookup"><span data-stu-id="fd67c-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="fd67c-121">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="fd67c-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="fd67c-122">-Hol. van</span><span class="sxs-lookup"><span data-stu-id="fd67c-122">-Match</span></span>
<span data-ttu-id="fd67c-123">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="fd67c-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="fd67c-124">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="fd67c-124">Default value is empty</span></span>

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd67c-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="fd67c-125">-MinServers</span></span>
<span data-ttu-id="fd67c-126">A mindig egészségesként megjelölt kiszolgálók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="fd67c-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="fd67c-127">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="fd67c-127">Default value is 0</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd67c-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd67c-128">-Name</span></span>
<span data-ttu-id="fd67c-129">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd67c-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="fd67c-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="fd67c-130">-Path</span></span>
<span data-ttu-id="fd67c-131">A szonda relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd67c-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="fd67c-132">Az érvényes elérési út a perjel (/) karakterrel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="fd67c-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="fd67c-133">A szondát a program a \<Protocol\> ://: értékre küldi \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="fd67c-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="fd67c-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fd67c-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="fd67c-135">Azt, hogy az állomásfejléc a backend http-beállításai között legyen-e kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="fd67c-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="fd67c-136">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="fd67c-136">Default value is false</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd67c-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="fd67c-137">-Protocol</span></span>
<span data-ttu-id="fd67c-138">A szonda küldéséhez használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd67c-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="fd67c-139">Ez a parancsmag csak a HTTP-t támogatja.</span><span class="sxs-lookup"><span data-stu-id="fd67c-139">This cmdlet supports HTTP only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd67c-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="fd67c-140">-Timeout</span></span>
<span data-ttu-id="fd67c-141">A szonda időkorlátját adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="fd67c-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="fd67c-142">Ez a parancsmag a szondát hibásnak minősíti, ha az időtúllépési időszakmal nem érkezik érvényes válasz.</span><span class="sxs-lookup"><span data-stu-id="fd67c-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="fd67c-143">Az érvényes értékek 1 másodperc és 86400 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="fd67c-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="fd67c-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="fd67c-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="fd67c-145">A szonda ismételt ismételt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd67c-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="fd67c-146">A backend-kiszolgáló az egymást követő Szondák meghibásodása után nem éri el az egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="fd67c-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="fd67c-147">Az érvényes értékek 1 másodperc és 20 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="fd67c-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="fd67c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd67c-148">CommonParameters</span></span>
<span data-ttu-id="fd67c-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd67c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd67c-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd67c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd67c-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd67c-151">INPUTS</span></span>

### <span data-ttu-id="fd67c-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd67c-152">PSApplicationGateway</span></span>
<span data-ttu-id="fd67c-153">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="fd67c-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="fd67c-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd67c-154">OUTPUTS</span></span>

### <span data-ttu-id="fd67c-155">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd67c-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fd67c-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd67c-156">NOTES</span></span>

## <span data-ttu-id="fd67c-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd67c-157">RELATED LINKS</span></span>

[<span data-ttu-id="fd67c-158">Szonda hozzáadása meglévő alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="fd67c-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="fd67c-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fd67c-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fd67c-160">Új – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fd67c-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fd67c-161">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fd67c-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fd67c-162">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fd67c-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

