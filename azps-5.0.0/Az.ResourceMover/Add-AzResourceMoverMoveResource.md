---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188220"
---
# <span data-ttu-id="227f7-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="227f7-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="227f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="227f7-102">SYNOPSIS</span></span>
<span data-ttu-id="227f7-103">Áthelyezési erőforrás létrehozása vagy frissítése az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="227f7-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="227f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="227f7-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="227f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="227f7-105">DESCRIPTION</span></span>
<span data-ttu-id="227f7-106">Áthelyezési erőforrás létrehozása vagy frissítése az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="227f7-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="227f7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="227f7-107">EXAMPLES</span></span>

### <span data-ttu-id="227f7-108">1. példa: erőforrás felvétele az áthelyezési gyűjteménybe</span><span class="sxs-lookup"><span data-stu-id="227f7-108">Example 1: Adding a resource to the move collection.</span></span>
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

<span data-ttu-id="227f7-109">Erőforrás hozzáadása az áthelyezés gyűjteményhez a megadott előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="227f7-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="227f7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="227f7-110">PARAMETERS</span></span>

### <span data-ttu-id="227f7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="227f7-111">-AsJob</span></span>
<span data-ttu-id="227f7-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="227f7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="227f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="227f7-113">-DefaultProfile</span></span>
<span data-ttu-id="227f7-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="227f7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="227f7-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="227f7-115">-DependsOnOverride</span></span>
<span data-ttu-id="227f7-116">Beolvassa vagy beállítja az erőforrás-függőségek felülírását.</span><span class="sxs-lookup"><span data-stu-id="227f7-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="227f7-117">A kivitelezéshez tekintse meg a DEPENDSONOVERRIDE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="227f7-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="227f7-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="227f7-118">-ExistingTargetId</span></span>
<span data-ttu-id="227f7-119">Az erőforrás meglévő célzóna azonosítóját kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="227f7-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="227f7-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="227f7-120">-MoveCollectionName</span></span>
<span data-ttu-id="227f7-121">Az áthelyezés gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="227f7-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="227f7-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="227f7-122">-Name</span></span>
<span data-ttu-id="227f7-123">Az erőforrás nevének áthelyezése</span><span class="sxs-lookup"><span data-stu-id="227f7-123">The Move Resource Name.</span></span>

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

### <span data-ttu-id="227f7-124">-Várva</span><span class="sxs-lookup"><span data-stu-id="227f7-124">-NoWait</span></span>
<span data-ttu-id="227f7-125">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="227f7-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="227f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="227f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="227f7-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="227f7-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="227f7-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="227f7-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="227f7-129">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="227f7-129">The resource type.</span></span>
<span data-ttu-id="227f7-130">Az érték lehet például Microsoft. számítási/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="227f7-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="227f7-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="227f7-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="227f7-132">A cél erőforrás nevének beolvasása vagy megadására szolgáló beállítás.</span><span class="sxs-lookup"><span data-stu-id="227f7-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="227f7-133">-SourceId forrásazonosító</span><span class="sxs-lookup"><span data-stu-id="227f7-133">-SourceId</span></span>
<span data-ttu-id="227f7-134">Beilleszti vagy beállítja az erőforrás forrásául szolgáló azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="227f7-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="227f7-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="227f7-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="227f7-136">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="227f7-136">The resource type.</span></span>
<span data-ttu-id="227f7-137">Az érték lehet például Microsoft. számítási/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="227f7-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="227f7-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="227f7-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="227f7-139">A cél erőforrás nevének beolvasása vagy megadására szolgáló beállítás.</span><span class="sxs-lookup"><span data-stu-id="227f7-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="227f7-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="227f7-140">-SubscriptionId</span></span>
<span data-ttu-id="227f7-141">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="227f7-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="227f7-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="227f7-142">-Confirm</span></span>
<span data-ttu-id="227f7-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="227f7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="227f7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="227f7-144">-WhatIf</span></span>
<span data-ttu-id="227f7-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="227f7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="227f7-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="227f7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="227f7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="227f7-147">CommonParameters</span></span>
<span data-ttu-id="227f7-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="227f7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="227f7-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="227f7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="227f7-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="227f7-150">INPUTS</span></span>

## <span data-ttu-id="227f7-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="227f7-151">OUTPUTS</span></span>

### <span data-ttu-id="227f7-152">Microsoft. Azure. PowerShell. parancsmagok. ResourceMover. modellek. Api20191001Preview. IMoveResource</span><span class="sxs-lookup"><span data-stu-id="227f7-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="227f7-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="227f7-153">NOTES</span></span>

<span data-ttu-id="227f7-154">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="227f7-154">ALIASES</span></span>

<span data-ttu-id="227f7-155">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="227f7-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="227f7-156">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="227f7-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="227f7-157">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="227f7-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="227f7-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride [] >: beilleszti vagy beállítja az erőforrás-függőségek felülírását.</span><span class="sxs-lookup"><span data-stu-id="227f7-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="227f7-159">`[Id <String>]`: Beilleszti vagy beállítja a függő erőforrás ARM AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="227f7-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="227f7-160">`[TargetId <String>]`: A MoveResource vagy a függő erőforrás erőforrás-karja AZONOSÍTÓját adja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="227f7-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="227f7-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="227f7-161">RELATED LINKS</span></span>

