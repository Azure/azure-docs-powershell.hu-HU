---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverbulkremove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
ms.openlocfilehash: f9815c32526a5ce462a50ec167771d30bc840b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999989"
---
# <span data-ttu-id="13e37-101">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="13e37-101">Invoke-AzResourceMoverBulkRemove</span></span>

## <span data-ttu-id="13e37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13e37-102">SYNOPSIS</span></span>
<span data-ttu-id="13e37-103">Eltávolítja a kérelem törzsében szereplő áthelyezési erőforrások készletét az áthelyezési gyűjteményből.</span><span class="sxs-lookup"><span data-stu-id="13e37-103">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="13e37-104">A veretiont szervizelés szerint kell lefektetni.</span><span class="sxs-lookup"><span data-stu-id="13e37-104">The orchestration is done by service.</span></span>
<span data-ttu-id="13e37-105">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="13e37-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="13e37-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13e37-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverBulkRemove -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-MoveResource <String[]>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13e37-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13e37-107">DESCRIPTION</span></span>
<span data-ttu-id="13e37-108">Eltávolítja a kérelem törzsében szereplő áthelyezési erőforrások készletét az áthelyezési gyűjteményből.</span><span class="sxs-lookup"><span data-stu-id="13e37-108">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="13e37-109">A veretiont szervizelés szerint kell lefektetni.</span><span class="sxs-lookup"><span data-stu-id="13e37-109">The orchestration is done by service.</span></span>
<span data-ttu-id="13e37-110">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="13e37-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="13e37-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13e37-111">EXAMPLES</span></span>

### <span data-ttu-id="13e37-112">1. példa: A függő tényezők ellenőrzése az Erőforrások áthelyezése gyűjteményből eltávolítása előtt</span><span class="sxs-lookup"><span data-stu-id="13e37-112">Example 1: Validate the dependecies before remove of the Move Resources from Move Collection</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:52:28 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Message        : 
Name           : b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:52:28 PM
Status         : Succeeded

```

<span data-ttu-id="13e37-113">Ellenőrizze a függőségeket, mielőtt eltávolítja az áthelyezési erőforrásokat az Áthelyezési gyűjteményből.</span><span class="sxs-lookup"><span data-stu-id="13e37-113">Validate the dependecies before remove of the move resources from Move Collection.</span></span>

### <span data-ttu-id="13e37-114">2. példa: Az Erőforrás áthelyezése a Gyűjtemény áthelyezéséből a "MoveResource Name" beviteli mező használatával</span><span class="sxs-lookup"><span data-stu-id="13e37-114">Example 2: Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:58:10 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d4827071-b797-45c5-b88c-00ddd7818d42
Message        : 
Name           : d4827071-b797-45c5-b88c-00ddd7818d42
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:57:08 PM
Status         : Succeeded
```

<span data-ttu-id="13e37-115">Az Erőforrás áthelyezése gyűjteményből eltávolítása bemenetként a "MoveResource Name" használatával</span><span class="sxs-lookup"><span data-stu-id="13e37-115">Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="13e37-116">3. példa: Az Erőforrás áthelyezése az áthelyezési gyűjteményből bemenetként a "SourceARMID" használatával</span><span class="sxs-lookup"><span data-stu-id="13e37-116">Example 3: Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:05:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/7b6904e2-fc3f-400d-b248-8908fcb282fb
Message        : 
Name           : 7b6904e2-fc3f-400d-b248-8908fcb282fb
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:05:00 PM
Status         : Succeeded
```

<span data-ttu-id="13e37-117">Az Erőforrás áthelyezése a gyűjteményből a "SourceARMID" bemenettel</span><span class="sxs-lookup"><span data-stu-id="13e37-117">Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="13e37-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13e37-118">PARAMETERS</span></span>

### <span data-ttu-id="13e37-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13e37-119">-AsJob</span></span>
<span data-ttu-id="13e37-120">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="13e37-120">Run the command as a job</span></span>

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

### <span data-ttu-id="13e37-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e37-121">-DefaultProfile</span></span>
<span data-ttu-id="13e37-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13e37-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13e37-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="13e37-123">-MoveCollectionName</span></span>
<span data-ttu-id="13e37-124">.</span><span class="sxs-lookup"><span data-stu-id="13e37-124">.</span></span>

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

### <span data-ttu-id="13e37-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="13e37-125">-MoveResource</span></span>
<span data-ttu-id="13e37-126">Beállítja vagy beállítja az erőforrás-azonosítók listáját, alapértelmezés szerint elfogadja az erőforrás-azonosítók áthelyezését, hacsak a beviteli típust a MoveResourceInputType tulajdonságon keresztül nem váltja át.</span><span class="sxs-lookup"><span data-stu-id="13e37-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13e37-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="13e37-127">-MoveResourceInputType</span></span>
<span data-ttu-id="13e37-128">Az áthelyezési erőforrás beviteli típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="13e37-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="13e37-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="13e37-129">-NoWait</span></span>
<span data-ttu-id="13e37-130">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="13e37-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="13e37-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13e37-131">-ResourceGroupName</span></span>
<span data-ttu-id="13e37-132">.</span><span class="sxs-lookup"><span data-stu-id="13e37-132">.</span></span>

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

### <span data-ttu-id="13e37-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13e37-133">-SubscriptionId</span></span>
<span data-ttu-id="13e37-134">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="13e37-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="13e37-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="13e37-135">-ValidateOnly</span></span>
<span data-ttu-id="13e37-136">Beállítja vagy beállítja azt az értéket, amely jelzi, hogy a műveletnek csak előfeltételt kell-e futtatnia.</span><span class="sxs-lookup"><span data-stu-id="13e37-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="13e37-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13e37-137">-Confirm</span></span>
<span data-ttu-id="13e37-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="13e37-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13e37-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13e37-139">-WhatIf</span></span>
<span data-ttu-id="13e37-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="13e37-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13e37-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13e37-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13e37-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e37-142">CommonParameters</span></span>
<span data-ttu-id="13e37-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13e37-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e37-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13e37-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e37-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13e37-145">INPUTS</span></span>

## <span data-ttu-id="13e37-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13e37-146">OUTPUTS</span></span>

### <span data-ttu-id="13e37-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="13e37-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="13e37-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13e37-148">NOTES</span></span>

<span data-ttu-id="13e37-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="13e37-149">ALIASES</span></span>

## <span data-ttu-id="13e37-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13e37-150">RELATED LINKS</span></span>

