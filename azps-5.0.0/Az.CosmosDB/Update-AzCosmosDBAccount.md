---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299105"
---
# <span data-ttu-id="10783-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="10783-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="10783-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10783-102">SYNOPSIS</span></span>
<span data-ttu-id="10783-103">CosmosDB-fiók attribútumainak frissítése</span><span class="sxs-lookup"><span data-stu-id="10783-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="10783-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10783-104">SYNTAX</span></span>

### <span data-ttu-id="10783-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10783-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10783-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10783-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10783-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10783-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10783-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="10783-108">DESCRIPTION</span></span>
<span data-ttu-id="10783-109">Frissítheti egy CosmosDB-fiók tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="10783-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="10783-110">Más tulajdonságokkal nem frissíthetők a simulataneously.</span><span class="sxs-lookup"><span data-stu-id="10783-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="10783-111">Példák</span><span class="sxs-lookup"><span data-stu-id="10783-111">EXAMPLES</span></span>

### <span data-ttu-id="10783-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="10783-112">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="10783-113">A DefaultConsistencyLevel frissítve: "Strong", engedélyezve van a AutomaticFailover, engedélyezve van a MultipleWriteLocations és a VirtualNetwork használata az CosmosDB-fiókhoz a név accountName.</span><span class="sxs-lookup"><span data-stu-id="10783-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="10783-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10783-114">PARAMETERS</span></span>

### <span data-ttu-id="10783-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10783-115">-AsJob</span></span>
<span data-ttu-id="10783-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="10783-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10783-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="10783-117">-Confirm</span></span>
<span data-ttu-id="10783-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="10783-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10783-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="10783-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="10783-120">A Cosmos DB adatbázis-fiók alapértelmezett egységességi szintje.</span><span class="sxs-lookup"><span data-stu-id="10783-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="10783-121">Elfogadott értékek: BoundedStaleness, ConsistentPrefix, lehetséges, munkamenet, erős</span><span class="sxs-lookup"><span data-stu-id="10783-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="10783-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10783-122">-DefaultProfile</span></span>
<span data-ttu-id="10783-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10783-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10783-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="10783-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="10783-125">Az írási műveletek letiltása a metaadat-erőforrásokban (adatbázisokban, tárolókban, adatforgalomban) a fiók kulcsain keresztül</span><span class="sxs-lookup"><span data-stu-id="10783-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="10783-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="10783-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="10783-127">Bool: annak jelzése, hogy engedélyezve van-e a AnalyticalStorage a fiókban.</span><span class="sxs-lookup"><span data-stu-id="10783-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="10783-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="10783-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="10783-129">Engedélyezi az írási tartomány automatikus feladatátvételét abban az esetben, ha a régió áramkimaradás miatt nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="10783-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="10783-130">Az automatikus feladatátvétel a fiók új írási területét fogja eredményezni, és a fiókhoz konfigurált feladatátvételi prioritások alapján lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="10783-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="10783-131">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="10783-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="10783-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="10783-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="10783-133">Több írási hely engedélyezése</span><span class="sxs-lookup"><span data-stu-id="10783-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="10783-134">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="10783-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="10783-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="10783-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="10783-136">Lehetővé teszi a virtuális hálózat számára a Cosmos DB adatbázis-fiókját.</span><span class="sxs-lookup"><span data-stu-id="10783-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="10783-137">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="10783-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="10783-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10783-138">-InputObject</span></span>
<span data-ttu-id="10783-139">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="10783-139">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10783-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="10783-140">-IpRule</span></span>
<span data-ttu-id="10783-141">Tűzfal támogatása</span><span class="sxs-lookup"><span data-stu-id="10783-141">Firewall support.</span></span> <span data-ttu-id="10783-142">Az CIDR űrlap IP-címeinek vagy IP-címeinek halmazát adja meg, hogy az adott adatbázis-fiókhoz tartozó ügyfél IP-címei engedélyezettek legyenek.</span><span class="sxs-lookup"><span data-stu-id="10783-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="10783-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="10783-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="10783-144">A beboltozatok URI-ja</span><span class="sxs-lookup"><span data-stu-id="10783-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="10783-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="10783-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="10783-146">Ha a kötött állandósági konzisztenciát használja, ez az érték azt jelzi, hogy mennyi idő áll fenn (a időszak-ban).</span><span class="sxs-lookup"><span data-stu-id="10783-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="10783-147">Az érték elfogadott köre az 5-86400.</span><span class="sxs-lookup"><span data-stu-id="10783-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="10783-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="10783-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="10783-149">Ha a kötött állandósági konzisztenciát használja, ez az érték a tolerált lejárt kérelmek számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="10783-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="10783-150">Az érték elfogadott köre 1 – 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="10783-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="10783-151">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="10783-151">-Name</span></span>
<span data-ttu-id="10783-152">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="10783-152">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10783-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="10783-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="10783-154">A kiszolgálón engedélyezve van-e a nyilvános végpontok elérése.</span><span class="sxs-lookup"><span data-stu-id="10783-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="10783-155">A lehetséges értékek a következők: "engedélyezve", "Letiltva"</span><span class="sxs-lookup"><span data-stu-id="10783-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="10783-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10783-156">-ResourceGroupName</span></span>
<span data-ttu-id="10783-157">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="10783-157">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10783-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10783-158">-ResourceId</span></span>
<span data-ttu-id="10783-159">Az erőforrás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="10783-159">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10783-160">-Címke</span><span class="sxs-lookup"><span data-stu-id="10783-160">-Tag</span></span>
<span data-ttu-id="10783-161">Hashtablea kulcs-érték párokként.</span><span class="sxs-lookup"><span data-stu-id="10783-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="10783-162">A meglévő címke törléséhez használjon üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="10783-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="10783-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="10783-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="10783-164">A virtuális hálózat ACL-értékeinek tömbje</span><span class="sxs-lookup"><span data-stu-id="10783-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="10783-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="10783-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="10783-166">A virtuális hálózat PSVirtualNetworkRuleObjects tömbje.</span><span class="sxs-lookup"><span data-stu-id="10783-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="10783-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10783-167">-WhatIf</span></span>
<span data-ttu-id="10783-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="10783-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10783-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10783-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10783-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10783-170">CommonParameters</span></span>
<span data-ttu-id="10783-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10783-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10783-172">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="10783-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10783-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10783-173">INPUTS</span></span>

### <span data-ttu-id="10783-174">Microsoft. Azure. Command. CosmosDB. models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="10783-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="10783-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10783-175">OUTPUTS</span></span>

### <span data-ttu-id="10783-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="10783-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="10783-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10783-177">NOTES</span></span>

## <span data-ttu-id="10783-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10783-178">RELATED LINKS</span></span>
