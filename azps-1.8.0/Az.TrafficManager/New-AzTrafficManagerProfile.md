---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: aed780d75280f38ba8fa99052c3af0cd8bbe9612
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668401"
---
# <span data-ttu-id="88600-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="88600-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="88600-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88600-102">SYNOPSIS</span></span>
<span data-ttu-id="88600-103">Forgalomirányító-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="88600-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="88600-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88600-104">SYNTAX</span></span>

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88600-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="88600-105">DESCRIPTION</span></span>
<span data-ttu-id="88600-106">A **New-AzTrafficManagerProfile** parancsmag egy Azure Traffic Manager-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="88600-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="88600-107">Adja meg a *Name* paramétert és a szükséges beállításokat.</span><span class="sxs-lookup"><span data-stu-id="88600-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="88600-108">Ez a parancsmag egy olyan helyi objektumot ad eredményül, amely az új profilt jelképezi.</span><span class="sxs-lookup"><span data-stu-id="88600-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="88600-109">Ez a parancsmag nem állítja be a forgalomirányítási végpontokat.</span><span class="sxs-lookup"><span data-stu-id="88600-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="88600-110">A helyi profil objektum a Add-AzTrafficManagerEndpointConfig parancsmag segítségével frissíthető.</span><span class="sxs-lookup"><span data-stu-id="88600-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="88600-111">Ezután töltse fel a Traffic Manager módosításait a Set-AzTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="88600-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="88600-112">Másik lehetőségként az New-AzTrafficManagerEndpoint parancsmag használatával is hozzáadhat végpontokat.</span><span class="sxs-lookup"><span data-stu-id="88600-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="88600-113">Példák</span><span class="sxs-lookup"><span data-stu-id="88600-113">EXAMPLES</span></span>

### <span data-ttu-id="88600-114">Példa 1: profil létrehozása</span><span class="sxs-lookup"><span data-stu-id="88600-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="88600-115">Ez a parancs létrehoz egy ContosoProfile nevű Azure Traffic Manager-profilt az erőforráscsoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="88600-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="88600-116">A DNS FQDN a contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="88600-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="88600-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88600-117">PARAMETERS</span></span>

### <span data-ttu-id="88600-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="88600-118">-CustomHeader</span></span>
<span data-ttu-id="88600-119">Az egyéni élőfej neve és az érték párok listája a szonda-kérésekhez.</span><span class="sxs-lookup"><span data-stu-id="88600-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="88600-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88600-120">-DefaultProfile</span></span>
<span data-ttu-id="88600-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88600-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88600-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="88600-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="88600-123">A szonda-kérelmek várható HTTP-állapotkódot tartalmazó tartományai.</span><span class="sxs-lookup"><span data-stu-id="88600-123">List of expected HTTP status code ranges for probe requests.</span></span>

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

### <span data-ttu-id="88600-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="88600-124">-MaxReturn</span></span>
<span data-ttu-id="88600-125">A profilokhoz a többértékű útválasztási módszerrel kapott válaszok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="88600-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

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

### <span data-ttu-id="88600-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="88600-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="88600-127">Annak az intervallumnak (másodpercben), amelyen a forgalmi vezető a profil minden végpontjának állapotát ellenőrizni fogja.</span><span class="sxs-lookup"><span data-stu-id="88600-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="88600-128">Az alapértelmezett érték 30.</span><span class="sxs-lookup"><span data-stu-id="88600-128">The default is 30.</span></span>

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

### <span data-ttu-id="88600-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="88600-129">-MonitorPath</span></span>
<span data-ttu-id="88600-130">A végpontok állapotának figyeléséhez használt elérési utat adja meg.</span><span class="sxs-lookup"><span data-stu-id="88600-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="88600-131">Adjon meg egy értéket a végpont tartománynevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="88600-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="88600-132">Ennek az értéknek perjelet (/) kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="88600-132">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="88600-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="88600-133">-MonitorPort</span></span>
<span data-ttu-id="88600-134">Azt a TCP-portot adja meg, amely a végpontok állapotának figyeléséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="88600-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="88600-135">Az érvényes értékek 1 és 65535 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="88600-135">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="88600-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="88600-136">-MonitorProtocol</span></span>
<span data-ttu-id="88600-137">A végpontok állapotának figyeléséhez használható protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="88600-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="88600-138">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="88600-138">Valid values are:</span></span>

- <span data-ttu-id="88600-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="88600-139">HTTP</span></span>
- <span data-ttu-id="88600-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="88600-140">HTTPS</span></span>

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

### <span data-ttu-id="88600-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="88600-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="88600-142">A forgalmi vezető időpontja (másodpercben) lehetővé teszi, hogy az ebben a profilban szereplő végpontok megválaszolják az állapot-ellenőrzést.</span><span class="sxs-lookup"><span data-stu-id="88600-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="88600-143">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="88600-143">The default is 10.</span></span>

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

### <span data-ttu-id="88600-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="88600-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="88600-145">Az egymást követő sikertelen állapot-ellenőrzések száma, amelyeket a Traffic Manager a következő egymást követő sikertelen állapot-ellenőrzés után a következő egymást követő sikertelen állapot ellenőrzése után tolerálja.</span><span class="sxs-lookup"><span data-stu-id="88600-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="88600-146">Az alapértelmezett érték a 3.</span><span class="sxs-lookup"><span data-stu-id="88600-146">The default is 3.</span></span>

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

### <span data-ttu-id="88600-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88600-147">-Name</span></span>
<span data-ttu-id="88600-148">A parancsmag által létrehozott Traffic Manager-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88600-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="88600-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="88600-149">-ProfileStatus</span></span>
<span data-ttu-id="88600-150">A profil állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="88600-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="88600-151">Az érvényes értékek: engedélyezve és letiltva.</span><span class="sxs-lookup"><span data-stu-id="88600-151">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="88600-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="88600-152">-RelativeDnsName</span></span>
<span data-ttu-id="88600-153">Azt a relatív DNS-nevet adja meg, amelyre ez a forgalomirányító-profil nyújt.</span><span class="sxs-lookup"><span data-stu-id="88600-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="88600-154">A Traffic Manager kombinálja ezt az értéket és azt a DNS-tartománynevet, amelyet az Azure Traffic Manager a profil teljes tartománynevét (FQDN) alkot.</span><span class="sxs-lookup"><span data-stu-id="88600-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="88600-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88600-155">-ResourceGroupName</span></span>
<span data-ttu-id="88600-156">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88600-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="88600-157">Ez a parancsmag létrehoz egy Traffic Manager-profilt abban a csoportban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="88600-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="88600-158">-Címke</span><span class="sxs-lookup"><span data-stu-id="88600-158">-Tag</span></span>
<span data-ttu-id="88600-159">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="88600-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="88600-160">Példa:</span><span class="sxs-lookup"><span data-stu-id="88600-160">For example:</span></span>

<span data-ttu-id="88600-161">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="88600-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="88600-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="88600-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="88600-163">A forgalmi útválasztási módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="88600-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="88600-164">Ez a módszer azt határozza meg, hogy a végpont-forgalmi vezető milyen válaszokat ad a bejövő DNS-lekérdezésekre válaszul.</span><span class="sxs-lookup"><span data-stu-id="88600-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="88600-165">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="88600-165">Valid values are:</span></span>

- <span data-ttu-id="88600-166">Teljesítmény</span><span class="sxs-lookup"><span data-stu-id="88600-166">Performance</span></span>
- <span data-ttu-id="88600-167">Súlyozott</span><span class="sxs-lookup"><span data-stu-id="88600-167">Weighted</span></span>
- <span data-ttu-id="88600-168">Prioritás</span><span class="sxs-lookup"><span data-stu-id="88600-168">Priority</span></span>
- <span data-ttu-id="88600-169">Földrajzi</span><span class="sxs-lookup"><span data-stu-id="88600-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88600-170">-TTL (TTL)</span><span class="sxs-lookup"><span data-stu-id="88600-170">-Ttl</span></span>
<span data-ttu-id="88600-171">A TTL (élettartam) beállítás értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88600-171">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="88600-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88600-172">CommonParameters</span></span>
<span data-ttu-id="88600-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88600-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88600-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88600-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88600-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88600-175">INPUTS</span></span>

### <span data-ttu-id="88600-176">Nincs</span><span class="sxs-lookup"><span data-stu-id="88600-176">None</span></span>

## <span data-ttu-id="88600-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88600-177">OUTPUTS</span></span>

### <span data-ttu-id="88600-178">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="88600-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="88600-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88600-179">NOTES</span></span>

## <span data-ttu-id="88600-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88600-180">RELATED LINKS</span></span>

[<span data-ttu-id="88600-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="88600-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="88600-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="88600-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="88600-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="88600-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="88600-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="88600-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="88600-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="88600-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="88600-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="88600-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


