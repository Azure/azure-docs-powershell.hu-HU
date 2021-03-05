---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 95ad5dad6bd375595a452881e1dfe72a9f314207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999941"
---
# <span data-ttu-id="79620-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="79620-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="79620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79620-102">SYNOPSIS</span></span>
<span data-ttu-id="79620-103">A kérés törzsében szereplő erőforrásokra való felkészülést kezdeményezi.</span><span class="sxs-lookup"><span data-stu-id="79620-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="79620-104">Az előkészítési művelet a "PreparePending" vagy a "PrepareFailed" moveState "PrepareFailed" moveResources műveleten van, és sikeresen befejeződött a moveResource moveState áttűnés a Függőben műveletre.</span><span class="sxs-lookup"><span data-stu-id="79620-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="79620-105">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="79620-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="79620-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79620-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="79620-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79620-107">DESCRIPTION</span></span>
<span data-ttu-id="79620-108">A kérés törzsében szereplő erőforrásokra való felkészülést kezdeményezi.</span><span class="sxs-lookup"><span data-stu-id="79620-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="79620-109">Az előkészítési művelet a "PreparePending" vagy a "PrepareFailed" moveState "PrepareFailed" moveResources műveleten van, és sikeresen befejeződött a moveResource moveState áttűnés a Függőben műveletre.</span><span class="sxs-lookup"><span data-stu-id="79620-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="79620-110">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="79620-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="79620-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79620-111">EXAMPLES</span></span>

### <span data-ttu-id="79620-112">1. példa: Az erőforrások előkészítése előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="79620-112">Example 1: Validate the dependecies before prepare of the resources.</span></span> <span data-ttu-id="79620-113">Szerezze be a szükséges függő erőforrásokat, amelyekre szintén fel kell készülni.</span><span class="sxs-lookup"><span data-stu-id="79620-113">Get the required dependent resources that also need to be prepared.</span></span>
```powershell
PS C:\> $resp = Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 2/9/2021 9:04:15 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/PS-centralus-westcentralus-demoRMS/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 9:04:14 AM
Status         : Failed

PS C:> $resp.Code
MoveCollectionMissingRequiredDependentResources

PS C:> $resp.AdditionalInfo[0].InfoMoveResource

SourceId                                                                                                                                  
--------                                                                                                                                  
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg

```

<span data-ttu-id="79620-114">Az erőforrások előkészítése előtt ellenőrizze a függőségeket.</span><span class="sxs-lookup"><span data-stu-id="79620-114">Validate the dependecies before prepare of the resources.</span></span>
<span data-ttu-id="79620-115">Szerezze be a szükséges függő erőforrásokat, amelyekre szintén fel kell készülni.</span><span class="sxs-lookup"><span data-stu-id="79620-115">Get the required dependent resources that also need to be prepared.</span></span>

### <span data-ttu-id="79620-116">2. példa: Az Áthelyezési gyűjtemény erőforráskészletének előkészítése a "MoveResource Name" bemenettel.</span><span class="sxs-lookup"><span data-stu-id="79620-116">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM','psdemovm111', 'PSDemoRM-vnet','PSDemoVM-nsg')

AAdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/9/2021 11:25:13 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/49e4429
                 4-24ac-4eac-93da-e7e1c815554d
Message        : 
Name           : 49e44294-24ac-4eac-93da-e7e1c815554d
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 10:55:53 AM
Status         : Succeeded
```

<span data-ttu-id="79620-117">Az Áthelyezési gyűjtemény erőforráskészletének előkészítése a "MoveResource Name" bemenettel.</span><span class="sxs-lookup"><span data-stu-id="79620-117">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="79620-118">3. példa: A "SourceARMID" használatával készüljön fel az áthelyezési gyűjtemény erőforráskészletére.</span><span class="sxs-lookup"><span data-stu-id="79620-118">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRMS/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 2/9/2021 11:09:30 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRMS/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 11:05:27 AM
Status         : Succeeded

```

<span data-ttu-id="79620-119">Készüljön fel az erőforráskészletre az Áthelyezési gyűjteményben a "SourceARMID" használatával.</span><span class="sxs-lookup"><span data-stu-id="79620-119">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="79620-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79620-120">PARAMETERS</span></span>

### <span data-ttu-id="79620-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79620-121">-AsJob</span></span>
<span data-ttu-id="79620-122">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="79620-122">Run the command as a job</span></span>

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

### <span data-ttu-id="79620-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79620-123">-DefaultProfile</span></span>
<span data-ttu-id="79620-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79620-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79620-125">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="79620-125">-MoveCollectionName</span></span>
<span data-ttu-id="79620-126">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="79620-126">The Move Collection Name.</span></span>

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

### <span data-ttu-id="79620-127">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="79620-127">-MoveResource</span></span>
<span data-ttu-id="79620-128">Beállítja vagy beállítja az erőforrás-azonosítók listáját, alapértelmezés szerint elfogadja az erőforrás-azonosítók áthelyezését, hacsak a beviteli típust a MoveResourceInputType tulajdonságon keresztül nem váltja át.</span><span class="sxs-lookup"><span data-stu-id="79620-128">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="79620-129">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="79620-129">-MoveResourceInputType</span></span>
<span data-ttu-id="79620-130">Az áthelyezési erőforrás beviteli típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="79620-130">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="79620-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="79620-131">-NoWait</span></span>
<span data-ttu-id="79620-132">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="79620-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="79620-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79620-133">-ResourceGroupName</span></span>
<span data-ttu-id="79620-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="79620-134">The Resource Group Name.</span></span>

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

### <span data-ttu-id="79620-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79620-135">-SubscriptionId</span></span>
<span data-ttu-id="79620-136">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="79620-136">The Subscription ID.</span></span>

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

### <span data-ttu-id="79620-137">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="79620-137">-ValidateOnly</span></span>
<span data-ttu-id="79620-138">Beállítja vagy beállítja azt az értéket, amely jelzi, hogy a műveletnek csak előfeltételt kell-e futtatnia.</span><span class="sxs-lookup"><span data-stu-id="79620-138">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="79620-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79620-139">-Confirm</span></span>
<span data-ttu-id="79620-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="79620-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79620-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79620-141">-WhatIf</span></span>
<span data-ttu-id="79620-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="79620-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79620-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79620-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79620-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79620-144">CommonParameters</span></span>
<span data-ttu-id="79620-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79620-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79620-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79620-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79620-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79620-147">INPUTS</span></span>

## <span data-ttu-id="79620-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79620-148">OUTPUTS</span></span>

### <span data-ttu-id="79620-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="79620-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="79620-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79620-150">NOTES</span></span>

<span data-ttu-id="79620-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="79620-151">ALIASES</span></span>

## <span data-ttu-id="79620-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79620-152">RELATED LINKS</span></span>

