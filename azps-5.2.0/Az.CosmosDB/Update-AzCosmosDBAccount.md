---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356955"
---
# <span data-ttu-id="55a3d-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="55a3d-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="55a3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="55a3d-103">Frissítheti a 2010-es fiók attribútumát.</span><span class="sxs-lookup"><span data-stu-id="55a3d-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="55a3d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55a3d-104">SYNTAX</span></span>

### <span data-ttu-id="55a3d-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55a3d-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a3d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55a3d-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a3d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55a3d-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55a3d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55a3d-108">DESCRIPTION</span></span>
<span data-ttu-id="55a3d-109">Frissítse a 2010-es fiók tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="55a3d-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="55a3d-110">A fiókrégió nem frissíthető egymás után más tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="55a3d-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="55a3d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55a3d-111">EXAMPLES</span></span>

### <span data-ttu-id="55a3d-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="55a3d-112">Example 1</span></span>
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

<span data-ttu-id="55a3d-113">Frissítettük a DefaultConsistencyLevel értéket "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations és Enabled VirtualNetwork forFogsDB account with name accountName (Engedélyezve a MultipleWriteLocations) beállításra.</span><span class="sxs-lookup"><span data-stu-id="55a3d-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="55a3d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55a3d-114">PARAMETERS</span></span>

### <span data-ttu-id="55a3d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55a3d-115">-AsJob</span></span>
<span data-ttu-id="55a3d-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="55a3d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55a3d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55a3d-117">-Confirm</span></span>
<span data-ttu-id="55a3d-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="55a3d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a3d-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="55a3d-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="55a3d-120">ATans DB-adatbázisfiók alapértelmezett konzisztenciaszintje.</span><span class="sxs-lookup"><span data-stu-id="55a3d-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="55a3d-121">Elfogadott értékek: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="55a3d-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="55a3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a3d-122">-DefaultProfile</span></span>
<span data-ttu-id="55a3d-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55a3d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a3d-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="55a3d-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="55a3d-125">Metaadat-erőforrások (adatbázisok, tárolók, átviteli sebesség) írási műveleteinek letiltása a fiókkulcsokkal</span><span class="sxs-lookup"><span data-stu-id="55a3d-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="55a3d-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="55a3d-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="55a3d-127">Bool , amely azt jelzi, hogy engedélyezve van-e az AnalyticalStorage a fiókban.</span><span class="sxs-lookup"><span data-stu-id="55a3d-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="55a3d-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="55a3d-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="55a3d-129">Engedélyezi az írási terület automatikus feladatátvételét abban a ritka esetben, amikor a régió kimaradás miatt nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="55a3d-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="55a3d-130">Az automatikus feladatátvétel új írási régiót eredményez a fiók számára, és a fiókhoz konfigurált feladatátvételi prioritások alapján lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="55a3d-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="55a3d-131">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="55a3d-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="55a3d-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="55a3d-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="55a3d-133">Több írási hely engedélyezése</span><span class="sxs-lookup"><span data-stu-id="55a3d-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="55a3d-134">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="55a3d-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="55a3d-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="55a3d-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="55a3d-136">Engedélyezi a virtuális hálózatot aTans DB adatbázisfiókban.</span><span class="sxs-lookup"><span data-stu-id="55a3d-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="55a3d-137">Elfogadott értékek: hamis, igaz</span><span class="sxs-lookup"><span data-stu-id="55a3d-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="55a3d-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55a3d-138">-InputObject</span></span>
<span data-ttu-id="55a3d-139">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="55a3d-139">CosmosDB Account object</span></span>

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

### <span data-ttu-id="55a3d-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="55a3d-140">-IpRule</span></span>
<span data-ttu-id="55a3d-141">Tűzfal támogatása.</span><span class="sxs-lookup"><span data-stu-id="55a3d-141">Firewall support.</span></span> <span data-ttu-id="55a3d-142">Azt adja meg, hogy a CIDR-űrlap IP-címeinek és IP-címtartományainak készletét adja meg az adott adatbázisfiók ügyfél IP-címeinek engedélyezett listájában.</span><span class="sxs-lookup"><span data-stu-id="55a3d-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="55a3d-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="55a3d-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="55a3d-144">A KeyVault URI-ja</span><span class="sxs-lookup"><span data-stu-id="55a3d-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="55a3d-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="55a3d-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="55a3d-146">A Kötött elavultság konzisztens használatakor ez az érték a kortalanság (időszakban) megfelelő időmennyiségét jelzi.</span><span class="sxs-lookup"><span data-stu-id="55a3d-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="55a3d-147">Az érték elfogadott tartománya 5-86400.</span><span class="sxs-lookup"><span data-stu-id="55a3d-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="55a3d-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="55a3d-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="55a3d-149">A Kötött elavultság konzisztens használata esetén ez az érték a felhasznált elavult kérelmek számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="55a3d-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="55a3d-150">Az érték elfogadott tartománya 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="55a3d-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="55a3d-151">-Name</span><span class="sxs-lookup"><span data-stu-id="55a3d-151">-Name</span></span>
<span data-ttu-id="55a3d-152">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="55a3d-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="55a3d-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="55a3d-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="55a3d-154">A nyilvános végponthoz való hozzáférés engedélyezett-e ehhez a kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="55a3d-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="55a3d-155">Lehetséges értékek: "Engedélyezve", "Letiltva"</span><span class="sxs-lookup"><span data-stu-id="55a3d-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="55a3d-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a3d-156">-ResourceGroupName</span></span>
<span data-ttu-id="55a3d-157">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="55a3d-157">Name of resource group.</span></span>

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

### <span data-ttu-id="55a3d-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55a3d-158">-ResourceId</span></span>
<span data-ttu-id="55a3d-159">Az erőforrás Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="55a3d-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="55a3d-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="55a3d-160">-Tag</span></span>
<span data-ttu-id="55a3d-161">Címkék kivonata kulcsérték-párokként.</span><span class="sxs-lookup"><span data-stu-id="55a3d-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="55a3d-162">Meglévő címke kiürítása üres karakterlánc használatával.</span><span class="sxs-lookup"><span data-stu-id="55a3d-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="55a3d-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="55a3d-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="55a3d-164">A virtuális hálózat ACL-ében lévő karakterláncértékek tömbje.</span><span class="sxs-lookup"><span data-stu-id="55a3d-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="55a3d-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="55a3d-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="55a3d-166">A VIRTUÁLIS hálózat PSVirtualNetworkRuleObjects tömbje.</span><span class="sxs-lookup"><span data-stu-id="55a3d-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="55a3d-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a3d-167">-WhatIf</span></span>
<span data-ttu-id="55a3d-168">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="55a3d-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a3d-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55a3d-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a3d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a3d-170">CommonParameters</span></span>
<span data-ttu-id="55a3d-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a3d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a3d-172">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55a3d-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a3d-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55a3d-173">INPUTS</span></span>

### <span data-ttu-id="55a3d-174">Microsoft.Azure.Commands.FogsDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="55a3d-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="55a3d-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55a3d-175">OUTPUTS</span></span>

### <span data-ttu-id="55a3d-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="55a3d-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="55a3d-177">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55a3d-177">NOTES</span></span>

## <span data-ttu-id="55a3d-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55a3d-178">RELATED LINKS</span></span>
