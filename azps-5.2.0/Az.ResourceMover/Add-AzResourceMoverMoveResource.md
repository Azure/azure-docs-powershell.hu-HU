---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358790"
---
# <span data-ttu-id="2740b-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="2740b-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="2740b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2740b-102">SYNOPSIS</span></span>
<span data-ttu-id="2740b-103">Létrehozza vagy frissíti az áthelyezési erőforrást az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="2740b-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="2740b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2740b-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2740b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2740b-105">DESCRIPTION</span></span>
<span data-ttu-id="2740b-106">Létrehozza vagy frissíti az áthelyezési erőforrást az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="2740b-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="2740b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2740b-107">EXAMPLES</span></span>

### <span data-ttu-id="2740b-108">1. példa: Erőforrás hozzáadása az áthelyezési gyűjteményhez.</span><span class="sxs-lookup"><span data-stu-id="2740b-108">Example 1: Adding a resource to the move collection.</span></span>
```powershell
PS C:\> Add-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM" -SourceId "/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM" -Name PSDemoVM -ResourceSettingResourceType "Microsoft.Compute/virtualMachines" -ResourceSettingTargetResourceName PSDemoVM

Output:

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migr
                                          ate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          : DependencyComputationPending
MoveStatusDetail                        : {}
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       : The dependency computation is not completed for resource - /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resou
                                          rceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM.
                                              Possible Causes: Dependency computation is pending for resource.
                                              Recommended Action: Validate dependencies to compute the dependencies.

MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachi
                                          nes/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type          

```

<span data-ttu-id="2740b-109">Erőforrás hozzáadása az áthelyezési gyűjteményhez a megadott előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="2740b-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="2740b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2740b-110">PARAMETERS</span></span>

### <span data-ttu-id="2740b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2740b-111">-AsJob</span></span>
<span data-ttu-id="2740b-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="2740b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="2740b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2740b-113">-DefaultProfile</span></span>
<span data-ttu-id="2740b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2740b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2740b-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="2740b-115">-DependsOnOverride</span></span>
<span data-ttu-id="2740b-116">Beállítja vagy felülbírálja az áthelyezési erőforrás-függőségeket.</span><span class="sxs-lookup"><span data-stu-id="2740b-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="2740b-117">Ennek létrehozásáról a DEPENDSONOVERRIDE tulajdonságokat és egy kivonattáblát hoz létre a NOTES (JEGYZETEK) szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="2740b-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResourceDependencyOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2740b-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="2740b-118">-ExistingTargetId</span></span>
<span data-ttu-id="2740b-119">Beállítja vagy beállítja ARM erőforrás azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="2740b-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="2740b-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="2740b-120">-MoveCollectionName</span></span>
<span data-ttu-id="2740b-121">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="2740b-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="2740b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2740b-122">-Name</span></span>
<span data-ttu-id="2740b-123">Az Erőforrás neve áthelyezése</span><span class="sxs-lookup"><span data-stu-id="2740b-123">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2740b-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2740b-124">-NoWait</span></span>
<span data-ttu-id="2740b-125">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="2740b-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2740b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2740b-126">-ResourceGroupName</span></span>
<span data-ttu-id="2740b-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2740b-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="2740b-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="2740b-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="2740b-129">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="2740b-129">The resource type.</span></span>
<span data-ttu-id="2740b-130">Az érték lehet például Microsoft.Compute/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="2740b-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="2740b-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="2740b-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="2740b-132">Beállítja vagy beállítja a célerőforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="2740b-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="2740b-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="2740b-133">-SourceId</span></span>
<span data-ttu-id="2740b-134">Beállítja vagy beállítja az ARM forrásazonosítóját.</span><span class="sxs-lookup"><span data-stu-id="2740b-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="2740b-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="2740b-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="2740b-136">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="2740b-136">The resource type.</span></span>
<span data-ttu-id="2740b-137">Az érték lehet például Microsoft.Compute/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="2740b-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="2740b-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="2740b-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="2740b-139">Beállítja vagy beállítja a célerőforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="2740b-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="2740b-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2740b-140">-SubscriptionId</span></span>
<span data-ttu-id="2740b-141">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2740b-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="2740b-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2740b-142">-Confirm</span></span>
<span data-ttu-id="2740b-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2740b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2740b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2740b-144">-WhatIf</span></span>
<span data-ttu-id="2740b-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2740b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2740b-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2740b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2740b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2740b-147">CommonParameters</span></span>
<span data-ttu-id="2740b-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2740b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2740b-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2740b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2740b-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2740b-150">INPUTS</span></span>

## <span data-ttu-id="2740b-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2740b-151">OUTPUTS</span></span>

### <span data-ttu-id="2740b-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span><span class="sxs-lookup"><span data-stu-id="2740b-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="2740b-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2740b-153">NOTES</span></span>

<span data-ttu-id="2740b-154">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2740b-154">ALIASES</span></span>

<span data-ttu-id="2740b-155">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2740b-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2740b-156">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2740b-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2740b-157">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2740b-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2740b-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Beállítja vagy beállítja az áthelyezési erőforrás-függőségek felülbírálásokat.</span><span class="sxs-lookup"><span data-stu-id="2740b-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="2740b-159">`[Id <String>]`: Beállítja vagy beállítja ARM függő erőforrás azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="2740b-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="2740b-160">`[TargetId <String>]`: Beállítja vagy beállítja ARM MoveResource vagy a függő erőforrás ARM azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="2740b-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="2740b-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2740b-161">RELATED LINKS</span></span>

