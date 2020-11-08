---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025063"
---
# <span data-ttu-id="9c1b2-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="9c1b2-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="9c1b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c1b2-102">SYNOPSIS</span></span>
<span data-ttu-id="9c1b2-103">Előkészületeket kezdeményez a kérés törzsében található erőforrások készletére.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="9c1b2-104">Az előkészítési művelet a "PreparePending" vagy a "PrepareFailed" moveState található moveResources, és a sikeres Befejezés érdekében a moveResource moveState MovePending áttűnést hajt végre a.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="9c1b2-105">Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="9c1b2-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c1b2-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c1b2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c1b2-107">DESCRIPTION</span></span>
<span data-ttu-id="9c1b2-108">Előkészületeket kezdeményez a kérés törzsében található erőforrások készletére.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="9c1b2-109">Az előkészítési művelet a "PreparePending" vagy a "PrepareFailed" moveState található moveResources, és a sikeres Befejezés érdekében a moveResource moveState MovePending áttűnést hajt végre a.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="9c1b2-110">Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="9c1b2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9c1b2-111">EXAMPLES</span></span>

### <span data-ttu-id="9c1b2-112">Példa 1: a dependecies érvényesítése az erőforrások előkészítése előtt</span><span class="sxs-lookup"><span data-stu-id="9c1b2-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 8/21/2020 6:04:15 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/MoveCollection-cus-wcus-eus2/operations/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:04:14 AM
Status         : Failed

```

<span data-ttu-id="9c1b2-113">Ellenőrizze a dependecies, mielőtt felkészüljenek az erőforrásokra.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="9c1b2-114">2. példa: Felkészülés az erőforrások készletére az áthelyezés gyűjteményben a "MoveResource név" értékkel bemenetként</span><span class="sxs-lookup"><span data-stu-id="9c1b2-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm','psdemovm62', 'PSDemoVM-ip', 'PSDemoRM-vnet','PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:18:09 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/da65e9c7-7fb9-44ef-af99-6f65b21e9951
Message        :
Name           : da65e9c7-7fb9-44ef-af99-6f65b21e9951
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:18:08 AM
Status         : Succeeded
```

<span data-ttu-id="9c1b2-115">A "MoveResource név" érték beírásával kezdeményezi az áthelyezési gyűjteményben az erőforrások készletére való felkészülést.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="9c1b2-116">3. példa: Felkészülés az erőforrások készletére az áthelyezés gyűjteményben a "SourceARMID" használatával</span><span class="sxs-lookup"><span data-stu-id="9c1b2-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:35:30 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:35:27 AM
Status         : Succeeded

```

<span data-ttu-id="9c1b2-117">Az áthelyezés gyűjteményben az "SourceARMID" kifejezésre való felkészülést kezdeményez az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="9c1b2-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c1b2-118">PARAMETERS</span></span>

### <span data-ttu-id="9c1b2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c1b2-119">-AsJob</span></span>
<span data-ttu-id="9c1b2-120">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="9c1b2-120">Run the command as a job</span></span>

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

### <span data-ttu-id="9c1b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c1b2-121">-DefaultProfile</span></span>
<span data-ttu-id="9c1b2-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c1b2-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="9c1b2-123">-MoveCollectionName</span></span>
<span data-ttu-id="9c1b2-124">Az áthelyezés gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="9c1b2-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="9c1b2-125">-MoveResource</span></span>
<span data-ttu-id="9c1b2-126">Beállítja vagy beállítja az erőforrás-azonosítók listáját, alapértelmezés szerint elfogadja az erőforrás-azonosító áthelyezését, hacsak a bemeneti típus nincs átváltva a moveResourceInputType tulajdonságon keresztül.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="9c1b2-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="9c1b2-127">-MoveResourceInputType</span></span>
<span data-ttu-id="9c1b2-128">Az erőforrás bemeneti típusának áthelyezési típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="9c1b2-129">-Várva</span><span class="sxs-lookup"><span data-stu-id="9c1b2-129">-NoWait</span></span>
<span data-ttu-id="9c1b2-130">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="9c1b2-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9c1b2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c1b2-131">-ResourceGroupName</span></span>
<span data-ttu-id="9c1b2-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="9c1b2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c1b2-133">-SubscriptionId</span></span>
<span data-ttu-id="9c1b2-134">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="9c1b2-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="9c1b2-135">-ValidateOnly</span></span>
<span data-ttu-id="9c1b2-136">Beolvassa vagy beállítja azt az értéket, amely azt jelzi, hogy a műveletnek csak előre szükségesnek kell-e futnia.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="9c1b2-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c1b2-137">-Confirm</span></span>
<span data-ttu-id="9c1b2-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c1b2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c1b2-139">-WhatIf</span></span>
<span data-ttu-id="9c1b2-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c1b2-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c1b2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c1b2-142">CommonParameters</span></span>
<span data-ttu-id="9c1b2-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c1b2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c1b2-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c1b2-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c1b2-145">INPUTS</span></span>

## <span data-ttu-id="9c1b2-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c1b2-146">OUTPUTS</span></span>

### <span data-ttu-id="9c1b2-147">Microsoft. Azure. PowerShell. parancsmagok. ResourceMover. modellek. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="9c1b2-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="9c1b2-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c1b2-148">NOTES</span></span>

<span data-ttu-id="9c1b2-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9c1b2-149">ALIASES</span></span>

## <span data-ttu-id="9c1b2-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c1b2-150">RELATED LINKS</span></span>

