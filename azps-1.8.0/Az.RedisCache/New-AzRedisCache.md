---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: ab0b84578339568e48458de8a89daccd83092e65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669547"
---
# <span data-ttu-id="ef70f-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef70f-101">New-AzRedisCache</span></span>

## <span data-ttu-id="ef70f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef70f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef70f-103">Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ef70f-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="ef70f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef70f-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef70f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef70f-105">DESCRIPTION</span></span>
<span data-ttu-id="ef70f-106">A **New-AzRedisCache** parancsmag Azure Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ef70f-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="ef70f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ef70f-107">EXAMPLES</span></span>

### <span data-ttu-id="ef70f-108">Példa 1: Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="ef70f-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="ef70f-109">Ez a parancs Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ef70f-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="ef70f-110">2. példa: szabványos SKU Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="ef70f-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="ef70f-111">Ez a parancs Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ef70f-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="ef70f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef70f-112">PARAMETERS</span></span>

### <span data-ttu-id="ef70f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef70f-113">-DefaultProfile</span></span>
<span data-ttu-id="ef70f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef70f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef70f-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="ef70f-115">-EnableNonSslPort</span></span>
<span data-ttu-id="ef70f-116">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="ef70f-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="ef70f-117">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="ef70f-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="ef70f-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="ef70f-118">-Location</span></span>
<span data-ttu-id="ef70f-119">A Redis-gyorsítótár létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef70f-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="ef70f-120">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="ef70f-120">Valid values are:</span></span> 
- <span data-ttu-id="ef70f-121">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="ef70f-121">North Central US</span></span>
- <span data-ttu-id="ef70f-122">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="ef70f-122">South Central US</span></span>
- <span data-ttu-id="ef70f-123">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="ef70f-123">Central US</span></span>
- <span data-ttu-id="ef70f-124">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="ef70f-124">West Europe</span></span>
- <span data-ttu-id="ef70f-125">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="ef70f-125">North Europe</span></span>
- <span data-ttu-id="ef70f-126">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="ef70f-126">West US</span></span>
- <span data-ttu-id="ef70f-127">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="ef70f-127">East US</span></span>
- <span data-ttu-id="ef70f-128">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="ef70f-128">East US 2</span></span>
- <span data-ttu-id="ef70f-129">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="ef70f-129">Japan East</span></span>
- <span data-ttu-id="ef70f-130">Japán West</span><span class="sxs-lookup"><span data-stu-id="ef70f-130">Japan West</span></span>
- <span data-ttu-id="ef70f-131">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="ef70f-131">Brazil South</span></span>
- <span data-ttu-id="ef70f-132">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="ef70f-132">Southeast Asia</span></span>
- <span data-ttu-id="ef70f-133">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="ef70f-133">East Asia</span></span>
- <span data-ttu-id="ef70f-134">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="ef70f-134">Australia East</span></span>
- <span data-ttu-id="ef70f-135">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="ef70f-135">Australia Southeast</span></span>

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

### <span data-ttu-id="ef70f-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef70f-136">-Name</span></span>
<span data-ttu-id="ef70f-137">A létrehozandó Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef70f-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="ef70f-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef70f-138">-RedisConfiguration</span></span>
<span data-ttu-id="ef70f-139">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef70f-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="ef70f-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ef70f-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef70f-141">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="ef70f-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="ef70f-142">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ef70f-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="ef70f-143">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="ef70f-143">Premium tier only.</span></span>
- <span data-ttu-id="ef70f-144">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="ef70f-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="ef70f-145">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef70f-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="ef70f-146">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="ef70f-146">Premium tier only.</span></span>
- <span data-ttu-id="ef70f-147">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="ef70f-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="ef70f-148">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef70f-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="ef70f-149">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="ef70f-149">Premium tier only.</span></span> 
- <span data-ttu-id="ef70f-150">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="ef70f-150">maxmemory-reserved.</span></span>
<span data-ttu-id="ef70f-151">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="ef70f-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="ef70f-152">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="ef70f-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ef70f-153">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="ef70f-153">maxmemory-policy.</span></span>
<span data-ttu-id="ef70f-154">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="ef70f-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="ef70f-155">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="ef70f-155">All pricing tiers.</span></span> 
- <span data-ttu-id="ef70f-156">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="ef70f-156">notify-keyspace-events.</span></span>
<span data-ttu-id="ef70f-157">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="ef70f-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="ef70f-158">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="ef70f-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="ef70f-159">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="ef70f-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="ef70f-160">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="ef70f-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ef70f-161">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="ef70f-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ef70f-162">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="ef70f-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="ef70f-163">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="ef70f-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ef70f-164">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="ef70f-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ef70f-165">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="ef70f-165">set-max-intset-entries.</span></span>
<span data-ttu-id="ef70f-166">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="ef70f-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ef70f-167">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="ef70f-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ef70f-168">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="ef70f-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="ef70f-169">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="ef70f-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ef70f-170">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="ef70f-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ef70f-171">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="ef70f-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="ef70f-172">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="ef70f-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ef70f-173">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="ef70f-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ef70f-174">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="ef70f-174">databases.</span></span>
<span data-ttu-id="ef70f-175">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="ef70f-175">Configures the number of databases.</span></span>
<span data-ttu-id="ef70f-176">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="ef70f-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="ef70f-177">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="ef70f-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="ef70f-178">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="ef70f-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="ef70f-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef70f-179">-ResourceGroupName</span></span>
<span data-ttu-id="ef70f-180">Annak az erőforráscsoportnek a nevét adja meg, amelybe a Redis-gyorsítótárat létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="ef70f-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="ef70f-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="ef70f-181">-ShardCount</span></span>
<span data-ttu-id="ef70f-182">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef70f-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="ef70f-183">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ef70f-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef70f-184">1</span><span class="sxs-lookup"><span data-stu-id="ef70f-184">1</span></span>
- <span data-ttu-id="ef70f-185">2</span><span class="sxs-lookup"><span data-stu-id="ef70f-185">2</span></span>
- <span data-ttu-id="ef70f-186">3</span><span class="sxs-lookup"><span data-stu-id="ef70f-186">3</span></span>
- <span data-ttu-id="ef70f-187">4</span><span class="sxs-lookup"><span data-stu-id="ef70f-187">4</span></span>
- <span data-ttu-id="ef70f-188">5</span><span class="sxs-lookup"><span data-stu-id="ef70f-188">5</span></span>
- <span data-ttu-id="ef70f-189">6</span><span class="sxs-lookup"><span data-stu-id="ef70f-189">6</span></span>
- <span data-ttu-id="ef70f-190">7</span><span class="sxs-lookup"><span data-stu-id="ef70f-190">7</span></span>
- <span data-ttu-id="ef70f-191">8</span><span class="sxs-lookup"><span data-stu-id="ef70f-191">8</span></span>
- <span data-ttu-id="ef70f-192">9</span><span class="sxs-lookup"><span data-stu-id="ef70f-192">9</span></span> 
- <span data-ttu-id="ef70f-193">10</span><span class="sxs-lookup"><span data-stu-id="ef70f-193">10</span></span>

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

### <span data-ttu-id="ef70f-194">-Méret</span><span class="sxs-lookup"><span data-stu-id="ef70f-194">-Size</span></span>
<span data-ttu-id="ef70f-195">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef70f-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="ef70f-196">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="ef70f-196">Valid values are:</span></span> 
- <span data-ttu-id="ef70f-197">P1</span><span class="sxs-lookup"><span data-stu-id="ef70f-197">P1</span></span>
- <span data-ttu-id="ef70f-198">P2</span><span class="sxs-lookup"><span data-stu-id="ef70f-198">P2</span></span>
- <span data-ttu-id="ef70f-199">P3</span><span class="sxs-lookup"><span data-stu-id="ef70f-199">P3</span></span>
- <span data-ttu-id="ef70f-200">P4</span><span class="sxs-lookup"><span data-stu-id="ef70f-200">P4</span></span>
- <span data-ttu-id="ef70f-201">C0</span><span class="sxs-lookup"><span data-stu-id="ef70f-201">C0</span></span>
- <span data-ttu-id="ef70f-202">C1</span><span class="sxs-lookup"><span data-stu-id="ef70f-202">C1</span></span>
- <span data-ttu-id="ef70f-203">C2</span><span class="sxs-lookup"><span data-stu-id="ef70f-203">C2</span></span>
- <span data-ttu-id="ef70f-204">C3</span><span class="sxs-lookup"><span data-stu-id="ef70f-204">C3</span></span>
- <span data-ttu-id="ef70f-205">C4</span><span class="sxs-lookup"><span data-stu-id="ef70f-205">C4</span></span>
- <span data-ttu-id="ef70f-206">C5</span><span class="sxs-lookup"><span data-stu-id="ef70f-206">C5</span></span>
- <span data-ttu-id="ef70f-207">C6</span><span class="sxs-lookup"><span data-stu-id="ef70f-207">C6</span></span>
- <span data-ttu-id="ef70f-208">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="ef70f-208">250MB</span></span>
- <span data-ttu-id="ef70f-209">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="ef70f-209">1GB</span></span>
- <span data-ttu-id="ef70f-210">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="ef70f-210">2.5GB</span></span>
- <span data-ttu-id="ef70f-211">6GB</span><span class="sxs-lookup"><span data-stu-id="ef70f-211">6GB</span></span>
- <span data-ttu-id="ef70f-212">13GB</span><span class="sxs-lookup"><span data-stu-id="ef70f-212">13GB</span></span>
- <span data-ttu-id="ef70f-213">26GB</span><span class="sxs-lookup"><span data-stu-id="ef70f-213">26GB</span></span>
- <span data-ttu-id="ef70f-214">53GB az alapértelmezett érték 1GB vagy C1.</span><span class="sxs-lookup"><span data-stu-id="ef70f-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="ef70f-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="ef70f-215">-Sku</span></span>
<span data-ttu-id="ef70f-216">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="ef70f-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="ef70f-217">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="ef70f-217">Valid values are:</span></span> 
- <span data-ttu-id="ef70f-218">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="ef70f-218">Basic</span></span>
- <span data-ttu-id="ef70f-219">Standard</span><span class="sxs-lookup"><span data-stu-id="ef70f-219">Standard</span></span>
- <span data-ttu-id="ef70f-220">Prémium: az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="ef70f-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="ef70f-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="ef70f-221">-StaticIP</span></span>
<span data-ttu-id="ef70f-222">Egy egyedi IP-címet ad meg a Redis-gyorsítótár alhálózatában.</span><span class="sxs-lookup"><span data-stu-id="ef70f-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="ef70f-223">Ha nem ad meg értéket ehhez a paraméterhez, ez a parancsmag egy IP-címet választ az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="ef70f-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="ef70f-224">– NetI</span><span class="sxs-lookup"><span data-stu-id="ef70f-224">-SubnetId</span></span>
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

### <span data-ttu-id="ef70f-225">-Címke</span><span class="sxs-lookup"><span data-stu-id="ef70f-225">-Tag</span></span>
<span data-ttu-id="ef70f-226">A címkéket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="ef70f-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="ef70f-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="ef70f-227">-TenantSettings</span></span>
<span data-ttu-id="ef70f-228">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="ef70f-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="ef70f-229">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="ef70f-229">-Zone</span></span>
<span data-ttu-id="ef70f-230">A zónák listája.</span><span class="sxs-lookup"><span data-stu-id="ef70f-230">List of zones.</span></span>

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

### <span data-ttu-id="ef70f-231">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef70f-231">-Confirm</span></span>
<span data-ttu-id="ef70f-232">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef70f-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef70f-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef70f-233">-WhatIf</span></span>
<span data-ttu-id="ef70f-234">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef70f-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef70f-235">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef70f-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef70f-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef70f-236">CommonParameters</span></span>
<span data-ttu-id="ef70f-237">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef70f-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef70f-238">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef70f-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef70f-239">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef70f-239">INPUTS</span></span>

### <span data-ttu-id="ef70f-240">System. String</span><span class="sxs-lookup"><span data-stu-id="ef70f-240">System.String</span></span>

### <span data-ttu-id="ef70f-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ef70f-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ef70f-242">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ef70f-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ef70f-243">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ef70f-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ef70f-244">System. string []</span><span class="sxs-lookup"><span data-stu-id="ef70f-244">System.String[]</span></span>

## <span data-ttu-id="ef70f-245">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef70f-245">OUTPUTS</span></span>

### <span data-ttu-id="ef70f-246">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="ef70f-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="ef70f-247">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef70f-247">NOTES</span></span>

## <span data-ttu-id="ef70f-248">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef70f-248">RELATED LINKS</span></span>

[<span data-ttu-id="ef70f-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef70f-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="ef70f-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef70f-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ef70f-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef70f-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


