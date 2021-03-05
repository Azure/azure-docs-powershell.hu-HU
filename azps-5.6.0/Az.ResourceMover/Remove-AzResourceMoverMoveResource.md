---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: fc146f4d7581db84b79df82055faf2cdd8b000e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999861"
---
# <span data-ttu-id="69f04-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="69f04-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="69f04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69f04-102">SYNOPSIS</span></span>
<span data-ttu-id="69f04-103">Erőforrás áthelyezése az áthelyezési gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="69f04-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="69f04-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69f04-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="69f04-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69f04-105">DESCRIPTION</span></span>
<span data-ttu-id="69f04-106">Erőforrás áthelyezése az áthelyezési gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="69f04-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="69f04-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69f04-107">EXAMPLES</span></span>

### <span data-ttu-id="69f04-108">1. példa: Egy Áthelyezési rresource eltávolítása az áthelyezési gyűjteményből.</span><span class="sxs-lookup"><span data-stu-id="69f04-108">Example 1: Remove one Move Rresource from the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -Name "psdemorm-vnet"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:08:49 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/bee69758-c7cb-4160-b3e0-8e4b69ec3731
Message        : 
Name           : bee69758-c7cb-4160-b3e0-8e4b69ec3731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:08:47 PM
Status         : Succeeded

```

<span data-ttu-id="69f04-109">Távolítsa el az Egyik Áthelyezés rresource-t az Áthelyezési gyűjteményből.</span><span class="sxs-lookup"><span data-stu-id="69f04-109">Remove one Move Rresource from the Move Collection.</span></span>

## <span data-ttu-id="69f04-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69f04-110">PARAMETERS</span></span>

### <span data-ttu-id="69f04-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69f04-111">-AsJob</span></span>
<span data-ttu-id="69f04-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="69f04-112">Run the command as a job</span></span>

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

### <span data-ttu-id="69f04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f04-113">-DefaultProfile</span></span>
<span data-ttu-id="69f04-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69f04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69f04-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="69f04-115">-MoveCollectionName</span></span>
<span data-ttu-id="69f04-116">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="69f04-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="69f04-117">-Name</span><span class="sxs-lookup"><span data-stu-id="69f04-117">-Name</span></span>
<span data-ttu-id="69f04-118">Az Erőforrás neve áthelyezése</span><span class="sxs-lookup"><span data-stu-id="69f04-118">The Move Resource Name.</span></span>

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

### <span data-ttu-id="69f04-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="69f04-119">-NoWait</span></span>
<span data-ttu-id="69f04-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="69f04-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69f04-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69f04-121">-PassThru</span></span>
<span data-ttu-id="69f04-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="69f04-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="69f04-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69f04-123">-ResourceGroupName</span></span>
<span data-ttu-id="69f04-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="69f04-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="69f04-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69f04-125">-SubscriptionId</span></span>
<span data-ttu-id="69f04-126">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="69f04-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="69f04-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69f04-127">-Confirm</span></span>
<span data-ttu-id="69f04-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="69f04-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69f04-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69f04-129">-WhatIf</span></span>
<span data-ttu-id="69f04-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="69f04-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69f04-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69f04-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69f04-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f04-132">CommonParameters</span></span>
<span data-ttu-id="69f04-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f04-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f04-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69f04-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f04-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69f04-135">INPUTS</span></span>

## <span data-ttu-id="69f04-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69f04-136">OUTPUTS</span></span>

### <span data-ttu-id="69f04-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="69f04-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="69f04-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69f04-138">NOTES</span></span>

<span data-ttu-id="69f04-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="69f04-139">ALIASES</span></span>

## <span data-ttu-id="69f04-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69f04-140">RELATED LINKS</span></span>

