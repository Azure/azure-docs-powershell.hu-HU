---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672420"
---
# <span data-ttu-id="dbade-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbade-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="dbade-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dbade-102">SYNOPSIS</span></span>
<span data-ttu-id="dbade-103">Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dbade-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbade-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dbade-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbade-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dbade-105">DESCRIPTION</span></span>
<span data-ttu-id="dbade-106">A **New-AzureRmRedisCache** parancsmag Azure Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dbade-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="dbade-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dbade-107">EXAMPLES</span></span>

### <span data-ttu-id="dbade-108">Példa 1: Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="dbade-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
```

<span data-ttu-id="dbade-109">Ez a parancs Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dbade-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="dbade-110">2. példa: szabványos SKU Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="dbade-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
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

<span data-ttu-id="dbade-111">Ez a parancs létrehoz egy Redis-gyorsítótárat, vagy ha már létezik, frissíti a Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="dbade-111">This command creates a Redis Cache or updates the Redis Cache if it already exists.</span></span>

## <span data-ttu-id="dbade-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dbade-112">PARAMETERS</span></span>

### <span data-ttu-id="dbade-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="dbade-113">-EnableNonSslPort</span></span>
<span data-ttu-id="dbade-114">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="dbade-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="dbade-115">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="dbade-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="dbade-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="dbade-116">-Location</span></span>
<span data-ttu-id="dbade-117">A Redis-gyorsítótár létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbade-117">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="dbade-118">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dbade-118">Valid values are:</span></span> 

- <span data-ttu-id="dbade-119">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="dbade-119">North Central US</span></span>
- <span data-ttu-id="dbade-120">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="dbade-120">South Central US</span></span>
- <span data-ttu-id="dbade-121">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="dbade-121">Central US</span></span>
- <span data-ttu-id="dbade-122">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="dbade-122">West Europe</span></span>
- <span data-ttu-id="dbade-123">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="dbade-123">North Europe</span></span>
- <span data-ttu-id="dbade-124">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="dbade-124">West US</span></span>
- <span data-ttu-id="dbade-125">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="dbade-125">East US</span></span>
- <span data-ttu-id="dbade-126">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="dbade-126">East US 2</span></span>
- <span data-ttu-id="dbade-127">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="dbade-127">Japan East</span></span>
- <span data-ttu-id="dbade-128">Japán West</span><span class="sxs-lookup"><span data-stu-id="dbade-128">Japan West</span></span>
- <span data-ttu-id="dbade-129">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="dbade-129">Brazil South</span></span>
- <span data-ttu-id="dbade-130">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="dbade-130">Southeast Asia</span></span>
- <span data-ttu-id="dbade-131">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="dbade-131">East Asia</span></span>
- <span data-ttu-id="dbade-132">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="dbade-132">Australia East</span></span>
- <span data-ttu-id="dbade-133">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="dbade-133">Australia Southeast</span></span>

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

### <span data-ttu-id="dbade-134">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="dbade-134">-MaxMemoryPolicy</span></span>
<span data-ttu-id="dbade-135">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="dbade-135">This parameter has been deprecated.</span></span>
<span data-ttu-id="dbade-136">A *RedisConfiguration* paraméterrel megadhatja a maxmemory-házirendet.</span><span class="sxs-lookup"><span data-stu-id="dbade-136">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="dbade-137">Példa:</span><span class="sxs-lookup"><span data-stu-id="dbade-137">For example:</span></span> 

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

### <span data-ttu-id="dbade-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dbade-138">-Name</span></span>
<span data-ttu-id="dbade-139">A létrehozandó Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbade-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="dbade-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbade-140">-RedisConfiguration</span></span>
<span data-ttu-id="dbade-141">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbade-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="dbade-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dbade-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dbade-143">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="dbade-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="dbade-144">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="dbade-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="dbade-145">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="dbade-145">Premium tier only.</span></span>
- <span data-ttu-id="dbade-146">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="dbade-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="dbade-147">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbade-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="dbade-148">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="dbade-148">Premium tier only.</span></span>
- <span data-ttu-id="dbade-149">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="dbade-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="dbade-150">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbade-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="dbade-151">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="dbade-151">Premium tier only.</span></span> 
- <span data-ttu-id="dbade-152">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="dbade-152">maxmemory-reserved.</span></span>
<span data-ttu-id="dbade-153">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="dbade-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="dbade-154">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbade-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbade-155">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="dbade-155">maxmemory-policy.</span></span>
<span data-ttu-id="dbade-156">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="dbade-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="dbade-157">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="dbade-157">All pricing tiers.</span></span> 
- <span data-ttu-id="dbade-158">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="dbade-158">notify-keyspace-events.</span></span>
<span data-ttu-id="dbade-159">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="dbade-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="dbade-160">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbade-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="dbade-161">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="dbade-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="dbade-162">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="dbade-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dbade-163">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbade-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbade-164">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="dbade-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="dbade-165">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="dbade-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dbade-166">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbade-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbade-167">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="dbade-167">set-max-intset-entries.</span></span>
<span data-ttu-id="dbade-168">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="dbade-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dbade-169">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbade-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbade-170">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="dbade-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="dbade-171">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="dbade-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dbade-172">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbade-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbade-173">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="dbade-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="dbade-174">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="dbade-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dbade-175">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbade-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbade-176">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="dbade-176">databases.</span></span>
<span data-ttu-id="dbade-177">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="dbade-177">Configures the number of databases.</span></span>
<span data-ttu-id="dbade-178">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="dbade-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="dbade-179">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbade-179">Standard and Premium tiers.</span></span>

<span data-ttu-id="dbade-180">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="dbade-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="dbade-181">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="dbade-181">-RedisVersion</span></span>
<span data-ttu-id="dbade-182">Ez a paraméter elavult, és a jövőbeli kiadásokból törlődik.</span><span class="sxs-lookup"><span data-stu-id="dbade-182">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="dbade-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbade-183">-ResourceGroupName</span></span>
<span data-ttu-id="dbade-184">Annak az erőforráscsoportnek a nevét adja meg, amelybe a Redis-gyorsítótárat létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="dbade-184">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="dbade-185">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="dbade-185">-ShardCount</span></span>
<span data-ttu-id="dbade-186">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbade-186">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="dbade-187">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dbade-187">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dbade-188">1</span><span class="sxs-lookup"><span data-stu-id="dbade-188">1</span></span>
- <span data-ttu-id="dbade-189">2</span><span class="sxs-lookup"><span data-stu-id="dbade-189">2</span></span>
- <span data-ttu-id="dbade-190">3</span><span class="sxs-lookup"><span data-stu-id="dbade-190">3</span></span>
- <span data-ttu-id="dbade-191">4</span><span class="sxs-lookup"><span data-stu-id="dbade-191">4</span></span>
- <span data-ttu-id="dbade-192">5</span><span class="sxs-lookup"><span data-stu-id="dbade-192">5</span></span>
- <span data-ttu-id="dbade-193">6</span><span class="sxs-lookup"><span data-stu-id="dbade-193">6</span></span>
- <span data-ttu-id="dbade-194">7</span><span class="sxs-lookup"><span data-stu-id="dbade-194">7</span></span>
- <span data-ttu-id="dbade-195">8</span><span class="sxs-lookup"><span data-stu-id="dbade-195">8</span></span>
- <span data-ttu-id="dbade-196">9</span><span class="sxs-lookup"><span data-stu-id="dbade-196">9</span></span> 
- <span data-ttu-id="dbade-197">10</span><span class="sxs-lookup"><span data-stu-id="dbade-197">10</span></span>

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

### <span data-ttu-id="dbade-198">-Méret</span><span class="sxs-lookup"><span data-stu-id="dbade-198">-Size</span></span>
<span data-ttu-id="dbade-199">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbade-199">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="dbade-200">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dbade-200">Valid values are:</span></span> 

- <span data-ttu-id="dbade-201">P1</span><span class="sxs-lookup"><span data-stu-id="dbade-201">P1</span></span>
- <span data-ttu-id="dbade-202">P2</span><span class="sxs-lookup"><span data-stu-id="dbade-202">P2</span></span>
- <span data-ttu-id="dbade-203">P3</span><span class="sxs-lookup"><span data-stu-id="dbade-203">P3</span></span>
- <span data-ttu-id="dbade-204">P4</span><span class="sxs-lookup"><span data-stu-id="dbade-204">P4</span></span>
- <span data-ttu-id="dbade-205">C0</span><span class="sxs-lookup"><span data-stu-id="dbade-205">C0</span></span>
- <span data-ttu-id="dbade-206">C1</span><span class="sxs-lookup"><span data-stu-id="dbade-206">C1</span></span>
- <span data-ttu-id="dbade-207">C2</span><span class="sxs-lookup"><span data-stu-id="dbade-207">C2</span></span>
- <span data-ttu-id="dbade-208">C3</span><span class="sxs-lookup"><span data-stu-id="dbade-208">C3</span></span>
- <span data-ttu-id="dbade-209">C4</span><span class="sxs-lookup"><span data-stu-id="dbade-209">C4</span></span>
- <span data-ttu-id="dbade-210">C5</span><span class="sxs-lookup"><span data-stu-id="dbade-210">C5</span></span>
- <span data-ttu-id="dbade-211">C6</span><span class="sxs-lookup"><span data-stu-id="dbade-211">C6</span></span>
- <span data-ttu-id="dbade-212">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="dbade-212">250MB</span></span>
- <span data-ttu-id="dbade-213">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="dbade-213">1GB</span></span>
- <span data-ttu-id="dbade-214">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="dbade-214">2.5GB</span></span>
- <span data-ttu-id="dbade-215">6GB</span><span class="sxs-lookup"><span data-stu-id="dbade-215">6GB</span></span>
- <span data-ttu-id="dbade-216">13GB</span><span class="sxs-lookup"><span data-stu-id="dbade-216">13GB</span></span>
- <span data-ttu-id="dbade-217">26GB</span><span class="sxs-lookup"><span data-stu-id="dbade-217">26GB</span></span>
- <span data-ttu-id="dbade-218">53GB</span><span class="sxs-lookup"><span data-stu-id="dbade-218">53GB</span></span>

<span data-ttu-id="dbade-219">Az alapértelmezett érték az 1GB vagy a C1.</span><span class="sxs-lookup"><span data-stu-id="dbade-219">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="dbade-220">-SKU</span><span class="sxs-lookup"><span data-stu-id="dbade-220">-Sku</span></span>
<span data-ttu-id="dbade-221">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="dbade-221">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="dbade-222">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dbade-222">Valid values are:</span></span> 

- <span data-ttu-id="dbade-223">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="dbade-223">Basic</span></span>
- <span data-ttu-id="dbade-224">Standard</span><span class="sxs-lookup"><span data-stu-id="dbade-224">Standard</span></span>
- <span data-ttu-id="dbade-225">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="dbade-225">Premium</span></span>

<span data-ttu-id="dbade-226">Az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="dbade-226">The default value is Standard.</span></span>

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

### <span data-ttu-id="dbade-227">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="dbade-227">-StaticIP</span></span>
<span data-ttu-id="dbade-228">Egy egyedi IP-címet ad meg a Redis-gyorsítótár alhálózatában.</span><span class="sxs-lookup"><span data-stu-id="dbade-228">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="dbade-229">Ha nem ad meg értéket ehhez a paraméterhez, ez a parancsmag egy IP-címet választ az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="dbade-229">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="dbade-230">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="dbade-230">-Subnet</span></span>
<span data-ttu-id="dbade-231">Annak az alhálózatnak a neve, amelybe a Redis-gyorsítótárat telepíteni kell.</span><span class="sxs-lookup"><span data-stu-id="dbade-231">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="dbade-232">– NetI</span><span class="sxs-lookup"><span data-stu-id="dbade-232">-SubnetId</span></span>
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

### <span data-ttu-id="dbade-233">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="dbade-233">-TenantSettings</span></span>
<span data-ttu-id="dbade-234">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="dbade-234">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="dbade-235">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dbade-235">-VirtualNetwork</span></span>
<span data-ttu-id="dbade-236">Annak a virtuális hálózatnak az erőforrás-AZONOSÍTÓját adja meg, amelybe telepíteni szeretné a Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="dbade-236">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="dbade-237">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbade-237">-DefaultProfile</span></span>
<span data-ttu-id="dbade-238">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dbade-238">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbade-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbade-239">CommonParameters</span></span>
<span data-ttu-id="dbade-240">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dbade-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbade-241">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbade-241">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbade-242">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbade-242">INPUTS</span></span>

### <span data-ttu-id="dbade-243">Nincs</span><span class="sxs-lookup"><span data-stu-id="dbade-243">None</span></span>
<span data-ttu-id="dbade-244">A parancsmagot név szerint, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="dbade-244">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="dbade-245">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbade-245">OUTPUTS</span></span>

### <span data-ttu-id="dbade-246">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="dbade-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="dbade-247">Ez a parancsmag a Redis-gyorsítótár minden attribútumát megjeleníti, az elsődleges és másodlagos elérési kulcsokat is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="dbade-247">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="dbade-248">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dbade-248">NOTES</span></span>

## <span data-ttu-id="dbade-249">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbade-249">RELATED LINKS</span></span>

[<span data-ttu-id="dbade-250">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbade-250">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="dbade-251">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbade-251">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="dbade-252">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbade-252">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


