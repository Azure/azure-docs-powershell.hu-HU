---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494393"
---
# <span data-ttu-id="2bbd8-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2bbd8-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="2bbd8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2bbd8-102">SYNOPSIS</span></span>
<span data-ttu-id="2bbd8-103">Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bbd8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2bbd8-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bbd8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2bbd8-105">DESCRIPTION</span></span>
<span data-ttu-id="2bbd8-106">A **New-AzureRmRedisCache** parancsmag Azure Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="2bbd8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2bbd8-107">EXAMPLES</span></span>

### <span data-ttu-id="2bbd8-108">Példa 1: Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="2bbd8-108">Example 1: Create a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="2bbd8-109">Ez a parancs Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="2bbd8-110">2. példa: szabványos SKU Redis-gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="2bbd8-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="2bbd8-111">Ez a parancs Redis-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="2bbd8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2bbd8-112">PARAMETERS</span></span>

### <span data-ttu-id="2bbd8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bbd8-113">-DefaultProfile</span></span>
<span data-ttu-id="2bbd8-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bbd8-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="2bbd8-115">-EnableNonSslPort</span></span>
<span data-ttu-id="2bbd8-116">Azt jelzi, hogy engedélyezve van-e a nem SSL-port.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="2bbd8-117">Az alapértelmezett érték $False (a nem SSL-port van letiltva).</span><span class="sxs-lookup"><span data-stu-id="2bbd8-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="2bbd8-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="2bbd8-118">-Location</span></span>
<span data-ttu-id="2bbd8-119">A Redis-gyorsítótár létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="2bbd8-120">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="2bbd8-120">Valid values are:</span></span> 

- <span data-ttu-id="2bbd8-121">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="2bbd8-121">North Central US</span></span>
- <span data-ttu-id="2bbd8-122">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="2bbd8-122">South Central US</span></span>
- <span data-ttu-id="2bbd8-123">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="2bbd8-123">Central US</span></span>
- <span data-ttu-id="2bbd8-124">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="2bbd8-124">West Europe</span></span>
- <span data-ttu-id="2bbd8-125">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="2bbd8-125">North Europe</span></span>
- <span data-ttu-id="2bbd8-126">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="2bbd8-126">West US</span></span>
- <span data-ttu-id="2bbd8-127">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="2bbd8-127">East US</span></span>
- <span data-ttu-id="2bbd8-128">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="2bbd8-128">East US 2</span></span>
- <span data-ttu-id="2bbd8-129">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="2bbd8-129">Japan East</span></span>
- <span data-ttu-id="2bbd8-130">Japán West</span><span class="sxs-lookup"><span data-stu-id="2bbd8-130">Japan West</span></span>
- <span data-ttu-id="2bbd8-131">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="2bbd8-131">Brazil South</span></span>
- <span data-ttu-id="2bbd8-132">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="2bbd8-132">Southeast Asia</span></span>
- <span data-ttu-id="2bbd8-133">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="2bbd8-133">East Asia</span></span>
- <span data-ttu-id="2bbd8-134">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="2bbd8-134">Australia East</span></span>
- <span data-ttu-id="2bbd8-135">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="2bbd8-135">Australia Southeast</span></span>

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

### <span data-ttu-id="2bbd8-136">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="2bbd8-136">-MaxMemoryPolicy</span></span>
<span data-ttu-id="2bbd8-137">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-137">This parameter has been deprecated.</span></span>
<span data-ttu-id="2bbd8-138">A *RedisConfiguration* paraméterrel megadhatja a maxmemory-házirendet.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-138">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="2bbd8-139">Példa:</span><span class="sxs-lookup"><span data-stu-id="2bbd8-139">For example:</span></span> 

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

### <span data-ttu-id="2bbd8-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2bbd8-140">-Name</span></span>
<span data-ttu-id="2bbd8-141">A létrehozandó Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-141">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="2bbd8-142">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bbd8-142">-RedisConfiguration</span></span>
<span data-ttu-id="2bbd8-143">A Redis konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-143">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="2bbd8-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2bbd8-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2bbd8-145">RDB – biztonsági másolat engedélyezve</span><span class="sxs-lookup"><span data-stu-id="2bbd8-145">rdb-backup-enabled.</span></span>
<span data-ttu-id="2bbd8-146">Megadja, hogy a Redis-adatmegőrzés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-146">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="2bbd8-147">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="2bbd8-147">Premium tier only.</span></span>
- <span data-ttu-id="2bbd8-148">RDB – tárolási kapcsolat – karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-148">rdb-storage-connection-string.</span></span>
<span data-ttu-id="2bbd8-149">A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-149">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="2bbd8-150">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="2bbd8-150">Premium tier only.</span></span>
- <span data-ttu-id="2bbd8-151">RDB-Backup-frekvencia.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-151">rdb-backup-frequency.</span></span>
<span data-ttu-id="2bbd8-152">A Redis adatmegőrzési gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-152">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="2bbd8-153">Prémium szint</span><span class="sxs-lookup"><span data-stu-id="2bbd8-153">Premium tier only.</span></span> 
- <span data-ttu-id="2bbd8-154">maxmemory – fenntartva.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-154">maxmemory-reserved.</span></span>
<span data-ttu-id="2bbd8-155">A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-155">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="2bbd8-156">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-156">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2bbd8-157">maxmemory – házirend.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-157">maxmemory-policy.</span></span>
<span data-ttu-id="2bbd8-158">A gyorsítótár kilakoltatási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-158">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="2bbd8-159">Minden árazási szint.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-159">All pricing tiers.</span></span> 
- <span data-ttu-id="2bbd8-160">értesítés – a szóköz – események.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-160">notify-keyspace-events.</span></span>
<span data-ttu-id="2bbd8-161">A szóközökkel kapcsolatos értesítések beállítása.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-161">Configures keyspace notifications.</span></span>
<span data-ttu-id="2bbd8-162">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-162">Standard and premium tiers.</span></span> 
- <span data-ttu-id="2bbd8-163">hash-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-163">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="2bbd8-164">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-164">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2bbd8-165">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-165">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2bbd8-166">hash-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-166">hash-max-ziplist-value.</span></span>
<span data-ttu-id="2bbd8-167">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-167">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2bbd8-168">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-168">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2bbd8-169">set-Max-intset-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-169">set-max-intset-entries.</span></span>
<span data-ttu-id="2bbd8-170">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-170">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2bbd8-171">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-171">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2bbd8-172">zset-Max-ZipList-bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-172">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="2bbd8-173">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-173">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2bbd8-174">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-174">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2bbd8-175">zset-Max-ZipList-érték.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-175">zset-max-ziplist-value.</span></span>
<span data-ttu-id="2bbd8-176">A kis összesített adattípusok memória-optimalizálását állítja be.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-176">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2bbd8-177">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-177">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2bbd8-178">adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-178">databases.</span></span>
<span data-ttu-id="2bbd8-179">Az adatbázisok számának beállítása.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-179">Configures the number of databases.</span></span>
<span data-ttu-id="2bbd8-180">Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-180">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="2bbd8-181">Standard és prémium szintek.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-181">Standard and Premium tiers.</span></span>

<span data-ttu-id="2bbd8-182">További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="2bbd8-182">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="2bbd8-183">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="2bbd8-183">-RedisVersion</span></span>
<span data-ttu-id="2bbd8-184">Ez a paraméter elavult, és a jövőbeli kiadásokból törlődik.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-184">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="2bbd8-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bbd8-185">-ResourceGroupName</span></span>
<span data-ttu-id="2bbd8-186">Annak az erőforráscsoportnek a nevét adja meg, amelybe a Redis-gyorsítótárat létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-186">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="2bbd8-187">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="2bbd8-187">-ShardCount</span></span>
<span data-ttu-id="2bbd8-188">A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-188">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="2bbd8-189">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2bbd8-189">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2bbd8-190">1</span><span class="sxs-lookup"><span data-stu-id="2bbd8-190">1</span></span>
- <span data-ttu-id="2bbd8-191">2</span><span class="sxs-lookup"><span data-stu-id="2bbd8-191">2</span></span>
- <span data-ttu-id="2bbd8-192">3</span><span class="sxs-lookup"><span data-stu-id="2bbd8-192">3</span></span>
- <span data-ttu-id="2bbd8-193">4</span><span class="sxs-lookup"><span data-stu-id="2bbd8-193">4</span></span>
- <span data-ttu-id="2bbd8-194">5</span><span class="sxs-lookup"><span data-stu-id="2bbd8-194">5</span></span>
- <span data-ttu-id="2bbd8-195">6</span><span class="sxs-lookup"><span data-stu-id="2bbd8-195">6</span></span>
- <span data-ttu-id="2bbd8-196">7</span><span class="sxs-lookup"><span data-stu-id="2bbd8-196">7</span></span>
- <span data-ttu-id="2bbd8-197">8</span><span class="sxs-lookup"><span data-stu-id="2bbd8-197">8</span></span>
- <span data-ttu-id="2bbd8-198">9</span><span class="sxs-lookup"><span data-stu-id="2bbd8-198">9</span></span> 
- <span data-ttu-id="2bbd8-199">10</span><span class="sxs-lookup"><span data-stu-id="2bbd8-199">10</span></span>

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

### <span data-ttu-id="2bbd8-200">-Méret</span><span class="sxs-lookup"><span data-stu-id="2bbd8-200">-Size</span></span>
<span data-ttu-id="2bbd8-201">A Redis-gyorsítótár méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-201">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="2bbd8-202">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="2bbd8-202">Valid values are:</span></span> 

- <span data-ttu-id="2bbd8-203">P1</span><span class="sxs-lookup"><span data-stu-id="2bbd8-203">P1</span></span>
- <span data-ttu-id="2bbd8-204">P2</span><span class="sxs-lookup"><span data-stu-id="2bbd8-204">P2</span></span>
- <span data-ttu-id="2bbd8-205">P3</span><span class="sxs-lookup"><span data-stu-id="2bbd8-205">P3</span></span>
- <span data-ttu-id="2bbd8-206">P4</span><span class="sxs-lookup"><span data-stu-id="2bbd8-206">P4</span></span>
- <span data-ttu-id="2bbd8-207">C0</span><span class="sxs-lookup"><span data-stu-id="2bbd8-207">C0</span></span>
- <span data-ttu-id="2bbd8-208">C1</span><span class="sxs-lookup"><span data-stu-id="2bbd8-208">C1</span></span>
- <span data-ttu-id="2bbd8-209">C2</span><span class="sxs-lookup"><span data-stu-id="2bbd8-209">C2</span></span>
- <span data-ttu-id="2bbd8-210">C3</span><span class="sxs-lookup"><span data-stu-id="2bbd8-210">C3</span></span>
- <span data-ttu-id="2bbd8-211">C4</span><span class="sxs-lookup"><span data-stu-id="2bbd8-211">C4</span></span>
- <span data-ttu-id="2bbd8-212">C5</span><span class="sxs-lookup"><span data-stu-id="2bbd8-212">C5</span></span>
- <span data-ttu-id="2bbd8-213">C6</span><span class="sxs-lookup"><span data-stu-id="2bbd8-213">C6</span></span>
- <span data-ttu-id="2bbd8-214">250 MB méretű</span><span class="sxs-lookup"><span data-stu-id="2bbd8-214">250MB</span></span>
- <span data-ttu-id="2bbd8-215">GIGABÁJTNÁL szükséges</span><span class="sxs-lookup"><span data-stu-id="2bbd8-215">1GB</span></span>
- <span data-ttu-id="2bbd8-216">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="2bbd8-216">2.5GB</span></span>
- <span data-ttu-id="2bbd8-217">6GB</span><span class="sxs-lookup"><span data-stu-id="2bbd8-217">6GB</span></span>
- <span data-ttu-id="2bbd8-218">13GB</span><span class="sxs-lookup"><span data-stu-id="2bbd8-218">13GB</span></span>
- <span data-ttu-id="2bbd8-219">26GB</span><span class="sxs-lookup"><span data-stu-id="2bbd8-219">26GB</span></span>
- <span data-ttu-id="2bbd8-220">53GB</span><span class="sxs-lookup"><span data-stu-id="2bbd8-220">53GB</span></span>

<span data-ttu-id="2bbd8-221">Az alapértelmezett érték az 1GB vagy a C1.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-221">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="2bbd8-222">-SKU</span><span class="sxs-lookup"><span data-stu-id="2bbd8-222">-Sku</span></span>
<span data-ttu-id="2bbd8-223">Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-223">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="2bbd8-224">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="2bbd8-224">Valid values are:</span></span> 

- <span data-ttu-id="2bbd8-225">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="2bbd8-225">Basic</span></span>
- <span data-ttu-id="2bbd8-226">Standard</span><span class="sxs-lookup"><span data-stu-id="2bbd8-226">Standard</span></span>
- <span data-ttu-id="2bbd8-227">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="2bbd8-227">Premium</span></span>

<span data-ttu-id="2bbd8-228">Az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-228">The default value is Standard.</span></span>

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

### <span data-ttu-id="2bbd8-229">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="2bbd8-229">-StaticIP</span></span>
<span data-ttu-id="2bbd8-230">Egy egyedi IP-címet ad meg a Redis-gyorsítótár alhálózatában.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-230">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="2bbd8-231">Ha nem ad meg értéket ehhez a paraméterhez, ez a parancsmag egy IP-címet választ az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-231">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="2bbd8-232">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="2bbd8-232">-Subnet</span></span>
<span data-ttu-id="2bbd8-233">Annak az alhálózatnak a neve, amelybe a Redis-gyorsítótárat telepíteni kell.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-233">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="2bbd8-234">– NetI</span><span class="sxs-lookup"><span data-stu-id="2bbd8-234">-SubnetId</span></span>
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

### <span data-ttu-id="2bbd8-235">-Címke</span><span class="sxs-lookup"><span data-stu-id="2bbd8-235">-Tag</span></span>
<span data-ttu-id="2bbd8-236">A címkéket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-236">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="2bbd8-237">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="2bbd8-237">-TenantSettings</span></span>
<span data-ttu-id="2bbd8-238">Ezt a paramétert érvénytelenítették.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-238">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="2bbd8-239">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2bbd8-239">-VirtualNetwork</span></span>
<span data-ttu-id="2bbd8-240">Annak a virtuális hálózatnak az erőforrás-AZONOSÍTÓját adja meg, amelybe telepíteni szeretné a Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-240">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="2bbd8-241">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="2bbd8-241">-Zone</span></span>
<span data-ttu-id="2bbd8-242">A zónák listája.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-242">List of zones.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bbd8-243">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2bbd8-243">-Confirm</span></span>
<span data-ttu-id="2bbd8-244">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bbd8-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bbd8-245">-WhatIf</span></span>
<span data-ttu-id="2bbd8-246">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-246">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bbd8-247">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bbd8-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bbd8-248">CommonParameters</span></span>
<span data-ttu-id="2bbd8-249">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2bbd8-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bbd8-250">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bbd8-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bbd8-251">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bbd8-251">INPUTS</span></span>

### <span data-ttu-id="2bbd8-252">Nincs</span><span class="sxs-lookup"><span data-stu-id="2bbd8-252">None</span></span>
<span data-ttu-id="2bbd8-253">A parancsmagot név szerint, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-253">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="2bbd8-254">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bbd8-254">OUTPUTS</span></span>

### <span data-ttu-id="2bbd8-255">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2bbd8-255">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="2bbd8-256">Ez a parancsmag a Redis-gyorsítótár minden attribútumát megjeleníti, az elsődleges és másodlagos elérési kulcsokat is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="2bbd8-256">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="2bbd8-257">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2bbd8-257">NOTES</span></span>

## <span data-ttu-id="2bbd8-258">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2bbd8-258">RELATED LINKS</span></span>

[<span data-ttu-id="2bbd8-259">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2bbd8-259">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="2bbd8-260">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2bbd8-260">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="2bbd8-261">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2bbd8-261">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


