---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: 22d0fed7c72aa5754b7393cdf06fb58a4bfc0db3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378180"
---
# <span data-ttu-id="d5389-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="d5389-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="d5389-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5389-102">SYNOPSIS</span></span>
<span data-ttu-id="d5389-103">Törli a RedisEnterprise gyorsítótár-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="d5389-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="d5389-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d5389-104">SYNTAX</span></span>

### <span data-ttu-id="d5389-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5389-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d5389-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d5389-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5389-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d5389-107">DESCRIPTION</span></span>
<span data-ttu-id="d5389-108">Törli a RedisEnterprise gyorsítótár-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="d5389-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="d5389-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d5389-109">EXAMPLES</span></span>

### <span data-ttu-id="d5389-110">1. példa: A redis enterprise cache eltávolítása és az eredmény visszaadése</span><span class="sxs-lookup"><span data-stu-id="d5389-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="d5389-111">Ez a parancs eltávolítja a Redis Enterprise cache-t, és megjeleníti, hogy a művelet sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="d5389-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="d5389-112">2. példa: A nagyvállalati gyorsítótár eltávolítása, és az eredmény nem jelenik meg</span><span class="sxs-lookup"><span data-stu-id="d5389-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="d5389-113">Ez a parancs eltávolítja a Redis Enterprise cache-t.</span><span class="sxs-lookup"><span data-stu-id="d5389-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="d5389-114">Mivel a PassThru paraméter nincs megadva, a művelet eredménye nem jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="d5389-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="d5389-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5389-115">PARAMETERS</span></span>

### <span data-ttu-id="d5389-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5389-116">-AsJob</span></span>
<span data-ttu-id="d5389-117">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="d5389-117">Run the command as a job</span></span>

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

### <span data-ttu-id="d5389-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d5389-118">-ClusterName</span></span>
<span data-ttu-id="d5389-119">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d5389-119">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5389-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5389-120">-DefaultProfile</span></span>
<span data-ttu-id="d5389-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5389-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5389-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5389-122">-InputObject</span></span>
<span data-ttu-id="d5389-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d5389-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5389-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d5389-124">-NoWait</span></span>
<span data-ttu-id="d5389-125">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="d5389-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d5389-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5389-126">-PassThru</span></span>
<span data-ttu-id="d5389-127">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="d5389-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d5389-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5389-128">-ResourceGroupName</span></span>
<span data-ttu-id="d5389-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d5389-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5389-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5389-130">-SubscriptionId</span></span>
<span data-ttu-id="d5389-131">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d5389-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d5389-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d5389-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5389-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5389-133">-Confirm</span></span>
<span data-ttu-id="d5389-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d5389-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5389-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5389-135">-WhatIf</span></span>
<span data-ttu-id="d5389-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d5389-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5389-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d5389-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5389-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5389-138">CommonParameters</span></span>
<span data-ttu-id="d5389-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5389-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5389-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5389-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5389-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5389-141">INPUTS</span></span>

### <span data-ttu-id="d5389-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="d5389-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="d5389-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5389-143">OUTPUTS</span></span>

### <span data-ttu-id="d5389-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d5389-144">System.Boolean</span></span>

## <span data-ttu-id="d5389-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d5389-145">NOTES</span></span>

<span data-ttu-id="d5389-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d5389-146">ALIASES</span></span>

<span data-ttu-id="d5389-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d5389-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5389-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d5389-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5389-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d5389-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5389-150">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d5389-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5389-151">`[ClusterName <String>]`: A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d5389-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="d5389-152">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d5389-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d5389-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d5389-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5389-154">`[Location <String>]`: A művelet régiójában.</span><span class="sxs-lookup"><span data-stu-id="d5389-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="d5389-155">`[OperationId <String>]`: A művelet egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d5389-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="d5389-156">`[PrivateEndpointConnectionName <String>]`: Az Azure-erőforráshoz társított privát végpontkapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="d5389-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="d5389-157">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d5389-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d5389-158">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d5389-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d5389-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d5389-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d5389-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5389-160">RELATED LINKS</span></span>

