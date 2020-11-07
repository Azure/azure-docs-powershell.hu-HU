---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 75688743c03db16c9683b84698ad41ddcb7fa52e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670397"
---
# <span data-ttu-id="001ba-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="001ba-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="001ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="001ba-102">SYNOPSIS</span></span>
<span data-ttu-id="001ba-103">Létrehoz egy egészségi szondát.</span><span class="sxs-lookup"><span data-stu-id="001ba-103">Creates a health probe.</span></span>

## <span data-ttu-id="001ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="001ba-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="001ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="001ba-105">DESCRIPTION</span></span>
<span data-ttu-id="001ba-106">Az New-AzApplicationGatewayProbeConfig parancsmag létrehoz egy állapottanúsítvány-adatszondát.</span><span class="sxs-lookup"><span data-stu-id="001ba-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="001ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="001ba-107">EXAMPLES</span></span>

### <span data-ttu-id="001ba-108">Example1: állapot-szonda létrehozása</span><span class="sxs-lookup"><span data-stu-id="001ba-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="001ba-109">Ez a parancs létrehoz egy Probe03 nevű, HTTP protokollt tartalmazó, 30 másodperces, 120 másodperces időkorlátot, valamint 8 újrapróbálkozáskor egy egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="001ba-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="001ba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="001ba-110">PARAMETERS</span></span>

### <span data-ttu-id="001ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="001ba-111">-DefaultProfile</span></span>
<span data-ttu-id="001ba-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="001ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="001ba-113">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="001ba-113">-HostName</span></span>
<span data-ttu-id="001ba-114">Azt az állomásnevet adja meg, amelyre a parancsmag elküldi a szonda nevet.</span><span class="sxs-lookup"><span data-stu-id="001ba-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="001ba-115">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="001ba-115">-Interval</span></span>
<span data-ttu-id="001ba-116">A szonda intervallumát másodpercben kifejezve adja meg.</span><span class="sxs-lookup"><span data-stu-id="001ba-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="001ba-117">Ez a két egymást követő szonda közötti időtartam.</span><span class="sxs-lookup"><span data-stu-id="001ba-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="001ba-118">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="001ba-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="001ba-119">-Hol. van</span><span class="sxs-lookup"><span data-stu-id="001ba-119">-Match</span></span>
<span data-ttu-id="001ba-120">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="001ba-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="001ba-121">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="001ba-121">Default value is empty</span></span>

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

### <span data-ttu-id="001ba-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="001ba-122">-MinServers</span></span>
<span data-ttu-id="001ba-123">A mindig egészségesként megjelölt kiszolgálók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="001ba-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="001ba-124">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="001ba-124">Default value is 0</span></span>

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

### <span data-ttu-id="001ba-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="001ba-125">-Name</span></span>
<span data-ttu-id="001ba-126">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="001ba-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="001ba-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="001ba-127">-Path</span></span>
<span data-ttu-id="001ba-128">A szonda relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="001ba-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="001ba-129">Az érvényes elérési utak a perjel karakterrel (/) kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="001ba-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="001ba-130">A szondát a rendszer elküldi a következő \< protokollnak \> ::// \< Host \> : \< port \> \< path \> .</span><span class="sxs-lookup"><span data-stu-id="001ba-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="001ba-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="001ba-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="001ba-132">Azt, hogy az állomásfejléc a backend http-beállításai között legyen-e kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="001ba-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="001ba-133">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="001ba-133">Default value is false</span></span>

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

### <span data-ttu-id="001ba-134">-Protocol</span><span class="sxs-lookup"><span data-stu-id="001ba-134">-Protocol</span></span>
<span data-ttu-id="001ba-135">A szonda küldéséhez használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="001ba-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="001ba-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="001ba-136">-Timeout</span></span>
<span data-ttu-id="001ba-137">A szonda időkorlátját adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="001ba-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="001ba-138">Ez a parancsmag a szondát hibásnak minősíti, ha az időtúllépési időszakmal nem érkezik érvényes válasz.</span><span class="sxs-lookup"><span data-stu-id="001ba-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="001ba-139">Az érvényes értékek 1 másodperc és 86400 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="001ba-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="001ba-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="001ba-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="001ba-141">A szonda ismételt ismételt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="001ba-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="001ba-142">A backend-kiszolgáló az egymást követő Szondák meghibásodása után nem éri el az egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="001ba-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="001ba-143">Az érvényes értékek 1 másodperc és 20 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="001ba-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="001ba-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="001ba-144">CommonParameters</span></span>
<span data-ttu-id="001ba-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="001ba-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="001ba-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="001ba-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="001ba-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="001ba-147">INPUTS</span></span>

### <span data-ttu-id="001ba-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="001ba-148">None</span></span>

## <span data-ttu-id="001ba-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="001ba-149">OUTPUTS</span></span>

### <span data-ttu-id="001ba-150">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="001ba-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="001ba-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="001ba-151">NOTES</span></span>

## <span data-ttu-id="001ba-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="001ba-152">RELATED LINKS</span></span>

[<span data-ttu-id="001ba-153">Egyéni szonda létrehozása az alkalmazás-átjáróhoz az Azure Resource Manager PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="001ba-153">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="001ba-154">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="001ba-154">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="001ba-155">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="001ba-155">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="001ba-156">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="001ba-156">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="001ba-157">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="001ba-157">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

