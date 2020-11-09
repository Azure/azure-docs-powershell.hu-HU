---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302483"
---
# <span data-ttu-id="3518c-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="3518c-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="3518c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3518c-102">SYNOPSIS</span></span>
<span data-ttu-id="3518c-103">Áthelyezési erőforrás törlése az áthelyezés gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="3518c-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="3518c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3518c-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3518c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3518c-105">DESCRIPTION</span></span>
<span data-ttu-id="3518c-106">Áthelyezési erőforrás törlése az áthelyezés gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="3518c-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="3518c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3518c-107">EXAMPLES</span></span>

### <span data-ttu-id="3518c-108">1. példa: az erőforrás eltávolítása az áthelyezés gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="3518c-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="3518c-109">Az erőforrás eltávolítása az áthelyezés gyűjteményből a megadott előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="3518c-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="3518c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3518c-110">PARAMETERS</span></span>

### <span data-ttu-id="3518c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3518c-111">-AsJob</span></span>
<span data-ttu-id="3518c-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="3518c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3518c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3518c-113">-DefaultProfile</span></span>
<span data-ttu-id="3518c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3518c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3518c-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="3518c-115">-MoveCollectionName</span></span>
<span data-ttu-id="3518c-116">Az áthelyezés gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="3518c-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="3518c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3518c-117">-Name</span></span>
<span data-ttu-id="3518c-118">Az erőforrás nevének áthelyezése</span><span class="sxs-lookup"><span data-stu-id="3518c-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3518c-119">-Várva</span><span class="sxs-lookup"><span data-stu-id="3518c-119">-NoWait</span></span>
<span data-ttu-id="3518c-120">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="3518c-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3518c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3518c-121">-PassThru</span></span>
<span data-ttu-id="3518c-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="3518c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3518c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3518c-123">-ResourceGroupName</span></span>
<span data-ttu-id="3518c-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3518c-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="3518c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3518c-125">-SubscriptionId</span></span>
<span data-ttu-id="3518c-126">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="3518c-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="3518c-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3518c-127">-Confirm</span></span>
<span data-ttu-id="3518c-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3518c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3518c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3518c-129">-WhatIf</span></span>
<span data-ttu-id="3518c-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3518c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3518c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3518c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3518c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3518c-132">CommonParameters</span></span>
<span data-ttu-id="3518c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3518c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3518c-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3518c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3518c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3518c-135">INPUTS</span></span>

## <span data-ttu-id="3518c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3518c-136">OUTPUTS</span></span>

### <span data-ttu-id="3518c-137">Microsoft. Azure. PowerShell. parancsmagok. ResourceMover. modellek. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="3518c-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="3518c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3518c-138">NOTES</span></span>

<span data-ttu-id="3518c-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3518c-139">ALIASES</span></span>

## <span data-ttu-id="3518c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3518c-140">RELATED LINKS</span></span>

