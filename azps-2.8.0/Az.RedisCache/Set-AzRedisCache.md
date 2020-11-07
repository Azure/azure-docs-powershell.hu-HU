---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: aaec1ed3f165338c0aea6bf93e38dfaa8460cdf3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838222"
---
# <span data-ttu-id="c54a3-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c54a3-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="c54a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c54a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c54a3-103">Módosítja egy Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="c54a3-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="c54a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c54a3-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c54a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c54a3-105">DESCRIPTION</span></span>
<span data-ttu-id="c54a3-106">A **set-AzRedisCache** parancsmag az Azure Redis-gyorsítótárát módosítja.</span><span class="sxs-lookup"><span data-stu-id="c54a3-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="c54a3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c54a3-107">EXAMPLES</span></span>

### <span data-ttu-id="c54a3-108">Példa 1: Redis-gyorsítótár módosítása</span><span class="sxs-lookup"><span data-stu-id="c54a3-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="c54a3-109">Ez a parancs frissíti a MyCache nevű Redis-gyorsítótár maxmemory-házirendjét.</span><span class="sxs-lookup"><span data-stu-id="c54a3-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="c54a3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c54a3-110">PARAMETERS</span></span>

### <span data-ttu-id="c54a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c54a3-111">-DefaultProfile</span></span>
<span data-ttu-id="c54a3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c54a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c54a3-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="c54a3-113">-EnableNonSslPort</span></span>
<span data-ttu-id="c54a3-114">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="c54a3-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="c54a3-115">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="c54a3-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c54a3-116">-Name</span></span>
<span data-ttu-id="c54a3-117">A frissítendő Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c54a3-117">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="c54a3-118">-RedisConfiguration</span></span>
<span data-ttu-id="c54a3-119">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="c54a3-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="c54a3-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c54a3-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c54a3-121">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="c54a3-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="c54a3-122">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="c54a3-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="c54a3-123">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="c54a3-123">Premium tier only.</span></span>
- <span data-ttu-id="c54a3-124">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="c54a3-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="c54a3-125">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c54a3-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="c54a3-126">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="c54a3-126">Premium tier only.</span></span>
- <span data-ttu-id="c54a3-127">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="c54a3-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="c54a3-128">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c54a3-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="c54a3-129">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="c54a3-129">Premium tier only.</span></span> 
- <span data-ttu-id="c54a3-130">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="c54a3-130">maxmemory-reserved.</span></span>
<span data-ttu-id="c54a3-131">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="c54a3-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="c54a3-132">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="c54a3-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c54a3-133">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="c54a3-133">maxmemory-policy.</span></span>
<span data-ttu-id="c54a3-134">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="c54a3-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="c54a3-135">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="c54a3-135">All pricing tiers.</span></span> 
- <span data-ttu-id="c54a3-136">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="c54a3-136">notify-keyspace-events.</span></span>
<span data-ttu-id="c54a3-137">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="c54a3-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="c54a3-138">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="c54a3-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="c54a3-139">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="c54a3-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="c54a3-140">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="c54a3-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c54a3-141">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="c54a3-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c54a3-142">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="c54a3-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="c54a3-143">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="c54a3-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c54a3-144">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="c54a3-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c54a3-145">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="c54a3-145">set-max-intset-entries.</span></span>
<span data-ttu-id="c54a3-146">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="c54a3-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c54a3-147">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="c54a3-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c54a3-148">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="c54a3-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="c54a3-149">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="c54a3-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c54a3-150">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="c54a3-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c54a3-151">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="c54a3-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="c54a3-152">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="c54a3-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c54a3-153">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="c54a3-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c54a3-154">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="c54a3-154">databases.</span></span>
<span data-ttu-id="c54a3-155">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="c54a3-155">Configures the number of databases.</span></span>
<span data-ttu-id="c54a3-156">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="c54a3-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="c54a3-157">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="c54a3-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="c54a3-158">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="c54a3-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c54a3-159">-ResourceGroupName</span></span>
<span data-ttu-id="c54a3-160">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c54a3-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="c54a3-161">-ShardCount</span></span>
<span data-ttu-id="c54a3-162">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c54a3-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-163">-Méret</span><span class="sxs-lookup"><span data-stu-id="c54a3-163">-Size</span></span>
<span data-ttu-id="c54a3-164">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c54a3-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="c54a3-165">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="c54a3-165">Valid values are:</span></span> 
- <span data-ttu-id="c54a3-166">P1</span><span class="sxs-lookup"><span data-stu-id="c54a3-166">P1</span></span>
- <span data-ttu-id="c54a3-167">P2</span><span class="sxs-lookup"><span data-stu-id="c54a3-167">P2</span></span>
- <span data-ttu-id="c54a3-168">P3</span><span class="sxs-lookup"><span data-stu-id="c54a3-168">P3</span></span>
- <span data-ttu-id="c54a3-169">P4</span><span class="sxs-lookup"><span data-stu-id="c54a3-169">P4</span></span>
- <span data-ttu-id="c54a3-170">P5</span><span class="sxs-lookup"><span data-stu-id="c54a3-170">P5</span></span>
- <span data-ttu-id="c54a3-171">C0</span><span class="sxs-lookup"><span data-stu-id="c54a3-171">C0</span></span>
- <span data-ttu-id="c54a3-172">C1</span><span class="sxs-lookup"><span data-stu-id="c54a3-172">C1</span></span>
- <span data-ttu-id="c54a3-173">C2</span><span class="sxs-lookup"><span data-stu-id="c54a3-173">C2</span></span>
- <span data-ttu-id="c54a3-174">C3</span><span class="sxs-lookup"><span data-stu-id="c54a3-174">C3</span></span>
- <span data-ttu-id="c54a3-175">C4</span><span class="sxs-lookup"><span data-stu-id="c54a3-175">C4</span></span>
- <span data-ttu-id="c54a3-176">C5</span><span class="sxs-lookup"><span data-stu-id="c54a3-176">C5</span></span>
- <span data-ttu-id="c54a3-177">C6</span><span class="sxs-lookup"><span data-stu-id="c54a3-177">C6</span></span>
- <span data-ttu-id="c54a3-178">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="c54a3-178">250MB</span></span>
- <span data-ttu-id="c54a3-179">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="c54a3-179">1GB</span></span>
- <span data-ttu-id="c54a3-180">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="c54a3-180">2.5GB</span></span>
- <span data-ttu-id="c54a3-181">6GB</span><span class="sxs-lookup"><span data-stu-id="c54a3-181">6GB</span></span>
- <span data-ttu-id="c54a3-182">13GB</span><span class="sxs-lookup"><span data-stu-id="c54a3-182">13GB</span></span>
- <span data-ttu-id="c54a3-183">26GB</span><span class="sxs-lookup"><span data-stu-id="c54a3-183">26GB</span></span>
- <span data-ttu-id="c54a3-184">53GB</span><span class="sxs-lookup"><span data-stu-id="c54a3-184">53GB</span></span>
- <span data-ttu-id="c54a3-185">120 MB: az alapértelmezett érték az 1GB vagy a C1.</span><span class="sxs-lookup"><span data-stu-id="c54a3-185">120GB The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-186">-SKU</span><span class="sxs-lookup"><span data-stu-id="c54a3-186">-Sku</span></span>
<span data-ttu-id="c54a3-187">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="c54a3-187">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="c54a3-188">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="c54a3-188">Valid values are:</span></span> 
- <span data-ttu-id="c54a3-189">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="c54a3-189">Basic</span></span>
- <span data-ttu-id="c54a3-190">Standard</span><span class="sxs-lookup"><span data-stu-id="c54a3-190">Standard</span></span>
- <span data-ttu-id="c54a3-191">Prémium: az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="c54a3-191">Premium The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-192">-Címke</span><span class="sxs-lookup"><span data-stu-id="c54a3-192">-Tag</span></span>
<span data-ttu-id="c54a3-193">A címkéket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="c54a3-193">A hash table which represents tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="c54a3-194">-TenantSettings</span></span>
<span data-ttu-id="c54a3-195">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="c54a3-195">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-196">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c54a3-196">-Confirm</span></span>
<span data-ttu-id="c54a3-197">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c54a3-197">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c54a3-198">-WhatIf</span></span>
<span data-ttu-id="c54a3-199">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c54a3-199">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c54a3-200">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c54a3-200">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c54a3-201">CommonParameters</span></span>
<span data-ttu-id="c54a3-202">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c54a3-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c54a3-203">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c54a3-203">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c54a3-204">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c54a3-204">INPUTS</span></span>

### <span data-ttu-id="c54a3-205">System. String</span><span class="sxs-lookup"><span data-stu-id="c54a3-205">System.String</span></span>

### <span data-ttu-id="c54a3-206">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c54a3-206">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c54a3-207">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c54a3-207">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c54a3-208">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c54a3-208">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c54a3-209">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c54a3-209">OUTPUTS</span></span>

### <span data-ttu-id="c54a3-210">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c54a3-210">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="c54a3-211">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c54a3-211">NOTES</span></span>

## <span data-ttu-id="c54a3-212">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c54a3-212">RELATED LINKS</span></span>

[<span data-ttu-id="c54a3-213">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c54a3-213">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="c54a3-214">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c54a3-214">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c54a3-215">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c54a3-215">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


