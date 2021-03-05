---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: 1b16f30b068eb41bf0202c65e95f55f94769ba2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000693"
---
# <span data-ttu-id="94234-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="94234-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="94234-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94234-102">SYNOPSIS</span></span>
<span data-ttu-id="94234-103">Meglévő RedisEnterprise-fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="94234-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="94234-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94234-104">SYNTAX</span></span>

### <span data-ttu-id="94234-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94234-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="94234-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="94234-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94234-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94234-107">DESCRIPTION</span></span>
<span data-ttu-id="94234-108">Meglévő RedisEnterprise-fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="94234-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="94234-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94234-109">EXAMPLES</span></span>

### <span data-ttu-id="94234-110">1. példa: A nagyvállalati gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="94234-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="94234-111">Ez a parancs frissíti a minimális TLS-verziót, és hozzáad egy MyCache nevű címkét a Redis Enterprise Cache-hez.</span><span class="sxs-lookup"><span data-stu-id="94234-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="94234-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94234-112">PARAMETERS</span></span>

### <span data-ttu-id="94234-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94234-113">-AsJob</span></span>
<span data-ttu-id="94234-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="94234-114">Run the command as a job</span></span>

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

### <span data-ttu-id="94234-115">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="94234-115">-Capacity</span></span>
<span data-ttu-id="94234-116">A RedisEnterprise fürt mérete.</span><span class="sxs-lookup"><span data-stu-id="94234-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="94234-117">Az alapérték 2 vagy 3 az adott termékváltozattól függően.</span><span class="sxs-lookup"><span data-stu-id="94234-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="94234-118">A nagyvállalati SKUs-k érvényes értékei (2, 4, 6, ...), a Flash-SK-k pedig (3, 9, 15, ...).</span><span class="sxs-lookup"><span data-stu-id="94234-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="94234-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="94234-119">-ClusterName</span></span>
<span data-ttu-id="94234-120">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="94234-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="94234-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94234-121">-DefaultProfile</span></span>
<span data-ttu-id="94234-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94234-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94234-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94234-123">-InputObject</span></span>
<span data-ttu-id="94234-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="94234-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94234-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="94234-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="94234-126">A támogatott fürt minimális TLS-verziója, például "1.2"</span><span class="sxs-lookup"><span data-stu-id="94234-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="94234-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="94234-127">-NoWait</span></span>
<span data-ttu-id="94234-128">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="94234-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="94234-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94234-129">-ResourceGroupName</span></span>
<span data-ttu-id="94234-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="94234-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="94234-131">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="94234-131">-Sku</span></span>
<span data-ttu-id="94234-132">A telepíthető RedisEnterprise-fürt típusa.</span><span class="sxs-lookup"><span data-stu-id="94234-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="94234-133">Lehetséges értékek: (Enterprise_E10, EnterpriseFlash_F300 stb.)</span><span class="sxs-lookup"><span data-stu-id="94234-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94234-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94234-134">-SubscriptionId</span></span>
<span data-ttu-id="94234-135">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="94234-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="94234-136">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="94234-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="94234-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="94234-137">-Tag</span></span>
<span data-ttu-id="94234-138">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="94234-138">Resource tags.</span></span>

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

### <span data-ttu-id="94234-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94234-139">-Confirm</span></span>
<span data-ttu-id="94234-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="94234-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94234-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94234-141">-WhatIf</span></span>
<span data-ttu-id="94234-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="94234-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94234-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94234-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94234-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94234-144">CommonParameters</span></span>
<span data-ttu-id="94234-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94234-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94234-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94234-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94234-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94234-147">INPUTS</span></span>

### <span data-ttu-id="94234-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="94234-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="94234-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94234-149">OUTPUTS</span></span>

### <span data-ttu-id="94234-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="94234-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="94234-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94234-151">NOTES</span></span>

<span data-ttu-id="94234-152">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="94234-152">ALIASES</span></span>

<span data-ttu-id="94234-153">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="94234-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94234-154">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="94234-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94234-155">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="94234-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94234-156">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="94234-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94234-157">`[ClusterName <String>]`: A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="94234-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="94234-158">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="94234-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="94234-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="94234-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94234-160">`[Location <String>]`: A művelet régiójában.</span><span class="sxs-lookup"><span data-stu-id="94234-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="94234-161">`[OperationId <String>]`: A művelet egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="94234-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="94234-162">`[PrivateEndpointConnectionName <String>]`: Az Azure-erőforráshoz társított privát végpontkapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="94234-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="94234-163">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="94234-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="94234-164">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="94234-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="94234-165">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="94234-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="94234-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94234-166">RELATED LINKS</span></span>

