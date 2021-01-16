---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339365"
---
# <span data-ttu-id="6cce8-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="6cce8-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="6cce8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cce8-102">SYNOPSIS</span></span>
<span data-ttu-id="6cce8-103">A kérelem törzsében szereplő erőforrások halmazának véglegesítésére.</span><span class="sxs-lookup"><span data-stu-id="6cce8-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="6cce8-104">A véglegesítési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "CommitFailed" műveletben sikeresen befejeződik, és a moveResource moveState áttűnés lekötöttre vált.</span><span class="sxs-lookup"><span data-stu-id="6cce8-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="6cce8-105">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak ahhoz a művelethez, amely a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="6cce8-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="6cce8-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6cce8-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cce8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6cce8-107">DESCRIPTION</span></span>
<span data-ttu-id="6cce8-108">A kérés törzsében szereplő erőforrások halmazának véglegesítésére.</span><span class="sxs-lookup"><span data-stu-id="6cce8-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="6cce8-109">A véglegesítési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "CommitFailed" műveletben sikeresen befejeződik, és a moveResource moveState áttűnés lekötöttre vált.</span><span class="sxs-lookup"><span data-stu-id="6cce8-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="6cce8-110">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="6cce8-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="6cce8-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6cce8-111">EXAMPLES</span></span>

### <span data-ttu-id="6cce8-112">1. példa: A függő tényezők ellenőrzése az erőforrások véglegesítése előtt</span><span class="sxs-lookup"><span data-stu-id="6cce8-112">Example 1: Validate the dependecies before commit of the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm') -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded

```

<span data-ttu-id="6cce8-113">Az erőforrások véglegesítése előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="6cce8-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="6cce8-114">2. példa: Erőforrások halmazának véglegesítése az Áthelyezési gyűjteményben a "MoveResource Name" bemenettel</span><span class="sxs-lookup"><span data-stu-id="6cce8-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded


```

<span data-ttu-id="6cce8-115">Erőforrások halmazának véglegesítése az Áthelyezési gyűjteményben a "MoveResource Name" bemenettel</span><span class="sxs-lookup"><span data-stu-id="6cce8-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="6cce8-116">3. példa: Erőforrások halmazának véglegesítése az Áthelyezési gyűjteményben a "SourceARMID" bemenettel</span><span class="sxs-lookup"><span data-stu-id="6cce8-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:19:29 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Message        :
Name           : aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:19:28 AM
Status         : Succeeded


```

<span data-ttu-id="6cce8-117">Erőforrások halmazának véglegesítése az Áthelyezési gyűjteményben bemenetként a "SourceARMID" használatával</span><span class="sxs-lookup"><span data-stu-id="6cce8-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="6cce8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cce8-118">PARAMETERS</span></span>

### <span data-ttu-id="6cce8-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cce8-119">-AsJob</span></span>
<span data-ttu-id="6cce8-120">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="6cce8-120">Run the command as a job</span></span>

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

### <span data-ttu-id="6cce8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cce8-121">-DefaultProfile</span></span>
<span data-ttu-id="6cce8-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cce8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cce8-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="6cce8-123">-MoveCollectionName</span></span>
<span data-ttu-id="6cce8-124">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="6cce8-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="6cce8-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="6cce8-125">-MoveResource</span></span>
<span data-ttu-id="6cce8-126">Beállítja vagy beállítja az erőforrás-azonosítók listáját, alapértelmezés szerint elfogadja az erőforrás-azonosítók áthelyezését, hacsak a beviteli típust a MoveResourceInputType tulajdonságon keresztül nem váltja át.</span><span class="sxs-lookup"><span data-stu-id="6cce8-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce8-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="6cce8-127">-MoveResourceInputType</span></span>
<span data-ttu-id="6cce8-128">Az áthelyezési erőforrás beviteli típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6cce8-128">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce8-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6cce8-129">-NoWait</span></span>
<span data-ttu-id="6cce8-130">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="6cce8-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6cce8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cce8-131">-ResourceGroupName</span></span>
<span data-ttu-id="6cce8-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cce8-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="6cce8-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cce8-133">-SubscriptionId</span></span>
<span data-ttu-id="6cce8-134">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cce8-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="6cce8-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="6cce8-135">-ValidateOnly</span></span>
<span data-ttu-id="6cce8-136">Beállítja vagy beállítja azt az értéket, amely jelzi, hogy a műveletnek csak előfeltételt kell-e futtatnia.</span><span class="sxs-lookup"><span data-stu-id="6cce8-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="6cce8-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cce8-137">-Confirm</span></span>
<span data-ttu-id="6cce8-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6cce8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cce8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cce8-139">-WhatIf</span></span>
<span data-ttu-id="6cce8-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6cce8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cce8-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cce8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cce8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cce8-142">CommonParameters</span></span>
<span data-ttu-id="6cce8-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cce8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cce8-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cce8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cce8-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cce8-145">INPUTS</span></span>

## <span data-ttu-id="6cce8-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cce8-146">OUTPUTS</span></span>

### <span data-ttu-id="6cce8-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="6cce8-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="6cce8-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6cce8-148">NOTES</span></span>

<span data-ttu-id="6cce8-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6cce8-149">ALIASES</span></span>

## <span data-ttu-id="6cce8-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cce8-150">RELATED LINKS</span></span>

