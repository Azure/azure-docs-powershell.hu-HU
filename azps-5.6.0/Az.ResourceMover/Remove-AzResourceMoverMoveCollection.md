---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: aa34a094631441c1ee13418d4d40306715c934b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999878"
---
# <span data-ttu-id="224f1-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="224f1-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="224f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="224f1-102">SYNOPSIS</span></span>
<span data-ttu-id="224f1-103">Egy áthelyezési gyűjtemény törlése.</span><span class="sxs-lookup"><span data-stu-id="224f1-103">Deletes a move collection.</span></span>

## <span data-ttu-id="224f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="224f1-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="224f1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="224f1-105">DESCRIPTION</span></span>
<span data-ttu-id="224f1-106">Egy áthelyezési gyűjtemény törlése.</span><span class="sxs-lookup"><span data-stu-id="224f1-106">Deletes a move collection.</span></span>

## <span data-ttu-id="224f1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="224f1-107">EXAMPLES</span></span>

### <span data-ttu-id="224f1-108">1. példa: Az Áthelyezési gyűjtemény eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="224f1-108">Example 1: Remove the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/ec788761-2f1b-46a2-97b7-f5056afd334d
Message        : 
Name           : 
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 
Status         : Succeeded
```

<span data-ttu-id="224f1-109">Távolítsa el az áthelyezési gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="224f1-109">Remove the Move Collection.</span></span>

## <span data-ttu-id="224f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="224f1-110">PARAMETERS</span></span>

### <span data-ttu-id="224f1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="224f1-111">-AsJob</span></span>
<span data-ttu-id="224f1-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="224f1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="224f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="224f1-113">-DefaultProfile</span></span>
<span data-ttu-id="224f1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="224f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="224f1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="224f1-115">-Name</span></span>
<span data-ttu-id="224f1-116">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="224f1-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="224f1-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="224f1-117">-NoWait</span></span>
<span data-ttu-id="224f1-118">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="224f1-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="224f1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="224f1-119">-PassThru</span></span>
<span data-ttu-id="224f1-120">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="224f1-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="224f1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="224f1-121">-ResourceGroupName</span></span>
<span data-ttu-id="224f1-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="224f1-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="224f1-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="224f1-123">-SubscriptionId</span></span>
<span data-ttu-id="224f1-124">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="224f1-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="224f1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="224f1-125">-Confirm</span></span>
<span data-ttu-id="224f1-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="224f1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="224f1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="224f1-127">-WhatIf</span></span>
<span data-ttu-id="224f1-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="224f1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="224f1-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="224f1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="224f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224f1-130">CommonParameters</span></span>
<span data-ttu-id="224f1-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="224f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224f1-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="224f1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224f1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="224f1-133">INPUTS</span></span>

## <span data-ttu-id="224f1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="224f1-134">OUTPUTS</span></span>

### <span data-ttu-id="224f1-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="224f1-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="224f1-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="224f1-136">NOTES</span></span>

<span data-ttu-id="224f1-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="224f1-137">ALIASES</span></span>

## <span data-ttu-id="224f1-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="224f1-138">RELATED LINKS</span></span>

