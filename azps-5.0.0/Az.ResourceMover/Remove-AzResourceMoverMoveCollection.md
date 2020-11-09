---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302486"
---
# <span data-ttu-id="b3ce7-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="b3ce7-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="b3ce7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ce7-103">Az áthelyezési gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="b3ce7-103">Deletes a move collection.</span></span>

## <span data-ttu-id="b3ce7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3ce7-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3ce7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="b3ce7-106">Az áthelyezési gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="b3ce7-106">Deletes a move collection.</span></span>

## <span data-ttu-id="b3ce7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b3ce7-107">EXAMPLES</span></span>

### <span data-ttu-id="b3ce7-108">1. példa: az áthelyezési gyűjtemény eltávolítása a megadott előfizetésből</span><span class="sxs-lookup"><span data-stu-id="b3ce7-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/12/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                    ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866d6
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/12/2020 3:27:27 PM
    Status         : Succeeded
```

<span data-ttu-id="b3ce7-109">Az áthelyezési gyűjtemény eltávolítása a megadott előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="b3ce7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3ce7-110">PARAMETERS</span></span>

### <span data-ttu-id="b3ce7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3ce7-111">-AsJob</span></span>
<span data-ttu-id="b3ce7-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="b3ce7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b3ce7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ce7-113">-DefaultProfile</span></span>
<span data-ttu-id="b3ce7-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3ce7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b3ce7-115">-Name</span></span>
<span data-ttu-id="b3ce7-116">Az áthelyezés gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="b3ce7-117">-Várva</span><span class="sxs-lookup"><span data-stu-id="b3ce7-117">-NoWait</span></span>
<span data-ttu-id="b3ce7-118">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="b3ce7-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b3ce7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3ce7-119">-PassThru</span></span>
<span data-ttu-id="b3ce7-120">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="b3ce7-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b3ce7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ce7-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3ce7-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="b3ce7-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3ce7-123">-SubscriptionId</span></span>
<span data-ttu-id="b3ce7-124">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="b3ce7-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b3ce7-125">-Confirm</span></span>
<span data-ttu-id="b3ce7-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3ce7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ce7-127">-WhatIf</span></span>
<span data-ttu-id="b3ce7-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ce7-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3ce7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ce7-130">CommonParameters</span></span>
<span data-ttu-id="b3ce7-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3ce7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ce7-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ce7-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3ce7-133">INPUTS</span></span>

## <span data-ttu-id="b3ce7-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3ce7-134">OUTPUTS</span></span>

### <span data-ttu-id="b3ce7-135">Microsoft. Azure. PowerShell. parancsmagok. ResourceMover. modellek. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="b3ce7-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="b3ce7-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3ce7-136">NOTES</span></span>

<span data-ttu-id="b3ce7-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b3ce7-137">ALIASES</span></span>

## <span data-ttu-id="b3ce7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3ce7-138">RELATED LINKS</span></span>

