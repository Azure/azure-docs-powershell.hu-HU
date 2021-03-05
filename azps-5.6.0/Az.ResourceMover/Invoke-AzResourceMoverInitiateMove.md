---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: e075da17009c863e8c564eb5379495a1bdaff505
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999942"
---
# <span data-ttu-id="eac90-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="eac90-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="eac90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eac90-102">SYNOPSIS</span></span>
<span data-ttu-id="eac90-103">Áthelyezi a kérelem törzsében szereplő erőforrások készletét.</span><span class="sxs-lookup"><span data-stu-id="eac90-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="eac90-104">Az áthelyezési művelet akkor indul el, ha a MoveResources a moveState "MovePending" vagy a "MoveFailed" (ÁthelyezésiFailed) művelettel sikeresen befejeződött, és a MoveResource moveState művelet véglegesítésre vált.</span><span class="sxs-lookup"><span data-stu-id="eac90-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="eac90-105">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="eac90-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="eac90-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eac90-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eac90-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eac90-107">DESCRIPTION</span></span>
<span data-ttu-id="eac90-108">Áthelyezi a kérelem törzsében szereplő erőforrások készletét.</span><span class="sxs-lookup"><span data-stu-id="eac90-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="eac90-109">Az áthelyezési művelet akkor indul el, ha a MoveResources a moveState "MovePending" vagy a "MoveFailed" (ÁthelyezésiFailed) művelettel sikeresen befejeződött, és a MoveResource moveState művelet véglegesítésre vált.</span><span class="sxs-lookup"><span data-stu-id="eac90-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="eac90-110">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="eac90-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="eac90-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eac90-111">EXAMPLES</span></span>

### <span data-ttu-id="eac90-112">1. példa: Az erőforrások áthelyezésének kezdeményezése előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="eac90-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly


AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 9:39:37 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 9:39:37 AM
Status         : Succeeded

```

<span data-ttu-id="eac90-113">Az erőforrások áthelyezésének kezdeményezése előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="eac90-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="eac90-114">2. példa: Áthelyezés kezdeményezése az Áthelyezés gyűjtemény erőforráscsoportja számára a "MoveResource Name" bemenettel.</span><span class="sxs-lookup"><span data-stu-id="eac90-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" 

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 11:56:33 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 11:55:21 AM
Status         : Succeeded

```

<span data-ttu-id="eac90-115">Az Áthelyezés gyűjtemény erőforráskészletének Áthelyezés kezdeményezése bemenetként a "MoveResource Name" használatával.</span><span class="sxs-lookup"><span data-stu-id="eac90-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="eac90-116">3. példa: Áthelyezés kezdeményezése az áthelyezési gyűjtemény erőforráscsoportja számára bemenetként a "SourceARMID" használatával.</span><span class="sxs-lookup"><span data-stu-id="eac90-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:01:35 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:00:21 PM
Status         : Succeeded

```

<span data-ttu-id="eac90-117">Az Áthelyezés gyűjtemény erőforráskészletének Áthelyezés kezdeményezése bemenetként a "SourceARMID" használatával.</span><span class="sxs-lookup"><span data-stu-id="eac90-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="eac90-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eac90-118">PARAMETERS</span></span>

### <span data-ttu-id="eac90-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eac90-119">-AsJob</span></span>
<span data-ttu-id="eac90-120">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="eac90-120">Run the command as a job</span></span>

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

### <span data-ttu-id="eac90-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac90-121">-DefaultProfile</span></span>
<span data-ttu-id="eac90-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eac90-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eac90-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="eac90-123">-MoveCollectionName</span></span>
<span data-ttu-id="eac90-124">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="eac90-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="eac90-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="eac90-125">-MoveResource</span></span>
<span data-ttu-id="eac90-126">Beállítja vagy beállítja az erőforrás-azonosítók listáját, alapértelmezés szerint elfogadja az erőforrás-azonosítók áthelyezését, hacsak a beviteli típust a MoveResourceInputType tulajdonságon keresztül nem váltja át.</span><span class="sxs-lookup"><span data-stu-id="eac90-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="eac90-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="eac90-127">-MoveResourceInputType</span></span>
<span data-ttu-id="eac90-128">Az áthelyezési erőforrás beviteli típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="eac90-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="eac90-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eac90-129">-NoWait</span></span>
<span data-ttu-id="eac90-130">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="eac90-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eac90-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac90-131">-ResourceGroupName</span></span>
<span data-ttu-id="eac90-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eac90-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="eac90-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eac90-133">-SubscriptionId</span></span>
<span data-ttu-id="eac90-134">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eac90-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="eac90-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="eac90-135">-ValidateOnly</span></span>
<span data-ttu-id="eac90-136">Beállítja vagy beállítja azt az értéket, amely jelzi, hogy a műveletnek csak előfeltételt kell-e futtatnia.</span><span class="sxs-lookup"><span data-stu-id="eac90-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="eac90-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eac90-137">-Confirm</span></span>
<span data-ttu-id="eac90-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eac90-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac90-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac90-139">-WhatIf</span></span>
<span data-ttu-id="eac90-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eac90-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eac90-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eac90-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac90-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac90-142">CommonParameters</span></span>
<span data-ttu-id="eac90-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eac90-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac90-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eac90-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac90-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eac90-145">INPUTS</span></span>

## <span data-ttu-id="eac90-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eac90-146">OUTPUTS</span></span>

### <span data-ttu-id="eac90-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="eac90-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="eac90-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eac90-148">NOTES</span></span>

<span data-ttu-id="eac90-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="eac90-149">ALIASES</span></span>

## <span data-ttu-id="eac90-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eac90-150">RELATED LINKS</span></span>

