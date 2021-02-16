---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 92d6855753bdf56941d6f6ca85ec021228894a2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161523"
---
# <span data-ttu-id="f8efa-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f8efa-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="f8efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8efa-102">SYNOPSIS</span></span>
<span data-ttu-id="f8efa-103">Egy Kusto-fürt egyszerű hozzárendelésének törlése.</span><span class="sxs-lookup"><span data-stu-id="f8efa-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="f8efa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f8efa-104">SYNTAX</span></span>

### <span data-ttu-id="f8efa-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8efa-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f8efa-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f8efa-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8efa-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f8efa-107">DESCRIPTION</span></span>
<span data-ttu-id="f8efa-108">Egy Kusto-fürt egyszerű hozzárendelésének törlése.</span><span class="sxs-lookup"><span data-stu-id="f8efa-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="f8efa-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f8efa-109">EXAMPLES</span></span>

### <span data-ttu-id="f8efa-110">1. példa: Meglévő Kusto-fürt – PrincipalAssignment törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="f8efa-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="f8efa-111">A fenti parancs törli a Kusto-fürt "testnewkustocluster" kustoprincipal1 nevű PrincipalAssignment rekordját.</span><span class="sxs-lookup"><span data-stu-id="f8efa-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="f8efa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8efa-112">PARAMETERS</span></span>

### <span data-ttu-id="f8efa-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8efa-113">-AsJob</span></span>
<span data-ttu-id="f8efa-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="f8efa-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f8efa-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f8efa-115">-ClusterName</span></span>
<span data-ttu-id="f8efa-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f8efa-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8efa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8efa-117">-DefaultProfile</span></span>
<span data-ttu-id="f8efa-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8efa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8efa-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8efa-119">-InputObject</span></span>
<span data-ttu-id="f8efa-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f8efa-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f8efa-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f8efa-121">-NoWait</span></span>
<span data-ttu-id="f8efa-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="f8efa-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f8efa-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8efa-123">-PassThru</span></span>
<span data-ttu-id="f8efa-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="f8efa-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f8efa-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f8efa-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="f8efa-126">A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="f8efa-126">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="f8efa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8efa-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8efa-128">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f8efa-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8efa-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8efa-129">-SubscriptionId</span></span>
<span data-ttu-id="f8efa-130">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f8efa-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f8efa-131">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f8efa-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f8efa-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8efa-132">-Confirm</span></span>
<span data-ttu-id="f8efa-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f8efa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8efa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8efa-134">-WhatIf</span></span>
<span data-ttu-id="f8efa-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f8efa-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8efa-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8efa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8efa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8efa-137">CommonParameters</span></span>
<span data-ttu-id="f8efa-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8efa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8efa-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8efa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8efa-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8efa-140">INPUTS</span></span>

### <span data-ttu-id="f8efa-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f8efa-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f8efa-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8efa-142">OUTPUTS</span></span>

### <span data-ttu-id="f8efa-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f8efa-143">System.Boolean</span></span>

## <span data-ttu-id="f8efa-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f8efa-144">NOTES</span></span>

<span data-ttu-id="f8efa-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f8efa-145">ALIASES</span></span>

<span data-ttu-id="f8efa-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f8efa-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8efa-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f8efa-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8efa-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f8efa-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8efa-149">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f8efa-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8efa-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="f8efa-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f8efa-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f8efa-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f8efa-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="f8efa-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f8efa-153">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f8efa-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f8efa-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f8efa-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8efa-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="f8efa-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f8efa-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="f8efa-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f8efa-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f8efa-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f8efa-158">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f8efa-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f8efa-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f8efa-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f8efa-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8efa-160">RELATED LINKS</span></span>

