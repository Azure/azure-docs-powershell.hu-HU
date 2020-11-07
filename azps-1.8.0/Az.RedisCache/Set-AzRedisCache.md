---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 637a1e634b0f8b6f890519bf4865378f50774e39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669525"
---
# <span data-ttu-id="cc9bc-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc9bc-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="cc9bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc9bc-102">SYNOPSIS</span></span>
<span data-ttu-id="cc9bc-103">Módosítja egy Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="cc9bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc9bc-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc9bc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc9bc-105">DESCRIPTION</span></span>
<span data-ttu-id="cc9bc-106">A **set-AzRedisCache** parancsmag az Azure Redis-gyorsítótárát módosítja.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="cc9bc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cc9bc-107">EXAMPLES</span></span>

### <span data-ttu-id="cc9bc-108">Példa 1: Redis-gyorsítótár módosítása</span><span class="sxs-lookup"><span data-stu-id="cc9bc-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="cc9bc-109">Ez a parancs frissíti a MyCache nevű Redis-gyorsítótár maxmemory-házirendjét.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="cc9bc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc9bc-110">PARAMETERS</span></span>

### <span data-ttu-id="cc9bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc9bc-111">-DefaultProfile</span></span>
<span data-ttu-id="cc9bc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc9bc-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="cc9bc-113">-EnableNonSslPort</span></span>
<span data-ttu-id="cc9bc-114">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="cc9bc-115">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="cc9bc-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="cc9bc-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc9bc-116">-Name</span></span>
<span data-ttu-id="cc9bc-117">A frissítendő Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="cc9bc-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc9bc-118">-RedisConfiguration</span></span>
<span data-ttu-id="cc9bc-119">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="cc9bc-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cc9bc-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc9bc-121">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="cc9bc-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="cc9bc-122">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="cc9bc-123">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="cc9bc-123">Premium tier only.</span></span>
- <span data-ttu-id="cc9bc-124">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="cc9bc-125">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="cc9bc-126">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="cc9bc-126">Premium tier only.</span></span>
- <span data-ttu-id="cc9bc-127">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="cc9bc-128">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="cc9bc-129">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="cc9bc-129">Premium tier only.</span></span> 
- <span data-ttu-id="cc9bc-130">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-130">maxmemory-reserved.</span></span>
<span data-ttu-id="cc9bc-131">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="cc9bc-132">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cc9bc-133">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-133">maxmemory-policy.</span></span>
<span data-ttu-id="cc9bc-134">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="cc9bc-135">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-135">All pricing tiers.</span></span> 
- <span data-ttu-id="cc9bc-136">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-136">notify-keyspace-events.</span></span>
<span data-ttu-id="cc9bc-137">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="cc9bc-138">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="cc9bc-139">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="cc9bc-140">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="cc9bc-141">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cc9bc-142">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="cc9bc-143">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="cc9bc-144">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cc9bc-145">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-145">set-max-intset-entries.</span></span>
<span data-ttu-id="cc9bc-146">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="cc9bc-147">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cc9bc-148">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="cc9bc-149">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="cc9bc-150">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cc9bc-151">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="cc9bc-152">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="cc9bc-153">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cc9bc-154">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-154">databases.</span></span>
<span data-ttu-id="cc9bc-155">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-155">Configures the number of databases.</span></span>
<span data-ttu-id="cc9bc-156">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="cc9bc-157">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="cc9bc-158">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="cc9bc-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="cc9bc-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc9bc-159">-ResourceGroupName</span></span>
<span data-ttu-id="cc9bc-160">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="cc9bc-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="cc9bc-161">-ShardCount</span></span>
<span data-ttu-id="cc9bc-162">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="cc9bc-163">-Méret</span><span class="sxs-lookup"><span data-stu-id="cc9bc-163">-Size</span></span>
<span data-ttu-id="cc9bc-164">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="cc9bc-165">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="cc9bc-165">Valid values are:</span></span> 
- <span data-ttu-id="cc9bc-166">P1</span><span class="sxs-lookup"><span data-stu-id="cc9bc-166">P1</span></span>
- <span data-ttu-id="cc9bc-167">P2</span><span class="sxs-lookup"><span data-stu-id="cc9bc-167">P2</span></span>
- <span data-ttu-id="cc9bc-168">P3</span><span class="sxs-lookup"><span data-stu-id="cc9bc-168">P3</span></span>
- <span data-ttu-id="cc9bc-169">P4</span><span class="sxs-lookup"><span data-stu-id="cc9bc-169">P4</span></span>
- <span data-ttu-id="cc9bc-170">C0</span><span class="sxs-lookup"><span data-stu-id="cc9bc-170">C0</span></span>
- <span data-ttu-id="cc9bc-171">C1</span><span class="sxs-lookup"><span data-stu-id="cc9bc-171">C1</span></span>
- <span data-ttu-id="cc9bc-172">C2</span><span class="sxs-lookup"><span data-stu-id="cc9bc-172">C2</span></span>
- <span data-ttu-id="cc9bc-173">C3</span><span class="sxs-lookup"><span data-stu-id="cc9bc-173">C3</span></span>
- <span data-ttu-id="cc9bc-174">C4</span><span class="sxs-lookup"><span data-stu-id="cc9bc-174">C4</span></span>
- <span data-ttu-id="cc9bc-175">C5</span><span class="sxs-lookup"><span data-stu-id="cc9bc-175">C5</span></span>
- <span data-ttu-id="cc9bc-176">C6</span><span class="sxs-lookup"><span data-stu-id="cc9bc-176">C6</span></span>
- <span data-ttu-id="cc9bc-177">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="cc9bc-177">250MB</span></span>
- <span data-ttu-id="cc9bc-178">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="cc9bc-178">1GB</span></span>
- <span data-ttu-id="cc9bc-179">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="cc9bc-179">2.5GB</span></span>
- <span data-ttu-id="cc9bc-180">6GB</span><span class="sxs-lookup"><span data-stu-id="cc9bc-180">6GB</span></span>
- <span data-ttu-id="cc9bc-181">13GB</span><span class="sxs-lookup"><span data-stu-id="cc9bc-181">13GB</span></span>
- <span data-ttu-id="cc9bc-182">26GB</span><span class="sxs-lookup"><span data-stu-id="cc9bc-182">26GB</span></span>
- <span data-ttu-id="cc9bc-183">53GB az alapértelmezett érték 1GB vagy C1.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="cc9bc-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="cc9bc-184">-Sku</span></span>
<span data-ttu-id="cc9bc-185">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="cc9bc-186">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="cc9bc-186">Valid values are:</span></span> 
- <span data-ttu-id="cc9bc-187">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="cc9bc-187">Basic</span></span>
- <span data-ttu-id="cc9bc-188">Standard</span><span class="sxs-lookup"><span data-stu-id="cc9bc-188">Standard</span></span>
- <span data-ttu-id="cc9bc-189">Prémium: az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="cc9bc-190">-Címke</span><span class="sxs-lookup"><span data-stu-id="cc9bc-190">-Tag</span></span>
<span data-ttu-id="cc9bc-191">A címkéket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="cc9bc-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="cc9bc-192">-TenantSettings</span></span>
<span data-ttu-id="cc9bc-193">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="cc9bc-194">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc9bc-194">-Confirm</span></span>
<span data-ttu-id="cc9bc-195">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc9bc-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc9bc-196">-WhatIf</span></span>
<span data-ttu-id="cc9bc-197">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc9bc-198">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc9bc-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc9bc-199">CommonParameters</span></span>
<span data-ttu-id="cc9bc-200">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc9bc-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc9bc-201">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc9bc-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc9bc-202">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc9bc-202">INPUTS</span></span>

### <span data-ttu-id="cc9bc-203">System. String</span><span class="sxs-lookup"><span data-stu-id="cc9bc-203">System.String</span></span>

### <span data-ttu-id="cc9bc-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cc9bc-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cc9bc-205">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cc9bc-205">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cc9bc-206">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cc9bc-206">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cc9bc-207">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc9bc-207">OUTPUTS</span></span>

### <span data-ttu-id="cc9bc-208">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="cc9bc-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="cc9bc-209">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc9bc-209">NOTES</span></span>

## <span data-ttu-id="cc9bc-210">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc9bc-210">RELATED LINKS</span></span>

[<span data-ttu-id="cc9bc-211">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc9bc-211">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="cc9bc-212">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc9bc-212">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="cc9bc-213">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc9bc-213">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


