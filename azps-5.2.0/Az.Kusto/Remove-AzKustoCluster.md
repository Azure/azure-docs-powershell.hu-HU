---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: e9bdea3820b8b8121e0e250c99283c0ca656ca61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333977"
---
# <span data-ttu-id="043a5-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="043a5-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="043a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="043a5-102">SYNOPSIS</span></span>
<span data-ttu-id="043a5-103">Egy Kusto-fürt törlése.</span><span class="sxs-lookup"><span data-stu-id="043a5-103">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="043a5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="043a5-104">SYNTAX</span></span>

### <span data-ttu-id="043a5-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="043a5-105">Delete (Default)</span></span>
```
Remove-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="043a5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="043a5-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="043a5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="043a5-107">DESCRIPTION</span></span>
<span data-ttu-id="043a5-108">Egy Kusto-fürt törlése.</span><span class="sxs-lookup"><span data-stu-id="043a5-108">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="043a5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="043a5-109">EXAMPLES</span></span>

### <span data-ttu-id="043a5-110">1. példa: Meglévő Kusto-fürt törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="043a5-110">Example 1: Delete an existing Kusto cluster by name</span></span>
```powershell
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="043a5-111">A fenti parancs törli a "testrg" erőforráscsoportban a "testnewkustocluster" nevű Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="043a5-111">The above command deletes the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="043a5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="043a5-112">PARAMETERS</span></span>

### <span data-ttu-id="043a5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="043a5-113">-AsJob</span></span>
<span data-ttu-id="043a5-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="043a5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="043a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="043a5-115">-DefaultProfile</span></span>
<span data-ttu-id="043a5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="043a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="043a5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="043a5-117">-InputObject</span></span>
<span data-ttu-id="043a5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="043a5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="043a5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="043a5-119">-Name</span></span>
<span data-ttu-id="043a5-120">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="043a5-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043a5-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="043a5-121">-NoWait</span></span>
<span data-ttu-id="043a5-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="043a5-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="043a5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="043a5-123">-PassThru</span></span>
<span data-ttu-id="043a5-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="043a5-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="043a5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="043a5-125">-ResourceGroupName</span></span>
<span data-ttu-id="043a5-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="043a5-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="043a5-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="043a5-127">-SubscriptionId</span></span>
<span data-ttu-id="043a5-128">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="043a5-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="043a5-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="043a5-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="043a5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="043a5-130">-Confirm</span></span>
<span data-ttu-id="043a5-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="043a5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="043a5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="043a5-132">-WhatIf</span></span>
<span data-ttu-id="043a5-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="043a5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="043a5-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="043a5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="043a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043a5-135">CommonParameters</span></span>
<span data-ttu-id="043a5-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="043a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043a5-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="043a5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043a5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="043a5-138">INPUTS</span></span>

### <span data-ttu-id="043a5-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="043a5-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="043a5-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="043a5-140">OUTPUTS</span></span>

### <span data-ttu-id="043a5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="043a5-141">System.Boolean</span></span>

## <span data-ttu-id="043a5-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="043a5-142">NOTES</span></span>

<span data-ttu-id="043a5-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="043a5-143">ALIASES</span></span>

<span data-ttu-id="043a5-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="043a5-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="043a5-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="043a5-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="043a5-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="043a5-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="043a5-147">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="043a5-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="043a5-148">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="043a5-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="043a5-149">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="043a5-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="043a5-150">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="043a5-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="043a5-151">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="043a5-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="043a5-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="043a5-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="043a5-153">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="043a5-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="043a5-154">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="043a5-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="043a5-155">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="043a5-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="043a5-156">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="043a5-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="043a5-157">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="043a5-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="043a5-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="043a5-158">RELATED LINKS</span></span>

