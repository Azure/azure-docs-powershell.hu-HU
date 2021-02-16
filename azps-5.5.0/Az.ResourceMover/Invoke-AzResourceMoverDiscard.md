---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169123"
---
# <span data-ttu-id="72726-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="72726-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="72726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72726-102">SYNOPSIS</span></span>
<span data-ttu-id="72726-103">Elveti a kérelem törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="72726-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="72726-104">Az elvetési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "DiscardFailed" (Függőben) áthelyezésiForráshelyre vált, és sikeresen befejeződik a moveResource moveState áttűnés a Függőben műveletre.</span><span class="sxs-lookup"><span data-stu-id="72726-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="72726-105">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak ahhoz a művelethez, amely a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="72726-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="72726-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="72726-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="72726-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="72726-107">DESCRIPTION</span></span>
<span data-ttu-id="72726-108">Elveti a kérelem törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="72726-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="72726-109">Az elvetési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "DiscardFailed" (Függőben) áthelyezésiForráshelyre vált, és sikeresen befejeződik a moveResource moveState áttűnés a Függőben műveletre.</span><span class="sxs-lookup"><span data-stu-id="72726-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="72726-110">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak ahhoz a művelethez, amely a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="72726-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="72726-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="72726-111">EXAMPLES</span></span>

### <span data-ttu-id="72726-112">1. példa: Az erőforrások elvetés előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="72726-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') -ValidateOnly

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 9:44:54 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/62861ceb-28c9-4e0c-811b-84692a203181
Message        :
Name           : 62861ceb-28c9-4e0c-811b-84692a203181
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 9:44:54 AM
Status         : Succeeded

```

<span data-ttu-id="72726-113">Az erőforrások elvetés előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="72726-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="72726-114">2. példa: Elveti az erőforrások áthelyezését a "MoveResource Name" bemenettel</span><span class="sxs-lookup"><span data-stu-id="72726-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:26:51 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/21f99cd3-89a4-4fcb-8b96-40d0572a6377
Message        :
Name           : 21f99cd3-89a4-4fcb-8b96-40d0572a6377
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:26:39 AM
Status         : Succeeded

```

<span data-ttu-id="72726-115">Az erőforrások áthelyezését a "MoveResource Name" bemenettel elveti.</span><span class="sxs-lookup"><span data-stu-id="72726-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="72726-116">3. példa: Elveti az erőforrások áthelyezését a "SourceARMID" bemenettel</span><span class="sxs-lookup"><span data-stu-id="72726-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:33:37 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/b842efcd-e5fd-42b0-a277-01ee8225deed
Message        :
Name           : b842efcd-e5fd-42b0-a277-01ee8225deed
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:33:23 AM
Status         : Succeeded


```

<span data-ttu-id="72726-117">A "SourceARMID" bemenettel elveti az erőforrások áthelyezését.</span><span class="sxs-lookup"><span data-stu-id="72726-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="72726-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72726-118">PARAMETERS</span></span>

### <span data-ttu-id="72726-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72726-119">-AsJob</span></span>
<span data-ttu-id="72726-120">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="72726-120">Run the command as a job</span></span>

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

### <span data-ttu-id="72726-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72726-121">-DefaultProfile</span></span>
<span data-ttu-id="72726-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72726-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72726-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="72726-123">-MoveResource</span></span>
<span data-ttu-id="72726-124">Beállítja vagy beállítja az erőforrás-azonosítók listáját, alapértelmezés szerint elfogadja az erőforrás-azonosítók áthelyezését, hacsak a beviteli típust a MoveResourceInputType tulajdonságon keresztül nem váltja át.</span><span class="sxs-lookup"><span data-stu-id="72726-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="72726-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="72726-125">-MoveResourceInputType</span></span>
<span data-ttu-id="72726-126">Az áthelyezési erőforrás beviteli típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="72726-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="72726-127">-Name</span><span class="sxs-lookup"><span data-stu-id="72726-127">-Name</span></span>
<span data-ttu-id="72726-128">A Gyűjtemény áthelyezése név.</span><span class="sxs-lookup"><span data-stu-id="72726-128">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72726-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="72726-129">-NoWait</span></span>
<span data-ttu-id="72726-130">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="72726-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="72726-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72726-131">-ResourceGroupName</span></span>
<span data-ttu-id="72726-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="72726-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="72726-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72726-133">-SubscriptionId</span></span>
<span data-ttu-id="72726-134">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="72726-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="72726-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="72726-135">-ValidateOnly</span></span>
<span data-ttu-id="72726-136">Beállítja vagy beállítja azt az értéket, amely jelzi, hogy a műveletnek csak előfeltételt kell-e futtatnia.</span><span class="sxs-lookup"><span data-stu-id="72726-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="72726-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72726-137">-Confirm</span></span>
<span data-ttu-id="72726-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="72726-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72726-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72726-139">-WhatIf</span></span>
<span data-ttu-id="72726-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="72726-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72726-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72726-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72726-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72726-142">CommonParameters</span></span>
<span data-ttu-id="72726-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72726-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72726-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72726-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72726-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72726-145">INPUTS</span></span>

## <span data-ttu-id="72726-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72726-146">OUTPUTS</span></span>

### <span data-ttu-id="72726-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="72726-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="72726-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="72726-148">NOTES</span></span>

<span data-ttu-id="72726-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="72726-149">ALIASES</span></span>

## <span data-ttu-id="72726-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72726-150">RELATED LINKS</span></span>

