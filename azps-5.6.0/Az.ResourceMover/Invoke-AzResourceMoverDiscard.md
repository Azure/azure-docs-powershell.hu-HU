---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: 5e54501e6337943561489a80adf4e8789a55a394
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999957"
---
# <span data-ttu-id="b3798-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="b3798-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="b3798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3798-102">SYNOPSIS</span></span>
<span data-ttu-id="b3798-103">Elveti a kérelem törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="b3798-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="b3798-104">Az elvetési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "DiscardFailed" (Függőben) áthelyezésiForráshelyre vált, és sikeresen befejeződik a MoveResource moveState áttűnés.</span><span class="sxs-lookup"><span data-stu-id="b3798-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="b3798-105">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="b3798-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b3798-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3798-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3798-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3798-107">DESCRIPTION</span></span>
<span data-ttu-id="b3798-108">Elveti a kérelem törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="b3798-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="b3798-109">Az elvetési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "DiscardFailed" (Függőben) áthelyezésiForráshelyre vált, és sikeresen befejeződik a MoveResource moveState áttűnés.</span><span class="sxs-lookup"><span data-stu-id="b3798-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="b3798-110">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="b3798-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b3798-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3798-111">EXAMPLES</span></span>

### <span data-ttu-id="b3798-112">1. példa: Az erőforrások elvetés előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="b3798-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:39:48 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:39:37 PM
Status         : Succeeded

```

<span data-ttu-id="b3798-113">Az erőforrások elvetés előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="b3798-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="b3798-114">2. példa: Elveti az erőforrások áthelyezését a "MoveResource Name" bemenettel.</span><span class="sxs-lookup"><span data-stu-id="b3798-114">Example 2: Discards the move of the resources using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:56:33 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:55:21 PM
Status         : Succeeded

```

<span data-ttu-id="b3798-115">Az erőforrások áthelyezését a "MoveResource Name" bemenettel elveti.</span><span class="sxs-lookup"><span data-stu-id="b3798-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="b3798-116">3. példa: Elveti az erőforrások áthelyezését a "SourceARMID" bemenettel.</span><span class="sxs-lookup"><span data-stu-id="b3798-116">Example 3: Discards the move of the resources using "SourceARMID" as input.</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:01:32 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:00:00 PM
Status         : Succeeded


```

<span data-ttu-id="b3798-117">A "SourceARMID" bemenettel elveti az erőforrások áthelyezését.</span><span class="sxs-lookup"><span data-stu-id="b3798-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="b3798-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3798-118">PARAMETERS</span></span>

### <span data-ttu-id="b3798-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3798-119">-AsJob</span></span>
<span data-ttu-id="b3798-120">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="b3798-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b3798-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3798-121">-DefaultProfile</span></span>
<span data-ttu-id="b3798-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3798-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3798-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="b3798-123">-MoveResource</span></span>
<span data-ttu-id="b3798-124">Beállítja vagy beállítja az erőforrás-azonosítók listáját, alapértelmezés szerint elfogadja az erőforrás-azonosítók áthelyezését, hacsak a beviteli típust a MoveResourceInputType tulajdonságon keresztül nem váltja át.</span><span class="sxs-lookup"><span data-stu-id="b3798-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="b3798-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="b3798-125">-MoveResourceInputType</span></span>
<span data-ttu-id="b3798-126">Az áthelyezési erőforrás beviteli típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b3798-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="b3798-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b3798-127">-Name</span></span>
<span data-ttu-id="b3798-128">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="b3798-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="b3798-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b3798-129">-NoWait</span></span>
<span data-ttu-id="b3798-130">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="b3798-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b3798-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3798-131">-ResourceGroupName</span></span>
<span data-ttu-id="b3798-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b3798-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="b3798-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3798-133">-SubscriptionId</span></span>
<span data-ttu-id="b3798-134">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b3798-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="b3798-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="b3798-135">-ValidateOnly</span></span>
<span data-ttu-id="b3798-136">Beállítja vagy beállítja azt az értéket, amely jelzi, hogy a műveletnek csak előfeltételt kell-e futtatnia.</span><span class="sxs-lookup"><span data-stu-id="b3798-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="b3798-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3798-137">-Confirm</span></span>
<span data-ttu-id="b3798-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b3798-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3798-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3798-139">-WhatIf</span></span>
<span data-ttu-id="b3798-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b3798-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3798-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3798-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3798-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3798-142">CommonParameters</span></span>
<span data-ttu-id="b3798-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3798-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3798-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3798-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3798-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3798-145">INPUTS</span></span>

## <span data-ttu-id="b3798-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3798-146">OUTPUTS</span></span>

### <span data-ttu-id="b3798-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="b3798-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="b3798-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3798-148">NOTES</span></span>

<span data-ttu-id="b3798-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b3798-149">ALIASES</span></span>

## <span data-ttu-id="b3798-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3798-150">RELATED LINKS</span></span>

