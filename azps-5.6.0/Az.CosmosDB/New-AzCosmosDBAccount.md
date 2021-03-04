---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 75085bed9c1f9b0cd0c0328b9a166c6dc08a60b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939633"
---
# <span data-ttu-id="73a69-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="73a69-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="73a69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73a69-102">SYNOPSIS</span></span>
<span data-ttu-id="73a69-103">Hozzon létre egy új Fiókot.</span><span class="sxs-lookup"><span data-stu-id="73a69-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="73a69-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="73a69-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>] [-Location <String[]>]
 [-LocationObject <PSLocation[]>] -ResourceGroupName <String> -Name <String>
 [-DefaultConsistencyLevel <String>] [-IpRule <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-PublicNetworkAccess <String>]
 [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob] [-NetworkAclBypass <String>]
 [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>] [-BackupIntervalInMinutes <Int32>]
 [-BackupRetentionIntervalInHours <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73a69-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="73a69-105">DESCRIPTION</span></span>
<span data-ttu-id="73a69-106">Hozzon létre egy új Fiókot a megadott ResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="73a69-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="73a69-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="73a69-107">EXAMPLES</span></span>

### <span data-ttu-id="73a69-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="73a69-108">Example 1</span></span>
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
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="73a69-109">Az ResourceGroup resourceGroupName erőforráscsoportban létrejön egy új,AccountName nevű fiók.</span><span class="sxs-lookup"><span data-stu-id="73a69-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="73a69-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73a69-110">PARAMETERS</span></span>

### <span data-ttu-id="73a69-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="73a69-111">-ApiKind</span></span>
<span data-ttu-id="73a69-112">A létrehozni szükséges db db-adatbázisfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="73a69-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="73a69-113">Elfogadott értékek: Sql, MongoDB, Gremlin, Table, Ésra.</span><span class="sxs-lookup"><span data-stu-id="73a69-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="73a69-114">Alapértelmezett érték: Sql</span><span class="sxs-lookup"><span data-stu-id="73a69-114">Default value: Sql</span></span>

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

### <span data-ttu-id="73a69-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73a69-115">-AsJob</span></span>
<span data-ttu-id="73a69-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="73a69-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73a69-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="73a69-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="73a69-118">Az az intervallum (percben), amellyel biztonsági másolatot készít (csak periodikus módú biztonsági másolatokkal rendelkező fiókok esetén)</span><span class="sxs-lookup"><span data-stu-id="73a69-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="73a69-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="73a69-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="73a69-120">Az az idő (órában), amelyben az egyes biztonsági másolatok megőrzve vannak (csak az periodikus biztonsági másolatokkal rendelkező fiókok esetén)</span><span class="sxs-lookup"><span data-stu-id="73a69-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="73a69-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73a69-121">-Confirm</span></span>
<span data-ttu-id="73a69-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="73a69-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73a69-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="73a69-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="73a69-124">ATans DB-adatbázisfiók alapértelmezett konzisztenciaszintje.</span><span class="sxs-lookup"><span data-stu-id="73a69-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="73a69-125">Elfogadott értékek: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="73a69-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="73a69-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a69-126">-DefaultProfile</span></span>
<span data-ttu-id="73a69-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73a69-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73a69-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="73a69-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="73a69-129">Metaadat-erőforrások (adatbázisok, tárolók, átviteli sebesség) írási műveleteinek letiltása a fiókkulcsokkal</span><span class="sxs-lookup"><span data-stu-id="73a69-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="73a69-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="73a69-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="73a69-131">Bool , amely azt jelzi, hogy engedélyezve van-e az AnalyticalStorage a fiókban.</span><span class="sxs-lookup"><span data-stu-id="73a69-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="73a69-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="73a69-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="73a69-133">Engedélyezi az írási terület automatikus feladatátvételét abban a ritka esetben, amikor a régió kimaradás miatt nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="73a69-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="73a69-134">Az automatikus feladatátvétel új írási régiót eredményez a fiók számára, és a fiókhoz konfigurált feladatátvételi prioritások alapján lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="73a69-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="73a69-135">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="73a69-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="73a69-136">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="73a69-136">-EnableFreeTier</span></span>
<span data-ttu-id="73a69-137">Bool , amely jelzi, hogy a FreeTier engedélyezve van-e a fiókban.</span><span class="sxs-lookup"><span data-stu-id="73a69-137">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="73a69-138">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="73a69-138">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="73a69-139">Több írási hely engedélyezése</span><span class="sxs-lookup"><span data-stu-id="73a69-139">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="73a69-140">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="73a69-140">Accepted values: false, true</span></span>

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

### <span data-ttu-id="73a69-141">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73a69-141">-EnableVirtualNetwork</span></span>
<span data-ttu-id="73a69-142">Engedélyezi a virtuális hálózatot aTans DB adatbázisfiókban.</span><span class="sxs-lookup"><span data-stu-id="73a69-142">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="73a69-143">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="73a69-143">Accepted values: false, true</span></span>

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

### <span data-ttu-id="73a69-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="73a69-144">-IpRule</span></span>
<span data-ttu-id="73a69-145">Tűzfal támogatása.</span><span class="sxs-lookup"><span data-stu-id="73a69-145">Firewall support.</span></span> <span data-ttu-id="73a69-146">Azt adja meg, hogy a CIDR űrlap IP-címeinek és IP-címtartományainak halmazát fel kell venni egy adott adatbázisfiók ügyfél IP-címeinek engedélyezett listájába.</span><span class="sxs-lookup"><span data-stu-id="73a69-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="73a69-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="73a69-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="73a69-148">A KeyVault URI-ja</span><span class="sxs-lookup"><span data-stu-id="73a69-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="73a69-149">-Location</span><span class="sxs-lookup"><span data-stu-id="73a69-149">-Location</span></span>
<span data-ttu-id="73a69-150">Vegyen fel egy helyet aTans DB adatbázisfiókba.</span><span class="sxs-lookup"><span data-stu-id="73a69-150">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="73a69-151">A feladatátvételi prioritás szerint rendezett karakterláncok tömbje.</span><span class="sxs-lookup"><span data-stu-id="73a69-151">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="73a69-152">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="73a69-152">-LocationObject</span></span>
<span data-ttu-id="73a69-153">Vegyen fel egy helyet aTans DB adatbázisfiókba.</span><span class="sxs-lookup"><span data-stu-id="73a69-153">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="73a69-154">PSLocation-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="73a69-154">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="73a69-155">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="73a69-155">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="73a69-156">A Kötött elavultság konzisztens használatakor ez az érték a kortalanság (időszakban) megfelelő időmennyiségét jelzi.</span><span class="sxs-lookup"><span data-stu-id="73a69-156">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="73a69-157">Az érték elfogadott tartománya 5-86400.</span><span class="sxs-lookup"><span data-stu-id="73a69-157">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="73a69-158">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="73a69-158">-MaxStalenessPrefix</span></span>
<span data-ttu-id="73a69-159">A Kötött elavultság konzisztens használata esetén ez az érték a felhasznált elavult kérelmek számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="73a69-159">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="73a69-160">Az érték elfogadott tartománya 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="73a69-160">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="73a69-161">-Name</span><span class="sxs-lookup"><span data-stu-id="73a69-161">-Name</span></span>
<span data-ttu-id="73a69-162">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="73a69-162">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="73a69-163">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="73a69-163">-NetworkAclBypass</span></span>
<span data-ttu-id="73a69-164">Engedélyezve van-e a Hálózati Acl bypass funkció a Synapse Link szolgáltatásban ehhez a fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="73a69-164">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="73a69-165">Lehetséges értékek: "Nincs", "AzureServices".</span><span class="sxs-lookup"><span data-stu-id="73a69-165">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="73a69-166">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="73a69-166">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="73a69-167">Azon erőforrás-azonosítók listája, amelyek engedélyezik a hálózati Acl bypass for Synapse linket.</span><span class="sxs-lookup"><span data-stu-id="73a69-167">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="73a69-168">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="73a69-168">-PublicNetworkAccess</span></span>
<span data-ttu-id="73a69-169">A nyilvános végponthoz való hozzáférés engedélyezett-e ehhez a kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="73a69-169">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="73a69-170">Lehetséges értékek: "Engedélyezve", "Letiltva"</span><span class="sxs-lookup"><span data-stu-id="73a69-170">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="73a69-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a69-171">-ResourceGroupName</span></span>
<span data-ttu-id="73a69-172">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="73a69-172">Name of resource group.</span></span>

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

### <span data-ttu-id="73a69-173">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="73a69-173">-ServerVersion</span></span>
<span data-ttu-id="73a69-174">A ServerVersion csak MongoDB-fiókok esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="73a69-174">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="73a69-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="73a69-175">-Tag</span></span>
<span data-ttu-id="73a69-176">Címkék kivonata kulcsérték-párokként.</span><span class="sxs-lookup"><span data-stu-id="73a69-176">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="73a69-177">Meglévő címke kiürítása üres karakterlánc használatával.</span><span class="sxs-lookup"><span data-stu-id="73a69-177">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="73a69-178">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="73a69-178">-VirtualNetworkRule</span></span>
<span data-ttu-id="73a69-179">A virtuális hálózat ACL-ében lévő karakterláncértékek tömbje.</span><span class="sxs-lookup"><span data-stu-id="73a69-179">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="73a69-180">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="73a69-180">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="73a69-181">A VIRTUÁLIS hálózat PSVirtualNetworkRuleObjects tömbje.</span><span class="sxs-lookup"><span data-stu-id="73a69-181">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="73a69-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73a69-182">-WhatIf</span></span>
<span data-ttu-id="73a69-183">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="73a69-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73a69-184">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73a69-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73a69-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a69-185">CommonParameters</span></span>
<span data-ttu-id="73a69-186">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a69-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a69-187">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73a69-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a69-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73a69-188">INPUTS</span></span>

### <span data-ttu-id="73a69-189">Microsoft.Azure.Commands.FogsDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="73a69-189">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="73a69-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73a69-190">OUTPUTS</span></span>

### <span data-ttu-id="73a69-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="73a69-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="73a69-192">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="73a69-192">NOTES</span></span>

## <span data-ttu-id="73a69-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73a69-193">RELATED LINKS</span></span>
