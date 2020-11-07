---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 0e3c0c9a3f1c47163a28dc1732ef488f87014c63
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848154"
---
# <span data-ttu-id="4eb88-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4eb88-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="4eb88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4eb88-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb88-103">Létrehoz egy egészségi szondát.</span><span class="sxs-lookup"><span data-stu-id="4eb88-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eb88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4eb88-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eb88-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4eb88-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb88-106">Az New-AzureRmApplicationGatewayProbeConfig parancsmag létrehoz egy állapottanúsítvány-adatszondát.</span><span class="sxs-lookup"><span data-stu-id="4eb88-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="4eb88-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4eb88-107">EXAMPLES</span></span>

### <span data-ttu-id="4eb88-108">Example1: állapot-szonda létrehozása</span><span class="sxs-lookup"><span data-stu-id="4eb88-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="4eb88-109">Ez a parancs létrehoz egy Probe03 nevű, HTTP protokollt tartalmazó, 30 másodperces, 120 másodperces időkorlátot, valamint 8 újrapróbálkozáskor egy egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="4eb88-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="4eb88-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4eb88-110">PARAMETERS</span></span>

### <span data-ttu-id="4eb88-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb88-111">-DefaultProfile</span></span>
<span data-ttu-id="4eb88-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4eb88-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eb88-113">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="4eb88-113">-HostName</span></span>
<span data-ttu-id="4eb88-114">Azt az állomásnevet adja meg, amelyre a parancsmag elküldi a szonda nevet.</span><span class="sxs-lookup"><span data-stu-id="4eb88-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="4eb88-115">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="4eb88-115">-Interval</span></span>
<span data-ttu-id="4eb88-116">A szonda intervallumát másodpercben kifejezve adja meg.</span><span class="sxs-lookup"><span data-stu-id="4eb88-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="4eb88-117">Ez a két egymást követő szonda közötti időtartam.</span><span class="sxs-lookup"><span data-stu-id="4eb88-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="4eb88-118">Ez az érték 1 másodperc és 86400 másodperc között van.</span><span class="sxs-lookup"><span data-stu-id="4eb88-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="4eb88-119">-Hol. van</span><span class="sxs-lookup"><span data-stu-id="4eb88-119">-Match</span></span>
<span data-ttu-id="4eb88-120">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="4eb88-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="4eb88-121">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="4eb88-121">Default value is empty</span></span>

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

### <span data-ttu-id="4eb88-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="4eb88-122">-MinServers</span></span>
<span data-ttu-id="4eb88-123">A mindig egészségesként megjelölt kiszolgálók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="4eb88-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="4eb88-124">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="4eb88-124">Default value is 0</span></span>

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

### <span data-ttu-id="4eb88-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4eb88-125">-Name</span></span>
<span data-ttu-id="4eb88-126">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4eb88-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="4eb88-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="4eb88-127">-Path</span></span>
<span data-ttu-id="4eb88-128">A szonda relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4eb88-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="4eb88-129">Az érvényes elérési utak a perjel karakterrel (/) kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="4eb88-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="4eb88-130">A szondát a program a \<Protocol\> ://: értékre küldi \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="4eb88-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="4eb88-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4eb88-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="4eb88-132">Azt, hogy az állomásfejléc a backend http-beállításai között legyen-e kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="4eb88-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="4eb88-133">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="4eb88-133">Default value is false</span></span>

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

### <span data-ttu-id="4eb88-134">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4eb88-134">-Protocol</span></span>
<span data-ttu-id="4eb88-135">A szonda küldéséhez használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="4eb88-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="4eb88-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="4eb88-136">-Timeout</span></span>
<span data-ttu-id="4eb88-137">A szonda időkorlátját adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="4eb88-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="4eb88-138">Ez a parancsmag a szondát hibásnak minősíti, ha az időtúllépési időszakmal nem érkezik érvényes válasz.</span><span class="sxs-lookup"><span data-stu-id="4eb88-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="4eb88-139">Az érvényes értékek 1 másodperc és 86400 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="4eb88-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="4eb88-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="4eb88-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="4eb88-141">A szonda ismételt ismételt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4eb88-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="4eb88-142">A backend-kiszolgáló az egymást követő Szondák meghibásodása után nem éri el az egészségtelen küszöböt.</span><span class="sxs-lookup"><span data-stu-id="4eb88-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="4eb88-143">Az érvényes értékek 1 másodperc és 20 másodperc között jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="4eb88-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="4eb88-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb88-144">CommonParameters</span></span>
<span data-ttu-id="4eb88-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4eb88-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb88-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb88-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb88-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eb88-147">INPUTS</span></span>

## <span data-ttu-id="4eb88-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eb88-148">OUTPUTS</span></span>

### <span data-ttu-id="4eb88-149">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="4eb88-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="4eb88-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4eb88-150">NOTES</span></span>

## <span data-ttu-id="4eb88-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4eb88-151">RELATED LINKS</span></span>

[<span data-ttu-id="4eb88-152">Egyéni szonda létrehozása az alkalmazás-átjáróhoz az Azure Resource Manager PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="4eb88-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="4eb88-153">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4eb88-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4eb88-154">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4eb88-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4eb88-155">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4eb88-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4eb88-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4eb88-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

