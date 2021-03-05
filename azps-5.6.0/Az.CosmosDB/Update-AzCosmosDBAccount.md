---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: cbee0ef9ce750dbb72af5be484106ccabec79321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010741"
---
# <span data-ttu-id="b3a95-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="b3a95-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="b3a95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a95-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a95-103">Frissítheti a 2010-es fiók attribútumát.</span><span class="sxs-lookup"><span data-stu-id="b3a95-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="b3a95-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3a95-104">SYNTAX</span></span>

### <span data-ttu-id="b3a95-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3a95-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a95-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a95-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a95-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a95-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3a95-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3a95-108">DESCRIPTION</span></span>
<span data-ttu-id="b3a95-109">Frissítse a 2010-es fiók tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b3a95-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="b3a95-110">A fiókrégió nem frissíthető egymás után más tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="b3a95-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="b3a95-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3a95-111">EXAMPLES</span></span>

### <span data-ttu-id="b3a95-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="b3a95-112">Example 1</span></span>
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
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="b3a95-113">Frissítettük a DefaultConsistencyLevel értéket "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations és Enabled VirtualNetwork forFogsDB account with name accountName névre.</span><span class="sxs-lookup"><span data-stu-id="b3a95-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="b3a95-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3a95-114">PARAMETERS</span></span>

### <span data-ttu-id="b3a95-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3a95-115">-AsJob</span></span>
<span data-ttu-id="b3a95-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b3a95-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3a95-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="b3a95-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="b3a95-118">Az az intervallum (percben), amellyel biztonsági másolatot készít (csak periodikus módú biztonsági másolatokkal rendelkező fiókok esetén)</span><span class="sxs-lookup"><span data-stu-id="b3a95-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="b3a95-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="b3a95-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="b3a95-120">Az az idő (órában), amelyben az egyes biztonsági másolatok megőrzve vannak (csak az periodikus biztonsági másolatokkal rendelkező fiókok esetén)</span><span class="sxs-lookup"><span data-stu-id="b3a95-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="b3a95-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3a95-121">-Confirm</span></span>
<span data-ttu-id="b3a95-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b3a95-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3a95-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="b3a95-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="b3a95-124">ATans DB-adatbázisfiók alapértelmezett konzisztenciaszintje.</span><span class="sxs-lookup"><span data-stu-id="b3a95-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="b3a95-125">Elfogadott értékek: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="b3a95-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="b3a95-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a95-126">-DefaultProfile</span></span>
<span data-ttu-id="b3a95-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3a95-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a95-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="b3a95-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="b3a95-129">Metaadat-erőforrások (adatbázisok, tárolók, átviteli sebesség) írási műveleteinek letiltása a fiókkulcsokkal</span><span class="sxs-lookup"><span data-stu-id="b3a95-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="b3a95-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="b3a95-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="b3a95-131">Bool , amely azt jelzi, hogy engedélyezve van-e az AnalyticalStorage a fiókban.</span><span class="sxs-lookup"><span data-stu-id="b3a95-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="b3a95-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="b3a95-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="b3a95-133">Engedélyezi az írási terület automatikus feladatátvételét abban a ritka esetben, amikor a régió kimaradás miatt nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="b3a95-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="b3a95-134">Az automatikus feladatátvétel új írási régiót eredményez a fiók számára, és a fiókhoz konfigurált feladatátvételi prioritások alapján lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="b3a95-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="b3a95-135">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="b3a95-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b3a95-136">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="b3a95-136">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="b3a95-137">Több írási hely engedélyezése</span><span class="sxs-lookup"><span data-stu-id="b3a95-137">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="b3a95-138">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="b3a95-138">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b3a95-139">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b3a95-139">-EnableVirtualNetwork</span></span>
<span data-ttu-id="b3a95-140">Engedélyezi a virtuális hálózatot aTans DB adatbázisfiókban.</span><span class="sxs-lookup"><span data-stu-id="b3a95-140">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="b3a95-141">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="b3a95-141">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b3a95-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3a95-142">-InputObject</span></span>
<span data-ttu-id="b3a95-143">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="b3a95-143">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b3a95-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="b3a95-144">-IpRule</span></span>
<span data-ttu-id="b3a95-145">Tűzfal támogatása.</span><span class="sxs-lookup"><span data-stu-id="b3a95-145">Firewall support.</span></span> <span data-ttu-id="b3a95-146">Azt adja meg, hogy a CIDR űrlap IP-címeinek és IP-címtartományainak halmazát fel kell venni egy adott adatbázisfiók ügyfél IP-címeinek engedélyezett listájába.</span><span class="sxs-lookup"><span data-stu-id="b3a95-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="b3a95-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="b3a95-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="b3a95-148">A KeyVault URI-ja</span><span class="sxs-lookup"><span data-stu-id="b3a95-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="b3a95-149">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b3a95-149">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="b3a95-150">A Kötött elavultság konzisztens használatakor ez az érték a kortalanság (időszakban) megfelelő időmennyiségét jelzi.</span><span class="sxs-lookup"><span data-stu-id="b3a95-150">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="b3a95-151">Az érték elfogadott tartománya 5-86400.</span><span class="sxs-lookup"><span data-stu-id="b3a95-151">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="b3a95-152">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="b3a95-152">-MaxStalenessPrefix</span></span>
<span data-ttu-id="b3a95-153">A Kötött elavultság konzisztens használata esetén ez az érték a felhasznált elavult kérelmek számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="b3a95-153">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="b3a95-154">Az érték elfogadott tartománya 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="b3a95-154">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="b3a95-155">-Name</span><span class="sxs-lookup"><span data-stu-id="b3a95-155">-Name</span></span>
<span data-ttu-id="b3a95-156">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="b3a95-156">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b3a95-157">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="b3a95-157">-NetworkAclBypass</span></span>
<span data-ttu-id="b3a95-158">Engedélyezve van-e a Hálózati Acl bypass funkció a Synapse Link szolgáltatásban ehhez a fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="b3a95-158">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="b3a95-159">Lehetséges értékek: "Nincs", "AzureServices".</span><span class="sxs-lookup"><span data-stu-id="b3a95-159">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="b3a95-160">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a95-160">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="b3a95-161">Azon erőforrás-azonosítók listája, amelyek engedélyezik a hálózati Acl bypass for Synapse linket.</span><span class="sxs-lookup"><span data-stu-id="b3a95-161">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="b3a95-162">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="b3a95-162">-PublicNetworkAccess</span></span>
<span data-ttu-id="b3a95-163">A nyilvános végponthoz való hozzáférés engedélyezett-e ehhez a kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="b3a95-163">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="b3a95-164">Lehetséges értékek: "Engedélyezve", "Letiltva"</span><span class="sxs-lookup"><span data-stu-id="b3a95-164">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="b3a95-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a95-165">-ResourceGroupName</span></span>
<span data-ttu-id="b3a95-166">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b3a95-166">Name of resource group.</span></span>

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

### <span data-ttu-id="b3a95-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a95-167">-ResourceId</span></span>
<span data-ttu-id="b3a95-168">Az erőforrás Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="b3a95-168">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="b3a95-169">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b3a95-169">-ServerVersion</span></span>
<span data-ttu-id="b3a95-170">A ServerVersion csak MongoDB-fiókok esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="b3a95-170">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="b3a95-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3a95-171">-Tag</span></span>
<span data-ttu-id="b3a95-172">Címkék kivonata kulcsérték-párokként.</span><span class="sxs-lookup"><span data-stu-id="b3a95-172">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="b3a95-173">Meglévő címke kiürítása üres karakterlánc használatával.</span><span class="sxs-lookup"><span data-stu-id="b3a95-173">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="b3a95-174">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b3a95-174">-VirtualNetworkRule</span></span>
<span data-ttu-id="b3a95-175">A virtuális hálózat ACL-ében lévő karakterláncértékek tömbje.</span><span class="sxs-lookup"><span data-stu-id="b3a95-175">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="b3a95-176">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="b3a95-176">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="b3a95-177">A VIRTUÁLIS hálózat PSVirtualNetworkRuleObjects tömbje.</span><span class="sxs-lookup"><span data-stu-id="b3a95-177">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="b3a95-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a95-178">-WhatIf</span></span>
<span data-ttu-id="b3a95-179">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b3a95-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3a95-180">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3a95-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3a95-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a95-181">CommonParameters</span></span>
<span data-ttu-id="b3a95-182">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a95-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a95-183">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3a95-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a95-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3a95-184">INPUTS</span></span>

### <span data-ttu-id="b3a95-185">Microsoft.Azure.Commands.FogsDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="b3a95-185">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="b3a95-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3a95-186">OUTPUTS</span></span>

### <span data-ttu-id="b3a95-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b3a95-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b3a95-188">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3a95-188">NOTES</span></span>

## <span data-ttu-id="b3a95-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3a95-189">RELATED LINKS</span></span>
