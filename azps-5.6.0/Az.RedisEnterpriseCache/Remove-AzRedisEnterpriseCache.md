---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: d6b030cfbc6233d917d252f2d271eb7d4bfe65bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000741"
---
# <span data-ttu-id="3e259-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="3e259-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="3e259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e259-102">SYNOPSIS</span></span>
<span data-ttu-id="3e259-103">Törli a RedisEnterprise gyorsítótár-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="3e259-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="3e259-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e259-104">SYNTAX</span></span>

### <span data-ttu-id="3e259-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e259-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3e259-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3e259-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3e259-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e259-107">DESCRIPTION</span></span>
<span data-ttu-id="3e259-108">Törli a RedisEnterprise gyorsítótár-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="3e259-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="3e259-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e259-109">EXAMPLES</span></span>

### <span data-ttu-id="3e259-110">1. példa: A redis enterprise cache eltávolítása és az eredmény visszaadése</span><span class="sxs-lookup"><span data-stu-id="3e259-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="3e259-111">Ez a parancs eltávolítja a Redis Enterprise cache-t, és megjeleníti, hogy a művelet sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="3e259-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="3e259-112">2. példa: A nagyvállalati gyorsítótár eltávolítása, és az eredmény nem jelenik meg</span><span class="sxs-lookup"><span data-stu-id="3e259-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="3e259-113">Ez a parancs eltávolítja a Redis Enterprise cache-t.</span><span class="sxs-lookup"><span data-stu-id="3e259-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="3e259-114">Mivel a PassThru paraméter nincs megadva, a művelet eredménye nem jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="3e259-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="3e259-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e259-115">PARAMETERS</span></span>

### <span data-ttu-id="3e259-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e259-116">-AsJob</span></span>
<span data-ttu-id="3e259-117">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="3e259-117">Run the command as a job</span></span>

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

### <span data-ttu-id="3e259-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3e259-118">-ClusterName</span></span>
<span data-ttu-id="3e259-119">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="3e259-119">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="3e259-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e259-120">-DefaultProfile</span></span>
<span data-ttu-id="3e259-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e259-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e259-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e259-122">-InputObject</span></span>
<span data-ttu-id="3e259-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3e259-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3e259-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3e259-124">-NoWait</span></span>
<span data-ttu-id="3e259-125">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="3e259-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3e259-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e259-126">-PassThru</span></span>
<span data-ttu-id="3e259-127">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="3e259-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3e259-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e259-128">-ResourceGroupName</span></span>
<span data-ttu-id="3e259-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e259-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="3e259-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e259-130">-SubscriptionId</span></span>
<span data-ttu-id="3e259-131">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3e259-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e259-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3e259-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3e259-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e259-133">-Confirm</span></span>
<span data-ttu-id="3e259-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3e259-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e259-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e259-135">-WhatIf</span></span>
<span data-ttu-id="3e259-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3e259-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e259-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e259-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e259-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e259-138">CommonParameters</span></span>
<span data-ttu-id="3e259-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e259-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e259-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e259-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e259-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e259-141">INPUTS</span></span>

### <span data-ttu-id="3e259-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="3e259-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="3e259-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e259-143">OUTPUTS</span></span>

### <span data-ttu-id="3e259-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e259-144">System.Boolean</span></span>

## <span data-ttu-id="3e259-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e259-145">NOTES</span></span>

<span data-ttu-id="3e259-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3e259-146">ALIASES</span></span>

<span data-ttu-id="3e259-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="3e259-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3e259-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="3e259-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e259-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e259-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3e259-150">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="3e259-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3e259-151">`[ClusterName <String>]`: A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="3e259-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="3e259-152">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3e259-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3e259-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3e259-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e259-154">`[Location <String>]`: A művelet régiójában.</span><span class="sxs-lookup"><span data-stu-id="3e259-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="3e259-155">`[OperationId <String>]`: A művelet egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3e259-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="3e259-156">`[PrivateEndpointConnectionName <String>]`: Az Azure-erőforráshoz társított privát végpontkapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="3e259-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="3e259-157">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e259-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3e259-158">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3e259-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="3e259-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3e259-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3e259-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e259-160">RELATED LINKS</span></span>

