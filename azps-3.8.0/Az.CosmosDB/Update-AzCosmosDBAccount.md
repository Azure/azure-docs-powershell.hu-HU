---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: a31df71a1242f4f4e9eb01a37d31eb54ec874a99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010552"
---
# <span data-ttu-id="98f33-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="98f33-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="98f33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98f33-102">SYNOPSIS</span></span>
<span data-ttu-id="98f33-103">CosmosDB-fiók attribútumainak frissítése</span><span class="sxs-lookup"><span data-stu-id="98f33-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="98f33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98f33-104">SYNTAX</span></span>

### <span data-ttu-id="98f33-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98f33-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98f33-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98f33-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98f33-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98f33-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98f33-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="98f33-108">DESCRIPTION</span></span>
<span data-ttu-id="98f33-109">Frissítheti egy CosmosDB-fiók tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="98f33-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="98f33-110">Más tulajdonságokkal nem frissíthetők a simulataneously.</span><span class="sxs-lookup"><span data-stu-id="98f33-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="98f33-111">Példák</span><span class="sxs-lookup"><span data-stu-id="98f33-111">EXAMPLES</span></span>

### <span data-ttu-id="98f33-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="98f33-112">Example 1</span></span>
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

<span data-ttu-id="98f33-113">A DefaultConsistencyLevel frissítve: "Strong", engedélyezve van a AutomaticFailover, engedélyezve van a MultipleWriteLocations és a VirtualNetwork használata az CosmosDB-fiókhoz a név accountName.</span><span class="sxs-lookup"><span data-stu-id="98f33-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="98f33-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98f33-114">PARAMETERS</span></span>

### <span data-ttu-id="98f33-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98f33-115">-AsJob</span></span>
<span data-ttu-id="98f33-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="98f33-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98f33-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98f33-117">-Confirm</span></span>
<span data-ttu-id="98f33-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98f33-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f33-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="98f33-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="98f33-120">A Cosmos DB adatbázis-fiók alapértelmezett egységességi szintje.</span><span class="sxs-lookup"><span data-stu-id="98f33-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="98f33-121">Elfogadott értékek: BoundedStaleness, ConsistentPrefix, lehetséges, munkamenet, erős</span><span class="sxs-lookup"><span data-stu-id="98f33-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="98f33-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f33-122">-DefaultProfile</span></span>
<span data-ttu-id="98f33-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98f33-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f33-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="98f33-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="98f33-125">Az írási műveletek letiltása a metaadat-erőforrásokban (adatbázisokban, tárolókban, adatforgalomban) a fiók kulcsain keresztül</span><span class="sxs-lookup"><span data-stu-id="98f33-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="98f33-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="98f33-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="98f33-127">Engedélyezi az írási tartomány automatikus feladatátvételét abban az esetben, ha a régió áramkimaradás miatt nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="98f33-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="98f33-128">Az automatikus feladatátvétel a fiók új írási területét fogja eredményezni, és a fiókhoz konfigurált feladatátvételi prioritások alapján lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="98f33-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="98f33-129">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="98f33-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="98f33-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="98f33-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="98f33-131">Több írási hely engedélyezése</span><span class="sxs-lookup"><span data-stu-id="98f33-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="98f33-132">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="98f33-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="98f33-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="98f33-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="98f33-134">Lehetővé teszi a virtuális hálózat számára a Cosmos DB adatbázis-fiókját.</span><span class="sxs-lookup"><span data-stu-id="98f33-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="98f33-135">Elfogadott értékek: false, True</span><span class="sxs-lookup"><span data-stu-id="98f33-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="98f33-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98f33-136">-InputObject</span></span>
<span data-ttu-id="98f33-137">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="98f33-137">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98f33-138">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="98f33-138">-IpRangeFilter</span></span>
<span data-ttu-id="98f33-139">Tűzfal támogatása</span><span class="sxs-lookup"><span data-stu-id="98f33-139">Firewall support.</span></span>
<span data-ttu-id="98f33-140">Az CIDR-űrlap IP-címeinek vagy IP-címeinek a halmazát adja meg, amely az adott adatbázis-fiókhoz tartozó ügyfél-IP-címek engedélyezett listájának része.</span><span class="sxs-lookup"><span data-stu-id="98f33-140">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="98f33-141">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="98f33-141">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="98f33-142">Ha a kötött állandósági konzisztenciát használja, ez az érték azt jelzi, hogy mennyi idő áll fenn (a időszak-ban).</span><span class="sxs-lookup"><span data-stu-id="98f33-142">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="98f33-143">Az érték elfogadott köre az 5-86400.</span><span class="sxs-lookup"><span data-stu-id="98f33-143">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="98f33-144">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="98f33-144">-MaxStalenessPrefix</span></span>
<span data-ttu-id="98f33-145">Ha a kötött állandósági konzisztenciát használja, ez az érték a tolerált lejárt kérelmek számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="98f33-145">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="98f33-146">Az érték elfogadott köre 1 – 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="98f33-146">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="98f33-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98f33-147">-Name</span></span>
<span data-ttu-id="98f33-148">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="98f33-148">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="98f33-149">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="98f33-149">-PublicNetworkAccess</span></span>
<span data-ttu-id="98f33-150">A kiszolgálón engedélyezve van-e a nyilvános végpontok elérése.</span><span class="sxs-lookup"><span data-stu-id="98f33-150">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="98f33-151">A lehetséges értékek a következők: "engedélyezve", "Letiltva"</span><span class="sxs-lookup"><span data-stu-id="98f33-151">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="98f33-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f33-152">-ResourceGroupName</span></span>
<span data-ttu-id="98f33-153">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="98f33-153">Name of resource group.</span></span>

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

### <span data-ttu-id="98f33-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98f33-154">-ResourceId</span></span>
<span data-ttu-id="98f33-155">Az erőforrás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="98f33-155">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="98f33-156">-Címke</span><span class="sxs-lookup"><span data-stu-id="98f33-156">-Tag</span></span>
<span data-ttu-id="98f33-157">Hashtablea kulcs-érték párokként.</span><span class="sxs-lookup"><span data-stu-id="98f33-157">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="98f33-158">A meglévő címke törléséhez használjon üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="98f33-158">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="98f33-159">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="98f33-159">-VirtualNetworkRule</span></span>
<span data-ttu-id="98f33-160">A virtuális hálózat ACL-értékeinek tömbje</span><span class="sxs-lookup"><span data-stu-id="98f33-160">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="98f33-161">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="98f33-161">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="98f33-162">A virtuális hálózat PSVirtualNetworkRuleObjects tömbje.</span><span class="sxs-lookup"><span data-stu-id="98f33-162">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98f33-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f33-163">-WhatIf</span></span>
<span data-ttu-id="98f33-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98f33-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f33-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98f33-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98f33-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f33-166">CommonParameters</span></span>
<span data-ttu-id="98f33-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98f33-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f33-168">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="98f33-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f33-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98f33-169">INPUTS</span></span>

### <span data-ttu-id="98f33-170">Microsoft. Azure. Command. CosmosDB. models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="98f33-170">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="98f33-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98f33-171">OUTPUTS</span></span>

### <span data-ttu-id="98f33-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="98f33-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="98f33-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98f33-173">NOTES</span></span>

## <span data-ttu-id="98f33-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98f33-174">RELATED LINKS</span></span>
