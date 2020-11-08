---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017677"
---
# <span data-ttu-id="dbed7-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbed7-101">New-AzRedisCache</span></span>

## <span data-ttu-id="dbed7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dbed7-102">SYNOPSIS</span></span>
<span data-ttu-id="dbed7-103">Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dbed7-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="dbed7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dbed7-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbed7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dbed7-105">DESCRIPTION</span></span>
<span data-ttu-id="dbed7-106">A **New-AzRedisCache** parancsmag Azure Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dbed7-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="dbed7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dbed7-107">EXAMPLES</span></span>

### <span data-ttu-id="dbed7-108">Példa 1: Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="dbed7-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="dbed7-109">Ez a parancs Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dbed7-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="dbed7-110">2. példa: szabványos SKU Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="dbed7-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="dbed7-111">Ez a parancs Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dbed7-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="dbed7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dbed7-112">PARAMETERS</span></span>

### <span data-ttu-id="dbed7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbed7-113">-DefaultProfile</span></span>
<span data-ttu-id="dbed7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dbed7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbed7-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="dbed7-115">-EnableNonSslPort</span></span>
<span data-ttu-id="dbed7-116">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="dbed7-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="dbed7-117">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="dbed7-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="dbed7-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="dbed7-118">-Location</span></span>
<span data-ttu-id="dbed7-119">A Redis-gyorsítótár létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbed7-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="dbed7-120">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dbed7-120">Valid values are:</span></span> 
- <span data-ttu-id="dbed7-121">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="dbed7-121">North Central US</span></span>
- <span data-ttu-id="dbed7-122">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="dbed7-122">South Central US</span></span>
- <span data-ttu-id="dbed7-123">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="dbed7-123">Central US</span></span>
- <span data-ttu-id="dbed7-124">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="dbed7-124">West Europe</span></span>
- <span data-ttu-id="dbed7-125">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="dbed7-125">North Europe</span></span>
- <span data-ttu-id="dbed7-126">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="dbed7-126">West US</span></span>
- <span data-ttu-id="dbed7-127">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="dbed7-127">East US</span></span>
- <span data-ttu-id="dbed7-128">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="dbed7-128">East US 2</span></span>
- <span data-ttu-id="dbed7-129">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="dbed7-129">Japan East</span></span>
- <span data-ttu-id="dbed7-130">Japán West</span><span class="sxs-lookup"><span data-stu-id="dbed7-130">Japan West</span></span>
- <span data-ttu-id="dbed7-131">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="dbed7-131">Brazil South</span></span>
- <span data-ttu-id="dbed7-132">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="dbed7-132">Southeast Asia</span></span>
- <span data-ttu-id="dbed7-133">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="dbed7-133">East Asia</span></span>
- <span data-ttu-id="dbed7-134">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="dbed7-134">Australia East</span></span>
- <span data-ttu-id="dbed7-135">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="dbed7-135">Australia Southeast</span></span>

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

### <span data-ttu-id="dbed7-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="dbed7-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="dbed7-137">Adja meg az ügyfelek által a gyorsítótárhoz való csatlakozáshoz szükséges TLS-verziót.</span><span class="sxs-lookup"><span data-stu-id="dbed7-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="dbed7-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dbed7-138">-Name</span></span>
<span data-ttu-id="dbed7-139">A létrehozandó Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbed7-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="dbed7-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbed7-140">-RedisConfiguration</span></span>
<span data-ttu-id="dbed7-141">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbed7-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="dbed7-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dbed7-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dbed7-143">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="dbed7-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="dbed7-144">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="dbed7-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="dbed7-145">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="dbed7-145">Premium tier only.</span></span>
- <span data-ttu-id="dbed7-146">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="dbed7-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="dbed7-147">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbed7-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="dbed7-148">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="dbed7-148">Premium tier only.</span></span>
- <span data-ttu-id="dbed7-149">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="dbed7-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="dbed7-150">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbed7-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="dbed7-151">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="dbed7-151">Premium tier only.</span></span> 
- <span data-ttu-id="dbed7-152">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="dbed7-152">maxmemory-reserved.</span></span>
<span data-ttu-id="dbed7-153">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="dbed7-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="dbed7-154">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbed7-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbed7-155">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="dbed7-155">maxmemory-policy.</span></span>
<span data-ttu-id="dbed7-156">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="dbed7-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="dbed7-157">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="dbed7-157">All pricing tiers.</span></span> 
- <span data-ttu-id="dbed7-158">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="dbed7-158">notify-keyspace-events.</span></span>
<span data-ttu-id="dbed7-159">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="dbed7-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="dbed7-160">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbed7-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="dbed7-161">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="dbed7-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="dbed7-162">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="dbed7-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dbed7-163">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbed7-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbed7-164">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="dbed7-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="dbed7-165">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="dbed7-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dbed7-166">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbed7-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbed7-167">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="dbed7-167">set-max-intset-entries.</span></span>
<span data-ttu-id="dbed7-168">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="dbed7-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dbed7-169">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbed7-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbed7-170">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="dbed7-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="dbed7-171">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="dbed7-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dbed7-172">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbed7-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbed7-173">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="dbed7-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="dbed7-174">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="dbed7-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dbed7-175">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbed7-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dbed7-176">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="dbed7-176">databases.</span></span>
<span data-ttu-id="dbed7-177">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="dbed7-177">Configures the number of databases.</span></span>
<span data-ttu-id="dbed7-178">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="dbed7-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="dbed7-179">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="dbed7-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="dbed7-180">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="dbed7-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="dbed7-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbed7-181">-ResourceGroupName</span></span>
<span data-ttu-id="dbed7-182">Annak az erőforráscsoportnek a nevét adja meg, amelybe a Redis-gyorsítótárat létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="dbed7-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="dbed7-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="dbed7-183">-ShardCount</span></span>
<span data-ttu-id="dbed7-184">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbed7-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="dbed7-185">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dbed7-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dbed7-186">1</span><span class="sxs-lookup"><span data-stu-id="dbed7-186">1</span></span>
- <span data-ttu-id="dbed7-187">2</span><span class="sxs-lookup"><span data-stu-id="dbed7-187">2</span></span>
- <span data-ttu-id="dbed7-188">3</span><span class="sxs-lookup"><span data-stu-id="dbed7-188">3</span></span>
- <span data-ttu-id="dbed7-189">4</span><span class="sxs-lookup"><span data-stu-id="dbed7-189">4</span></span>
- <span data-ttu-id="dbed7-190">5</span><span class="sxs-lookup"><span data-stu-id="dbed7-190">5</span></span>
- <span data-ttu-id="dbed7-191">6</span><span class="sxs-lookup"><span data-stu-id="dbed7-191">6</span></span>
- <span data-ttu-id="dbed7-192">7</span><span class="sxs-lookup"><span data-stu-id="dbed7-192">7</span></span>
- <span data-ttu-id="dbed7-193">8</span><span class="sxs-lookup"><span data-stu-id="dbed7-193">8</span></span>
- <span data-ttu-id="dbed7-194">9</span><span class="sxs-lookup"><span data-stu-id="dbed7-194">9</span></span> 
- <span data-ttu-id="dbed7-195">10</span><span class="sxs-lookup"><span data-stu-id="dbed7-195">10</span></span>

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

### <span data-ttu-id="dbed7-196">-Méret</span><span class="sxs-lookup"><span data-stu-id="dbed7-196">-Size</span></span>
<span data-ttu-id="dbed7-197">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbed7-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="dbed7-198">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dbed7-198">Valid values are:</span></span> 
- <span data-ttu-id="dbed7-199">P1</span><span class="sxs-lookup"><span data-stu-id="dbed7-199">P1</span></span>
- <span data-ttu-id="dbed7-200">P2</span><span class="sxs-lookup"><span data-stu-id="dbed7-200">P2</span></span>
- <span data-ttu-id="dbed7-201">P3</span><span class="sxs-lookup"><span data-stu-id="dbed7-201">P3</span></span>
- <span data-ttu-id="dbed7-202">P4</span><span class="sxs-lookup"><span data-stu-id="dbed7-202">P4</span></span>
- <span data-ttu-id="dbed7-203">P5</span><span class="sxs-lookup"><span data-stu-id="dbed7-203">P5</span></span>
- <span data-ttu-id="dbed7-204">C0</span><span class="sxs-lookup"><span data-stu-id="dbed7-204">C0</span></span>
- <span data-ttu-id="dbed7-205">C1</span><span class="sxs-lookup"><span data-stu-id="dbed7-205">C1</span></span>
- <span data-ttu-id="dbed7-206">C2</span><span class="sxs-lookup"><span data-stu-id="dbed7-206">C2</span></span>
- <span data-ttu-id="dbed7-207">C3</span><span class="sxs-lookup"><span data-stu-id="dbed7-207">C3</span></span>
- <span data-ttu-id="dbed7-208">C4</span><span class="sxs-lookup"><span data-stu-id="dbed7-208">C4</span></span>
- <span data-ttu-id="dbed7-209">C5</span><span class="sxs-lookup"><span data-stu-id="dbed7-209">C5</span></span>
- <span data-ttu-id="dbed7-210">C6</span><span class="sxs-lookup"><span data-stu-id="dbed7-210">C6</span></span>
- <span data-ttu-id="dbed7-211">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="dbed7-211">250MB</span></span>
- <span data-ttu-id="dbed7-212">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="dbed7-212">1GB</span></span>
- <span data-ttu-id="dbed7-213">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="dbed7-213">2.5GB</span></span>
- <span data-ttu-id="dbed7-214">6GB</span><span class="sxs-lookup"><span data-stu-id="dbed7-214">6GB</span></span>
- <span data-ttu-id="dbed7-215">13GB</span><span class="sxs-lookup"><span data-stu-id="dbed7-215">13GB</span></span>
- <span data-ttu-id="dbed7-216">26GB</span><span class="sxs-lookup"><span data-stu-id="dbed7-216">26GB</span></span>
- <span data-ttu-id="dbed7-217">53GB az alapértelmezett érték 1GB vagy C1.</span><span class="sxs-lookup"><span data-stu-id="dbed7-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="dbed7-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="dbed7-218">-Sku</span></span>
<span data-ttu-id="dbed7-219">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="dbed7-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="dbed7-220">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dbed7-220">Valid values are:</span></span> 
- <span data-ttu-id="dbed7-221">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="dbed7-221">Basic</span></span>
- <span data-ttu-id="dbed7-222">Standard</span><span class="sxs-lookup"><span data-stu-id="dbed7-222">Standard</span></span>
- <span data-ttu-id="dbed7-223">Prémium: az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="dbed7-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="dbed7-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="dbed7-224">-StaticIP</span></span>
<span data-ttu-id="dbed7-225">Egy egyedi IP-címet ad meg a Redis-gyorsítótár alhálózatában.</span><span class="sxs-lookup"><span data-stu-id="dbed7-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="dbed7-226">Ha nem ad meg értéket ehhez a paraméterhez, ez a parancsmag egy IP-címet választ az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="dbed7-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="dbed7-227">– NetI</span><span class="sxs-lookup"><span data-stu-id="dbed7-227">-SubnetId</span></span>
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

### <span data-ttu-id="dbed7-228">-Címke</span><span class="sxs-lookup"><span data-stu-id="dbed7-228">-Tag</span></span>
<span data-ttu-id="dbed7-229">A címkéket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="dbed7-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="dbed7-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="dbed7-230">-TenantSettings</span></span>
<span data-ttu-id="dbed7-231">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="dbed7-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="dbed7-232">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="dbed7-232">-Zone</span></span>
<span data-ttu-id="dbed7-233">A zónák listája.</span><span class="sxs-lookup"><span data-stu-id="dbed7-233">List of zones.</span></span>

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

### <span data-ttu-id="dbed7-234">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dbed7-234">-Confirm</span></span>
<span data-ttu-id="dbed7-235">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dbed7-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbed7-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbed7-236">-WhatIf</span></span>
<span data-ttu-id="dbed7-237">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dbed7-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbed7-238">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dbed7-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbed7-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbed7-239">CommonParameters</span></span>
<span data-ttu-id="dbed7-240">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dbed7-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbed7-241">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dbed7-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbed7-242">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbed7-242">INPUTS</span></span>

### <span data-ttu-id="dbed7-243">System. String</span><span class="sxs-lookup"><span data-stu-id="dbed7-243">System.String</span></span>

### <span data-ttu-id="dbed7-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dbed7-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dbed7-245">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dbed7-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dbed7-246">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dbed7-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dbed7-247">System. string []</span><span class="sxs-lookup"><span data-stu-id="dbed7-247">System.String[]</span></span>

## <span data-ttu-id="dbed7-248">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbed7-248">OUTPUTS</span></span>

### <span data-ttu-id="dbed7-249">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="dbed7-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="dbed7-250">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dbed7-250">NOTES</span></span>

## <span data-ttu-id="dbed7-251">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbed7-251">RELATED LINKS</span></span>

[<span data-ttu-id="dbed7-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbed7-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="dbed7-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbed7-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="dbed7-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbed7-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


