---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 4e31ae75f6fcea77c179757312988a0abbbb58f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480586"
---
# <span data-ttu-id="fe04e-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="fe04e-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="fe04e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe04e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe04e-103">Hozzon létre egy új Fiókot a 3DB-hez.</span><span class="sxs-lookup"><span data-stu-id="fe04e-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="fe04e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fe04e-104">SYNTAX</span></span>

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

## <span data-ttu-id="fe04e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fe04e-105">DESCRIPTION</span></span>
<span data-ttu-id="fe04e-106">Hozzon létre egy új Fiókot a megadott ResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="fe04e-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="fe04e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fe04e-107">EXAMPLES</span></span>

### <span data-ttu-id="fe04e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fe04e-108">Example 1</span></span>
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

<span data-ttu-id="fe04e-109">Az ResourceGroup resourceGroupName erőforráscsoportban létrejön egy új,AccountName nevű fiók.</span><span class="sxs-lookup"><span data-stu-id="fe04e-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="fe04e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe04e-110">PARAMETERS</span></span>

### <span data-ttu-id="fe04e-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="fe04e-111">-ApiKind</span></span>
<span data-ttu-id="fe04e-112">A létrehozni szükséges db db-adatbázisfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="fe04e-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="fe04e-113">Elfogadott értékek: Sql, MongoDB, Gremlin, Table, Ésra.</span><span class="sxs-lookup"><span data-stu-id="fe04e-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="fe04e-114">Alapértelmezett érték: Sql</span><span class="sxs-lookup"><span data-stu-id="fe04e-114">Default value: Sql</span></span>

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

### <span data-ttu-id="fe04e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe04e-115">-AsJob</span></span>
<span data-ttu-id="fe04e-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fe04e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe04e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe04e-117">-Confirm</span></span>
<span data-ttu-id="fe04e-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fe04e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe04e-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="fe04e-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="fe04e-120">ATans DB-adatbázisfiók alapértelmezett konzisztenciaszintje.</span><span class="sxs-lookup"><span data-stu-id="fe04e-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="fe04e-121">Elfogadott értékek: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="fe04e-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="fe04e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe04e-122">-DefaultProfile</span></span>
<span data-ttu-id="fe04e-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe04e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe04e-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="fe04e-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="fe04e-125">Metaadat-erőforrások (adatbázisok, tárolók, átviteli sebesség) írási műveleteinek letiltása a fiókkulcsokkal</span><span class="sxs-lookup"><span data-stu-id="fe04e-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="fe04e-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="fe04e-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="fe04e-127">Bool , amely azt jelzi, hogy engedélyezve van-e az AnalyticalStorage a fiókban.</span><span class="sxs-lookup"><span data-stu-id="fe04e-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="fe04e-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="fe04e-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="fe04e-129">Engedélyezi az írási terület automatikus feladatátvételét abban a ritka esetben, amikor a régió kimaradás miatt nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="fe04e-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="fe04e-130">Az automatikus feladatátvétel új írási régiót eredményez a fiók számára, és a fiókhoz konfigurált feladatátvételi prioritások alapján lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="fe04e-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="fe04e-131">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="fe04e-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="fe04e-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="fe04e-132">-EnableFreeTier</span></span>
<span data-ttu-id="fe04e-133">Bool , amely jelzi, hogy a FreeTier engedélyezve van-e a fiókban.</span><span class="sxs-lookup"><span data-stu-id="fe04e-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="fe04e-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="fe04e-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="fe04e-135">Több írási hely engedélyezése</span><span class="sxs-lookup"><span data-stu-id="fe04e-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="fe04e-136">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="fe04e-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="fe04e-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fe04e-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="fe04e-138">Engedélyezi a virtuális hálózatot aTans DB adatbázisfiókban.</span><span class="sxs-lookup"><span data-stu-id="fe04e-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="fe04e-139">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="fe04e-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="fe04e-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="fe04e-140">-IpRule</span></span>
<span data-ttu-id="fe04e-141">Tűzfal támogatása.</span><span class="sxs-lookup"><span data-stu-id="fe04e-141">Firewall support.</span></span> <span data-ttu-id="fe04e-142">Azt adja meg, hogy a CIDR-űrlap IP-címeinek és IP-címtartományainak készletét adja meg az adott adatbázisfiók ügyfél IP-címeinek engedélyezett listájában.</span><span class="sxs-lookup"><span data-stu-id="fe04e-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="fe04e-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="fe04e-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="fe04e-144">A KeyVault URI-ja</span><span class="sxs-lookup"><span data-stu-id="fe04e-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="fe04e-145">-Location</span><span class="sxs-lookup"><span data-stu-id="fe04e-145">-Location</span></span>
<span data-ttu-id="fe04e-146">Vegyen fel egy helyet aTans DB adatbázisfiókba.</span><span class="sxs-lookup"><span data-stu-id="fe04e-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="fe04e-147">A feladatátvételi prioritás szerint rendezett karakterláncok tömbje.</span><span class="sxs-lookup"><span data-stu-id="fe04e-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="fe04e-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="fe04e-148">-LocationObject</span></span>
<span data-ttu-id="fe04e-149">Vegyen fel egy helyet aTans DB adatbázisfiókba.</span><span class="sxs-lookup"><span data-stu-id="fe04e-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="fe04e-150">PSLocation-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="fe04e-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="fe04e-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="fe04e-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="fe04e-152">A Kötött elavultság konzisztens használatakor ez az érték a kortalanság (időszakban) megfelelő időmennyiségét jelzi.</span><span class="sxs-lookup"><span data-stu-id="fe04e-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="fe04e-153">Az érték elfogadott tartománya 5-86400.</span><span class="sxs-lookup"><span data-stu-id="fe04e-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="fe04e-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="fe04e-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="fe04e-155">A Kötött elavultság konzisztens használata esetén ez az érték a felhasznált elavult kérelmek számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="fe04e-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="fe04e-156">Az érték elfogadott tartománya 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="fe04e-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="fe04e-157">-Name</span><span class="sxs-lookup"><span data-stu-id="fe04e-157">-Name</span></span>
<span data-ttu-id="fe04e-158">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="fe04e-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fe04e-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="fe04e-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="fe04e-160">A nyilvános végponthoz való hozzáférés engedélyezett-e ehhez a kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="fe04e-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="fe04e-161">Lehetséges értékek: "Engedélyezve", "Letiltva"</span><span class="sxs-lookup"><span data-stu-id="fe04e-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="fe04e-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe04e-162">-ResourceGroupName</span></span>
<span data-ttu-id="fe04e-163">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fe04e-163">Name of resource group.</span></span>

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

### <span data-ttu-id="fe04e-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="fe04e-164">-ServerVersion</span></span>
<span data-ttu-id="fe04e-165">A ServerVersion csak MongoDB-fiókok esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="fe04e-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="fe04e-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe04e-166">-Tag</span></span>
<span data-ttu-id="fe04e-167">Címkék kivonata kulcsérték-párokként.</span><span class="sxs-lookup"><span data-stu-id="fe04e-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="fe04e-168">Meglévő címke kiürítása üres karakterlánc használatával.</span><span class="sxs-lookup"><span data-stu-id="fe04e-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="fe04e-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fe04e-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="fe04e-170">A virtuális hálózat ACL-ében lévő karakterláncértékek tömbje.</span><span class="sxs-lookup"><span data-stu-id="fe04e-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="fe04e-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="fe04e-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="fe04e-172">A VIRTUÁLIS hálózat PSVirtualNetworkRuleObjects tömbje.</span><span class="sxs-lookup"><span data-stu-id="fe04e-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="fe04e-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe04e-173">-WhatIf</span></span>
<span data-ttu-id="fe04e-174">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fe04e-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe04e-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe04e-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe04e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe04e-176">CommonParameters</span></span>
<span data-ttu-id="fe04e-177">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe04e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe04e-178">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe04e-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe04e-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe04e-179">INPUTS</span></span>

### <span data-ttu-id="fe04e-180">Microsoft.Azure.Commands.FogarasDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="fe04e-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="fe04e-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe04e-181">OUTPUTS</span></span>

### <span data-ttu-id="fe04e-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="fe04e-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="fe04e-183">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fe04e-183">NOTES</span></span>

## <span data-ttu-id="fe04e-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe04e-184">RELATED LINKS</span></span>
 
