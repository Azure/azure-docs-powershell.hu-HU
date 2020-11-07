---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846922"
---
# <span data-ttu-id="018c7-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="018c7-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="018c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="018c7-102">SYNOPSIS</span></span>
<span data-ttu-id="018c7-103">Módosítja egy Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="018c7-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="018c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="018c7-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="018c7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="018c7-105">DESCRIPTION</span></span>
<span data-ttu-id="018c7-106">A **set-AzRedisCache** parancsmag az Azure Redis-gyorsítótárát módosítja.</span><span class="sxs-lookup"><span data-stu-id="018c7-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="018c7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="018c7-107">EXAMPLES</span></span>

### <span data-ttu-id="018c7-108">Példa 1: Redis-gyorsítótár módosítása</span><span class="sxs-lookup"><span data-stu-id="018c7-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="018c7-109">Ez a parancs frissíti a MyCache nevű Redis-gyorsítótár maxmemory-házirendjét.</span><span class="sxs-lookup"><span data-stu-id="018c7-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="018c7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="018c7-110">PARAMETERS</span></span>

### <span data-ttu-id="018c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018c7-111">-DefaultProfile</span></span>
<span data-ttu-id="018c7-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="018c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="018c7-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="018c7-113">-EnableNonSslPort</span></span>
<span data-ttu-id="018c7-114">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="018c7-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="018c7-115">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="018c7-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="018c7-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="018c7-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="018c7-117">Adja meg az ügyfelek által a gyorsítótárhoz való csatlakozáshoz szükséges TLS-verziót.</span><span class="sxs-lookup"><span data-stu-id="018c7-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="018c7-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="018c7-118">-Name</span></span>
<span data-ttu-id="018c7-119">A frissítendő Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="018c7-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="018c7-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="018c7-120">-RedisConfiguration</span></span>
<span data-ttu-id="018c7-121">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="018c7-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="018c7-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="018c7-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="018c7-123">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="018c7-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="018c7-124">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="018c7-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="018c7-125">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="018c7-125">Premium tier only.</span></span>
- <span data-ttu-id="018c7-126">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="018c7-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="018c7-127">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="018c7-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="018c7-128">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="018c7-128">Premium tier only.</span></span>
- <span data-ttu-id="018c7-129">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="018c7-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="018c7-130">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="018c7-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="018c7-131">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="018c7-131">Premium tier only.</span></span> 
- <span data-ttu-id="018c7-132">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="018c7-132">maxmemory-reserved.</span></span>
<span data-ttu-id="018c7-133">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="018c7-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="018c7-134">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="018c7-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="018c7-135">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="018c7-135">maxmemory-policy.</span></span>
<span data-ttu-id="018c7-136">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="018c7-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="018c7-137">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="018c7-137">All pricing tiers.</span></span> 
- <span data-ttu-id="018c7-138">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="018c7-138">notify-keyspace-events.</span></span>
<span data-ttu-id="018c7-139">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="018c7-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="018c7-140">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="018c7-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="018c7-141">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="018c7-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="018c7-142">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="018c7-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="018c7-143">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="018c7-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="018c7-144">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="018c7-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="018c7-145">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="018c7-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="018c7-146">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="018c7-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="018c7-147">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="018c7-147">set-max-intset-entries.</span></span>
<span data-ttu-id="018c7-148">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="018c7-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="018c7-149">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="018c7-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="018c7-150">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="018c7-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="018c7-151">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="018c7-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="018c7-152">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="018c7-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="018c7-153">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="018c7-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="018c7-154">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="018c7-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="018c7-155">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="018c7-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="018c7-156">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="018c7-156">databases.</span></span>
<span data-ttu-id="018c7-157">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="018c7-157">Configures the number of databases.</span></span>
<span data-ttu-id="018c7-158">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="018c7-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="018c7-159">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="018c7-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="018c7-160">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="018c7-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="018c7-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="018c7-161">-ResourceGroupName</span></span>
<span data-ttu-id="018c7-162">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="018c7-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="018c7-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="018c7-163">-ShardCount</span></span>
<span data-ttu-id="018c7-164">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="018c7-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="018c7-165">-Méret</span><span class="sxs-lookup"><span data-stu-id="018c7-165">-Size</span></span>
<span data-ttu-id="018c7-166">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="018c7-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="018c7-167">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="018c7-167">Valid values are:</span></span> 
- <span data-ttu-id="018c7-168">P1</span><span class="sxs-lookup"><span data-stu-id="018c7-168">P1</span></span>
- <span data-ttu-id="018c7-169">P2</span><span class="sxs-lookup"><span data-stu-id="018c7-169">P2</span></span>
- <span data-ttu-id="018c7-170">P3</span><span class="sxs-lookup"><span data-stu-id="018c7-170">P3</span></span>
- <span data-ttu-id="018c7-171">P4</span><span class="sxs-lookup"><span data-stu-id="018c7-171">P4</span></span>
- <span data-ttu-id="018c7-172">P5</span><span class="sxs-lookup"><span data-stu-id="018c7-172">P5</span></span>
- <span data-ttu-id="018c7-173">C0</span><span class="sxs-lookup"><span data-stu-id="018c7-173">C0</span></span>
- <span data-ttu-id="018c7-174">C1</span><span class="sxs-lookup"><span data-stu-id="018c7-174">C1</span></span>
- <span data-ttu-id="018c7-175">C2</span><span class="sxs-lookup"><span data-stu-id="018c7-175">C2</span></span>
- <span data-ttu-id="018c7-176">C3</span><span class="sxs-lookup"><span data-stu-id="018c7-176">C3</span></span>
- <span data-ttu-id="018c7-177">C4</span><span class="sxs-lookup"><span data-stu-id="018c7-177">C4</span></span>
- <span data-ttu-id="018c7-178">C5</span><span class="sxs-lookup"><span data-stu-id="018c7-178">C5</span></span>
- <span data-ttu-id="018c7-179">C6</span><span class="sxs-lookup"><span data-stu-id="018c7-179">C6</span></span>
- <span data-ttu-id="018c7-180">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="018c7-180">250MB</span></span>
- <span data-ttu-id="018c7-181">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="018c7-181">1GB</span></span>
- <span data-ttu-id="018c7-182">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="018c7-182">2.5GB</span></span>
- <span data-ttu-id="018c7-183">6GB</span><span class="sxs-lookup"><span data-stu-id="018c7-183">6GB</span></span>
- <span data-ttu-id="018c7-184">13GB</span><span class="sxs-lookup"><span data-stu-id="018c7-184">13GB</span></span>
- <span data-ttu-id="018c7-185">26GB</span><span class="sxs-lookup"><span data-stu-id="018c7-185">26GB</span></span>
- <span data-ttu-id="018c7-186">53GB</span><span class="sxs-lookup"><span data-stu-id="018c7-186">53GB</span></span>
- <span data-ttu-id="018c7-187">120 MB: az alapértelmezett érték az 1GB vagy a C1.</span><span class="sxs-lookup"><span data-stu-id="018c7-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="018c7-188">-SKU</span><span class="sxs-lookup"><span data-stu-id="018c7-188">-Sku</span></span>
<span data-ttu-id="018c7-189">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="018c7-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="018c7-190">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="018c7-190">Valid values are:</span></span> 
- <span data-ttu-id="018c7-191">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="018c7-191">Basic</span></span>
- <span data-ttu-id="018c7-192">Standard</span><span class="sxs-lookup"><span data-stu-id="018c7-192">Standard</span></span>
- <span data-ttu-id="018c7-193">Prémium: az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="018c7-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="018c7-194">-Címke</span><span class="sxs-lookup"><span data-stu-id="018c7-194">-Tag</span></span>
<span data-ttu-id="018c7-195">A címkéket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="018c7-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="018c7-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="018c7-196">-TenantSettings</span></span>
<span data-ttu-id="018c7-197">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="018c7-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="018c7-198">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="018c7-198">-Confirm</span></span>
<span data-ttu-id="018c7-199">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="018c7-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="018c7-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="018c7-200">-WhatIf</span></span>
<span data-ttu-id="018c7-201">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="018c7-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="018c7-202">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="018c7-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="018c7-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018c7-203">CommonParameters</span></span>
<span data-ttu-id="018c7-204">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="018c7-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018c7-205">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="018c7-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018c7-206">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="018c7-206">INPUTS</span></span>

### <span data-ttu-id="018c7-207">System. String</span><span class="sxs-lookup"><span data-stu-id="018c7-207">System.String</span></span>

### <span data-ttu-id="018c7-208">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="018c7-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="018c7-209">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="018c7-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="018c7-210">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="018c7-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="018c7-211">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="018c7-211">OUTPUTS</span></span>

### <span data-ttu-id="018c7-212">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="018c7-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="018c7-213">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="018c7-213">NOTES</span></span>

## <span data-ttu-id="018c7-214">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="018c7-214">RELATED LINKS</span></span>

[<span data-ttu-id="018c7-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="018c7-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="018c7-216">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="018c7-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="018c7-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="018c7-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


