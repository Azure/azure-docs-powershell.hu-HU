---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: b2dd7c125fbf2529e7dc214efdc9ef5fdef1ace0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001254"
---
# <span data-ttu-id="25ce6-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="25ce6-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="25ce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="25ce6-103">Egy Kusto-fürt egyszerű hozzárendelésének törlése.</span><span class="sxs-lookup"><span data-stu-id="25ce6-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="25ce6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25ce6-104">SYNTAX</span></span>

### <span data-ttu-id="25ce6-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25ce6-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25ce6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25ce6-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25ce6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25ce6-107">DESCRIPTION</span></span>
<span data-ttu-id="25ce6-108">Egy Kusto-fürt egyszerű hozzárendelésének törlése.</span><span class="sxs-lookup"><span data-stu-id="25ce6-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="25ce6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25ce6-109">EXAMPLES</span></span>

### <span data-ttu-id="25ce6-110">1. példa: Meglévő Kusto-fürt – PrincipalAssignment törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="25ce6-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="25ce6-111">A fenti parancs törli a Kusto-fürt "testnewkustocluster" kustoprincipal1 nevű PrincipalAssignment rekordját.</span><span class="sxs-lookup"><span data-stu-id="25ce6-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="25ce6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25ce6-112">PARAMETERS</span></span>

### <span data-ttu-id="25ce6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25ce6-113">-AsJob</span></span>
<span data-ttu-id="25ce6-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="25ce6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="25ce6-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="25ce6-115">-ClusterName</span></span>
<span data-ttu-id="25ce6-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="25ce6-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="25ce6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ce6-117">-DefaultProfile</span></span>
<span data-ttu-id="25ce6-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25ce6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25ce6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25ce6-119">-InputObject</span></span>
<span data-ttu-id="25ce6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="25ce6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25ce6-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="25ce6-121">-NoWait</span></span>
<span data-ttu-id="25ce6-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="25ce6-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="25ce6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25ce6-123">-PassThru</span></span>
<span data-ttu-id="25ce6-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="25ce6-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="25ce6-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="25ce6-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="25ce6-126">A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="25ce6-126">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="25ce6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25ce6-127">-ResourceGroupName</span></span>
<span data-ttu-id="25ce6-128">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="25ce6-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="25ce6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25ce6-129">-SubscriptionId</span></span>
<span data-ttu-id="25ce6-130">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="25ce6-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="25ce6-131">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="25ce6-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="25ce6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25ce6-132">-Confirm</span></span>
<span data-ttu-id="25ce6-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="25ce6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25ce6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25ce6-134">-WhatIf</span></span>
<span data-ttu-id="25ce6-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="25ce6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25ce6-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25ce6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25ce6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ce6-137">CommonParameters</span></span>
<span data-ttu-id="25ce6-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25ce6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ce6-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25ce6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ce6-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25ce6-140">INPUTS</span></span>

### <span data-ttu-id="25ce6-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="25ce6-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="25ce6-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25ce6-142">OUTPUTS</span></span>

### <span data-ttu-id="25ce6-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25ce6-143">System.Boolean</span></span>

## <span data-ttu-id="25ce6-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25ce6-144">NOTES</span></span>

<span data-ttu-id="25ce6-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="25ce6-145">ALIASES</span></span>

<span data-ttu-id="25ce6-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="25ce6-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="25ce6-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="25ce6-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25ce6-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="25ce6-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="25ce6-149">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="25ce6-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25ce6-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="25ce6-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="25ce6-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="25ce6-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="25ce6-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="25ce6-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="25ce6-153">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="25ce6-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="25ce6-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="25ce6-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25ce6-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="25ce6-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="25ce6-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="25ce6-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="25ce6-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="25ce6-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="25ce6-158">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="25ce6-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="25ce6-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="25ce6-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="25ce6-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25ce6-160">RELATED LINKS</span></span>

