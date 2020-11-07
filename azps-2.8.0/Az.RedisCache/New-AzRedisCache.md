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
ms.locfileid: "93838517"
---
# <span data-ttu-id="04e70-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04e70-101">New-AzRedisCache</span></span>

## <span data-ttu-id="04e70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04e70-102">SYNOPSIS</span></span>
<span data-ttu-id="04e70-103">Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="04e70-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="04e70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04e70-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04e70-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04e70-105">DESCRIPTION</span></span>
<span data-ttu-id="04e70-106">A **New-AzRedisCache** parancsmag Azure Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="04e70-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="04e70-107">Példák</span><span class="sxs-lookup"><span data-stu-id="04e70-107">EXAMPLES</span></span>

### <span data-ttu-id="04e70-108">Példa 1: Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="04e70-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="04e70-109">Ez a parancs Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="04e70-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="04e70-110">2. példa: szabványos SKU Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="04e70-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="04e70-111">Ez a parancs Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="04e70-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="04e70-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04e70-112">PARAMETERS</span></span>

### <span data-ttu-id="04e70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e70-113">-DefaultProfile</span></span>
<span data-ttu-id="04e70-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04e70-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04e70-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="04e70-115">-EnableNonSslPort</span></span>
<span data-ttu-id="04e70-116">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="04e70-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="04e70-117">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="04e70-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="04e70-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="04e70-118">-Location</span></span>
<span data-ttu-id="04e70-119">A Redis-gyorsítótár létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04e70-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="04e70-120">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="04e70-120">Valid values are:</span></span> 
- <span data-ttu-id="04e70-121">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="04e70-121">North Central US</span></span>
- <span data-ttu-id="04e70-122">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="04e70-122">South Central US</span></span>
- <span data-ttu-id="04e70-123">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="04e70-123">Central US</span></span>
- <span data-ttu-id="04e70-124">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="04e70-124">West Europe</span></span>
- <span data-ttu-id="04e70-125">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="04e70-125">North Europe</span></span>
- <span data-ttu-id="04e70-126">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="04e70-126">West US</span></span>
- <span data-ttu-id="04e70-127">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="04e70-127">East US</span></span>
- <span data-ttu-id="04e70-128">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="04e70-128">East US 2</span></span>
- <span data-ttu-id="04e70-129">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="04e70-129">Japan East</span></span>
- <span data-ttu-id="04e70-130">Japán West</span><span class="sxs-lookup"><span data-stu-id="04e70-130">Japan West</span></span>
- <span data-ttu-id="04e70-131">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="04e70-131">Brazil South</span></span>
- <span data-ttu-id="04e70-132">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="04e70-132">Southeast Asia</span></span>
- <span data-ttu-id="04e70-133">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="04e70-133">East Asia</span></span>
- <span data-ttu-id="04e70-134">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="04e70-134">Australia East</span></span>
- <span data-ttu-id="04e70-135">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="04e70-135">Australia Southeast</span></span>

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

### <span data-ttu-id="04e70-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04e70-136">-Name</span></span>
<span data-ttu-id="04e70-137">A létrehozandó Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04e70-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="04e70-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="04e70-138">-RedisConfiguration</span></span>
<span data-ttu-id="04e70-139">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="04e70-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="04e70-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="04e70-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04e70-141">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="04e70-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="04e70-142">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="04e70-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="04e70-143">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="04e70-143">Premium tier only.</span></span>
- <span data-ttu-id="04e70-144">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="04e70-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="04e70-145">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="04e70-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="04e70-146">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="04e70-146">Premium tier only.</span></span>
- <span data-ttu-id="04e70-147">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="04e70-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="04e70-148">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="04e70-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="04e70-149">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="04e70-149">Premium tier only.</span></span> 
- <span data-ttu-id="04e70-150">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="04e70-150">maxmemory-reserved.</span></span>
<span data-ttu-id="04e70-151">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="04e70-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="04e70-152">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="04e70-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04e70-153">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="04e70-153">maxmemory-policy.</span></span>
<span data-ttu-id="04e70-154">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="04e70-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="04e70-155">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="04e70-155">All pricing tiers.</span></span> 
- <span data-ttu-id="04e70-156">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="04e70-156">notify-keyspace-events.</span></span>
<span data-ttu-id="04e70-157">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="04e70-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="04e70-158">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="04e70-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="04e70-159">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="04e70-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="04e70-160">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="04e70-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04e70-161">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="04e70-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04e70-162">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="04e70-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="04e70-163">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="04e70-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04e70-164">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="04e70-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04e70-165">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="04e70-165">set-max-intset-entries.</span></span>
<span data-ttu-id="04e70-166">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="04e70-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04e70-167">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="04e70-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04e70-168">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="04e70-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="04e70-169">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="04e70-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04e70-170">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="04e70-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04e70-171">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="04e70-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="04e70-172">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="04e70-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04e70-173">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="04e70-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04e70-174">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="04e70-174">databases.</span></span>
<span data-ttu-id="04e70-175">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="04e70-175">Configures the number of databases.</span></span>
<span data-ttu-id="04e70-176">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="04e70-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="04e70-177">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="04e70-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="04e70-178">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="04e70-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="04e70-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04e70-179">-ResourceGroupName</span></span>
<span data-ttu-id="04e70-180">Annak az erőforráscsoportnek a nevét adja meg, amelybe a Redis-gyorsítótárat létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="04e70-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="04e70-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="04e70-181">-ShardCount</span></span>
<span data-ttu-id="04e70-182">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="04e70-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="04e70-183">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="04e70-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04e70-184">1</span><span class="sxs-lookup"><span data-stu-id="04e70-184">1</span></span>
- <span data-ttu-id="04e70-185">2</span><span class="sxs-lookup"><span data-stu-id="04e70-185">2</span></span>
- <span data-ttu-id="04e70-186">3</span><span class="sxs-lookup"><span data-stu-id="04e70-186">3</span></span>
- <span data-ttu-id="04e70-187">4</span><span class="sxs-lookup"><span data-stu-id="04e70-187">4</span></span>
- <span data-ttu-id="04e70-188">5</span><span class="sxs-lookup"><span data-stu-id="04e70-188">5</span></span>
- <span data-ttu-id="04e70-189">6</span><span class="sxs-lookup"><span data-stu-id="04e70-189">6</span></span>
- <span data-ttu-id="04e70-190">7</span><span class="sxs-lookup"><span data-stu-id="04e70-190">7</span></span>
- <span data-ttu-id="04e70-191">8</span><span class="sxs-lookup"><span data-stu-id="04e70-191">8</span></span>
- <span data-ttu-id="04e70-192">9</span><span class="sxs-lookup"><span data-stu-id="04e70-192">9</span></span> 
- <span data-ttu-id="04e70-193">10</span><span class="sxs-lookup"><span data-stu-id="04e70-193">10</span></span>

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

### <span data-ttu-id="04e70-194">-Méret</span><span class="sxs-lookup"><span data-stu-id="04e70-194">-Size</span></span>
<span data-ttu-id="04e70-195">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04e70-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="04e70-196">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="04e70-196">Valid values are:</span></span> 
- <span data-ttu-id="04e70-197">P1</span><span class="sxs-lookup"><span data-stu-id="04e70-197">P1</span></span>
- <span data-ttu-id="04e70-198">P2</span><span class="sxs-lookup"><span data-stu-id="04e70-198">P2</span></span>
- <span data-ttu-id="04e70-199">P3</span><span class="sxs-lookup"><span data-stu-id="04e70-199">P3</span></span>
- <span data-ttu-id="04e70-200">P4</span><span class="sxs-lookup"><span data-stu-id="04e70-200">P4</span></span>
- <span data-ttu-id="04e70-201">C0</span><span class="sxs-lookup"><span data-stu-id="04e70-201">C0</span></span>
- <span data-ttu-id="04e70-202">C1</span><span class="sxs-lookup"><span data-stu-id="04e70-202">C1</span></span>
- <span data-ttu-id="04e70-203">C2</span><span class="sxs-lookup"><span data-stu-id="04e70-203">C2</span></span>
- <span data-ttu-id="04e70-204">C3</span><span class="sxs-lookup"><span data-stu-id="04e70-204">C3</span></span>
- <span data-ttu-id="04e70-205">C4</span><span class="sxs-lookup"><span data-stu-id="04e70-205">C4</span></span>
- <span data-ttu-id="04e70-206">C5</span><span class="sxs-lookup"><span data-stu-id="04e70-206">C5</span></span>
- <span data-ttu-id="04e70-207">C6</span><span class="sxs-lookup"><span data-stu-id="04e70-207">C6</span></span>
- <span data-ttu-id="04e70-208">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="04e70-208">250MB</span></span>
- <span data-ttu-id="04e70-209">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="04e70-209">1GB</span></span>
- <span data-ttu-id="04e70-210">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="04e70-210">2.5GB</span></span>
- <span data-ttu-id="04e70-211">6GB</span><span class="sxs-lookup"><span data-stu-id="04e70-211">6GB</span></span>
- <span data-ttu-id="04e70-212">13GB</span><span class="sxs-lookup"><span data-stu-id="04e70-212">13GB</span></span>
- <span data-ttu-id="04e70-213">26GB</span><span class="sxs-lookup"><span data-stu-id="04e70-213">26GB</span></span>
- <span data-ttu-id="04e70-214">53GB az alapértelmezett érték 1GB vagy C1.</span><span class="sxs-lookup"><span data-stu-id="04e70-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="04e70-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="04e70-215">-Sku</span></span>
<span data-ttu-id="04e70-216">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="04e70-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="04e70-217">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="04e70-217">Valid values are:</span></span> 
- <span data-ttu-id="04e70-218">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="04e70-218">Basic</span></span>
- <span data-ttu-id="04e70-219">Standard</span><span class="sxs-lookup"><span data-stu-id="04e70-219">Standard</span></span>
- <span data-ttu-id="04e70-220">Prémium: az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="04e70-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="04e70-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="04e70-221">-StaticIP</span></span>
<span data-ttu-id="04e70-222">Egy egyedi IP-címet ad meg a Redis-gyorsítótár alhálózatában.</span><span class="sxs-lookup"><span data-stu-id="04e70-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="04e70-223">Ha nem ad meg értéket ehhez a paraméterhez, ez a parancsmag egy IP-címet választ az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="04e70-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="04e70-224">– NetI</span><span class="sxs-lookup"><span data-stu-id="04e70-224">-SubnetId</span></span>
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

### <span data-ttu-id="04e70-225">-Címke</span><span class="sxs-lookup"><span data-stu-id="04e70-225">-Tag</span></span>
<span data-ttu-id="04e70-226">A címkéket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="04e70-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="04e70-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="04e70-227">-TenantSettings</span></span>
<span data-ttu-id="04e70-228">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="04e70-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="04e70-229">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="04e70-229">-Zone</span></span>
<span data-ttu-id="04e70-230">A zónák listája.</span><span class="sxs-lookup"><span data-stu-id="04e70-230">List of zones.</span></span>

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

### <span data-ttu-id="04e70-231">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="04e70-231">-Confirm</span></span>
<span data-ttu-id="04e70-232">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="04e70-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04e70-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04e70-233">-WhatIf</span></span>
<span data-ttu-id="04e70-234">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="04e70-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04e70-235">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04e70-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04e70-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e70-236">CommonParameters</span></span>
<span data-ttu-id="04e70-237">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04e70-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e70-238">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04e70-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e70-239">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04e70-239">INPUTS</span></span>

### <span data-ttu-id="04e70-240">System. String</span><span class="sxs-lookup"><span data-stu-id="04e70-240">System.String</span></span>

### <span data-ttu-id="04e70-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="04e70-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="04e70-242">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04e70-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="04e70-243">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04e70-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="04e70-244">System. string []</span><span class="sxs-lookup"><span data-stu-id="04e70-244">System.String[]</span></span>

## <span data-ttu-id="04e70-245">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04e70-245">OUTPUTS</span></span>

### <span data-ttu-id="04e70-246">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="04e70-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="04e70-247">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04e70-247">NOTES</span></span>

## <span data-ttu-id="04e70-248">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04e70-248">RELATED LINKS</span></span>

[<span data-ttu-id="04e70-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04e70-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="04e70-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04e70-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="04e70-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04e70-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


