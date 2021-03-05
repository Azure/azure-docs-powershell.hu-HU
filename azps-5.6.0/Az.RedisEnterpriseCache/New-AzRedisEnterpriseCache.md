---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: 43ad21450666fb2db9a25e1e2803651eacf511d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000758"
---
# <span data-ttu-id="2fcaa-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="2fcaa-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="2fcaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fcaa-102">SYNOPSIS</span></span>
<span data-ttu-id="2fcaa-103">Redis Enterpise gyorsítótár-fürt és egy társított adatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="2fcaa-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="2fcaa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2fcaa-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2fcaa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2fcaa-105">DESCRIPTION</span></span>
<span data-ttu-id="2fcaa-106">Egy meglévő (felülírás/újraírás, esetleg állásidővel járó) gyorsítótárcsoport és egy "alapértelmezett" nevű társított adatbázis létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="2fcaa-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="2fcaa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2fcaa-107">EXAMPLES</span></span>

### <span data-ttu-id="2fcaa-108">1. példa: A nagyvállalati gyorsítótár újradiskedése</span><span class="sxs-lookup"><span data-stu-id="2fcaa-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="2fcaa-109">Ez a parancs létrehoz egy MyCache nevű Redis Enterprise Cachet.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="2fcaa-110">2. példa: A nagyvállalati gyorsítótár létrehozása néhány választható paraméter használatával</span><span class="sxs-lookup"><span data-stu-id="2fcaa-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="2fcaa-111">Ez a parancs létrehoz egy MyCache nevű Redis Enterprise Cachet néhány választható paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="2fcaa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fcaa-112">PARAMETERS</span></span>

### <span data-ttu-id="2fcaa-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fcaa-113">-AsJob</span></span>
<span data-ttu-id="2fcaa-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="2fcaa-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2fcaa-115">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="2fcaa-115">-Capacity</span></span>
<span data-ttu-id="2fcaa-116">A RedisEnterprise fürt mérete.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="2fcaa-117">Az alapérték 2 vagy 3 az adott termékváltozattól függően.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="2fcaa-118">A nagyvállalati SKUs-k érvényes értékei (2, 4, 6, ...), a Flash-SK-k pedig (3, 9, 15, ...).</span><span class="sxs-lookup"><span data-stu-id="2fcaa-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="2fcaa-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="2fcaa-119">-ClientProtocol</span></span>
<span data-ttu-id="2fcaa-120">Azt adja meg, hogy a redis clients csatlakozhatnak-e TLS-titkosítással vagy egyszerű szöveges redis protokollal.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="2fcaa-121">Az alapértelmezett beállítás a TLS által titkosított.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-121">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="2fcaa-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="2fcaa-122">-ClusteringPolicy</span></span>
<span data-ttu-id="2fcaa-123">Fürtözési házirend – az alapértelmezett érték az OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="2fcaa-124">A létrehozási időpontban van megadva.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-124">Specified at create time.</span></span>

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

### <span data-ttu-id="2fcaa-125">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2fcaa-125">-ClusterName</span></span>
<span data-ttu-id="2fcaa-126">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-126">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="2fcaa-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fcaa-127">-DefaultProfile</span></span>
<span data-ttu-id="2fcaa-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fcaa-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="2fcaa-129">-EvictionPolicy</span></span>
<span data-ttu-id="2fcaa-130">Redis kiviction policy - default is VolatileLRU.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-130">Redis eviction policy - default is VolatileLRU.</span></span>

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

### <span data-ttu-id="2fcaa-131">-Location</span><span class="sxs-lookup"><span data-stu-id="2fcaa-131">-Location</span></span>
<span data-ttu-id="2fcaa-132">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="2fcaa-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="2fcaa-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="2fcaa-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="2fcaa-134">A támogatott fürt minimális TLS-verziója, például 1.2</span><span class="sxs-lookup"><span data-stu-id="2fcaa-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

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

### <span data-ttu-id="2fcaa-135">-Module</span><span class="sxs-lookup"><span data-stu-id="2fcaa-135">-Module</span></span>
<span data-ttu-id="2fcaa-136">Az adatbázisban engedélyezhető redis modulok opcionális készlete – a modulok csak létrehozási időben hozzáadhatóak.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="2fcaa-137">A MODUL tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="2fcaa-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2fcaa-138">-NoWait</span></span>
<span data-ttu-id="2fcaa-139">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="2fcaa-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2fcaa-140">-Port</span><span class="sxs-lookup"><span data-stu-id="2fcaa-140">-Port</span></span>
<span data-ttu-id="2fcaa-141">Az adatbázis végpontjának TCP-portja.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="2fcaa-142">A létrehozási időpontban van megadva.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-142">Specified at create time.</span></span>
<span data-ttu-id="2fcaa-143">Alapértelmezés szerint egy elérhető port van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-143">Defaults to an available port.</span></span>

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

### <span data-ttu-id="2fcaa-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fcaa-144">-ResourceGroupName</span></span>
<span data-ttu-id="2fcaa-145">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-145">The name of the resource group.</span></span>

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

### <span data-ttu-id="2fcaa-146">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="2fcaa-146">-Sku</span></span>
<span data-ttu-id="2fcaa-147">A telepíthető RedisEnterprise-fürt típusa.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="2fcaa-148">Lehetséges értékek: (Enterprise_E10, EnterpriseFlash_F300 stb.)</span><span class="sxs-lookup"><span data-stu-id="2fcaa-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

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

### <span data-ttu-id="2fcaa-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2fcaa-149">-SubscriptionId</span></span>
<span data-ttu-id="2fcaa-150">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2fcaa-151">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-151">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2fcaa-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="2fcaa-152">-Tag</span></span>
<span data-ttu-id="2fcaa-153">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-153">Resource tags.</span></span>

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

### <span data-ttu-id="2fcaa-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="2fcaa-154">-Zone</span></span>
<span data-ttu-id="2fcaa-155">A fürt üzembe helyezésének zónái.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-155">The zones where this cluster will be deployed.</span></span>

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

### <span data-ttu-id="2fcaa-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fcaa-156">-Confirm</span></span>
<span data-ttu-id="2fcaa-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fcaa-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fcaa-158">-WhatIf</span></span>
<span data-ttu-id="2fcaa-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fcaa-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fcaa-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fcaa-161">CommonParameters</span></span>
<span data-ttu-id="2fcaa-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fcaa-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fcaa-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fcaa-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2fcaa-164">INPUTS</span></span>

## <span data-ttu-id="2fcaa-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fcaa-165">OUTPUTS</span></span>

### <span data-ttu-id="2fcaa-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="2fcaa-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="2fcaa-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2fcaa-167">NOTES</span></span>

<span data-ttu-id="2fcaa-168">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2fcaa-168">ALIASES</span></span>

<span data-ttu-id="2fcaa-169">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2fcaa-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2fcaa-170">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2fcaa-171">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2fcaa-172">MODULE <IModule[]>: Az adatbázisban engedélyezhető redismodulok opcionális készlete – a modulok csak létrehozási időben hozzáadhatóak.</span><span class="sxs-lookup"><span data-stu-id="2fcaa-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="2fcaa-173">`Name <String>`: A modul neve, például "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="2fcaa-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="2fcaa-174">`[Arg <String>]`: A modul konfigurációs beállításai, például "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="2fcaa-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="2fcaa-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fcaa-175">RELATED LINKS</span></span>

