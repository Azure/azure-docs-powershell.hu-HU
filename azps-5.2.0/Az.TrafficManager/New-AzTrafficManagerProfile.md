---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: c5e1f69e8a11f09e4f7b838c5e489c8a240d40e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330462"
---
# <span data-ttu-id="6fd64-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6fd64-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="6fd64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fd64-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd64-103">Létrehoz egy Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="6fd64-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="6fd64-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6fd64-104">SYNTAX</span></span>

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

## <span data-ttu-id="6fd64-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6fd64-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd64-106">A **New-AzTrafficManagerProfile parancsmag** létrehoz egy Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="6fd64-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="6fd64-107">Adja meg *a Name paramétert* és a kötelező beállításokat.</span><span class="sxs-lookup"><span data-stu-id="6fd64-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="6fd64-108">Ez a parancsmag egy helyi objektumot ad vissza, amely az új profilt képviseli.</span><span class="sxs-lookup"><span data-stu-id="6fd64-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="6fd64-109">Ez a parancsmag nem konfigurálja a Traffic Manager-végpontokat.</span><span class="sxs-lookup"><span data-stu-id="6fd64-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="6fd64-110">A helyi profilobjektumot frissítheti a Add-AzTrafficManagerEndpointConfig parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="6fd64-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="6fd64-111">Ezután töltse fel a változásokat a Traffic Managerbe a Set-AzTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="6fd64-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="6fd64-112">Másik lehetőségként végpontokat is hozzáadhat a New-AzTrafficManagerEndpoint parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="6fd64-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="6fd64-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6fd64-113">EXAMPLES</span></span>

### <span data-ttu-id="6fd64-114">1. példa: Profil létrehozása</span><span class="sxs-lookup"><span data-stu-id="6fd64-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="6fd64-115">Ez a parancs létrehoz egy ContosoProfile nevű Azure Traffic Manager-profilt az Erőforráscsoport11 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="6fd64-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="6fd64-116">A DNS teljes tartománynevét (FQDN) contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="6fd64-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="6fd64-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fd64-117">PARAMETERS</span></span>

### <span data-ttu-id="6fd64-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="6fd64-118">-CustomHeader</span></span>
<span data-ttu-id="6fd64-119">Egyéni fejlécnév és értékpárok listája a kérések igényléséhez.</span><span class="sxs-lookup"><span data-stu-id="6fd64-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="6fd64-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd64-120">-DefaultProfile</span></span>
<span data-ttu-id="6fd64-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6fd64-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fd64-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="6fd64-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="6fd64-123">A kérések várható HTTP-állapotkód-tartományai.</span><span class="sxs-lookup"><span data-stu-id="6fd64-123">List of expected HTTP status code ranges for probe requests.</span></span>

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

### <span data-ttu-id="6fd64-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="6fd64-124">-MaxReturn</span></span>
<span data-ttu-id="6fd64-125">A többértékű útválasztási módszerrel használt profilokra adott válaszok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="6fd64-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

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

### <span data-ttu-id="6fd64-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6fd64-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="6fd64-127">Az az intervallum (másodpercben), amikor a Traffic Manager ellenőrzi a profil egyes végpontjainak állapotát.</span><span class="sxs-lookup"><span data-stu-id="6fd64-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="6fd64-128">Az alapértelmezett érték 30.</span><span class="sxs-lookup"><span data-stu-id="6fd64-128">The default is 30.</span></span>

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

### <span data-ttu-id="6fd64-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="6fd64-129">-MonitorPath</span></span>
<span data-ttu-id="6fd64-130">A végpont állapotának figyelése használt elérési út.</span><span class="sxs-lookup"><span data-stu-id="6fd64-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="6fd64-131">Adjon meg egy értéket a végpont tartománynevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="6fd64-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="6fd64-132">Ennek az értéknek perjellel (/) kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="6fd64-132">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="6fd64-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="6fd64-133">-MonitorPort</span></span>
<span data-ttu-id="6fd64-134">A végpontok állapotának figyelése érdekében használt TCP-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fd64-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="6fd64-135">Az érvényes értékek az 1 és 65535 között egész értékek.</span><span class="sxs-lookup"><span data-stu-id="6fd64-135">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="6fd64-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="6fd64-136">-MonitorProtocol</span></span>
<span data-ttu-id="6fd64-137">A végpont állapotának figyelése érdekében használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fd64-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="6fd64-138">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="6fd64-138">Valid values are:</span></span>

- <span data-ttu-id="6fd64-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="6fd64-139">HTTP</span></span>
- <span data-ttu-id="6fd64-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="6fd64-140">HTTPS</span></span>

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

### <span data-ttu-id="6fd64-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="6fd64-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="6fd64-142">Az az idő (másodpercben), amikor a Traffic Manager engedélyezi a profil végpontjainak, hogy válaszoljanak az állapot-ellenőrzésre.</span><span class="sxs-lookup"><span data-stu-id="6fd64-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="6fd64-143">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="6fd64-143">The default is 10.</span></span>

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

### <span data-ttu-id="6fd64-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="6fd64-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="6fd64-145">Az egymást követő sikertelen állapot-ellenőrzések száma, amit a Forgalomkezelő a profil végpontjának deklarálása előtt leépül, a következő sikertelen állapot-ellenőrzés után.</span><span class="sxs-lookup"><span data-stu-id="6fd64-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="6fd64-146">Az alapértelmezett érték 3.</span><span class="sxs-lookup"><span data-stu-id="6fd64-146">The default is 3.</span></span>

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

### <span data-ttu-id="6fd64-147">-Name</span><span class="sxs-lookup"><span data-stu-id="6fd64-147">-Name</span></span>
<span data-ttu-id="6fd64-148">A parancsmag által létrehozott Traffic Manager-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fd64-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6fd64-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="6fd64-149">-ProfileStatus</span></span>
<span data-ttu-id="6fd64-150">A profil állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fd64-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="6fd64-151">Érvényes értékek: Engedélyezve és Letiltva.</span><span class="sxs-lookup"><span data-stu-id="6fd64-151">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="6fd64-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="6fd64-152">-RelativeDnsName</span></span>
<span data-ttu-id="6fd64-153">Megadja a Traffic Manager-profil relatív DNS-nevét.</span><span class="sxs-lookup"><span data-stu-id="6fd64-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="6fd64-154">A Traffic Manager egyesíti ezt az értéket és azt a DNS-tartománynevet, amely alapján az Azure Traffic Manager a profil teljes tartománynevét (FQDN) használja.</span><span class="sxs-lookup"><span data-stu-id="6fd64-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="6fd64-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd64-155">-ResourceGroupName</span></span>
<span data-ttu-id="6fd64-156">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fd64-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6fd64-157">Ez a parancsmag létrehoz egy Traffic Manager-profilt a paraméter által megadott csoportban.</span><span class="sxs-lookup"><span data-stu-id="6fd64-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6fd64-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="6fd64-158">-Tag</span></span>
<span data-ttu-id="6fd64-159">Kulcsérték-párok a kiszolgálón címkékként beállított kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="6fd64-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="6fd64-160">Például:</span><span class="sxs-lookup"><span data-stu-id="6fd64-160">For example:</span></span>

<span data-ttu-id="6fd64-161">@{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="6fd64-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6fd64-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="6fd64-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="6fd64-163">A forgalom útválasztási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fd64-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="6fd64-164">Ez a módszer határozza meg, hogy a Traffic Manager melyik végpontot adja vissza a bejövő DNS-lekérdezések válaszában.</span><span class="sxs-lookup"><span data-stu-id="6fd64-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="6fd64-165">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="6fd64-165">Valid values are:</span></span>

- <span data-ttu-id="6fd64-166">Teljesítmény</span><span class="sxs-lookup"><span data-stu-id="6fd64-166">Performance</span></span>
- <span data-ttu-id="6fd64-167">Súlyozott</span><span class="sxs-lookup"><span data-stu-id="6fd64-167">Weighted</span></span>
- <span data-ttu-id="6fd64-168">Prioritás</span><span class="sxs-lookup"><span data-stu-id="6fd64-168">Priority</span></span>
- <span data-ttu-id="6fd64-169">Földrajzi</span><span class="sxs-lookup"><span data-stu-id="6fd64-169">Geographic</span></span>

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

### <span data-ttu-id="6fd64-170">-Ttl</span><span class="sxs-lookup"><span data-stu-id="6fd64-170">-Ttl</span></span>
<span data-ttu-id="6fd64-171">A DNS Time to Live (TTL) értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fd64-171">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="6fd64-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd64-172">CommonParameters</span></span>
<span data-ttu-id="6fd64-173">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd64-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd64-174">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd64-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd64-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fd64-175">INPUTS</span></span>

### <span data-ttu-id="6fd64-176">Nincs</span><span class="sxs-lookup"><span data-stu-id="6fd64-176">None</span></span>

## <span data-ttu-id="6fd64-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fd64-177">OUTPUTS</span></span>

### <span data-ttu-id="6fd64-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6fd64-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="6fd64-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6fd64-179">NOTES</span></span>

## <span data-ttu-id="6fd64-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fd64-180">RELATED LINKS</span></span>

[<span data-ttu-id="6fd64-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6fd64-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="6fd64-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6fd64-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="6fd64-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6fd64-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="6fd64-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6fd64-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="6fd64-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6fd64-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="6fd64-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6fd64-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


