---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 43c74d2edd2cfd07f65b7d5437bf1cf5c0dfca9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841406"
---
# <span data-ttu-id="ee2e6-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ee2e6-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ee2e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee2e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2e6-103">Létrehoz egy egészségi szondát.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-103">Creates a health probe.</span></span>

## <span data-ttu-id="ee2e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee2e6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee2e6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee2e6-105">DESCRIPTION</span></span>
<span data-ttu-id="ee2e6-106">Az New-AzApplicationGatewayProbeConfig parancsmag létrehoz egy állapottanúsítvány-adatszondát.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="ee2e6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ee2e6-107">EXAMPLES</span></span>

### <span data-ttu-id="ee2e6-108">Example1: állapot-szonda létrehozása</span><span class="sxs-lookup"><span data-stu-id="ee2e6-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="ee2e6-109">Ez a parancs létrehoz egy Probe03 nevű, HTTP protokollt tartalmazó, 30 másodperces, 120 másodperces időkorlátot, valamint 8 újrapróbálkozáskor egy egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="ee2e6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee2e6-110">PARAMETERS</span></span>

### <span data-ttu-id="ee2e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2e6-111">-DefaultProfile</span></span>
<span data-ttu-id="ee2e6-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee2e6-113">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="ee2e6-113">-HostName</span></span>
<span data-ttu-id="ee2e6-114">Azt az állomásnevet adja meg, amelyre a parancsmag elküldi a szonda nevet.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="ee2e6-115">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="ee2e6-115">-Interval</span></span>
<span data-ttu-id="ee2e6-116">A szonda intervallumát másodpercben kifejezve adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="ee2e6-117">Ez a két egymást követő szonda közötti időtartam.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="ee2e6-118">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ee2e6-119">-Hol. van</span><span class="sxs-lookup"><span data-stu-id="ee2e6-119">-Match</span></span>
<span data-ttu-id="ee2e6-120">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="ee2e6-121">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="ee2e6-121">Default value is empty</span></span>

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

### <span data-ttu-id="ee2e6-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="ee2e6-122">-MinServers</span></span>
<span data-ttu-id="ee2e6-123">A mindig egészségesként megjelölt kiszolgálók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="ee2e6-124">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="ee2e6-124">Default value is 0</span></span>

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

### <span data-ttu-id="ee2e6-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee2e6-125">-Name</span></span>
<span data-ttu-id="ee2e6-126">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="ee2e6-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="ee2e6-127">-Path</span></span>
<span data-ttu-id="ee2e6-128">A szonda relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="ee2e6-129">Az érvényes elérési utak a perjel karakterrel (/) kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="ee2e6-130">A szondát a rendszer elküldi a következő \< protokollnak \> ::// \< Host \> : \< port \> \< path \> .</span><span class="sxs-lookup"><span data-stu-id="ee2e6-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="ee2e6-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ee2e6-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="ee2e6-132">Azt, hogy az állomásfejléc a backend http-beállításai között legyen-e kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="ee2e6-133">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="ee2e6-133">Default value is false</span></span>

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

### <span data-ttu-id="ee2e6-134">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ee2e6-134">-Protocol</span></span>
<span data-ttu-id="ee2e6-135">A szonda küldéséhez használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="ee2e6-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="ee2e6-136">-Timeout</span></span>
<span data-ttu-id="ee2e6-137">A szonda időkorlátját adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="ee2e6-138">Ez a parancsmag a szondát hibásnak minősíti, ha az időtúllépési időszakmal nem érkezik érvényes válasz.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="ee2e6-139">Az érvényes értékek 1 másodperc és 86400 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ee2e6-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="ee2e6-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="ee2e6-141">A szonda ismételt ismételt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="ee2e6-142">A backend-kiszolgáló az egymást követő Szondák meghibásodása után nem éri el az egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="ee2e6-143">Az érvényes értékek 1 másodperc és 20 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="ee2e6-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="ee2e6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2e6-144">CommonParameters</span></span>
<span data-ttu-id="ee2e6-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee2e6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2e6-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee2e6-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2e6-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee2e6-147">INPUTS</span></span>

## <span data-ttu-id="ee2e6-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee2e6-148">OUTPUTS</span></span>

### <span data-ttu-id="ee2e6-149">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="ee2e6-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="ee2e6-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee2e6-150">NOTES</span></span>

## <span data-ttu-id="ee2e6-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee2e6-151">RELATED LINKS</span></span>

[<span data-ttu-id="ee2e6-152">Egyéni szonda létrehozása az alkalmazás-átjáróhoz az Azure Resource Manager PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="ee2e6-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="ee2e6-153">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ee2e6-153">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ee2e6-154">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ee2e6-154">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ee2e6-155">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ee2e6-155">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ee2e6-156">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ee2e6-156">Set-AzApplicationGatewayProbeConfig</span></span>]()

