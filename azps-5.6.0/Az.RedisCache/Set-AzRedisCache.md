---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 809939a4e218005c9b4c41846e0885dfca553964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000917"
---
# <span data-ttu-id="58ce0-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="58ce0-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="58ce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="58ce0-103">Módosítja a redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="58ce0-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="58ce0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58ce0-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ce0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="58ce0-106">A **Set-AzRedisCache** parancsmag módosítja az Azure Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="58ce0-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="58ce0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58ce0-107">EXAMPLES</span></span>

### <span data-ttu-id="58ce0-108">1. példa: Redis-gyorsítótár módosítása</span><span class="sxs-lookup"><span data-stu-id="58ce0-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="58ce0-109">Ez a parancs frissíti a MyCache nevű Redis cache maxmemory-házirendet.</span><span class="sxs-lookup"><span data-stu-id="58ce0-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="58ce0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58ce0-110">PARAMETERS</span></span>

### <span data-ttu-id="58ce0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ce0-111">-DefaultProfile</span></span>
<span data-ttu-id="58ce0-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58ce0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58ce0-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="58ce0-113">-EnableNonSslPort</span></span>
<span data-ttu-id="58ce0-114">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="58ce0-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="58ce0-115">Az alapértelmezett érték $False (a nem SSL-port le van tiltva).</span><span class="sxs-lookup"><span data-stu-id="58ce0-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="58ce0-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="58ce0-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="58ce0-117">Adja meg az ügyfelek által a gyorsítótárhoz való csatlakozáshoz szükséges TLS-verziót.</span><span class="sxs-lookup"><span data-stu-id="58ce0-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="58ce0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="58ce0-118">-Name</span></span>
<span data-ttu-id="58ce0-119">A frissítenie kell a redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="58ce0-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="58ce0-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="58ce0-120">-RedisConfiguration</span></span>
<span data-ttu-id="58ce0-121">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="58ce0-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="58ce0-122">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="58ce0-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58ce0-123">rdb-backup-enabled.</span><span class="sxs-lookup"><span data-stu-id="58ce0-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="58ce0-124">Azt adja meg, hogy a Redis data persistence engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="58ce0-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="58ce0-125">Csak prémium szint.</span><span class="sxs-lookup"><span data-stu-id="58ce0-125">Premium tier only.</span></span>
- <span data-ttu-id="58ce0-126">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="58ce0-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="58ce0-127">A Redis adatmegőrzéshez a Tárfiókhoz való kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="58ce0-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="58ce0-128">Csak prémium szint.</span><span class="sxs-lookup"><span data-stu-id="58ce0-128">Premium tier only.</span></span>
- <span data-ttu-id="58ce0-129">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="58ce0-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="58ce0-130">A redis data persistence biztonsági mentési gyakoriságát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="58ce0-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="58ce0-131">Csak prémium szint.</span><span class="sxs-lookup"><span data-stu-id="58ce0-131">Premium tier only.</span></span> 
- <span data-ttu-id="58ce0-132">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="58ce0-132">maxmemory-reserved.</span></span>
<span data-ttu-id="58ce0-133">A nem gyorsítótáras folyamatok számára fenntartott memóriát konfigurálja.</span><span class="sxs-lookup"><span data-stu-id="58ce0-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="58ce0-134">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="58ce0-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="58ce0-135">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="58ce0-135">maxmemory-policy.</span></span>
<span data-ttu-id="58ce0-136">Konfigurálja a kiviction házirendet a gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="58ce0-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="58ce0-137">Az összes árazási szint.</span><span class="sxs-lookup"><span data-stu-id="58ce0-137">All pricing tiers.</span></span> 
- <span data-ttu-id="58ce0-138">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="58ce0-138">notify-keyspace-events.</span></span>
<span data-ttu-id="58ce0-139">Konfigurálja a keyspace-értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="58ce0-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="58ce0-140">Normál és prémiumszintek.</span><span class="sxs-lookup"><span data-stu-id="58ce0-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="58ce0-141">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="58ce0-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="58ce0-142">A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.</span><span class="sxs-lookup"><span data-stu-id="58ce0-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="58ce0-143">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="58ce0-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="58ce0-144">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="58ce0-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="58ce0-145">A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.</span><span class="sxs-lookup"><span data-stu-id="58ce0-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="58ce0-146">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="58ce0-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="58ce0-147">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="58ce0-147">set-max-intset-entries.</span></span>
<span data-ttu-id="58ce0-148">A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.</span><span class="sxs-lookup"><span data-stu-id="58ce0-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="58ce0-149">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="58ce0-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="58ce0-150">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="58ce0-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="58ce0-151">A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.</span><span class="sxs-lookup"><span data-stu-id="58ce0-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="58ce0-152">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="58ce0-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="58ce0-153">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="58ce0-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="58ce0-154">A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.</span><span class="sxs-lookup"><span data-stu-id="58ce0-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="58ce0-155">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="58ce0-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="58ce0-156">adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="58ce0-156">databases.</span></span>
<span data-ttu-id="58ce0-157">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="58ce0-157">Configures the number of databases.</span></span>
<span data-ttu-id="58ce0-158">Ez a tulajdonság csak gyorsítótár-létrehozáskor konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="58ce0-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="58ce0-159">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="58ce0-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="58ce0-160">További információt az Azure Redis Cache kezelése az Azure PowerShell használatával http://go.microsoft.com/fwlink/?LinkId=800051 ( . http://go.microsoft.com/fwlink/?LinkId=800051)</span><span class="sxs-lookup"><span data-stu-id="58ce0-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="58ce0-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ce0-161">-ResourceGroupName</span></span>
<span data-ttu-id="58ce0-162">A redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="58ce0-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="58ce0-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="58ce0-163">-ShardCount</span></span>
<span data-ttu-id="58ce0-164">A prémium szintű fürt-gyorsítótárban létrehozható szegmensek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="58ce0-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="58ce0-165">-Size</span><span class="sxs-lookup"><span data-stu-id="58ce0-165">-Size</span></span>
<span data-ttu-id="58ce0-166">A Redis Cache mérete.</span><span class="sxs-lookup"><span data-stu-id="58ce0-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="58ce0-167">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="58ce0-167">Valid values are:</span></span> 
- <span data-ttu-id="58ce0-168">P1</span><span class="sxs-lookup"><span data-stu-id="58ce0-168">P1</span></span>
- <span data-ttu-id="58ce0-169">P2</span><span class="sxs-lookup"><span data-stu-id="58ce0-169">P2</span></span>
- <span data-ttu-id="58ce0-170">P3</span><span class="sxs-lookup"><span data-stu-id="58ce0-170">P3</span></span>
- <span data-ttu-id="58ce0-171">P4</span><span class="sxs-lookup"><span data-stu-id="58ce0-171">P4</span></span>
- <span data-ttu-id="58ce0-172">P5</span><span class="sxs-lookup"><span data-stu-id="58ce0-172">P5</span></span>
- <span data-ttu-id="58ce0-173">C0</span><span class="sxs-lookup"><span data-stu-id="58ce0-173">C0</span></span>
- <span data-ttu-id="58ce0-174">C1</span><span class="sxs-lookup"><span data-stu-id="58ce0-174">C1</span></span>
- <span data-ttu-id="58ce0-175">C2</span><span class="sxs-lookup"><span data-stu-id="58ce0-175">C2</span></span>
- <span data-ttu-id="58ce0-176">C3</span><span class="sxs-lookup"><span data-stu-id="58ce0-176">C3</span></span>
- <span data-ttu-id="58ce0-177">C4</span><span class="sxs-lookup"><span data-stu-id="58ce0-177">C4</span></span>
- <span data-ttu-id="58ce0-178">C5</span><span class="sxs-lookup"><span data-stu-id="58ce0-178">C5</span></span>
- <span data-ttu-id="58ce0-179">C6</span><span class="sxs-lookup"><span data-stu-id="58ce0-179">C6</span></span>
- <span data-ttu-id="58ce0-180">250 MB</span><span class="sxs-lookup"><span data-stu-id="58ce0-180">250MB</span></span>
- <span data-ttu-id="58ce0-181">1 GB</span><span class="sxs-lookup"><span data-stu-id="58ce0-181">1GB</span></span>
- <span data-ttu-id="58ce0-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="58ce0-182">2.5GB</span></span>
- <span data-ttu-id="58ce0-183">6 GB</span><span class="sxs-lookup"><span data-stu-id="58ce0-183">6GB</span></span>
- <span data-ttu-id="58ce0-184">13 GB</span><span class="sxs-lookup"><span data-stu-id="58ce0-184">13GB</span></span>
- <span data-ttu-id="58ce0-185">26 GB</span><span class="sxs-lookup"><span data-stu-id="58ce0-185">26GB</span></span>
- <span data-ttu-id="58ce0-186">53 GB</span><span class="sxs-lookup"><span data-stu-id="58ce0-186">53GB</span></span>
- <span data-ttu-id="58ce0-187">120 GB Az alapértelmezett érték 1 GB vagy C1.</span><span class="sxs-lookup"><span data-stu-id="58ce0-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="58ce0-188">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="58ce0-188">-Sku</span></span>
<span data-ttu-id="58ce0-189">A létrehozni szükséges redis-gyorsítótár termékváltozatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="58ce0-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="58ce0-190">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="58ce0-190">Valid values are:</span></span> 
- <span data-ttu-id="58ce0-191">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="58ce0-191">Basic</span></span>
- <span data-ttu-id="58ce0-192">Normál</span><span class="sxs-lookup"><span data-stu-id="58ce0-192">Standard</span></span>
- <span data-ttu-id="58ce0-193">Prémium: Az alapértelmezett érték a Standard.</span><span class="sxs-lookup"><span data-stu-id="58ce0-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="58ce0-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="58ce0-194">-Tag</span></span>
<span data-ttu-id="58ce0-195">Címkéket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="58ce0-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="58ce0-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="58ce0-196">-TenantSettings</span></span>
<span data-ttu-id="58ce0-197">A paraméter elavult.</span><span class="sxs-lookup"><span data-stu-id="58ce0-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="58ce0-198">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58ce0-198">-Confirm</span></span>
<span data-ttu-id="58ce0-199">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="58ce0-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ce0-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ce0-200">-WhatIf</span></span>
<span data-ttu-id="58ce0-201">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="58ce0-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58ce0-202">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58ce0-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ce0-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ce0-203">CommonParameters</span></span>
<span data-ttu-id="58ce0-204">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58ce0-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ce0-205">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58ce0-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ce0-206">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58ce0-206">INPUTS</span></span>

### <span data-ttu-id="58ce0-207">System.String</span><span class="sxs-lookup"><span data-stu-id="58ce0-207">System.String</span></span>

### <span data-ttu-id="58ce0-208">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="58ce0-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="58ce0-209">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58ce0-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="58ce0-210">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58ce0-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="58ce0-211">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58ce0-211">OUTPUTS</span></span>

### <span data-ttu-id="58ce0-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="58ce0-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="58ce0-213">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58ce0-213">NOTES</span></span>

## <span data-ttu-id="58ce0-214">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58ce0-214">RELATED LINKS</span></span>

[<span data-ttu-id="58ce0-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="58ce0-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="58ce0-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="58ce0-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="58ce0-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="58ce0-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


