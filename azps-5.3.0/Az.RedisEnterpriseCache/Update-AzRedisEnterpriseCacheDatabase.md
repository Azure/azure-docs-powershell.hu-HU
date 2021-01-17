---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378152"
---
# <span data-ttu-id="7adc9-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="7adc9-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="7adc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7adc9-102">SYNOPSIS</span></span>
<span data-ttu-id="7adc9-103">Adatbázis frissítése</span><span class="sxs-lookup"><span data-stu-id="7adc9-103">Updates a database</span></span>

## <span data-ttu-id="7adc9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7adc9-104">SYNTAX</span></span>

### <span data-ttu-id="7adc9-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7adc9-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7adc9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7adc9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7adc9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7adc9-107">DESCRIPTION</span></span>
<span data-ttu-id="7adc9-108">Adatbázis frissítése</span><span class="sxs-lookup"><span data-stu-id="7adc9-108">Updates a database</span></span>

## <span data-ttu-id="7adc9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7adc9-109">EXAMPLES</span></span>

### <span data-ttu-id="7adc9-110">1. példa: Ügyfél protokoll frissítése</span><span class="sxs-lookup"><span data-stu-id="7adc9-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="7adc9-111">Ez a parancs frissíti a MyCache nevű Redis Enterprise Cache adatbázis ügyfél protokollját.</span><span class="sxs-lookup"><span data-stu-id="7adc9-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="7adc9-112">2. példa: Ügyfél protokoll- és kiviction-házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="7adc9-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="7adc9-113">Ez a parancs frissíti a MyCache nevű Redis Enterprise Cache adatbázis ügyfél protokoll- és kiviction házirendját.</span><span class="sxs-lookup"><span data-stu-id="7adc9-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="7adc9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7adc9-114">PARAMETERS</span></span>

### <span data-ttu-id="7adc9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7adc9-115">-AsJob</span></span>
<span data-ttu-id="7adc9-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="7adc9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7adc9-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="7adc9-117">-ClientProtocol</span></span>
<span data-ttu-id="7adc9-118">Azt adja meg, hogy a redis clients csatlakozhatnak-e TLS-titkosítással vagy egyszerű szöveges redis protokollal.</span><span class="sxs-lookup"><span data-stu-id="7adc9-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="7adc9-119">Az alapértelmezett beállítás a TLS által titkosított.</span><span class="sxs-lookup"><span data-stu-id="7adc9-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="7adc9-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="7adc9-120">-ClusteringPolicy</span></span>
<span data-ttu-id="7adc9-121">Fürtözési házirend – az alapértelmezett érték az OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="7adc9-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="7adc9-122">A létrehozási időpontban van megadva.</span><span class="sxs-lookup"><span data-stu-id="7adc9-122">Specified at create time.</span></span>

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

### <span data-ttu-id="7adc9-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7adc9-123">-ClusterName</span></span>
<span data-ttu-id="7adc9-124">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="7adc9-124">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7adc9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7adc9-125">-DefaultProfile</span></span>
<span data-ttu-id="7adc9-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7adc9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7adc9-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="7adc9-127">-EvictionPolicy</span></span>
<span data-ttu-id="7adc9-128">Redis eviction policy - default is VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="7adc9-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="7adc9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7adc9-129">-InputObject</span></span>
<span data-ttu-id="7adc9-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7adc9-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7adc9-131">-Module</span><span class="sxs-lookup"><span data-stu-id="7adc9-131">-Module</span></span>
<span data-ttu-id="7adc9-132">Az adatbázisban engedélyezhető redis modulok opcionális készlete – a modulok csak létrehozási időben hozzáadhatóak.</span><span class="sxs-lookup"><span data-stu-id="7adc9-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="7adc9-133">A MODUL tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="7adc9-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="7adc9-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7adc9-134">-NoWait</span></span>
<span data-ttu-id="7adc9-135">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="7adc9-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7adc9-136">-Port</span><span class="sxs-lookup"><span data-stu-id="7adc9-136">-Port</span></span>
<span data-ttu-id="7adc9-137">Az adatbázis végpontjának TCP-portja.</span><span class="sxs-lookup"><span data-stu-id="7adc9-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="7adc9-138">A létrehozási időpontban van megadva.</span><span class="sxs-lookup"><span data-stu-id="7adc9-138">Specified at create time.</span></span>
<span data-ttu-id="7adc9-139">Alapértelmezés szerint egy elérhető port van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="7adc9-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="7adc9-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7adc9-140">-ResourceGroupName</span></span>
<span data-ttu-id="7adc9-141">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7adc9-141">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7adc9-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7adc9-142">-SubscriptionId</span></span>
<span data-ttu-id="7adc9-143">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="7adc9-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7adc9-144">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7adc9-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7adc9-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7adc9-145">-Confirm</span></span>
<span data-ttu-id="7adc9-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7adc9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7adc9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7adc9-147">-WhatIf</span></span>
<span data-ttu-id="7adc9-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7adc9-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7adc9-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7adc9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7adc9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adc9-150">CommonParameters</span></span>
<span data-ttu-id="7adc9-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7adc9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adc9-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7adc9-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adc9-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7adc9-153">INPUTS</span></span>

### <span data-ttu-id="7adc9-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="7adc9-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="7adc9-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7adc9-155">OUTPUTS</span></span>

### <span data-ttu-id="7adc9-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="7adc9-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="7adc9-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7adc9-157">NOTES</span></span>

<span data-ttu-id="7adc9-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7adc9-158">ALIASES</span></span>

<span data-ttu-id="7adc9-159">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7adc9-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7adc9-160">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7adc9-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7adc9-161">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7adc9-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7adc9-162">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7adc9-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7adc9-163">`[ClusterName <String>]`: A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="7adc9-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="7adc9-164">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7adc9-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7adc9-165">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7adc9-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7adc9-166">`[Location <String>]`: A művelet régiójában.</span><span class="sxs-lookup"><span data-stu-id="7adc9-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="7adc9-167">`[OperationId <String>]`: A művelet egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7adc9-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="7adc9-168">`[PrivateEndpointConnectionName <String>]`: Az Azure-erőforráshoz társított privát végpontkapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="7adc9-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="7adc9-169">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7adc9-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7adc9-170">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="7adc9-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="7adc9-171">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7adc9-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="7adc9-172">MODULE <IModule[]>: Az adatbázisban engedélyezhető redismodulok opcionális készlete – a modulok csak létrehozási időben hozzáadhatóak.</span><span class="sxs-lookup"><span data-stu-id="7adc9-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="7adc9-173">`Name <String>`: A modul neve, például "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="7adc9-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="7adc9-174">`[Arg <String>]`: A modul konfigurációs beállításai, például "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="7adc9-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="7adc9-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7adc9-175">RELATED LINKS</span></span>

