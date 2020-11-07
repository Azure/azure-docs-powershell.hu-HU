---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 538020fa9ef55eedfdf7b181fca16f9499f46682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673159"
---
# <span data-ttu-id="e34dc-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e34dc-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="e34dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e34dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e34dc-103">Létrehoz egy egészségi szondát.</span><span class="sxs-lookup"><span data-stu-id="e34dc-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e34dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e34dc-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e34dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e34dc-105">DESCRIPTION</span></span>
<span data-ttu-id="e34dc-106">Az New-AzureRmApplicationGatewayProbeConfig parancsmag létrehoz egy állapottanúsítvány-adatszondát.</span><span class="sxs-lookup"><span data-stu-id="e34dc-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="e34dc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e34dc-107">EXAMPLES</span></span>

### <span data-ttu-id="e34dc-108">Example1: állapot-szonda létrehozása</span><span class="sxs-lookup"><span data-stu-id="e34dc-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="e34dc-109">Ez a parancs létrehoz egy Probe03 nevű, HTTP protokollt tartalmazó, 30 másodperces, 120 másodperces időkorlátot, valamint 8 újrapróbálkozáskor egy egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="e34dc-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="e34dc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e34dc-110">PARAMETERS</span></span>

### <span data-ttu-id="e34dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e34dc-111">-DefaultProfile</span></span>
<span data-ttu-id="e34dc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e34dc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e34dc-113">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="e34dc-113">-HostName</span></span>
<span data-ttu-id="e34dc-114">Azt az állomásnevet adja meg, amelyre a parancsmag elküldi a szonda nevet.</span><span class="sxs-lookup"><span data-stu-id="e34dc-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="e34dc-115">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="e34dc-115">-Interval</span></span>
<span data-ttu-id="e34dc-116">A szonda intervallumát másodpercben kifejezve adja meg.</span><span class="sxs-lookup"><span data-stu-id="e34dc-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="e34dc-117">Ez a két egymást követő szonda közötti időtartam.</span><span class="sxs-lookup"><span data-stu-id="e34dc-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="e34dc-118">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="e34dc-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e34dc-119">-Hol. van</span><span class="sxs-lookup"><span data-stu-id="e34dc-119">-Match</span></span>
<span data-ttu-id="e34dc-120">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="e34dc-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="e34dc-121">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="e34dc-121">Default value is empty</span></span>

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

### <span data-ttu-id="e34dc-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="e34dc-122">-MinServers</span></span>
<span data-ttu-id="e34dc-123">A mindig egészségesként megjelölt kiszolgálók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="e34dc-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="e34dc-124">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="e34dc-124">Default value is 0</span></span>

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

### <span data-ttu-id="e34dc-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e34dc-125">-Name</span></span>
<span data-ttu-id="e34dc-126">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e34dc-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="e34dc-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="e34dc-127">-Path</span></span>
<span data-ttu-id="e34dc-128">A szonda relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e34dc-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="e34dc-129">Az érvényes elérési utak a perjel karakterrel (/) kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="e34dc-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="e34dc-130">A szondát a program a \<Protocol\> ://: értékre küldi \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="e34dc-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="e34dc-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e34dc-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="e34dc-132">Azt, hogy az állomásfejléc a backend http-beállításai között legyen-e kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="e34dc-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="e34dc-133">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="e34dc-133">Default value is false</span></span>

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

### <span data-ttu-id="e34dc-134">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e34dc-134">-Protocol</span></span>
<span data-ttu-id="e34dc-135">A szonda küldéséhez használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="e34dc-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="e34dc-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="e34dc-136">-Timeout</span></span>
<span data-ttu-id="e34dc-137">A szonda időkorlátját adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="e34dc-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="e34dc-138">Ez a parancsmag a szondát hibásnak minősíti, ha az időtúllépési időszakmal nem érkezik érvényes válasz.</span><span class="sxs-lookup"><span data-stu-id="e34dc-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="e34dc-139">Az érvényes értékek 1 másodperc és 86400 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="e34dc-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e34dc-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="e34dc-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="e34dc-141">A szonda ismételt ismételt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e34dc-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="e34dc-142">A backend-kiszolgáló az egymást követő Szondák meghibásodása után nem éri el az egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="e34dc-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="e34dc-143">Az érvényes értékek 1 másodperc és 20 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="e34dc-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="e34dc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e34dc-144">CommonParameters</span></span>
<span data-ttu-id="e34dc-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e34dc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e34dc-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e34dc-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e34dc-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e34dc-147">INPUTS</span></span>

### <span data-ttu-id="e34dc-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="e34dc-148">None</span></span>

## <span data-ttu-id="e34dc-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e34dc-149">OUTPUTS</span></span>

### <span data-ttu-id="e34dc-150">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="e34dc-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="e34dc-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e34dc-151">NOTES</span></span>

## <span data-ttu-id="e34dc-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e34dc-152">RELATED LINKS</span></span>

[<span data-ttu-id="e34dc-153">Egyéni szonda létrehozása az alkalmazás-átjáróhoz az Azure Resource Manager PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="e34dc-153">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="e34dc-154">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e34dc-154">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e34dc-155">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e34dc-155">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e34dc-156">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e34dc-156">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e34dc-157">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e34dc-157">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

