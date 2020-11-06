---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 484c72dd77ada862536b064cb2bcaec07ef51bb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503423"
---
# <span data-ttu-id="2b52e-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2b52e-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="2b52e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b52e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b52e-103">Módosítja egy Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="2b52e-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b52e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b52e-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b52e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b52e-105">DESCRIPTION</span></span>
<span data-ttu-id="2b52e-106">A **set-AzureRmRedisCache** parancsmag az Azure Redis-gyorsítótárát módosítja.</span><span class="sxs-lookup"><span data-stu-id="2b52e-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="2b52e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2b52e-107">EXAMPLES</span></span>

### <span data-ttu-id="2b52e-108">Példa 1: Redis-gyorsítótár módosítása</span><span class="sxs-lookup"><span data-stu-id="2b52e-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="2b52e-109">Ez a parancs frissíti a MyCache nevű Redis-gyorsítótár maxmemory-házirendjét.</span><span class="sxs-lookup"><span data-stu-id="2b52e-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="2b52e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b52e-110">PARAMETERS</span></span>

### <span data-ttu-id="2b52e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b52e-111">-DefaultProfile</span></span>
<span data-ttu-id="2b52e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b52e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b52e-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="2b52e-113">-EnableNonSslPort</span></span>
<span data-ttu-id="2b52e-114">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="2b52e-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="2b52e-115">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="2b52e-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="2b52e-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b52e-116">-Name</span></span>
<span data-ttu-id="2b52e-117">A frissítendő Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b52e-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="2b52e-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b52e-118">-RedisConfiguration</span></span>
<span data-ttu-id="2b52e-119">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b52e-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="2b52e-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2b52e-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b52e-121">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="2b52e-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="2b52e-122">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2b52e-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="2b52e-123">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="2b52e-123">Premium tier only.</span></span>
- <span data-ttu-id="2b52e-124">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="2b52e-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="2b52e-125">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b52e-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="2b52e-126">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="2b52e-126">Premium tier only.</span></span>
- <span data-ttu-id="2b52e-127">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="2b52e-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="2b52e-128">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b52e-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="2b52e-129">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="2b52e-129">Premium tier only.</span></span> 
- <span data-ttu-id="2b52e-130">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="2b52e-130">maxmemory-reserved.</span></span>
<span data-ttu-id="2b52e-131">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="2b52e-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="2b52e-132">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2b52e-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2b52e-133">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="2b52e-133">maxmemory-policy.</span></span>
<span data-ttu-id="2b52e-134">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="2b52e-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="2b52e-135">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="2b52e-135">All pricing tiers.</span></span> 
- <span data-ttu-id="2b52e-136">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="2b52e-136">notify-keyspace-events.</span></span>
<span data-ttu-id="2b52e-137">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="2b52e-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="2b52e-138">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2b52e-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="2b52e-139">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="2b52e-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="2b52e-140">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="2b52e-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2b52e-141">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2b52e-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2b52e-142">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="2b52e-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="2b52e-143">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="2b52e-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2b52e-144">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2b52e-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2b52e-145">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="2b52e-145">set-max-intset-entries.</span></span>
<span data-ttu-id="2b52e-146">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="2b52e-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2b52e-147">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2b52e-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2b52e-148">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="2b52e-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="2b52e-149">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="2b52e-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2b52e-150">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2b52e-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2b52e-151">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="2b52e-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="2b52e-152">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="2b52e-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2b52e-153">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2b52e-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2b52e-154">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="2b52e-154">databases.</span></span>
<span data-ttu-id="2b52e-155">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="2b52e-155">Configures the number of databases.</span></span>
<span data-ttu-id="2b52e-156">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="2b52e-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="2b52e-157">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2b52e-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="2b52e-158">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="2b52e-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="2b52e-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b52e-159">-ResourceGroupName</span></span>
<span data-ttu-id="2b52e-160">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b52e-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="2b52e-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="2b52e-161">-ShardCount</span></span>
<span data-ttu-id="2b52e-162">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b52e-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="2b52e-163">-Méret</span><span class="sxs-lookup"><span data-stu-id="2b52e-163">-Size</span></span>
<span data-ttu-id="2b52e-164">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b52e-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="2b52e-165">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="2b52e-165">Valid values are:</span></span> 
- <span data-ttu-id="2b52e-166">P1</span><span class="sxs-lookup"><span data-stu-id="2b52e-166">P1</span></span>
- <span data-ttu-id="2b52e-167">P2</span><span class="sxs-lookup"><span data-stu-id="2b52e-167">P2</span></span>
- <span data-ttu-id="2b52e-168">P3</span><span class="sxs-lookup"><span data-stu-id="2b52e-168">P3</span></span>
- <span data-ttu-id="2b52e-169">P4</span><span class="sxs-lookup"><span data-stu-id="2b52e-169">P4</span></span>
- <span data-ttu-id="2b52e-170">C0</span><span class="sxs-lookup"><span data-stu-id="2b52e-170">C0</span></span>
- <span data-ttu-id="2b52e-171">C1</span><span class="sxs-lookup"><span data-stu-id="2b52e-171">C1</span></span>
- <span data-ttu-id="2b52e-172">C2</span><span class="sxs-lookup"><span data-stu-id="2b52e-172">C2</span></span>
- <span data-ttu-id="2b52e-173">C3</span><span class="sxs-lookup"><span data-stu-id="2b52e-173">C3</span></span>
- <span data-ttu-id="2b52e-174">C4</span><span class="sxs-lookup"><span data-stu-id="2b52e-174">C4</span></span>
- <span data-ttu-id="2b52e-175">C5</span><span class="sxs-lookup"><span data-stu-id="2b52e-175">C5</span></span>
- <span data-ttu-id="2b52e-176">C6</span><span class="sxs-lookup"><span data-stu-id="2b52e-176">C6</span></span>
- <span data-ttu-id="2b52e-177">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="2b52e-177">250MB</span></span>
- <span data-ttu-id="2b52e-178">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="2b52e-178">1GB</span></span>
- <span data-ttu-id="2b52e-179">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="2b52e-179">2.5GB</span></span>
- <span data-ttu-id="2b52e-180">6GB</span><span class="sxs-lookup"><span data-stu-id="2b52e-180">6GB</span></span>
- <span data-ttu-id="2b52e-181">13GB</span><span class="sxs-lookup"><span data-stu-id="2b52e-181">13GB</span></span>
- <span data-ttu-id="2b52e-182">26GB</span><span class="sxs-lookup"><span data-stu-id="2b52e-182">26GB</span></span>
- <span data-ttu-id="2b52e-183">53GB az alapértelmezett érték 1GB vagy C1.</span><span class="sxs-lookup"><span data-stu-id="2b52e-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="2b52e-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="2b52e-184">-Sku</span></span>
<span data-ttu-id="2b52e-185">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="2b52e-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="2b52e-186">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="2b52e-186">Valid values are:</span></span> 
- <span data-ttu-id="2b52e-187">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="2b52e-187">Basic</span></span>
- <span data-ttu-id="2b52e-188">Standard</span><span class="sxs-lookup"><span data-stu-id="2b52e-188">Standard</span></span>
- <span data-ttu-id="2b52e-189">Prémium: az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="2b52e-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="2b52e-190">-Címke</span><span class="sxs-lookup"><span data-stu-id="2b52e-190">-Tag</span></span>
<span data-ttu-id="2b52e-191">A címkéket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="2b52e-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="2b52e-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="2b52e-192">-TenantSettings</span></span>
<span data-ttu-id="2b52e-193">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="2b52e-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="2b52e-194">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b52e-194">-Confirm</span></span>
<span data-ttu-id="2b52e-195">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b52e-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b52e-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b52e-196">-WhatIf</span></span>
<span data-ttu-id="2b52e-197">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b52e-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b52e-198">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b52e-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b52e-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b52e-199">CommonParameters</span></span>
<span data-ttu-id="2b52e-200">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b52e-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b52e-201">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b52e-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b52e-202">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b52e-202">INPUTS</span></span>

### <span data-ttu-id="2b52e-203">System. String</span><span class="sxs-lookup"><span data-stu-id="2b52e-203">System.String</span></span>

### <span data-ttu-id="2b52e-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2b52e-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2b52e-205">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2b52e-205">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2b52e-206">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2b52e-206">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2b52e-207">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b52e-207">OUTPUTS</span></span>

### <span data-ttu-id="2b52e-208">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2b52e-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="2b52e-209">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b52e-209">NOTES</span></span>

## <span data-ttu-id="2b52e-210">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b52e-210">RELATED LINKS</span></span>

[<span data-ttu-id="2b52e-211">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2b52e-211">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="2b52e-212">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2b52e-212">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="2b52e-213">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2b52e-213">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


