---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 76df37703882e799eb42542cd08d105f62787419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012565"
---
# <span data-ttu-id="9cc70-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="9cc70-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="9cc70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cc70-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc70-103">Hozzon létre egy új CosmosDB-fiókot.</span><span class="sxs-lookup"><span data-stu-id="9cc70-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="9cc70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cc70-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork] [-IpRangeFilter <String[]>]
 [-Location <String[]>] [-LocationObject <PSLocation[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-ApiKind <String>] [-PublicNetworkAccess <String>]
 [-DisableKeyBasedMetadataWriteAccess] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cc70-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cc70-105">DESCRIPTION</span></span>
<span data-ttu-id="9cc70-106">Hozzon létre egy új CosmosDB-fiókot az adott ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9cc70-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="9cc70-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9cc70-107">EXAMPLES</span></span>

### <span data-ttu-id="9cc70-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9cc70-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="9cc70-109">Új CosmosDB-fiók jön létre a databaseAccountName nevű ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="9cc70-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="9cc70-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cc70-110">PARAMETERS</span></span>

### <span data-ttu-id="9cc70-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="9cc70-111">-ApiKind</span></span>
<span data-ttu-id="9cc70-112">A létrehozandó Cosmos DB adatbázis-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="9cc70-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="9cc70-113">Elfogadott értékek: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="9cc70-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="9cc70-114">Alapértelmezett érték: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="9cc70-114">Default value: GlobalDocumentDB</span></span>

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

### <span data-ttu-id="9cc70-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cc70-115">-AsJob</span></span>
<span data-ttu-id="9cc70-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9cc70-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cc70-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9cc70-117">-Confirm</span></span>
<span data-ttu-id="9cc70-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9cc70-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc70-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="9cc70-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="9cc70-120">A Cosmos DB adatbázis-fiók alapértelmezett egységességi szintje.</span><span class="sxs-lookup"><span data-stu-id="9cc70-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="9cc70-121">Elfogadott értékek: BoundedStaleness, ConsistentPrefix, lehetséges, munkamenet, erős</span><span class="sxs-lookup"><span data-stu-id="9cc70-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="9cc70-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc70-122">-DefaultProfile</span></span>
<span data-ttu-id="9cc70-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cc70-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc70-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="9cc70-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="9cc70-125">Az írási műveletek letiltása a metaadat-erőforrásokban (adatbázisokban, tárolókban, adatforgalomban) a fiók kulcsain keresztül</span><span class="sxs-lookup"><span data-stu-id="9cc70-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="9cc70-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="9cc70-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="9cc70-127">Engedélyezi az írási tartomány automatikus feladatátvételét abban az esetben, ha a régió áramkimaradás miatt nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="9cc70-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="9cc70-128">Az automatikus feladatátvétel a fiók új írási területét fogja eredményezni, és a fiókhoz konfigurált feladatátvételi prioritások alapján lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="9cc70-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="9cc70-129">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="9cc70-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="9cc70-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="9cc70-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="9cc70-131">Több írási hely engedélyezése</span><span class="sxs-lookup"><span data-stu-id="9cc70-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="9cc70-132">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="9cc70-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="9cc70-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9cc70-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="9cc70-134">Lehetővé teszi a virtuális hálózat számára a Cosmos DB adatbázis-fiókját.</span><span class="sxs-lookup"><span data-stu-id="9cc70-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="9cc70-135">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="9cc70-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="9cc70-136">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="9cc70-136">-IpRangeFilter</span></span>
<span data-ttu-id="9cc70-137">Tűzfal támogatása</span><span class="sxs-lookup"><span data-stu-id="9cc70-137">Firewall support.</span></span>
<span data-ttu-id="9cc70-138">Az CIDR-űrlap IP-címeinek vagy IP-címeinek a halmazát adja meg, amely az adott adatbázis-fiókhoz tartozó ügyfél-IP-címek engedélyezett listájának része.</span><span class="sxs-lookup"><span data-stu-id="9cc70-138">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc70-139">-Hely</span><span class="sxs-lookup"><span data-stu-id="9cc70-139">-Location</span></span>
<span data-ttu-id="9cc70-140">Adjon meg egy helyet a Cosmos DB adatbázis-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="9cc70-140">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="9cc70-141">A feladatátvételi prioritás által rendezett karakterláncok tömbje</span><span class="sxs-lookup"><span data-stu-id="9cc70-141">Array of strings, ordered by failover priority.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc70-142">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="9cc70-142">-LocationObject</span></span>
<span data-ttu-id="9cc70-143">Adjon meg egy helyet a Cosmos DB adatbázis-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="9cc70-143">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="9cc70-144">PSLocation-objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="9cc70-144">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc70-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9cc70-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="9cc70-146">Ha a kötött állandósági konzisztenciát használja, ez az érték azt jelzi, hogy mennyi idő áll fenn (a időszak-ban).</span><span class="sxs-lookup"><span data-stu-id="9cc70-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="9cc70-147">Az érték elfogadott köre az 5-86400.</span><span class="sxs-lookup"><span data-stu-id="9cc70-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="9cc70-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="9cc70-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="9cc70-149">Ha a kötött állandósági konzisztenciát használja, ez az érték a tolerált lejárt kérelmek számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="9cc70-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="9cc70-150">Az érték elfogadott köre 1 – 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="9cc70-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="9cc70-151">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9cc70-151">-Name</span></span>
<span data-ttu-id="9cc70-152">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="9cc70-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9cc70-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="9cc70-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="9cc70-154">A kiszolgálón engedélyezve van-e a nyilvános végpontok elérése.</span><span class="sxs-lookup"><span data-stu-id="9cc70-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="9cc70-155">A lehetséges értékek a következők: "engedélyezve", "Letiltva"</span><span class="sxs-lookup"><span data-stu-id="9cc70-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="9cc70-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cc70-156">-ResourceGroupName</span></span>
<span data-ttu-id="9cc70-157">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9cc70-157">Name of resource group.</span></span>

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

### <span data-ttu-id="9cc70-158">-Címke</span><span class="sxs-lookup"><span data-stu-id="9cc70-158">-Tag</span></span>
<span data-ttu-id="9cc70-159">Hashtablea kulcs-érték párokként.</span><span class="sxs-lookup"><span data-stu-id="9cc70-159">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="9cc70-160">A meglévő címke törléséhez használjon üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="9cc70-160">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc70-161">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9cc70-161">-VirtualNetworkRule</span></span>
<span data-ttu-id="9cc70-162">A virtuális hálózat ACL-értékeinek tömbje</span><span class="sxs-lookup"><span data-stu-id="9cc70-162">Array of string values of ACL's for virtual network.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc70-163">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="9cc70-163">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="9cc70-164">A virtuális hálózat PSVirtualNetworkRuleObjects tömbje.</span><span class="sxs-lookup"><span data-stu-id="9cc70-164">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc70-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cc70-165">-WhatIf</span></span>
<span data-ttu-id="9cc70-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9cc70-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cc70-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9cc70-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc70-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc70-168">CommonParameters</span></span>
<span data-ttu-id="9cc70-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cc70-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc70-170">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9cc70-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc70-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cc70-171">INPUTS</span></span>

### <span data-ttu-id="9cc70-172">Microsoft. Azure. Command. CosmosDB. models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="9cc70-172">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="9cc70-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cc70-173">OUTPUTS</span></span>

### <span data-ttu-id="9cc70-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9cc70-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9cc70-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cc70-175">NOTES</span></span>

## <span data-ttu-id="9cc70-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cc70-176">RELATED LINKS</span></span>
