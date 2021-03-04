---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 66a5a844255f5a44000638877abf6a3ed5f908c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922377"
---
# <span data-ttu-id="f8b83-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f8b83-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="f8b83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8b83-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b83-103">Egy Kusto principalAssignment törlése.</span><span class="sxs-lookup"><span data-stu-id="f8b83-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="f8b83-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f8b83-104">SYNTAX</span></span>

### <span data-ttu-id="f8b83-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8b83-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f8b83-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f8b83-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8b83-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f8b83-107">DESCRIPTION</span></span>
<span data-ttu-id="f8b83-108">Egy Kusto principalAssignment törlése.</span><span class="sxs-lookup"><span data-stu-id="f8b83-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="f8b83-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f8b83-109">EXAMPLES</span></span>

### <span data-ttu-id="f8b83-110">1. példa: Meglévő Kusto-adatbázis principalAssignment törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="f8b83-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="f8b83-111">A fenti parancs törli a "kustoprincipal1" nevű PrincipalAssignment rekordot a Kusto-adatbázisban (mykustodatabase).</span><span class="sxs-lookup"><span data-stu-id="f8b83-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="f8b83-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8b83-112">PARAMETERS</span></span>

### <span data-ttu-id="f8b83-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8b83-113">-AsJob</span></span>
<span data-ttu-id="f8b83-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="f8b83-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f8b83-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f8b83-115">-ClusterName</span></span>
<span data-ttu-id="f8b83-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f8b83-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8b83-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8b83-117">-DatabaseName</span></span>
<span data-ttu-id="f8b83-118">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f8b83-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8b83-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b83-119">-DefaultProfile</span></span>
<span data-ttu-id="f8b83-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8b83-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8b83-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8b83-121">-InputObject</span></span>
<span data-ttu-id="f8b83-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f8b83-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f8b83-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f8b83-123">-NoWait</span></span>
<span data-ttu-id="f8b83-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="f8b83-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f8b83-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8b83-125">-PassThru</span></span>
<span data-ttu-id="f8b83-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="f8b83-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f8b83-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f8b83-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="f8b83-128">A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="f8b83-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="f8b83-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8b83-129">-ResourceGroupName</span></span>
<span data-ttu-id="f8b83-130">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f8b83-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8b83-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8b83-131">-SubscriptionId</span></span>
<span data-ttu-id="f8b83-132">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f8b83-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f8b83-133">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f8b83-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f8b83-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8b83-134">-Confirm</span></span>
<span data-ttu-id="f8b83-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f8b83-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8b83-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8b83-136">-WhatIf</span></span>
<span data-ttu-id="f8b83-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f8b83-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8b83-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8b83-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8b83-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b83-139">CommonParameters</span></span>
<span data-ttu-id="f8b83-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b83-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b83-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8b83-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b83-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8b83-142">INPUTS</span></span>

### <span data-ttu-id="f8b83-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f8b83-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f8b83-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8b83-144">OUTPUTS</span></span>

### <span data-ttu-id="f8b83-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f8b83-145">System.Boolean</span></span>

## <span data-ttu-id="f8b83-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f8b83-146">NOTES</span></span>

<span data-ttu-id="f8b83-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f8b83-147">ALIASES</span></span>

<span data-ttu-id="f8b83-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f8b83-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8b83-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f8b83-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8b83-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f8b83-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8b83-151">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f8b83-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8b83-152">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="f8b83-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f8b83-153">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f8b83-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f8b83-154">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="f8b83-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f8b83-155">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f8b83-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f8b83-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f8b83-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8b83-157">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="f8b83-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f8b83-158">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="f8b83-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f8b83-159">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f8b83-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f8b83-160">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f8b83-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f8b83-161">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f8b83-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f8b83-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8b83-162">RELATED LINKS</span></span>

