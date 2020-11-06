---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 896324e8d08cae69f24c195de9b44b325985c2c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495220"
---
# <span data-ttu-id="a3f0f-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3f0f-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="a3f0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f0f-103">Forgalomirányító-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3f0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3f0f-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3f0f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f0f-106">A **New-AzureRmTrafficManagerProfile** parancsmag egy Azure Traffic Manager-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="a3f0f-107">Adja meg a *Name* paramétert és a szükséges beállításokat.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="a3f0f-108">Ez a parancsmag egy olyan helyi objektumot ad eredményül, amely az új profilt jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="a3f0f-109">Ez a parancsmag nem állítja be a forgalomirányítási végpontokat.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="a3f0f-110">A helyi profil objektum a Add-AzureRmTrafficManagerEndpointConfig parancsmag segítségével frissíthető.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="a3f0f-111">Ezután töltse fel a Traffic Manager módosításait a Set-AzureRmTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="a3f0f-112">Másik lehetőségként az New-AzureRmTrafficManagerEndpoint parancsmag használatával is hozzáadhat végpontokat.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="a3f0f-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a3f0f-113">EXAMPLES</span></span>

### <span data-ttu-id="a3f0f-114">Példa 1: profil létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3f0f-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="a3f0f-115">Ez a parancs létrehoz egy ContosoProfile nevű Azure Traffic Manager-profilt az erőforráscsoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="a3f0f-116">A DNS FQDN a contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="a3f0f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3f0f-117">PARAMETERS</span></span>

### <span data-ttu-id="a3f0f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f0f-118">-DefaultProfile</span></span>
<span data-ttu-id="a3f0f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3f0f-120">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a3f0f-120">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="a3f0f-121">Annak az intervallumnak (másodpercben), amelyen a forgalmi vezető a profil minden végpontjának állapotát ellenőrizni fogja.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-121">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="a3f0f-122">Az alapértelmezett érték 30.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-122">The default is 30.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f0f-123">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="a3f0f-123">-MonitorPath</span></span>
<span data-ttu-id="a3f0f-124">A végpontok állapotának figyeléséhez használt elérési utat adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-124">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="a3f0f-125">Adjon meg egy értéket a végpont tartománynevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-125">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="a3f0f-126">Ennek az értéknek perjelet (/) kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-126">This value must begin with a slash (/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f0f-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="a3f0f-127">-MonitorPort</span></span>
<span data-ttu-id="a3f0f-128">Azt a TCP-portot adja meg, amely a végpontok állapotának figyeléséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-128">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="a3f0f-129">Az érvényes értékek 1 és 65535 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-129">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f0f-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="a3f0f-130">-MonitorProtocol</span></span>
<span data-ttu-id="a3f0f-131">A végpontok állapotának figyeléséhez használható protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="a3f0f-132">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="a3f0f-132">Valid values are:</span></span>

- <span data-ttu-id="a3f0f-133">HTTP</span><span class="sxs-lookup"><span data-stu-id="a3f0f-133">HTTP</span></span>
- <span data-ttu-id="a3f0f-134">HTTPS</span><span class="sxs-lookup"><span data-stu-id="a3f0f-134">HTTPS</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f0f-135">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="a3f0f-135">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="a3f0f-136">A forgalmi vezető időpontja (másodpercben) lehetővé teszi, hogy az ebben a profilban szereplő végpontok megválaszolják az állapot-ellenőrzést.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-136">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="a3f0f-137">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-137">The default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f0f-138">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="a3f0f-138">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="a3f0f-139">Az egymást követő sikertelen állapot-ellenőrzések száma, amelyeket a Traffic Manager a következő egymást követő sikertelen állapot-ellenőrzés után a következő egymást követő sikertelen állapot ellenőrzése után tolerálja.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-139">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="a3f0f-140">Az alapértelmezett érték a 3.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-140">The default is 3.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f0f-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3f0f-141">-Name</span></span>
<span data-ttu-id="a3f0f-142">A parancsmag által létrehozott Traffic Manager-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-142">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a3f0f-143">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="a3f0f-143">-ProfileStatus</span></span>
<span data-ttu-id="a3f0f-144">A profil állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-144">Specifies the status of the profile.</span></span>
<span data-ttu-id="a3f0f-145">Az érvényes értékek: engedélyezve és letiltva.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-145">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f0f-146">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="a3f0f-146">-RelativeDnsName</span></span>
<span data-ttu-id="a3f0f-147">Azt a relatív DNS-nevet adja meg, amelyre ez a forgalomirányító-profil nyújt.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-147">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="a3f0f-148">A Traffic Manager kombinálja ezt az értéket és azt a DNS-tartománynevet, amelyet az Azure Traffic Manager a profil teljes tartománynevét (FQDN) alkot.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-148">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="a3f0f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3f0f-149">-ResourceGroupName</span></span>
<span data-ttu-id="a3f0f-150">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a3f0f-151">Ez a parancsmag létrehoz egy Traffic Manager-profilt abban a csoportban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-151">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3f0f-152">-Címke</span><span class="sxs-lookup"><span data-stu-id="a3f0f-152">-Tag</span></span>
<span data-ttu-id="a3f0f-153">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-153">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="a3f0f-154">Példa:</span><span class="sxs-lookup"><span data-stu-id="a3f0f-154">For example:</span></span>

<span data-ttu-id="a3f0f-155">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="a3f0f-155">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f0f-156">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="a3f0f-156">-TrafficRoutingMethod</span></span>
<span data-ttu-id="a3f0f-157">A forgalmi útválasztási módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-157">Specifies the traffic routing method.</span></span>
<span data-ttu-id="a3f0f-158">Ez a módszer azt határozza meg, hogy a végpont-forgalmi vezető milyen válaszokat ad a bejövő DNS-lekérdezésekre válaszul.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-158">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="a3f0f-159">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="a3f0f-159">Valid values are:</span></span>

- <span data-ttu-id="a3f0f-160">Teljesítmény</span><span class="sxs-lookup"><span data-stu-id="a3f0f-160">Performance</span></span>
- <span data-ttu-id="a3f0f-161">Súlyozott</span><span class="sxs-lookup"><span data-stu-id="a3f0f-161">Weighted</span></span>
- <span data-ttu-id="a3f0f-162">Prioritás</span><span class="sxs-lookup"><span data-stu-id="a3f0f-162">Priority</span></span>
- <span data-ttu-id="a3f0f-163">Földrajzi</span><span class="sxs-lookup"><span data-stu-id="a3f0f-163">Geographic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f0f-164">-TTL (TTL)</span><span class="sxs-lookup"><span data-stu-id="a3f0f-164">-Ttl</span></span>
<span data-ttu-id="a3f0f-165">A TTL (élettartam) beállítás értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-165">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f0f-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f0f-166">CommonParameters</span></span>
<span data-ttu-id="a3f0f-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3f0f-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f0f-168">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3f0f-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f0f-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3f0f-169">INPUTS</span></span>

### <span data-ttu-id="a3f0f-170">Nincs</span><span class="sxs-lookup"><span data-stu-id="a3f0f-170">None</span></span>
<span data-ttu-id="a3f0f-171">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3f0f-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3f0f-172">OUTPUTS</span></span>

### <span data-ttu-id="a3f0f-173">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3f0f-173">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="a3f0f-174">Ez a parancsmag új TrafficManagerProfile-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="a3f0f-174">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="a3f0f-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3f0f-175">NOTES</span></span>

## <span data-ttu-id="a3f0f-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3f0f-176">RELATED LINKS</span></span>

[<span data-ttu-id="a3f0f-177">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="a3f0f-177">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="a3f0f-178">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3f0f-178">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a3f0f-179">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3f0f-179">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a3f0f-180">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3f0f-180">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a3f0f-181">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3f0f-181">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a3f0f-182">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3f0f-182">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


