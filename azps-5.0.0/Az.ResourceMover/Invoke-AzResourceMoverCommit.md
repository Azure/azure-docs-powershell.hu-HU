---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302501"
---
# <span data-ttu-id="9abfa-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="9abfa-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="9abfa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9abfa-102">SYNOPSIS</span></span>
<span data-ttu-id="9abfa-103">Véglegesíti a kérés törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="9abfa-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="9abfa-104">A véglegesítési művelet az "CommitPending" vagy a "CommitFailed" moveState moveResources lép fel, és a sikeres Befejezés érdekében a moveResource moveState az áttűnést végrehajtja.</span><span class="sxs-lookup"><span data-stu-id="9abfa-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="9abfa-105">Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.</span><span class="sxs-lookup"><span data-stu-id="9abfa-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="9abfa-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9abfa-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9abfa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9abfa-107">DESCRIPTION</span></span>
<span data-ttu-id="9abfa-108">Véglegesíti a kérés törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="9abfa-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="9abfa-109">A véglegesítési művelet az "CommitPending" vagy a "CommitFailed" moveState moveResources lép fel, és a sikeres Befejezés érdekében a moveResource moveState az áttűnést végrehajtja.</span><span class="sxs-lookup"><span data-stu-id="9abfa-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="9abfa-110">Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.</span><span class="sxs-lookup"><span data-stu-id="9abfa-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="9abfa-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9abfa-111">EXAMPLES</span></span>

### <span data-ttu-id="9abfa-112">Példa 1: a dependecies érvényesítése az erőforrások véglegesítése előtt</span><span class="sxs-lookup"><span data-stu-id="9abfa-112">Example 1: Validate the dependecies before commit of the resources</span></span>
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

<span data-ttu-id="9abfa-113">Ellenőrizze a dependecies az erőforrások véglegesítése előtt.</span><span class="sxs-lookup"><span data-stu-id="9abfa-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="9abfa-114">2. példa: erőforrások készletének véglegesítése az áthelyezés gyűjteményben a "MoveResource név" értékkel bemenetként</span><span class="sxs-lookup"><span data-stu-id="9abfa-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="9abfa-115">Erőforrások készletének véglegesítése az áthelyezés gyűjteményben a "MoveResource név" értékkel bemenetként</span><span class="sxs-lookup"><span data-stu-id="9abfa-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="9abfa-116">3. példa: erőforrások készletének véglegesítése az áthelyezés gyűjteményben a "SourceARMID" bemenettel</span><span class="sxs-lookup"><span data-stu-id="9abfa-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
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

<span data-ttu-id="9abfa-117">Erőforrások készletének véglegesítése az áthelyezés gyűjteményben a "SourceARMID" bemenettel</span><span class="sxs-lookup"><span data-stu-id="9abfa-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="9abfa-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9abfa-118">PARAMETERS</span></span>

### <span data-ttu-id="9abfa-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9abfa-119">-AsJob</span></span>
<span data-ttu-id="9abfa-120">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="9abfa-120">Run the command as a job</span></span>

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

### <span data-ttu-id="9abfa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abfa-121">-DefaultProfile</span></span>
<span data-ttu-id="9abfa-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9abfa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9abfa-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="9abfa-123">-MoveCollectionName</span></span>
<span data-ttu-id="9abfa-124">Az áthelyezés gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="9abfa-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="9abfa-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="9abfa-125">-MoveResource</span></span>
<span data-ttu-id="9abfa-126">Beállítja vagy beállítja az erőforrás-azonosítók listáját, alapértelmezés szerint elfogadja az erőforrás-azonosító áthelyezését, hacsak a bemeneti típus nincs átváltva a moveResourceInputType tulajdonságon keresztül.</span><span class="sxs-lookup"><span data-stu-id="9abfa-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="9abfa-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="9abfa-127">-MoveResourceInputType</span></span>
<span data-ttu-id="9abfa-128">Az erőforrás bemeneti típusának áthelyezési típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9abfa-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="9abfa-129">-Várva</span><span class="sxs-lookup"><span data-stu-id="9abfa-129">-NoWait</span></span>
<span data-ttu-id="9abfa-130">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="9abfa-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9abfa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9abfa-131">-ResourceGroupName</span></span>
<span data-ttu-id="9abfa-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9abfa-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="9abfa-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9abfa-133">-SubscriptionId</span></span>
<span data-ttu-id="9abfa-134">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="9abfa-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="9abfa-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="9abfa-135">-ValidateOnly</span></span>
<span data-ttu-id="9abfa-136">Beolvassa vagy beállítja azt az értéket, amely azt jelzi, hogy a műveletnek csak előre szükségesnek kell-e futnia.</span><span class="sxs-lookup"><span data-stu-id="9abfa-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="9abfa-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9abfa-137">-Confirm</span></span>
<span data-ttu-id="9abfa-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9abfa-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9abfa-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9abfa-139">-WhatIf</span></span>
<span data-ttu-id="9abfa-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9abfa-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9abfa-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9abfa-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9abfa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abfa-142">CommonParameters</span></span>
<span data-ttu-id="9abfa-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9abfa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abfa-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9abfa-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abfa-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9abfa-145">INPUTS</span></span>

## <span data-ttu-id="9abfa-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9abfa-146">OUTPUTS</span></span>

### <span data-ttu-id="9abfa-147">Microsoft. Azure. PowerShell. parancsmagok. ResourceMover. modellek. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="9abfa-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="9abfa-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9abfa-148">NOTES</span></span>

<span data-ttu-id="9abfa-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9abfa-149">ALIASES</span></span>

## <span data-ttu-id="9abfa-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9abfa-150">RELATED LINKS</span></span>

