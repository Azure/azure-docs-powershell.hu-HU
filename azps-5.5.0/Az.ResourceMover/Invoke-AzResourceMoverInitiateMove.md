---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153762"
---
# <span data-ttu-id="0e6ec-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="0e6ec-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="0e6ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6ec-103">Áthelyezi a kérelem törzsében szereplő erőforrások készletét.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="0e6ec-104">Az áthelyezési művelet akkor indul el, ha a moveResources a moveState "MovePending" vagy a "MoveFailed" (ÁthelyezésiFailed) műveletben van, és a moveResource moveState művelet véglegesítésre vált.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="0e6ec-105">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="0e6ec-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0e6ec-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0e6ec-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0e6ec-107">DESCRIPTION</span></span>
<span data-ttu-id="0e6ec-108">Áthelyezi a kérelem törzsében szereplő erőforrások készletét.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="0e6ec-109">Az áthelyezési művelet akkor indul el, ha a moveResources a moveState "MovePending" vagy a "MoveFailed" (ÁthelyezésiFailed) műveletben van, és a moveResource moveState művelet véglegesítésre vált.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="0e6ec-110">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="0e6ec-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0e6ec-111">EXAMPLES</span></span>

### <span data-ttu-id="0e6ec-112">1. példa: Az erőforrások áthelyezésének kezdeményezése előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg')  -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:07:36 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Message        :
Name           : 8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:07:35 AM
Status         : Succeeded

```

<span data-ttu-id="0e6ec-113">Az erőforrások áthelyezésének kezdeményezése előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="0e6ec-114">2. példa: Áthelyezés kezdeményezése az Áthelyezés gyűjtemény erőforrás-készletéhez bevitelként a "MoveResource Name" használatával</span><span class="sxs-lookup"><span data-stu-id="0e6ec-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') 

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:24:21 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/bc30d933-c2b6-47c9-b583-240d375b5864
Message        :
Name           : bc30d933-c2b6-47c9-b583-240d375b5864
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:24:21 AM
Status         : Succeeded

```

<span data-ttu-id="0e6ec-115">Az Áthelyezés gyűjtemény erőforráskészletének Áthelyezés kezdeményezése bemenetként a "MoveResource Name" használatával.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="0e6ec-116">3. példa: Áthelyezés kezdeményezése az áthelyezési gyűjtemény erőforráscsoportja számára bemenetként a "SourceARMID" használatával</span><span class="sxs-lookup"><span data-stu-id="0e6ec-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:38:33 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/cbc0f921-de9b-45d5-91da-60e36b841b10
Message        :
Name           : cbc0f921-de9b-45d5-91da-60e36b841b10
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:37:23 AM
Status         : Succeeded

```

<span data-ttu-id="0e6ec-117">Az Áthelyezés gyűjtemény erőforráskészletének Áthelyezés kezdeményezése bemenetként a "SourceARMID" használatával.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="0e6ec-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e6ec-118">PARAMETERS</span></span>

### <span data-ttu-id="0e6ec-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e6ec-119">-AsJob</span></span>
<span data-ttu-id="0e6ec-120">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="0e6ec-120">Run the command as a job</span></span>

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

### <span data-ttu-id="0e6ec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6ec-121">-DefaultProfile</span></span>
<span data-ttu-id="0e6ec-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e6ec-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="0e6ec-123">-MoveCollectionName</span></span>
<span data-ttu-id="0e6ec-124">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="0e6ec-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="0e6ec-125">-MoveResource</span></span>
<span data-ttu-id="0e6ec-126">Beállítja vagy beállítja az erőforrás-azonosítók listáját, alapértelmezés szerint elfogadja az erőforrás-azonosítók áthelyezését, hacsak a beviteli típust a MoveResourceInputType tulajdonságon keresztül nem váltja át.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="0e6ec-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="0e6ec-127">-MoveResourceInputType</span></span>
<span data-ttu-id="0e6ec-128">Az áthelyezési erőforrás beviteli típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="0e6ec-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0e6ec-129">-NoWait</span></span>
<span data-ttu-id="0e6ec-130">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="0e6ec-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0e6ec-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e6ec-131">-ResourceGroupName</span></span>
<span data-ttu-id="0e6ec-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="0e6ec-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e6ec-133">-SubscriptionId</span></span>
<span data-ttu-id="0e6ec-134">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="0e6ec-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="0e6ec-135">-ValidateOnly</span></span>
<span data-ttu-id="0e6ec-136">Beállítja vagy beállítja azt az értéket, amely jelzi, hogy a műveletnek csak előfeltételt kell-e futtatnia.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="0e6ec-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e6ec-137">-Confirm</span></span>
<span data-ttu-id="0e6ec-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e6ec-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e6ec-139">-WhatIf</span></span>
<span data-ttu-id="0e6ec-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e6ec-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e6ec-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6ec-142">CommonParameters</span></span>
<span data-ttu-id="0e6ec-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e6ec-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6ec-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e6ec-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6ec-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e6ec-145">INPUTS</span></span>

## <span data-ttu-id="0e6ec-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e6ec-146">OUTPUTS</span></span>

### <span data-ttu-id="0e6ec-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="0e6ec-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="0e6ec-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0e6ec-148">NOTES</span></span>

<span data-ttu-id="0e6ec-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0e6ec-149">ALIASES</span></span>

## <span data-ttu-id="0e6ec-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e6ec-150">RELATED LINKS</span></span>

