---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494719"
---
# <span data-ttu-id="263f8-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="263f8-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="263f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="263f8-102">SYNOPSIS</span></span>
<span data-ttu-id="263f8-103">Módosítja egy Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="263f8-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="263f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="263f8-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="263f8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="263f8-105">DESCRIPTION</span></span>
<span data-ttu-id="263f8-106">A **set-AzureRmRedisCache** parancsmag az Azure Redis-gyorsítótárát módosítja.</span><span class="sxs-lookup"><span data-stu-id="263f8-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="263f8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="263f8-107">EXAMPLES</span></span>

### <span data-ttu-id="263f8-108">Példa 1: Redis-gyorsítótár módosítása</span><span class="sxs-lookup"><span data-stu-id="263f8-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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
```

<span data-ttu-id="263f8-109">Ez a parancs frissíti a MyCache nevű Redis-gyorsítótár maxmemory-házirendjét.</span><span class="sxs-lookup"><span data-stu-id="263f8-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="263f8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="263f8-110">PARAMETERS</span></span>

### <span data-ttu-id="263f8-111">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="263f8-111">-EnableNonSslPort</span></span>
<span data-ttu-id="263f8-112">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="263f8-112">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="263f8-113">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="263f8-113">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="263f8-114">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="263f8-114">-MaxMemoryPolicy</span></span>
<span data-ttu-id="263f8-115">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="263f8-115">This parameter has been deprecated.</span></span>
<span data-ttu-id="263f8-116">A *RedisConfiguration* paraméterrel megadhatja a maxmemory-házirendet.</span><span class="sxs-lookup"><span data-stu-id="263f8-116">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="263f8-117">Példa:</span><span class="sxs-lookup"><span data-stu-id="263f8-117">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### <span data-ttu-id="263f8-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="263f8-118">-Name</span></span>
<span data-ttu-id="263f8-119">A frissítendő Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="263f8-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="263f8-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="263f8-120">-RedisConfiguration</span></span>
<span data-ttu-id="263f8-121">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="263f8-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="263f8-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="263f8-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="263f8-123">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="263f8-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="263f8-124">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="263f8-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="263f8-125">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="263f8-125">Premium tier only.</span></span>
- <span data-ttu-id="263f8-126">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="263f8-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="263f8-127">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="263f8-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="263f8-128">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="263f8-128">Premium tier only.</span></span>
- <span data-ttu-id="263f8-129">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="263f8-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="263f8-130">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="263f8-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="263f8-131">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="263f8-131">Premium tier only.</span></span> 
- <span data-ttu-id="263f8-132">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="263f8-132">maxmemory-reserved.</span></span>
<span data-ttu-id="263f8-133">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="263f8-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="263f8-134">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="263f8-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="263f8-135">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="263f8-135">maxmemory-policy.</span></span>
<span data-ttu-id="263f8-136">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="263f8-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="263f8-137">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="263f8-137">All pricing tiers.</span></span> 
- <span data-ttu-id="263f8-138">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="263f8-138">notify-keyspace-events.</span></span>
<span data-ttu-id="263f8-139">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="263f8-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="263f8-140">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="263f8-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="263f8-141">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="263f8-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="263f8-142">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="263f8-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="263f8-143">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="263f8-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="263f8-144">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="263f8-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="263f8-145">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="263f8-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="263f8-146">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="263f8-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="263f8-147">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="263f8-147">set-max-intset-entries.</span></span>
<span data-ttu-id="263f8-148">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="263f8-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="263f8-149">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="263f8-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="263f8-150">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="263f8-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="263f8-151">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="263f8-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="263f8-152">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="263f8-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="263f8-153">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="263f8-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="263f8-154">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="263f8-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="263f8-155">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="263f8-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="263f8-156">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="263f8-156">databases.</span></span>
<span data-ttu-id="263f8-157">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="263f8-157">Configures the number of databases.</span></span>
<span data-ttu-id="263f8-158">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="263f8-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="263f8-159">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="263f8-159">Standard and Premium tiers.</span></span>

<span data-ttu-id="263f8-160">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="263f8-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="263f8-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="263f8-161">-ResourceGroupName</span></span>
<span data-ttu-id="263f8-162">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="263f8-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="263f8-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="263f8-163">-ShardCount</span></span>
<span data-ttu-id="263f8-164">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="263f8-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="263f8-165">-Méret</span><span class="sxs-lookup"><span data-stu-id="263f8-165">-Size</span></span>
<span data-ttu-id="263f8-166">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="263f8-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="263f8-167">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="263f8-167">Valid values are:</span></span> 

- <span data-ttu-id="263f8-168">P1</span><span class="sxs-lookup"><span data-stu-id="263f8-168">P1</span></span>
- <span data-ttu-id="263f8-169">P2</span><span class="sxs-lookup"><span data-stu-id="263f8-169">P2</span></span>
- <span data-ttu-id="263f8-170">P3</span><span class="sxs-lookup"><span data-stu-id="263f8-170">P3</span></span>
- <span data-ttu-id="263f8-171">P4</span><span class="sxs-lookup"><span data-stu-id="263f8-171">P4</span></span>
- <span data-ttu-id="263f8-172">C0</span><span class="sxs-lookup"><span data-stu-id="263f8-172">C0</span></span>
- <span data-ttu-id="263f8-173">C1</span><span class="sxs-lookup"><span data-stu-id="263f8-173">C1</span></span>
- <span data-ttu-id="263f8-174">C2</span><span class="sxs-lookup"><span data-stu-id="263f8-174">C2</span></span>
- <span data-ttu-id="263f8-175">C3</span><span class="sxs-lookup"><span data-stu-id="263f8-175">C3</span></span>
- <span data-ttu-id="263f8-176">C4</span><span class="sxs-lookup"><span data-stu-id="263f8-176">C4</span></span>
- <span data-ttu-id="263f8-177">C5</span><span class="sxs-lookup"><span data-stu-id="263f8-177">C5</span></span>
- <span data-ttu-id="263f8-178">C6</span><span class="sxs-lookup"><span data-stu-id="263f8-178">C6</span></span>
- <span data-ttu-id="263f8-179">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="263f8-179">250MB</span></span>
- <span data-ttu-id="263f8-180">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="263f8-180">1GB</span></span>
- <span data-ttu-id="263f8-181">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="263f8-181">2.5GB</span></span>
- <span data-ttu-id="263f8-182">6GB</span><span class="sxs-lookup"><span data-stu-id="263f8-182">6GB</span></span>
- <span data-ttu-id="263f8-183">13GB</span><span class="sxs-lookup"><span data-stu-id="263f8-183">13GB</span></span>
- <span data-ttu-id="263f8-184">26GB</span><span class="sxs-lookup"><span data-stu-id="263f8-184">26GB</span></span>
- <span data-ttu-id="263f8-185">53GB</span><span class="sxs-lookup"><span data-stu-id="263f8-185">53GB</span></span>

<span data-ttu-id="263f8-186">Az alapértelmezett érték az 1GB vagy a C1.</span><span class="sxs-lookup"><span data-stu-id="263f8-186">The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="263f8-187">-SKU</span><span class="sxs-lookup"><span data-stu-id="263f8-187">-Sku</span></span>
<span data-ttu-id="263f8-188">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="263f8-188">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="263f8-189">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="263f8-189">Valid values are:</span></span> 

- <span data-ttu-id="263f8-190">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="263f8-190">Basic</span></span>
- <span data-ttu-id="263f8-191">Standard</span><span class="sxs-lookup"><span data-stu-id="263f8-191">Standard</span></span>
- <span data-ttu-id="263f8-192">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="263f8-192">Premium</span></span>

<span data-ttu-id="263f8-193">Az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="263f8-193">The default value is Standard.</span></span>

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

### <span data-ttu-id="263f8-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="263f8-194">-TenantSettings</span></span>
<span data-ttu-id="263f8-195">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="263f8-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="263f8-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="263f8-196">-DefaultProfile</span></span>
<span data-ttu-id="263f8-197">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="263f8-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263f8-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263f8-198">CommonParameters</span></span>
<span data-ttu-id="263f8-199">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="263f8-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263f8-200">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="263f8-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263f8-201">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="263f8-201">INPUTS</span></span>

### <span data-ttu-id="263f8-202">Nincs</span><span class="sxs-lookup"><span data-stu-id="263f8-202">None</span></span>
<span data-ttu-id="263f8-203">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="263f8-203">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="263f8-204">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="263f8-204">OUTPUTS</span></span>

### <span data-ttu-id="263f8-205">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="263f8-205">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="263f8-206">A Redis-gyorsítótár összes attribútumát számítja ki, az elsődleges és másodlagos elérési kulcsokat is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="263f8-206">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="263f8-207">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="263f8-207">NOTES</span></span>

## <span data-ttu-id="263f8-208">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="263f8-208">RELATED LINKS</span></span>

[<span data-ttu-id="263f8-209">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="263f8-209">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="263f8-210">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="263f8-210">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="263f8-211">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="263f8-211">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


