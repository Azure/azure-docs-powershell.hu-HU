---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c205354b68def88b00fb67959669633d5ba1fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999974"
---
# <span data-ttu-id="13f4c-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="13f4c-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="13f4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="13f4c-103">A kérelem törzsében szereplő erőforrások halmazának véglegesítésére.</span><span class="sxs-lookup"><span data-stu-id="13f4c-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="13f4c-104">A véglegesítési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "CommitFailed" műveletben sikeresen befejeződik, és a moveResource moveState áttűnés lekötöttre vált.</span><span class="sxs-lookup"><span data-stu-id="13f4c-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="13f4c-105">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="13f4c-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="13f4c-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13f4c-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13f4c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13f4c-107">DESCRIPTION</span></span>
<span data-ttu-id="13f4c-108">A kérelem törzsében szereplő erőforrások halmazának véglegesítésére.</span><span class="sxs-lookup"><span data-stu-id="13f4c-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="13f4c-109">A véglegesítési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "CommitFailed" műveletben sikeresen befejeződik, és a moveResource moveState áttűnés lekötöttre vált.</span><span class="sxs-lookup"><span data-stu-id="13f4c-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="13f4c-110">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="13f4c-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="13f4c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13f4c-111">EXAMPLES</span></span>

### <span data-ttu-id="13f4c-112">1. példa: Az erőforrások véglegesítése előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="13f4c-112">Example 1: Validate the dependecies before commit of the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:38:26 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/c194298b-b2eb-4aab-80b4-129d1473b75c
Message        : 
Name           : c194298b-b2eb-4aab-80b4-129d1473b75c
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:38:25 PM
Status         : Succeeded

```

<span data-ttu-id="13f4c-113">Az erőforrások véglegesítése előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="13f4c-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="13f4c-114">2. példa: Az Áthelyezési gyűjtemény erőforráskészletének véglegesítéséhez használja a "MoveResource Name" bemenetet.</span><span class="sxs-lookup"><span data-stu-id="13f4c-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:41:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/80c04850-7f3f-4e9c-aa68-b868978b59f3
Message        : 
Name           : 80c04850-7f3f-4e9c-aa68-b868978b59f3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:41:05 PM
Status         : Succeeded


```

<span data-ttu-id="13f4c-115">Az Áthelyezési gyűjteményben a "MoveResource Name" erőforráskészletet bemenetként véglegesítésére használja.</span><span class="sxs-lookup"><span data-stu-id="13f4c-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="13f4c-116">3. példa: Az Áthelyezési gyűjtemény erőforráskészletének véglegesítéséhez használja a "SourceARMID" bemenetet.</span><span class="sxs-lookup"><span data-stu-id="13f4c-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:42:46 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d36ca519-8ced-48c9-a968-cb5e9c4db731
Message        : 
Name           : d36ca519-8ced-48c9-a968-cb5e9c4db731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:42:41 PM
Status         : Succeeded


```

<span data-ttu-id="13f4c-117">Az Áthelyezési gyűjteményben a "SourceARMID" erőforráskészletet bemenetként véglegesítéssel kell véglegesen használnia.</span><span class="sxs-lookup"><span data-stu-id="13f4c-117">Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="13f4c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13f4c-118">PARAMETERS</span></span>

### <span data-ttu-id="13f4c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13f4c-119">-AsJob</span></span>
<span data-ttu-id="13f4c-120">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="13f4c-120">Run the command as a job</span></span>

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

### <span data-ttu-id="13f4c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f4c-121">-DefaultProfile</span></span>
<span data-ttu-id="13f4c-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13f4c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13f4c-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="13f4c-123">-MoveCollectionName</span></span>
<span data-ttu-id="13f4c-124">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="13f4c-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="13f4c-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="13f4c-125">-MoveResource</span></span>
<span data-ttu-id="13f4c-126">Beállítja vagy beállítja az erőforrás-azonosítók listáját, alapértelmezés szerint elfogadja az erőforrás-azonosítók áthelyezését, hacsak a beviteli típust a MoveResourceInputType tulajdonságon keresztül nem váltja át.</span><span class="sxs-lookup"><span data-stu-id="13f4c-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="13f4c-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="13f4c-127">-MoveResourceInputType</span></span>
<span data-ttu-id="13f4c-128">Az áthelyezési erőforrás beviteli típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="13f4c-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="13f4c-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="13f4c-129">-NoWait</span></span>
<span data-ttu-id="13f4c-130">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="13f4c-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="13f4c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f4c-131">-ResourceGroupName</span></span>
<span data-ttu-id="13f4c-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13f4c-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="13f4c-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13f4c-133">-SubscriptionId</span></span>
<span data-ttu-id="13f4c-134">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="13f4c-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="13f4c-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="13f4c-135">-ValidateOnly</span></span>
<span data-ttu-id="13f4c-136">Beállítja vagy beállítja azt az értéket, amely jelzi, hogy a műveletnek csak előfeltételt kell-e futtatnia.</span><span class="sxs-lookup"><span data-stu-id="13f4c-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="13f4c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13f4c-137">-Confirm</span></span>
<span data-ttu-id="13f4c-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="13f4c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13f4c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13f4c-139">-WhatIf</span></span>
<span data-ttu-id="13f4c-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="13f4c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13f4c-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13f4c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13f4c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f4c-142">CommonParameters</span></span>
<span data-ttu-id="13f4c-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f4c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f4c-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13f4c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f4c-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13f4c-145">INPUTS</span></span>

## <span data-ttu-id="13f4c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13f4c-146">OUTPUTS</span></span>

### <span data-ttu-id="13f4c-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="13f4c-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="13f4c-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13f4c-148">NOTES</span></span>

<span data-ttu-id="13f4c-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="13f4c-149">ALIASES</span></span>

## <span data-ttu-id="13f4c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13f4c-150">RELATED LINKS</span></span>

