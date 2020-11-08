---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 16499dfb72f973169769c35cd1ba427eba52fd0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014797"
---
# <span data-ttu-id="3ea8c-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3ea8c-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="3ea8c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ea8c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea8c-103">Létrehoz egy egészségi szondát.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-103">Creates a health probe.</span></span>

## <span data-ttu-id="3ea8c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ea8c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-Port <Int32>]
```

## <span data-ttu-id="3ea8c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ea8c-105">DESCRIPTION</span></span>
<span data-ttu-id="3ea8c-106">Az New-AzApplicationGatewayProbeConfig parancsmag létrehoz egy állapottanúsítvány-adatszondát.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="3ea8c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3ea8c-107">EXAMPLES</span></span>

### <span data-ttu-id="3ea8c-108">Example1: állapot-szonda létrehozása</span><span class="sxs-lookup"><span data-stu-id="3ea8c-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="3ea8c-109">Ez a parancs létrehoz egy Probe03 nevű, HTTP protokollt tartalmazó, 30 másodperces, 120 másodperces időkorlátot, valamint 8 újrapróbálkozáskor egy egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="3ea8c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ea8c-110">PARAMETERS</span></span>

### <span data-ttu-id="3ea8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea8c-111">-DefaultProfile</span></span>
<span data-ttu-id="3ea8c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ea8c-113">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="3ea8c-113">-HostName</span></span>
<span data-ttu-id="3ea8c-114">Azt az állomásnevet adja meg, amelyre a parancsmag elküldi a szonda nevet.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="3ea8c-115">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="3ea8c-115">-Interval</span></span>
<span data-ttu-id="3ea8c-116">A szonda intervallumát másodpercben kifejezve adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="3ea8c-117">Ez a két egymást követő szonda közötti időtartam.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="3ea8c-118">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="3ea8c-119">-Hol. van</span><span class="sxs-lookup"><span data-stu-id="3ea8c-119">-Match</span></span>
<span data-ttu-id="3ea8c-120">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="3ea8c-121">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="3ea8c-121">Default value is empty</span></span>

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

### <span data-ttu-id="3ea8c-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="3ea8c-122">-MinServers</span></span>
<span data-ttu-id="3ea8c-123">A mindig egészségesként megjelölt kiszolgálók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="3ea8c-124">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="3ea8c-124">Default value is 0</span></span>

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

### <span data-ttu-id="3ea8c-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ea8c-125">-Name</span></span>
<span data-ttu-id="3ea8c-126">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="3ea8c-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="3ea8c-127">-Path</span></span>
<span data-ttu-id="3ea8c-128">A szonda relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="3ea8c-129">Az érvényes elérési utak a perjel karakterrel (/) kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="3ea8c-130">A szondát a rendszer elküldi a következő \< protokollnak \> ::// \< Host \> : \< port \> \< path \> .</span><span class="sxs-lookup"><span data-stu-id="3ea8c-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="3ea8c-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3ea8c-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="3ea8c-132">Azt, hogy az állomásfejléc a backend http-beállításai között legyen-e kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="3ea8c-133">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="3ea8c-133">Default value is false</span></span>

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

### <span data-ttu-id="3ea8c-134">-Protocol</span><span class="sxs-lookup"><span data-stu-id="3ea8c-134">-Protocol</span></span>
<span data-ttu-id="3ea8c-135">A szonda küldéséhez használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="3ea8c-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="3ea8c-136">-Timeout</span></span>
<span data-ttu-id="3ea8c-137">A szonda időkorlátját adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="3ea8c-138">Ez a parancsmag a szondát hibásnak minősíti, ha az időtúllépési időszakmal nem érkezik érvényes válasz.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="3ea8c-139">Az érvényes értékek 1 másodperc és 86400 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="3ea8c-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="3ea8c-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="3ea8c-141">A szonda ismételt ismételt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="3ea8c-142">A backend-kiszolgáló az egymást követő Szondák meghibásodása után nem éri el az egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="3ea8c-143">Az érvényes értékek 1 másodperc és 20 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="3ea8c-144">-Port</span><span class="sxs-lookup"><span data-stu-id="3ea8c-144">-Port</span></span>
<span data-ttu-id="3ea8c-145">A kijelölő backend-kiszolgálókhoz használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea8c-145">Specifies the port used for probing backend servers.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe

## NOTES

## RELATED LINKS

[Create custom probe for Application Gateway using PowerShell for Azure Resource Manager](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[Add-AzApplicationGatewayProbeConfig](./Add-AzApplicationGatewayProbeConfig.md)

[Get-AzApplicationGatewayProbeConfig](./Get-AzApplicationGatewayProbeConfig.md)

[Remove-AzApplicationGatewayProbeConfig](./Remove-AzApplicationGatewayProbeConfig.md)

[Set-AzApplicationGatewayProbeConfig](./Set-AzApplicationGatewayProbeConfig.md)

