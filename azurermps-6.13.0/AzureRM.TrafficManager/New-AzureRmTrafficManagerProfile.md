---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bc59e5b317588317ae9dc428db76c924847895da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679806"
---
# <span data-ttu-id="7c9b3-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7c9b3-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="7c9b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="7c9b3-103">Forgalomirányító-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c9b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c9b3-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c9b3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c9b3-105">DESCRIPTION</span></span>
<span data-ttu-id="7c9b3-106">A **New-AzureRmTrafficManagerProfile** parancsmag egy Azure Traffic Manager-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7c9b3-107">Adja meg a *Name* paramétert és a szükséges beállításokat.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="7c9b3-108">Ez a parancsmag egy olyan helyi objektumot ad eredményül, amely az új profilt jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="7c9b3-109">Ez a parancsmag nem állítja be a forgalomirányítási végpontokat.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="7c9b3-110">A helyi profil objektum a Add-AzureRmTrafficManagerEndpointConfig parancsmag segítségével frissíthető.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="7c9b3-111">Ezután töltse fel a Traffic Manager módosításait a Set-AzureRmTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="7c9b3-112">Másik lehetőségként az New-AzureRmTrafficManagerEndpoint parancsmag használatával is hozzáadhat végpontokat.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="7c9b3-113">Példák</span><span class="sxs-lookup"><span data-stu-id="7c9b3-113">EXAMPLES</span></span>

### <span data-ttu-id="7c9b3-114">Példa 1: profil létrehozása</span><span class="sxs-lookup"><span data-stu-id="7c9b3-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="7c9b3-115">Ez a parancs létrehoz egy ContosoProfile nevű Azure Traffic Manager-profilt az erőforráscsoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="7c9b3-116">A DNS FQDN a contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="7c9b3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c9b3-117">PARAMETERS</span></span>

### <span data-ttu-id="7c9b3-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="7c9b3-118">-CustomHeader</span></span>
<span data-ttu-id="7c9b3-119">Az egyéni élőfej neve és az érték párok listája a szonda-kérésekhez.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-119">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c9b3-120">-DefaultProfile</span></span>
<span data-ttu-id="7c9b3-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c9b3-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="7c9b3-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="7c9b3-123">A szonda-kérelmek várható HTTP-állapotkódot tartalmazó tartományai.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-123">List of expected HTTP status code ranges for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="7c9b3-124">-MaxReturn</span></span>
<span data-ttu-id="7c9b3-125">A profilokhoz a többértékű útválasztási módszerrel kapott válaszok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7c9b3-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="7c9b3-127">Annak az intervallumnak (másodpercben), amelyen a forgalmi vezető a profil minden végpontjának állapotát ellenőrizni fogja.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="7c9b3-128">Az alapértelmezett érték 30.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-128">The default is 30.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="7c9b3-129">-MonitorPath</span></span>
<span data-ttu-id="7c9b3-130">A végpontok állapotának figyeléséhez használt elérési utat adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="7c9b3-131">Adjon meg egy értéket a végpont tartománynevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="7c9b3-132">Ennek az értéknek perjelet (/) kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-132">This value must begin with a slash (/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="7c9b3-133">-MonitorPort</span></span>
<span data-ttu-id="7c9b3-134">Azt a TCP-portot adja meg, amely a végpontok állapotának figyeléséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="7c9b3-135">Az érvényes értékek 1 és 65535 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-135">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="7c9b3-136">-MonitorProtocol</span></span>
<span data-ttu-id="7c9b3-137">A végpontok állapotának figyeléséhez használható protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="7c9b3-138">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="7c9b3-138">Valid values are:</span></span>

- <span data-ttu-id="7c9b3-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="7c9b3-139">HTTP</span></span>
- <span data-ttu-id="7c9b3-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="7c9b3-140">HTTPS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="7c9b3-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="7c9b3-142">A forgalmi vezető időpontja (másodpercben) lehetővé teszi, hogy az ebben a profilban szereplő végpontok megválaszolják az állapot-ellenőrzést.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="7c9b3-143">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-143">The default is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="7c9b3-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="7c9b3-145">Az egymást követő sikertelen állapot-ellenőrzések száma, amelyeket a Traffic Manager a következő egymást követő sikertelen állapot-ellenőrzés után a következő egymást követő sikertelen állapot ellenőrzése után tolerálja.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="7c9b3-146">Az alapértelmezett érték a 3.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-146">The default is 3.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c9b3-147">-Name</span></span>
<span data-ttu-id="7c9b3-148">A parancsmag által létrehozott Traffic Manager-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7c9b3-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="7c9b3-149">-ProfileStatus</span></span>
<span data-ttu-id="7c9b3-150">A profil állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="7c9b3-151">Az érvényes értékek: engedélyezve és letiltva.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-151">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="7c9b3-152">-RelativeDnsName</span></span>
<span data-ttu-id="7c9b3-153">Azt a relatív DNS-nevet adja meg, amelyre ez a forgalomirányító-profil nyújt.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="7c9b3-154">A Traffic Manager kombinálja ezt az értéket és azt a DNS-tartománynevet, amelyet az Azure Traffic Manager a profil teljes tartománynevét (FQDN) alkot.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="7c9b3-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c9b3-155">-ResourceGroupName</span></span>
<span data-ttu-id="7c9b3-156">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7c9b3-157">Ez a parancsmag létrehoz egy Traffic Manager-profilt abban a csoportban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c9b3-158">-Címke</span><span class="sxs-lookup"><span data-stu-id="7c9b3-158">-Tag</span></span>
<span data-ttu-id="7c9b3-159">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="7c9b3-160">Példa:</span><span class="sxs-lookup"><span data-stu-id="7c9b3-160">For example:</span></span>

<span data-ttu-id="7c9b3-161">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="7c9b3-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="7c9b3-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="7c9b3-163">A forgalmi útválasztási módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="7c9b3-164">Ez a módszer azt határozza meg, hogy a végpont-forgalmi vezető milyen válaszokat ad a bejövő DNS-lekérdezésekre válaszul.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="7c9b3-165">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="7c9b3-165">Valid values are:</span></span>

- <span data-ttu-id="7c9b3-166">Teljesítmény</span><span class="sxs-lookup"><span data-stu-id="7c9b3-166">Performance</span></span>
- <span data-ttu-id="7c9b3-167">Súlyozott</span><span class="sxs-lookup"><span data-stu-id="7c9b3-167">Weighted</span></span>
- <span data-ttu-id="7c9b3-168">Prioritás</span><span class="sxs-lookup"><span data-stu-id="7c9b3-168">Priority</span></span>
- <span data-ttu-id="7c9b3-169">Földrajzi</span><span class="sxs-lookup"><span data-stu-id="7c9b3-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-170">-TTL (TTL)</span><span class="sxs-lookup"><span data-stu-id="7c9b3-170">-Ttl</span></span>
<span data-ttu-id="7c9b3-171">A TTL (élettartam) beállítás értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-171">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9b3-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c9b3-172">CommonParameters</span></span>
<span data-ttu-id="7c9b3-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c9b3-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c9b3-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c9b3-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c9b3-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c9b3-175">INPUTS</span></span>

### <span data-ttu-id="7c9b3-176">Nincs</span><span class="sxs-lookup"><span data-stu-id="7c9b3-176">None</span></span>
<span data-ttu-id="7c9b3-177">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c9b3-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c9b3-178">OUTPUTS</span></span>

### <span data-ttu-id="7c9b3-179">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7c9b3-179">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="7c9b3-180">Ez a parancsmag új TrafficManagerProfile-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="7c9b3-180">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="7c9b3-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c9b3-181">NOTES</span></span>

## <span data-ttu-id="7c9b3-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c9b3-182">RELATED LINKS</span></span>

[<span data-ttu-id="7c9b3-183">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="7c9b3-183">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="7c9b3-184">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7c9b3-184">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7c9b3-185">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7c9b3-185">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7c9b3-186">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7c9b3-186">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7c9b3-187">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7c9b3-187">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7c9b3-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7c9b3-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


