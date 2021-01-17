---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369373"
---
# <span data-ttu-id="f2bae-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="f2bae-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="f2bae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2bae-102">SYNOPSIS</span></span>
<span data-ttu-id="f2bae-103">Törli a megadott nevű adatkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="f2bae-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="f2bae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2bae-104">SYNTAX</span></span>

### <span data-ttu-id="f2bae-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2bae-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f2bae-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2bae-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2bae-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2bae-107">DESCRIPTION</span></span>
<span data-ttu-id="f2bae-108">Törli a megadott nevű adatkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="f2bae-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="f2bae-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2bae-109">EXAMPLES</span></span>

### <span data-ttu-id="f2bae-110">1. példa: Meglévő adatkapcsolat törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="f2bae-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="f2bae-111">A fenti parancs törli a "mykustodataconnection" nevű adatkapcsolatot a meglévő "testnewkustocluster" "testnewkustocluster" nevű, a "testrg" erőforráscsoportban található "mykustodatabase" adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="f2bae-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="f2bae-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2bae-112">PARAMETERS</span></span>

### <span data-ttu-id="f2bae-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2bae-113">-AsJob</span></span>
<span data-ttu-id="f2bae-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="f2bae-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f2bae-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f2bae-115">-ClusterName</span></span>
<span data-ttu-id="f2bae-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f2bae-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f2bae-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f2bae-117">-DatabaseName</span></span>
<span data-ttu-id="f2bae-118">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f2bae-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f2bae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2bae-119">-DefaultProfile</span></span>
<span data-ttu-id="f2bae-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2bae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2bae-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2bae-121">-InputObject</span></span>
<span data-ttu-id="f2bae-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f2bae-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f2bae-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f2bae-123">-Name</span></span>
<span data-ttu-id="f2bae-124">Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="f2bae-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2bae-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f2bae-125">-NoWait</span></span>
<span data-ttu-id="f2bae-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="f2bae-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f2bae-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2bae-127">-PassThru</span></span>
<span data-ttu-id="f2bae-128">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="f2bae-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f2bae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2bae-129">-ResourceGroupName</span></span>
<span data-ttu-id="f2bae-130">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2bae-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f2bae-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2bae-131">-SubscriptionId</span></span>
<span data-ttu-id="f2bae-132">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f2bae-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f2bae-133">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f2bae-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f2bae-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2bae-134">-Confirm</span></span>
<span data-ttu-id="f2bae-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f2bae-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2bae-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2bae-136">-WhatIf</span></span>
<span data-ttu-id="f2bae-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f2bae-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2bae-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f2bae-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2bae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2bae-139">CommonParameters</span></span>
<span data-ttu-id="f2bae-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2bae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2bae-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2bae-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2bae-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2bae-142">INPUTS</span></span>

### <span data-ttu-id="f2bae-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f2bae-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f2bae-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2bae-144">OUTPUTS</span></span>

### <span data-ttu-id="f2bae-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2bae-145">System.Boolean</span></span>

## <span data-ttu-id="f2bae-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2bae-146">NOTES</span></span>

<span data-ttu-id="f2bae-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f2bae-147">ALIASES</span></span>

<span data-ttu-id="f2bae-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f2bae-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2bae-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f2bae-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2bae-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2bae-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2bae-151">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f2bae-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2bae-152">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="f2bae-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f2bae-153">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f2bae-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f2bae-154">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="f2bae-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f2bae-155">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f2bae-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f2bae-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f2bae-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2bae-157">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="f2bae-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f2bae-158">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="f2bae-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f2bae-159">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2bae-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f2bae-160">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f2bae-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f2bae-161">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f2bae-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f2bae-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2bae-162">RELATED LINKS</span></span>

