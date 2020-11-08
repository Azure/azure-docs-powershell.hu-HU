---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: f082f9390dd5a00fa5984aa2e0df26e8c3b63636
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025467"
---
# <span data-ttu-id="288b8-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="288b8-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="288b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="288b8-102">SYNOPSIS</span></span>
<span data-ttu-id="288b8-103">Hozzon létre egy új CosmosDB-fiókot.</span><span class="sxs-lookup"><span data-stu-id="288b8-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="288b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="288b8-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>]
 [-ServerVersion <String>] [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="288b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="288b8-105">DESCRIPTION</span></span>
<span data-ttu-id="288b8-106">Hozzon létre egy új CosmosDB-fiókot az adott ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="288b8-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="288b8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="288b8-107">EXAMPLES</span></span>

### <span data-ttu-id="288b8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="288b8-108">Example 1</span></span>
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

<span data-ttu-id="288b8-109">Új CosmosDB-fiók jön létre a databaseAccountName nevű ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="288b8-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="288b8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="288b8-110">PARAMETERS</span></span>

### <span data-ttu-id="288b8-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="288b8-111">-ApiKind</span></span>
<span data-ttu-id="288b8-112">A létrehozandó Cosmos DB adatbázis-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="288b8-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="288b8-113">Elfogadott értékek: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="288b8-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="288b8-114">Alapértelmezett érték: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="288b8-114">Default value: GlobalDocumentDB</span></span>

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

### <span data-ttu-id="288b8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="288b8-115">-AsJob</span></span>
<span data-ttu-id="288b8-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="288b8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="288b8-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="288b8-117">-Confirm</span></span>
<span data-ttu-id="288b8-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="288b8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="288b8-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="288b8-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="288b8-120">A Cosmos DB adatbázis-fiók alapértelmezett egységességi szintje.</span><span class="sxs-lookup"><span data-stu-id="288b8-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="288b8-121">Elfogadott értékek: BoundedStaleness, ConsistentPrefix, lehetséges, munkamenet, erős</span><span class="sxs-lookup"><span data-stu-id="288b8-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="288b8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288b8-122">-DefaultProfile</span></span>
<span data-ttu-id="288b8-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="288b8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="288b8-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="288b8-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="288b8-125">Az írási műveletek letiltása a metaadat-erőforrásokban (adatbázisokban, tárolókban, adatforgalomban) a fiók kulcsain keresztül</span><span class="sxs-lookup"><span data-stu-id="288b8-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="288b8-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="288b8-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="288b8-127">Bool: annak jelzése, hogy engedélyezve van-e a AnalyticalStorage a fiókban.</span><span class="sxs-lookup"><span data-stu-id="288b8-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="288b8-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="288b8-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="288b8-129">Engedélyezi az írási tartomány automatikus feladatátvételét abban az esetben, ha a régió áramkimaradás miatt nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="288b8-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="288b8-130">Az automatikus feladatátvétel a fiók új írási területét fogja eredményezni, és a fiókhoz konfigurált feladatátvételi prioritások alapján lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="288b8-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="288b8-131">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="288b8-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="288b8-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="288b8-132">-EnableFreeTier</span></span>
<span data-ttu-id="288b8-133">Bool: annak jelzése, hogy engedélyezve van-e a FreeTier a fiókban.</span><span class="sxs-lookup"><span data-stu-id="288b8-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="288b8-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="288b8-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="288b8-135">Több írási hely engedélyezése</span><span class="sxs-lookup"><span data-stu-id="288b8-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="288b8-136">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="288b8-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="288b8-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="288b8-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="288b8-138">Lehetővé teszi a virtuális hálózat számára a Cosmos DB adatbázis-fiókját.</span><span class="sxs-lookup"><span data-stu-id="288b8-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="288b8-139">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="288b8-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="288b8-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="288b8-140">-IpRule</span></span>
<span data-ttu-id="288b8-141">Tűzfal támogatása</span><span class="sxs-lookup"><span data-stu-id="288b8-141">Firewall support.</span></span> <span data-ttu-id="288b8-142">Az CIDR űrlap IP-címeinek vagy IP-címeinek halmazát adja meg, hogy az adott adatbázis-fiókhoz tartozó ügyfél IP-címei engedélyezettek legyenek.</span><span class="sxs-lookup"><span data-stu-id="288b8-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="288b8-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="288b8-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="288b8-144">A beboltozatok URI-ja</span><span class="sxs-lookup"><span data-stu-id="288b8-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="288b8-145">-Hely</span><span class="sxs-lookup"><span data-stu-id="288b8-145">-Location</span></span>
<span data-ttu-id="288b8-146">Adjon meg egy helyet a Cosmos DB adatbázis-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="288b8-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="288b8-147">A feladatátvételi prioritás által rendezett karakterláncok tömbje</span><span class="sxs-lookup"><span data-stu-id="288b8-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="288b8-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="288b8-148">-LocationObject</span></span>
<span data-ttu-id="288b8-149">Adjon meg egy helyet a Cosmos DB adatbázis-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="288b8-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="288b8-150">PSLocation-objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="288b8-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="288b8-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="288b8-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="288b8-152">Ha a kötött állandósági konzisztenciát használja, ez az érték azt jelzi, hogy mennyi idő áll fenn (a időszak-ban).</span><span class="sxs-lookup"><span data-stu-id="288b8-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="288b8-153">Az érték elfogadott köre az 5-86400.</span><span class="sxs-lookup"><span data-stu-id="288b8-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="288b8-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="288b8-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="288b8-155">Ha a kötött állandósági konzisztenciát használja, ez az érték a tolerált lejárt kérelmek számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="288b8-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="288b8-156">Az érték elfogadott köre 1 – 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="288b8-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="288b8-157">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="288b8-157">-Name</span></span>
<span data-ttu-id="288b8-158">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="288b8-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="288b8-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="288b8-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="288b8-160">A kiszolgálón engedélyezve van-e a nyilvános végpontok elérése.</span><span class="sxs-lookup"><span data-stu-id="288b8-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="288b8-161">A lehetséges értékek a következők: "engedélyezve", "Letiltva"</span><span class="sxs-lookup"><span data-stu-id="288b8-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="288b8-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288b8-162">-ResourceGroupName</span></span>
<span data-ttu-id="288b8-163">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="288b8-163">Name of resource group.</span></span>

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

### <span data-ttu-id="288b8-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="288b8-164">-ServerVersion</span></span>
<span data-ttu-id="288b8-165">ServerVersion, érvényes csak MongoDB-fiókok esetén.</span><span class="sxs-lookup"><span data-stu-id="288b8-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="288b8-166">-Címke</span><span class="sxs-lookup"><span data-stu-id="288b8-166">-Tag</span></span>
<span data-ttu-id="288b8-167">Hashtablea kulcs-érték párokként.</span><span class="sxs-lookup"><span data-stu-id="288b8-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="288b8-168">A meglévő címke törléséhez használjon üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="288b8-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="288b8-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="288b8-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="288b8-170">A virtuális hálózat ACL-értékeinek tömbje</span><span class="sxs-lookup"><span data-stu-id="288b8-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="288b8-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="288b8-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="288b8-172">A virtuális hálózat PSVirtualNetworkRuleObjects tömbje.</span><span class="sxs-lookup"><span data-stu-id="288b8-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="288b8-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="288b8-173">-WhatIf</span></span>
<span data-ttu-id="288b8-174">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="288b8-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="288b8-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="288b8-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="288b8-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288b8-176">CommonParameters</span></span>
<span data-ttu-id="288b8-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="288b8-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288b8-178">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="288b8-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288b8-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="288b8-179">INPUTS</span></span>

### <span data-ttu-id="288b8-180">Microsoft. Azure. Command. CosmosDB. models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="288b8-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="288b8-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="288b8-181">OUTPUTS</span></span>

### <span data-ttu-id="288b8-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="288b8-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="288b8-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="288b8-183">NOTES</span></span>

## <span data-ttu-id="288b8-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="288b8-184">RELATED LINKS</span></span>
