---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 951198c93918c08f69f28dc6db3c5fe605e6d3bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495281"
---
# <span data-ttu-id="6cf09-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cf09-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="6cf09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cf09-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf09-103">Módosítja egy Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="6cf09-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cf09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cf09-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cf09-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cf09-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf09-106">A **set-AzureRmRedisCache** parancsmag az Azure Redis-gyorsítótárát módosítja.</span><span class="sxs-lookup"><span data-stu-id="6cf09-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="6cf09-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6cf09-107">EXAMPLES</span></span>

### <span data-ttu-id="6cf09-108">Példa 1: Redis-gyorsítótár módosítása</span><span class="sxs-lookup"><span data-stu-id="6cf09-108">Example 1: Modify a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="6cf09-109">Ez a parancs frissíti a MyCache nevű Redis-gyorsítótár maxmemory-házirendjét.</span><span class="sxs-lookup"><span data-stu-id="6cf09-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="6cf09-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cf09-110">PARAMETERS</span></span>

### <span data-ttu-id="6cf09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf09-111">-DefaultProfile</span></span>
<span data-ttu-id="6cf09-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cf09-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="6cf09-113">-EnableNonSslPort</span></span>
<span data-ttu-id="6cf09-114">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="6cf09-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="6cf09-115">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="6cf09-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-116">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="6cf09-116">-MaxMemoryPolicy</span></span>
<span data-ttu-id="6cf09-117">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="6cf09-117">This parameter has been deprecated.</span></span>
<span data-ttu-id="6cf09-118">A *RedisConfiguration* paraméterrel megadhatja a maxmemory-házirendet.</span><span class="sxs-lookup"><span data-stu-id="6cf09-118">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="6cf09-119">Példa:</span><span class="sxs-lookup"><span data-stu-id="6cf09-119">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6cf09-120">-Name</span></span>
<span data-ttu-id="6cf09-121">A frissítendő Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cf09-121">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-122">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cf09-122">-RedisConfiguration</span></span>
<span data-ttu-id="6cf09-123">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cf09-123">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="6cf09-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6cf09-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6cf09-125">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="6cf09-125">rdb-backup-enabled.</span></span>
<span data-ttu-id="6cf09-126">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="6cf09-126">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="6cf09-127">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="6cf09-127">Premium tier only.</span></span>
- <span data-ttu-id="6cf09-128">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="6cf09-128">rdb-storage-connection-string.</span></span>
<span data-ttu-id="6cf09-129">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cf09-129">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="6cf09-130">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="6cf09-130">Premium tier only.</span></span>
- <span data-ttu-id="6cf09-131">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="6cf09-131">rdb-backup-frequency.</span></span>
<span data-ttu-id="6cf09-132">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cf09-132">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="6cf09-133">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="6cf09-133">Premium tier only.</span></span> 
- <span data-ttu-id="6cf09-134">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="6cf09-134">maxmemory-reserved.</span></span>
<span data-ttu-id="6cf09-135">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="6cf09-135">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="6cf09-136">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="6cf09-136">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cf09-137">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="6cf09-137">maxmemory-policy.</span></span>
<span data-ttu-id="6cf09-138">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="6cf09-138">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="6cf09-139">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="6cf09-139">All pricing tiers.</span></span> 
- <span data-ttu-id="6cf09-140">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="6cf09-140">notify-keyspace-events.</span></span>
<span data-ttu-id="6cf09-141">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="6cf09-141">Configures keyspace notifications.</span></span>
<span data-ttu-id="6cf09-142">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="6cf09-142">Standard and premium tiers.</span></span> 
- <span data-ttu-id="6cf09-143">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="6cf09-143">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="6cf09-144">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="6cf09-144">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cf09-145">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="6cf09-145">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cf09-146">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="6cf09-146">hash-max-ziplist-value.</span></span>
<span data-ttu-id="6cf09-147">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="6cf09-147">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cf09-148">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="6cf09-148">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cf09-149">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="6cf09-149">set-max-intset-entries.</span></span>
<span data-ttu-id="6cf09-150">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="6cf09-150">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cf09-151">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="6cf09-151">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cf09-152">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="6cf09-152">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="6cf09-153">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="6cf09-153">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cf09-154">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="6cf09-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cf09-155">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="6cf09-155">zset-max-ziplist-value.</span></span>
<span data-ttu-id="6cf09-156">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="6cf09-156">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cf09-157">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="6cf09-157">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cf09-158">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="6cf09-158">databases.</span></span>
<span data-ttu-id="6cf09-159">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="6cf09-159">Configures the number of databases.</span></span>
<span data-ttu-id="6cf09-160">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="6cf09-160">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="6cf09-161">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="6cf09-161">Standard and Premium tiers.</span></span>

<span data-ttu-id="6cf09-162">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="6cf09-162">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf09-163">-ResourceGroupName</span></span>
<span data-ttu-id="6cf09-164">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cf09-164">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-165">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="6cf09-165">-ShardCount</span></span>
<span data-ttu-id="6cf09-166">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cf09-166">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-167">-Méret</span><span class="sxs-lookup"><span data-stu-id="6cf09-167">-Size</span></span>
<span data-ttu-id="6cf09-168">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cf09-168">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="6cf09-169">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="6cf09-169">Valid values are:</span></span> 

- <span data-ttu-id="6cf09-170">P1</span><span class="sxs-lookup"><span data-stu-id="6cf09-170">P1</span></span>
- <span data-ttu-id="6cf09-171">P2</span><span class="sxs-lookup"><span data-stu-id="6cf09-171">P2</span></span>
- <span data-ttu-id="6cf09-172">P3</span><span class="sxs-lookup"><span data-stu-id="6cf09-172">P3</span></span>
- <span data-ttu-id="6cf09-173">P4</span><span class="sxs-lookup"><span data-stu-id="6cf09-173">P4</span></span>
- <span data-ttu-id="6cf09-174">C0</span><span class="sxs-lookup"><span data-stu-id="6cf09-174">C0</span></span>
- <span data-ttu-id="6cf09-175">C1</span><span class="sxs-lookup"><span data-stu-id="6cf09-175">C1</span></span>
- <span data-ttu-id="6cf09-176">C2</span><span class="sxs-lookup"><span data-stu-id="6cf09-176">C2</span></span>
- <span data-ttu-id="6cf09-177">C3</span><span class="sxs-lookup"><span data-stu-id="6cf09-177">C3</span></span>
- <span data-ttu-id="6cf09-178">C4</span><span class="sxs-lookup"><span data-stu-id="6cf09-178">C4</span></span>
- <span data-ttu-id="6cf09-179">C5</span><span class="sxs-lookup"><span data-stu-id="6cf09-179">C5</span></span>
- <span data-ttu-id="6cf09-180">C6</span><span class="sxs-lookup"><span data-stu-id="6cf09-180">C6</span></span>
- <span data-ttu-id="6cf09-181">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="6cf09-181">250MB</span></span>
- <span data-ttu-id="6cf09-182">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="6cf09-182">1GB</span></span>
- <span data-ttu-id="6cf09-183">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="6cf09-183">2.5GB</span></span>
- <span data-ttu-id="6cf09-184">6GB</span><span class="sxs-lookup"><span data-stu-id="6cf09-184">6GB</span></span>
- <span data-ttu-id="6cf09-185">13GB</span><span class="sxs-lookup"><span data-stu-id="6cf09-185">13GB</span></span>
- <span data-ttu-id="6cf09-186">26GB</span><span class="sxs-lookup"><span data-stu-id="6cf09-186">26GB</span></span>
- <span data-ttu-id="6cf09-187">53GB</span><span class="sxs-lookup"><span data-stu-id="6cf09-187">53GB</span></span>

<span data-ttu-id="6cf09-188">Az alapértelmezett érték az 1GB vagy a C1.</span><span class="sxs-lookup"><span data-stu-id="6cf09-188">The default value is 1GB or C1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-189">-SKU</span><span class="sxs-lookup"><span data-stu-id="6cf09-189">-Sku</span></span>
<span data-ttu-id="6cf09-190">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="6cf09-190">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="6cf09-191">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="6cf09-191">Valid values are:</span></span> 

- <span data-ttu-id="6cf09-192">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="6cf09-192">Basic</span></span>
- <span data-ttu-id="6cf09-193">Standard</span><span class="sxs-lookup"><span data-stu-id="6cf09-193">Standard</span></span>
- <span data-ttu-id="6cf09-194">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="6cf09-194">Premium</span></span>

<span data-ttu-id="6cf09-195">Az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="6cf09-195">The default value is Standard.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-196">-Címke</span><span class="sxs-lookup"><span data-stu-id="6cf09-196">-Tag</span></span>
<span data-ttu-id="6cf09-197">A címkéket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="6cf09-197">A hash table which represents tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-198">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="6cf09-198">-TenantSettings</span></span>
<span data-ttu-id="6cf09-199">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="6cf09-199">This parameter has been deprecated.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-200">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6cf09-200">-Confirm</span></span>
<span data-ttu-id="6cf09-201">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6cf09-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cf09-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cf09-202">-WhatIf</span></span>
<span data-ttu-id="6cf09-203">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6cf09-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cf09-204">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cf09-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cf09-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf09-205">CommonParameters</span></span>
<span data-ttu-id="6cf09-206">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cf09-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf09-207">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cf09-207">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf09-208">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cf09-208">INPUTS</span></span>

### <span data-ttu-id="6cf09-209">Nincs</span><span class="sxs-lookup"><span data-stu-id="6cf09-209">None</span></span>
<span data-ttu-id="6cf09-210">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="6cf09-210">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="6cf09-211">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cf09-211">OUTPUTS</span></span>

### <span data-ttu-id="6cf09-212">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="6cf09-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="6cf09-213">A Redis-gyorsítótár összes attribútumát számítja ki, az elsődleges és másodlagos elérési kulcsokat is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="6cf09-213">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="6cf09-214">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cf09-214">NOTES</span></span>

## <span data-ttu-id="6cf09-215">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cf09-215">RELATED LINKS</span></span>

[<span data-ttu-id="6cf09-216">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cf09-216">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="6cf09-217">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cf09-217">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="6cf09-218">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cf09-218">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


