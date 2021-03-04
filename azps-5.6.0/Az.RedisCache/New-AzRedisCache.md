---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 25469aa93f673d6a49bbbaa54fcaf22a91019d9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942226"
---
# <span data-ttu-id="03118-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03118-101">New-AzRedisCache</span></span>

## <span data-ttu-id="03118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03118-102">SYNOPSIS</span></span>
<span data-ttu-id="03118-103">Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="03118-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="03118-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03118-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03118-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03118-105">DESCRIPTION</span></span>
<span data-ttu-id="03118-106">A **New-AzRedisCache** parancsmag létrehoz egy Azure Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="03118-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="03118-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03118-107">EXAMPLES</span></span>

### <span data-ttu-id="03118-108">1. példa: Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="03118-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="03118-109">Ezzel a paranccsal redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="03118-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="03118-110">2. példa: Szabványos termékváltozat-újradis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="03118-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="03118-111">Ezzel a paranccsal redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="03118-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="03118-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03118-112">PARAMETERS</span></span>

### <span data-ttu-id="03118-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03118-113">-DefaultProfile</span></span>
<span data-ttu-id="03118-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03118-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03118-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="03118-115">-EnableNonSslPort</span></span>
<span data-ttu-id="03118-116">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="03118-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="03118-117">Az alapértelmezett érték $False (a nem SSL-port le van tiltva).</span><span class="sxs-lookup"><span data-stu-id="03118-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="03118-118">-Location</span><span class="sxs-lookup"><span data-stu-id="03118-118">-Location</span></span>
<span data-ttu-id="03118-119">Azt a helyet adja meg, ahol létre kell hoznia a redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="03118-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="03118-120">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="03118-120">Valid values are:</span></span> 
- <span data-ttu-id="03118-121">Észak-Közép-USA</span><span class="sxs-lookup"><span data-stu-id="03118-121">North Central US</span></span>
- <span data-ttu-id="03118-122">Usa déli részén</span><span class="sxs-lookup"><span data-stu-id="03118-122">South Central US</span></span>
- <span data-ttu-id="03118-123">Közép-USA</span><span class="sxs-lookup"><span data-stu-id="03118-123">Central US</span></span>
- <span data-ttu-id="03118-124">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="03118-124">West Europe</span></span>
- <span data-ttu-id="03118-125">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="03118-125">North Europe</span></span>
- <span data-ttu-id="03118-126">Nyugat-USA</span><span class="sxs-lookup"><span data-stu-id="03118-126">West US</span></span>
- <span data-ttu-id="03118-127">Usa keleti régiója</span><span class="sxs-lookup"><span data-stu-id="03118-127">East US</span></span>
- <span data-ttu-id="03118-128">Us 2. kelet</span><span class="sxs-lookup"><span data-stu-id="03118-128">East US 2</span></span>
- <span data-ttu-id="03118-129">Japán kelet</span><span class="sxs-lookup"><span data-stu-id="03118-129">Japan East</span></span>
- <span data-ttu-id="03118-130">Japán nyugati régiója</span><span class="sxs-lookup"><span data-stu-id="03118-130">Japan West</span></span>
- <span data-ttu-id="03118-131">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="03118-131">Brazil South</span></span>
- <span data-ttu-id="03118-132">Délkelet-Ázsia</span><span class="sxs-lookup"><span data-stu-id="03118-132">Southeast Asia</span></span>
- <span data-ttu-id="03118-133">Kelet-Ázsia</span><span class="sxs-lookup"><span data-stu-id="03118-133">East Asia</span></span>
- <span data-ttu-id="03118-134">Ausztrália keleti régiója</span><span class="sxs-lookup"><span data-stu-id="03118-134">Australia East</span></span>
- <span data-ttu-id="03118-135">Ausztrália délkeleti részén</span><span class="sxs-lookup"><span data-stu-id="03118-135">Australia Southeast</span></span>

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

### <span data-ttu-id="03118-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="03118-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="03118-137">Adja meg az ügyfelek által a gyorsítótárhoz való csatlakozáshoz szükséges TLS-verziót.</span><span class="sxs-lookup"><span data-stu-id="03118-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="03118-138">-Name</span><span class="sxs-lookup"><span data-stu-id="03118-138">-Name</span></span>
<span data-ttu-id="03118-139">A létrehozni szükséges redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03118-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="03118-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="03118-140">-RedisConfiguration</span></span>
<span data-ttu-id="03118-141">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="03118-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="03118-142">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="03118-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03118-143">rdb-backup-enabled.</span><span class="sxs-lookup"><span data-stu-id="03118-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="03118-144">Azt adja meg, hogy a Redis data persistence engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="03118-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="03118-145">Csak prémium szint.</span><span class="sxs-lookup"><span data-stu-id="03118-145">Premium tier only.</span></span>
- <span data-ttu-id="03118-146">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="03118-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="03118-147">A Redis adatmegőrzéshez a Tárfiókhoz való kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="03118-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="03118-148">Csak prémium szint.</span><span class="sxs-lookup"><span data-stu-id="03118-148">Premium tier only.</span></span>
- <span data-ttu-id="03118-149">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="03118-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="03118-150">A redis data persistence biztonsági mentési gyakoriságát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="03118-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="03118-151">Csak prémium szint.</span><span class="sxs-lookup"><span data-stu-id="03118-151">Premium tier only.</span></span> 
- <span data-ttu-id="03118-152">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="03118-152">maxmemory-reserved.</span></span>
<span data-ttu-id="03118-153">A nem gyorsítótáras folyamatok számára fenntartott memóriát konfigurálja.</span><span class="sxs-lookup"><span data-stu-id="03118-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="03118-154">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="03118-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03118-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="03118-155">maxmemory-policy.</span></span>
<span data-ttu-id="03118-156">Konfigurálja a kiviction házirendet a gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="03118-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="03118-157">Az összes árazási szint.</span><span class="sxs-lookup"><span data-stu-id="03118-157">All pricing tiers.</span></span> 
- <span data-ttu-id="03118-158">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="03118-158">notify-keyspace-events.</span></span>
<span data-ttu-id="03118-159">Konfigurálja a keyspace-értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="03118-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="03118-160">Normál és prémiumszintek.</span><span class="sxs-lookup"><span data-stu-id="03118-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="03118-161">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="03118-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="03118-162">A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.</span><span class="sxs-lookup"><span data-stu-id="03118-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="03118-163">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="03118-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03118-164">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="03118-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="03118-165">A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.</span><span class="sxs-lookup"><span data-stu-id="03118-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="03118-166">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="03118-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03118-167">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="03118-167">set-max-intset-entries.</span></span>
<span data-ttu-id="03118-168">A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.</span><span class="sxs-lookup"><span data-stu-id="03118-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="03118-169">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="03118-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03118-170">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="03118-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="03118-171">A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.</span><span class="sxs-lookup"><span data-stu-id="03118-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="03118-172">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="03118-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03118-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="03118-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="03118-174">A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.</span><span class="sxs-lookup"><span data-stu-id="03118-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="03118-175">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="03118-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03118-176">adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="03118-176">databases.</span></span>
<span data-ttu-id="03118-177">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="03118-177">Configures the number of databases.</span></span>
<span data-ttu-id="03118-178">Ez a tulajdonság csak gyorsítótár-létrehozáskor konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="03118-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="03118-179">Normál és Prémium szint.</span><span class="sxs-lookup"><span data-stu-id="03118-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="03118-180">További információt az Azure Redis Cache kezelése az Azure PowerShell használatával http://go.microsoft.com/fwlink/?LinkId=800051 ( . http://go.microsoft.com/fwlink/?LinkId=800051)</span><span class="sxs-lookup"><span data-stu-id="03118-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="03118-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03118-181">-ResourceGroupName</span></span>
<span data-ttu-id="03118-182">Annak az erőforráscsoportnak a nevét adja meg, amelyben létre kell hoznia a redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="03118-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="03118-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="03118-183">-ShardCount</span></span>
<span data-ttu-id="03118-184">A prémium szintű fürt-gyorsítótárban létrehozható szegmensek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03118-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="03118-185">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="03118-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03118-186">1</span><span class="sxs-lookup"><span data-stu-id="03118-186">1</span></span>
- <span data-ttu-id="03118-187">2</span><span class="sxs-lookup"><span data-stu-id="03118-187">2</span></span>
- <span data-ttu-id="03118-188">3</span><span class="sxs-lookup"><span data-stu-id="03118-188">3</span></span>
- <span data-ttu-id="03118-189">4</span><span class="sxs-lookup"><span data-stu-id="03118-189">4</span></span>
- <span data-ttu-id="03118-190">5</span><span class="sxs-lookup"><span data-stu-id="03118-190">5</span></span>
- <span data-ttu-id="03118-191">6</span><span class="sxs-lookup"><span data-stu-id="03118-191">6</span></span>
- <span data-ttu-id="03118-192">7</span><span class="sxs-lookup"><span data-stu-id="03118-192">7</span></span>
- <span data-ttu-id="03118-193">8</span><span class="sxs-lookup"><span data-stu-id="03118-193">8</span></span>
- <span data-ttu-id="03118-194">9</span><span class="sxs-lookup"><span data-stu-id="03118-194">9</span></span> 
- <span data-ttu-id="03118-195">10</span><span class="sxs-lookup"><span data-stu-id="03118-195">10</span></span>

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

### <span data-ttu-id="03118-196">-Size</span><span class="sxs-lookup"><span data-stu-id="03118-196">-Size</span></span>
<span data-ttu-id="03118-197">A Redis Cache mérete.</span><span class="sxs-lookup"><span data-stu-id="03118-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="03118-198">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="03118-198">Valid values are:</span></span> 
- <span data-ttu-id="03118-199">P1</span><span class="sxs-lookup"><span data-stu-id="03118-199">P1</span></span>
- <span data-ttu-id="03118-200">P2</span><span class="sxs-lookup"><span data-stu-id="03118-200">P2</span></span>
- <span data-ttu-id="03118-201">P3</span><span class="sxs-lookup"><span data-stu-id="03118-201">P3</span></span>
- <span data-ttu-id="03118-202">P4</span><span class="sxs-lookup"><span data-stu-id="03118-202">P4</span></span>
- <span data-ttu-id="03118-203">P5</span><span class="sxs-lookup"><span data-stu-id="03118-203">P5</span></span>
- <span data-ttu-id="03118-204">C0</span><span class="sxs-lookup"><span data-stu-id="03118-204">C0</span></span>
- <span data-ttu-id="03118-205">C1</span><span class="sxs-lookup"><span data-stu-id="03118-205">C1</span></span>
- <span data-ttu-id="03118-206">C2</span><span class="sxs-lookup"><span data-stu-id="03118-206">C2</span></span>
- <span data-ttu-id="03118-207">C3</span><span class="sxs-lookup"><span data-stu-id="03118-207">C3</span></span>
- <span data-ttu-id="03118-208">C4</span><span class="sxs-lookup"><span data-stu-id="03118-208">C4</span></span>
- <span data-ttu-id="03118-209">C5</span><span class="sxs-lookup"><span data-stu-id="03118-209">C5</span></span>
- <span data-ttu-id="03118-210">C6</span><span class="sxs-lookup"><span data-stu-id="03118-210">C6</span></span>
- <span data-ttu-id="03118-211">250 MB</span><span class="sxs-lookup"><span data-stu-id="03118-211">250MB</span></span>
- <span data-ttu-id="03118-212">1 GB</span><span class="sxs-lookup"><span data-stu-id="03118-212">1GB</span></span>
- <span data-ttu-id="03118-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="03118-213">2.5GB</span></span>
- <span data-ttu-id="03118-214">6 GB</span><span class="sxs-lookup"><span data-stu-id="03118-214">6GB</span></span>
- <span data-ttu-id="03118-215">13 GB</span><span class="sxs-lookup"><span data-stu-id="03118-215">13GB</span></span>
- <span data-ttu-id="03118-216">26 GB</span><span class="sxs-lookup"><span data-stu-id="03118-216">26GB</span></span>
- <span data-ttu-id="03118-217">53 GB Az alapértelmezett érték 1 GB vagy C1.</span><span class="sxs-lookup"><span data-stu-id="03118-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="03118-218">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="03118-218">-Sku</span></span>
<span data-ttu-id="03118-219">A létrehozni szükséges redis-gyorsítótár termékváltozatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03118-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="03118-220">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="03118-220">Valid values are:</span></span> 
- <span data-ttu-id="03118-221">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="03118-221">Basic</span></span>
- <span data-ttu-id="03118-222">Normál</span><span class="sxs-lookup"><span data-stu-id="03118-222">Standard</span></span>
- <span data-ttu-id="03118-223">Prémium: Az alapértelmezett érték a Standard.</span><span class="sxs-lookup"><span data-stu-id="03118-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="03118-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="03118-224">-StaticIP</span></span>
<span data-ttu-id="03118-225">Egyedi IP-címet ad meg az alhálózatban a redis-gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="03118-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="03118-226">Ha nem ad meg értéket ehhez a paraméterhez, ez a parancsmag kiválaszt egy IP-címet az alhálózatból.</span><span class="sxs-lookup"><span data-stu-id="03118-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="03118-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="03118-227">-SubnetId</span></span>
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

### <span data-ttu-id="03118-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="03118-228">-Tag</span></span>
<span data-ttu-id="03118-229">Címkéket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="03118-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="03118-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="03118-230">-TenantSettings</span></span>
<span data-ttu-id="03118-231">A paraméter elavult.</span><span class="sxs-lookup"><span data-stu-id="03118-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="03118-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="03118-232">-Zone</span></span>
<span data-ttu-id="03118-233">Zónák listája.</span><span class="sxs-lookup"><span data-stu-id="03118-233">List of zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03118-234">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03118-234">-Confirm</span></span>
<span data-ttu-id="03118-235">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03118-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03118-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03118-236">-WhatIf</span></span>
<span data-ttu-id="03118-237">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03118-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03118-238">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03118-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03118-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03118-239">CommonParameters</span></span>
<span data-ttu-id="03118-240">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03118-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03118-241">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03118-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03118-242">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03118-242">INPUTS</span></span>

### <span data-ttu-id="03118-243">System.String</span><span class="sxs-lookup"><span data-stu-id="03118-243">System.String</span></span>

### <span data-ttu-id="03118-244">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="03118-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="03118-245">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="03118-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="03118-246">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="03118-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="03118-247">System.String[]</span><span class="sxs-lookup"><span data-stu-id="03118-247">System.String[]</span></span>

## <span data-ttu-id="03118-248">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03118-248">OUTPUTS</span></span>

### <span data-ttu-id="03118-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="03118-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="03118-250">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03118-250">NOTES</span></span>

## <span data-ttu-id="03118-251">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03118-251">RELATED LINKS</span></span>

[<span data-ttu-id="03118-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03118-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="03118-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03118-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="03118-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03118-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


