---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302498"
---
# <span data-ttu-id="9485e-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="9485e-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="9485e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9485e-102">SYNOPSIS</span></span>
<span data-ttu-id="9485e-103">Elveti a kérés törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="9485e-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="9485e-104">Az elvetési művelet az "CommitPending" vagy a "DiscardFailed" moveState moveResources vált, és a sikeres Befejezés érdekében a moveResource moveState MovePending.</span><span class="sxs-lookup"><span data-stu-id="9485e-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="9485e-105">Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.</span><span class="sxs-lookup"><span data-stu-id="9485e-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="9485e-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9485e-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9485e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9485e-107">DESCRIPTION</span></span>
<span data-ttu-id="9485e-108">Elveti a kérés törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="9485e-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="9485e-109">Az elvetési művelet az "CommitPending" vagy a "DiscardFailed" moveState moveResources vált, és a sikeres Befejezés érdekében a moveResource moveState MovePending.</span><span class="sxs-lookup"><span data-stu-id="9485e-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="9485e-110">Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.</span><span class="sxs-lookup"><span data-stu-id="9485e-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="9485e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9485e-111">EXAMPLES</span></span>

### <span data-ttu-id="9485e-112">Példa 1: a dependecies érvényesítése az erőforrások elvetése előtt.</span><span class="sxs-lookup"><span data-stu-id="9485e-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
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

<span data-ttu-id="9485e-113">Ellenőrizze a dependecies, mielőtt elveti az erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="9485e-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="9485e-114">2. példa: az erőforrások áthelyezésének eldobása bemenetként "MoveResource név" használatával</span><span class="sxs-lookup"><span data-stu-id="9485e-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="9485e-115">Visszaadja az erőforrások áthelyezését bemenetként a "MoveResource név" kifejezés használatával.</span><span class="sxs-lookup"><span data-stu-id="9485e-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="9485e-116">3. példa: az erőforrások áthelyezésének eldobása bemenetként "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="9485e-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
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

<span data-ttu-id="9485e-117">Visszaadja az erőforrások áthelyezését bemenetként a "SourceARMID" paranccsal.</span><span class="sxs-lookup"><span data-stu-id="9485e-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="9485e-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9485e-118">PARAMETERS</span></span>

### <span data-ttu-id="9485e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9485e-119">-AsJob</span></span>
<span data-ttu-id="9485e-120">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="9485e-120">Run the command as a job</span></span>

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

### <span data-ttu-id="9485e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9485e-121">-DefaultProfile</span></span>
<span data-ttu-id="9485e-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9485e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9485e-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="9485e-123">-MoveResource</span></span>
<span data-ttu-id="9485e-124">Beállítja vagy beállítja az erőforrás-azonosítók listáját, alapértelmezés szerint elfogadja az erőforrás-azonosító áthelyezését, hacsak a bemeneti típus nincs átváltva a moveResourceInputType tulajdonságon keresztül.</span><span class="sxs-lookup"><span data-stu-id="9485e-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="9485e-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="9485e-125">-MoveResourceInputType</span></span>
<span data-ttu-id="9485e-126">Az erőforrás bemeneti típusának áthelyezési típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9485e-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="9485e-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9485e-127">-Name</span></span>
<span data-ttu-id="9485e-128">Az áthelyezés gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="9485e-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="9485e-129">-Várva</span><span class="sxs-lookup"><span data-stu-id="9485e-129">-NoWait</span></span>
<span data-ttu-id="9485e-130">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="9485e-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9485e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9485e-131">-ResourceGroupName</span></span>
<span data-ttu-id="9485e-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9485e-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="9485e-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9485e-133">-SubscriptionId</span></span>
<span data-ttu-id="9485e-134">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="9485e-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="9485e-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="9485e-135">-ValidateOnly</span></span>
<span data-ttu-id="9485e-136">Beolvassa vagy beállítja azt az értéket, amely azt jelzi, hogy a műveletnek csak előre szükségesnek kell-e futnia.</span><span class="sxs-lookup"><span data-stu-id="9485e-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="9485e-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9485e-137">-Confirm</span></span>
<span data-ttu-id="9485e-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9485e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9485e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9485e-139">-WhatIf</span></span>
<span data-ttu-id="9485e-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9485e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9485e-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9485e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9485e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9485e-142">CommonParameters</span></span>
<span data-ttu-id="9485e-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9485e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9485e-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9485e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9485e-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9485e-145">INPUTS</span></span>

## <span data-ttu-id="9485e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9485e-146">OUTPUTS</span></span>

### <span data-ttu-id="9485e-147">Microsoft. Azure. PowerShell. parancsmagok. ResourceMover. modellek. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="9485e-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="9485e-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9485e-148">NOTES</span></span>

<span data-ttu-id="9485e-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9485e-149">ALIASES</span></span>

## <span data-ttu-id="9485e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9485e-150">RELATED LINKS</span></span>

