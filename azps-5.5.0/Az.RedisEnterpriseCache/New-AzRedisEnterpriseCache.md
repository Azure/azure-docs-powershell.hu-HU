---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: f2f996bc212772b3b44202796e270ec345898a11
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169195"
---
# <span data-ttu-id="e9b2e-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="e9b2e-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="e9b2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b2e-103">Redis Enterpise gyorsítótárcsoportot és kapcsolódó adatbázist hoz létre</span><span class="sxs-lookup"><span data-stu-id="e9b2e-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="e9b2e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9b2e-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e9b2e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9b2e-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b2e-106">Egy meglévő (felülírás/újraírás, esetleg állásidővel járó) gyorsítótárcsoport és egy "alapértelmezett" nevű társított adatbázis létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="e9b2e-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="e9b2e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9b2e-107">EXAMPLES</span></span>

### <span data-ttu-id="e9b2e-108">1. példa: Redis Nagyvállalati gyorsítótár létrehozása</span><span class="sxs-lookup"><span data-stu-id="e9b2e-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="e9b2e-109">Ez a parancs létrehoz egy MyCache nevű Redis Enterprise Cachet.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="e9b2e-110">2. példa: A nagyvállalati gyorsítótár létrehozása néhány választható paraméter használatával</span><span class="sxs-lookup"><span data-stu-id="e9b2e-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="e9b2e-111">Ez a parancs létrehoz egy MyCache nevű Redis Enterprise Cachet néhány választható paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="e9b2e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9b2e-112">PARAMETERS</span></span>

### <span data-ttu-id="e9b2e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9b2e-113">-AsJob</span></span>
<span data-ttu-id="e9b2e-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="e9b2e-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-115">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="e9b2e-115">-Capacity</span></span>
<span data-ttu-id="e9b2e-116">A RedisEnterprise fürt mérete.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="e9b2e-117">Az alapérték a termékváltozattól függően 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="e9b2e-118">A nagyvállalati SKUs-k érvényes értékei (2, 4, 6, ...), a Flash-SK-k pedig (3, 9, 15, ...).</span><span class="sxs-lookup"><span data-stu-id="e9b2e-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: SkuCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="e9b2e-119">-ClientProtocol</span></span>
<span data-ttu-id="e9b2e-120">Azt adja meg, hogy a redis clients csatlakozhatnak-e TLS-titkosítással vagy egyszerű szöveges redis protokollal.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="e9b2e-121">Az alapértelmezett beállítás a TLS által titkosított.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-121">Default is TLS-encrypted.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="e9b2e-122">-ClusteringPolicy</span></span>
<span data-ttu-id="e9b2e-123">Fürtözési házirend – az alapértelmezett érték az OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="e9b2e-124">A létrehozási időpontban van megadva.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-124">Specified at create time.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-125">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e9b2e-125">-ClusterName</span></span>
<span data-ttu-id="e9b2e-126">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-126">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b2e-127">-DefaultProfile</span></span>
<span data-ttu-id="e9b2e-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="e9b2e-129">-EvictionPolicy</span></span>
<span data-ttu-id="e9b2e-130">Redis eviction policy - default is VolatileLRU.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-130">Redis eviction policy - default is VolatileLRU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-131">-Location</span><span class="sxs-lookup"><span data-stu-id="e9b2e-131">-Location</span></span>
<span data-ttu-id="e9b2e-132">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="e9b2e-132">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e9b2e-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="e9b2e-134">A támogatott fürt minimális TLS-verziója, például 1.2</span><span class="sxs-lookup"><span data-stu-id="e9b2e-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-135">-Module</span><span class="sxs-lookup"><span data-stu-id="e9b2e-135">-Module</span></span>
<span data-ttu-id="e9b2e-136">Az adatbázisban engedélyezhető redis modulok opcionális készlete – a modulok csak létrehozási időben hozzáadhatóak.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="e9b2e-137">A MODUL tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK című szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e9b2e-138">-NoWait</span></span>
<span data-ttu-id="e9b2e-139">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="e9b2e-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-140">-Port</span><span class="sxs-lookup"><span data-stu-id="e9b2e-140">-Port</span></span>
<span data-ttu-id="e9b2e-141">Az adatbázis végpontjának TCP-portja.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="e9b2e-142">A létrehozási időpontban van megadva.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-142">Specified at create time.</span></span>
<span data-ttu-id="e9b2e-143">Alapértelmezés szerint egy elérhető port van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-143">Defaults to an available port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b2e-144">-ResourceGroupName</span></span>
<span data-ttu-id="e9b2e-145">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-146">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="e9b2e-146">-Sku</span></span>
<span data-ttu-id="e9b2e-147">A telepíthető RedisEnterprise-fürt típusa.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="e9b2e-148">Lehetséges értékek: (Enterprise_E10, EnterpriseFlash_F300 stb.)</span><span class="sxs-lookup"><span data-stu-id="e9b2e-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9b2e-149">-SubscriptionId</span></span>
<span data-ttu-id="e9b2e-150">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e9b2e-151">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-151">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9b2e-152">-Tag</span></span>
<span data-ttu-id="e9b2e-153">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-153">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="e9b2e-154">-Zone</span></span>
<span data-ttu-id="e9b2e-155">A fürt üzembe helyezésének zónái.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-155">The zones where this cluster will be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b2e-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9b2e-156">-Confirm</span></span>
<span data-ttu-id="e9b2e-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9b2e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9b2e-158">-WhatIf</span></span>
<span data-ttu-id="e9b2e-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9b2e-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9b2e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b2e-161">CommonParameters</span></span>
<span data-ttu-id="e9b2e-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b2e-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9b2e-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b2e-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9b2e-164">INPUTS</span></span>

## <span data-ttu-id="e9b2e-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9b2e-165">OUTPUTS</span></span>

### <span data-ttu-id="e9b2e-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="e9b2e-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="e9b2e-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9b2e-167">NOTES</span></span>

<span data-ttu-id="e9b2e-168">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e9b2e-168">ALIASES</span></span>

<span data-ttu-id="e9b2e-169">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e9b2e-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e9b2e-170">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e9b2e-171">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e9b2e-172">MODULE <IModule[]>: Az adatbázisban engedélyezhető redismodulok opcionális készlete – a modulok csak létrehozási időben hozzáadhatóak.</span><span class="sxs-lookup"><span data-stu-id="e9b2e-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="e9b2e-173">`Name <String>`: A modul neve, például "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="e9b2e-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="e9b2e-174">`[Arg <String>]`: A modul konfigurációs beállításai, például "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="e9b2e-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="e9b2e-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9b2e-175">RELATED LINKS</span></span>

