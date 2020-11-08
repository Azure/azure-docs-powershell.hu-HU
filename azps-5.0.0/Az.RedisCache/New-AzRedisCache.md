---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194187"
---
# <span data-ttu-id="d5e64-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d5e64-101">New-AzRedisCache</span></span>

## <span data-ttu-id="d5e64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5e64-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e64-103">Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d5e64-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="d5e64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5e64-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5e64-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5e64-105">DESCRIPTION</span></span>
<span data-ttu-id="d5e64-106">A **New-AzRedisCache** parancsmag Azure Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d5e64-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="d5e64-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d5e64-107">EXAMPLES</span></span>

### <span data-ttu-id="d5e64-108">Példa 1: Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="d5e64-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="d5e64-109">Ez a parancs Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d5e64-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="d5e64-110">2. példa: szabványos SKU Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="d5e64-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="d5e64-111">Ez a parancs Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d5e64-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="d5e64-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5e64-112">PARAMETERS</span></span>

### <span data-ttu-id="d5e64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e64-113">-DefaultProfile</span></span>
<span data-ttu-id="d5e64-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5e64-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5e64-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="d5e64-115">-EnableNonSslPort</span></span>
<span data-ttu-id="d5e64-116">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="d5e64-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="d5e64-117">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="d5e64-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="d5e64-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="d5e64-118">-Location</span></span>
<span data-ttu-id="d5e64-119">A Redis-gyorsítótár létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5e64-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="d5e64-120">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d5e64-120">Valid values are:</span></span> 
- <span data-ttu-id="d5e64-121">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="d5e64-121">North Central US</span></span>
- <span data-ttu-id="d5e64-122">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="d5e64-122">South Central US</span></span>
- <span data-ttu-id="d5e64-123">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="d5e64-123">Central US</span></span>
- <span data-ttu-id="d5e64-124">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="d5e64-124">West Europe</span></span>
- <span data-ttu-id="d5e64-125">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="d5e64-125">North Europe</span></span>
- <span data-ttu-id="d5e64-126">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="d5e64-126">West US</span></span>
- <span data-ttu-id="d5e64-127">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="d5e64-127">East US</span></span>
- <span data-ttu-id="d5e64-128">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="d5e64-128">East US 2</span></span>
- <span data-ttu-id="d5e64-129">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="d5e64-129">Japan East</span></span>
- <span data-ttu-id="d5e64-130">Japán West</span><span class="sxs-lookup"><span data-stu-id="d5e64-130">Japan West</span></span>
- <span data-ttu-id="d5e64-131">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="d5e64-131">Brazil South</span></span>
- <span data-ttu-id="d5e64-132">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="d5e64-132">Southeast Asia</span></span>
- <span data-ttu-id="d5e64-133">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="d5e64-133">East Asia</span></span>
- <span data-ttu-id="d5e64-134">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="d5e64-134">Australia East</span></span>
- <span data-ttu-id="d5e64-135">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="d5e64-135">Australia Southeast</span></span>

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

### <span data-ttu-id="d5e64-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d5e64-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="d5e64-137">Adja meg az ügyfelek által a gyorsítótárhoz való csatlakozáshoz szükséges TLS-verziót.</span><span class="sxs-lookup"><span data-stu-id="d5e64-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="d5e64-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5e64-138">-Name</span></span>
<span data-ttu-id="d5e64-139">A létrehozandó Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5e64-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="d5e64-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5e64-140">-RedisConfiguration</span></span>
<span data-ttu-id="d5e64-141">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5e64-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="d5e64-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d5e64-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d5e64-143">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="d5e64-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="d5e64-144">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="d5e64-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="d5e64-145">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="d5e64-145">Premium tier only.</span></span>
- <span data-ttu-id="d5e64-146">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="d5e64-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="d5e64-147">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5e64-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="d5e64-148">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="d5e64-148">Premium tier only.</span></span>
- <span data-ttu-id="d5e64-149">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="d5e64-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="d5e64-150">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5e64-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="d5e64-151">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="d5e64-151">Premium tier only.</span></span> 
- <span data-ttu-id="d5e64-152">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="d5e64-152">maxmemory-reserved.</span></span>
<span data-ttu-id="d5e64-153">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="d5e64-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="d5e64-154">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="d5e64-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d5e64-155">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="d5e64-155">maxmemory-policy.</span></span>
<span data-ttu-id="d5e64-156">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="d5e64-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="d5e64-157">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="d5e64-157">All pricing tiers.</span></span> 
- <span data-ttu-id="d5e64-158">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="d5e64-158">notify-keyspace-events.</span></span>
<span data-ttu-id="d5e64-159">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="d5e64-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="d5e64-160">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="d5e64-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="d5e64-161">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="d5e64-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="d5e64-162">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="d5e64-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d5e64-163">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="d5e64-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d5e64-164">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="d5e64-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="d5e64-165">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="d5e64-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d5e64-166">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="d5e64-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d5e64-167">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="d5e64-167">set-max-intset-entries.</span></span>
<span data-ttu-id="d5e64-168">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="d5e64-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d5e64-169">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="d5e64-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d5e64-170">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="d5e64-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="d5e64-171">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="d5e64-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d5e64-172">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="d5e64-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d5e64-173">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="d5e64-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="d5e64-174">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="d5e64-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d5e64-175">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="d5e64-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d5e64-176">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="d5e64-176">databases.</span></span>
<span data-ttu-id="d5e64-177">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="d5e64-177">Configures the number of databases.</span></span>
<span data-ttu-id="d5e64-178">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="d5e64-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="d5e64-179">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="d5e64-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="d5e64-180">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="d5e64-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="d5e64-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e64-181">-ResourceGroupName</span></span>
<span data-ttu-id="d5e64-182">Annak az erőforráscsoportnek a nevét adja meg, amelybe a Redis-gyorsítótárat létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="d5e64-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="d5e64-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="d5e64-183">-ShardCount</span></span>
<span data-ttu-id="d5e64-184">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5e64-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="d5e64-185">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d5e64-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d5e64-186">1</span><span class="sxs-lookup"><span data-stu-id="d5e64-186">1</span></span>
- <span data-ttu-id="d5e64-187">2</span><span class="sxs-lookup"><span data-stu-id="d5e64-187">2</span></span>
- <span data-ttu-id="d5e64-188">3</span><span class="sxs-lookup"><span data-stu-id="d5e64-188">3</span></span>
- <span data-ttu-id="d5e64-189">4</span><span class="sxs-lookup"><span data-stu-id="d5e64-189">4</span></span>
- <span data-ttu-id="d5e64-190">5</span><span class="sxs-lookup"><span data-stu-id="d5e64-190">5</span></span>
- <span data-ttu-id="d5e64-191">6</span><span class="sxs-lookup"><span data-stu-id="d5e64-191">6</span></span>
- <span data-ttu-id="d5e64-192">7</span><span class="sxs-lookup"><span data-stu-id="d5e64-192">7</span></span>
- <span data-ttu-id="d5e64-193">8</span><span class="sxs-lookup"><span data-stu-id="d5e64-193">8</span></span>
- <span data-ttu-id="d5e64-194">9</span><span class="sxs-lookup"><span data-stu-id="d5e64-194">9</span></span> 
- <span data-ttu-id="d5e64-195">10</span><span class="sxs-lookup"><span data-stu-id="d5e64-195">10</span></span>

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

### <span data-ttu-id="d5e64-196">-Méret</span><span class="sxs-lookup"><span data-stu-id="d5e64-196">-Size</span></span>
<span data-ttu-id="d5e64-197">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5e64-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="d5e64-198">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d5e64-198">Valid values are:</span></span> 
- <span data-ttu-id="d5e64-199">P1</span><span class="sxs-lookup"><span data-stu-id="d5e64-199">P1</span></span>
- <span data-ttu-id="d5e64-200">P2</span><span class="sxs-lookup"><span data-stu-id="d5e64-200">P2</span></span>
- <span data-ttu-id="d5e64-201">P3</span><span class="sxs-lookup"><span data-stu-id="d5e64-201">P3</span></span>
- <span data-ttu-id="d5e64-202">P4</span><span class="sxs-lookup"><span data-stu-id="d5e64-202">P4</span></span>
- <span data-ttu-id="d5e64-203">P5</span><span class="sxs-lookup"><span data-stu-id="d5e64-203">P5</span></span>
- <span data-ttu-id="d5e64-204">C0</span><span class="sxs-lookup"><span data-stu-id="d5e64-204">C0</span></span>
- <span data-ttu-id="d5e64-205">C1</span><span class="sxs-lookup"><span data-stu-id="d5e64-205">C1</span></span>
- <span data-ttu-id="d5e64-206">C2</span><span class="sxs-lookup"><span data-stu-id="d5e64-206">C2</span></span>
- <span data-ttu-id="d5e64-207">C3</span><span class="sxs-lookup"><span data-stu-id="d5e64-207">C3</span></span>
- <span data-ttu-id="d5e64-208">C4</span><span class="sxs-lookup"><span data-stu-id="d5e64-208">C4</span></span>
- <span data-ttu-id="d5e64-209">C5</span><span class="sxs-lookup"><span data-stu-id="d5e64-209">C5</span></span>
- <span data-ttu-id="d5e64-210">C6</span><span class="sxs-lookup"><span data-stu-id="d5e64-210">C6</span></span>
- <span data-ttu-id="d5e64-211">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="d5e64-211">250MB</span></span>
- <span data-ttu-id="d5e64-212">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="d5e64-212">1GB</span></span>
- <span data-ttu-id="d5e64-213">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="d5e64-213">2.5GB</span></span>
- <span data-ttu-id="d5e64-214">6GB</span><span class="sxs-lookup"><span data-stu-id="d5e64-214">6GB</span></span>
- <span data-ttu-id="d5e64-215">13GB</span><span class="sxs-lookup"><span data-stu-id="d5e64-215">13GB</span></span>
- <span data-ttu-id="d5e64-216">26GB</span><span class="sxs-lookup"><span data-stu-id="d5e64-216">26GB</span></span>
- <span data-ttu-id="d5e64-217">53GB az alapértelmezett érték 1GB vagy C1.</span><span class="sxs-lookup"><span data-stu-id="d5e64-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="d5e64-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="d5e64-218">-Sku</span></span>
<span data-ttu-id="d5e64-219">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="d5e64-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="d5e64-220">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d5e64-220">Valid values are:</span></span> 
- <span data-ttu-id="d5e64-221">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="d5e64-221">Basic</span></span>
- <span data-ttu-id="d5e64-222">Standard</span><span class="sxs-lookup"><span data-stu-id="d5e64-222">Standard</span></span>
- <span data-ttu-id="d5e64-223">Prémium: az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="d5e64-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="d5e64-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="d5e64-224">-StaticIP</span></span>
<span data-ttu-id="d5e64-225">Egy egyedi IP-címet ad meg a Redis-gyorsítótár alhálózatában.</span><span class="sxs-lookup"><span data-stu-id="d5e64-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="d5e64-226">Ha nem ad meg értéket ehhez a paraméterhez, ez a parancsmag egy IP-címet választ az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="d5e64-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="d5e64-227">– NetI</span><span class="sxs-lookup"><span data-stu-id="d5e64-227">-SubnetId</span></span>
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

### <span data-ttu-id="d5e64-228">-Címke</span><span class="sxs-lookup"><span data-stu-id="d5e64-228">-Tag</span></span>
<span data-ttu-id="d5e64-229">A címkéket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="d5e64-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="d5e64-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="d5e64-230">-TenantSettings</span></span>
<span data-ttu-id="d5e64-231">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="d5e64-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="d5e64-232">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="d5e64-232">-Zone</span></span>
<span data-ttu-id="d5e64-233">A zónák listája.</span><span class="sxs-lookup"><span data-stu-id="d5e64-233">List of zones.</span></span>

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

### <span data-ttu-id="d5e64-234">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d5e64-234">-Confirm</span></span>
<span data-ttu-id="d5e64-235">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d5e64-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5e64-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5e64-236">-WhatIf</span></span>
<span data-ttu-id="d5e64-237">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d5e64-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5e64-238">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d5e64-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5e64-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e64-239">CommonParameters</span></span>
<span data-ttu-id="d5e64-240">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5e64-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e64-241">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d5e64-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e64-242">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5e64-242">INPUTS</span></span>

### <span data-ttu-id="d5e64-243">System. String</span><span class="sxs-lookup"><span data-stu-id="d5e64-243">System.String</span></span>

### <span data-ttu-id="d5e64-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d5e64-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d5e64-245">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d5e64-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d5e64-246">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d5e64-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d5e64-247">System. string []</span><span class="sxs-lookup"><span data-stu-id="d5e64-247">System.String[]</span></span>

## <span data-ttu-id="d5e64-248">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5e64-248">OUTPUTS</span></span>

### <span data-ttu-id="d5e64-249">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d5e64-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="d5e64-250">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5e64-250">NOTES</span></span>

## <span data-ttu-id="d5e64-251">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5e64-251">RELATED LINKS</span></span>

[<span data-ttu-id="d5e64-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d5e64-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="d5e64-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d5e64-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d5e64-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d5e64-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


