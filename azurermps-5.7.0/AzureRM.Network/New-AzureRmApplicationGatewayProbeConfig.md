---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 955f5179340351dd662979385ca3d3dc2a39b9f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500504"
---
# <span data-ttu-id="5204b-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5204b-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="5204b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5204b-102">SYNOPSIS</span></span>
<span data-ttu-id="5204b-103">Létrehoz egy egészségi szondát.</span><span class="sxs-lookup"><span data-stu-id="5204b-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5204b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5204b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5204b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5204b-105">DESCRIPTION</span></span>
<span data-ttu-id="5204b-106">Az New-AzureRmApplicationGatewayProbeConfig parancsmag létrehoz egy állapottanúsítvány-adatszondát.</span><span class="sxs-lookup"><span data-stu-id="5204b-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="5204b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5204b-107">EXAMPLES</span></span>

### <span data-ttu-id="5204b-108">Example1: állapot-szonda létrehozása</span><span class="sxs-lookup"><span data-stu-id="5204b-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="5204b-109">Ez a parancs létrehoz egy Probe03 nevű, HTTP protokollt tartalmazó, 30 másodperces, 120 másodperces időkorlátot, valamint 8 újrapróbálkozáskor egy egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="5204b-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="5204b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5204b-110">PARAMETERS</span></span>

### <span data-ttu-id="5204b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5204b-111">-DefaultProfile</span></span>
<span data-ttu-id="5204b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5204b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5204b-113">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="5204b-113">-HostName</span></span>
<span data-ttu-id="5204b-114">Azt az állomásnevet adja meg, amelyre a parancsmag elküldi a szonda nevet.</span><span class="sxs-lookup"><span data-stu-id="5204b-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="5204b-115">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="5204b-115">-Interval</span></span>
<span data-ttu-id="5204b-116">A szonda intervallumát másodpercben kifejezve adja meg.</span><span class="sxs-lookup"><span data-stu-id="5204b-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="5204b-117">Ez a két egymást követő szonda közötti időtartam.</span><span class="sxs-lookup"><span data-stu-id="5204b-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="5204b-118">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="5204b-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="5204b-119">-Hol. van</span><span class="sxs-lookup"><span data-stu-id="5204b-119">-Match</span></span>
<span data-ttu-id="5204b-120">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="5204b-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="5204b-121">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="5204b-121">Default value is empty</span></span>

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

### <span data-ttu-id="5204b-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="5204b-122">-MinServers</span></span>
<span data-ttu-id="5204b-123">A mindig egészségesként megjelölt kiszolgálók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="5204b-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="5204b-124">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="5204b-124">Default value is 0</span></span>

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

### <span data-ttu-id="5204b-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5204b-125">-Name</span></span>
<span data-ttu-id="5204b-126">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5204b-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="5204b-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="5204b-127">-Path</span></span>
<span data-ttu-id="5204b-128">A szonda relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5204b-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="5204b-129">Az érvényes elérési utak a perjel karakterrel (/) kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="5204b-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="5204b-130">A szondát a program a \<Protocol\> ://: értékre küldi \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="5204b-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="5204b-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5204b-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="5204b-132">Azt, hogy az állomásfejléc a backend http-beállításai között legyen-e kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="5204b-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="5204b-133">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="5204b-133">Default value is false</span></span>

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

### <span data-ttu-id="5204b-134">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5204b-134">-Protocol</span></span>
<span data-ttu-id="5204b-135">A szonda küldéséhez használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="5204b-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="5204b-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="5204b-136">-Timeout</span></span>
<span data-ttu-id="5204b-137">A szonda időkorlátját adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="5204b-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="5204b-138">Ez a parancsmag a szondát hibásnak minősíti, ha az időtúllépési időszakmal nem érkezik érvényes válasz.</span><span class="sxs-lookup"><span data-stu-id="5204b-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="5204b-139">Az érvényes értékek 1 másodperc és 86400 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="5204b-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="5204b-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="5204b-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="5204b-141">A szonda ismételt ismételt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5204b-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="5204b-142">A backend-kiszolgáló az egymást követő Szondák meghibásodása után nem éri el az egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="5204b-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="5204b-143">Az érvényes értékek 1 másodperc és 20 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="5204b-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="5204b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5204b-144">CommonParameters</span></span>
<span data-ttu-id="5204b-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5204b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5204b-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5204b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5204b-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5204b-147">INPUTS</span></span>

### <span data-ttu-id="5204b-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="5204b-148">None</span></span>
<span data-ttu-id="5204b-149">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5204b-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5204b-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5204b-150">OUTPUTS</span></span>

### <span data-ttu-id="5204b-151">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="5204b-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="5204b-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5204b-152">NOTES</span></span>

## <span data-ttu-id="5204b-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5204b-153">RELATED LINKS</span></span>

[<span data-ttu-id="5204b-154">Egyéni szonda létrehozása az alkalmazás-átjáróhoz az Azure Resource Manager PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="5204b-154">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="5204b-155">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5204b-155">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5204b-156">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5204b-156">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5204b-157">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5204b-157">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5204b-158">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5204b-158">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

