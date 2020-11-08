---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183347"
---
# <span data-ttu-id="dc15d-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="dc15d-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="dc15d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc15d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc15d-103">Az áthelyezés gyűjteményben lévő moveResources függőségeinek kiszámítása és érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="dc15d-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="dc15d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc15d-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dc15d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc15d-105">DESCRIPTION</span></span>
<span data-ttu-id="dc15d-106">Az áthelyezés gyűjteményben lévő moveResources függőségeinek kiszámítása és érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="dc15d-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="dc15d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dc15d-107">EXAMPLES</span></span>

### <span data-ttu-id="dc15d-108">1. példa: kiszámítja, megoldja és validálja a moveresources az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="dc15d-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 8/16/2020 2:28:18 PM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveCollections/PS-ce
                 ntralus-westcentralus-demoRM/operations/bce85a10-1ff3-4815-a677-7b188f7b441a
Message        : The resolve dependencies operation of one ore more resources has failed. Check the move status of the resource for more details. 
Possible Causes: The resolve dependencies operation of one ore more resources has failed.
Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : bce85a10-1ff3-4815-a677-7b188f7b441a
Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/16/2020 2:28:16 PM
Status         : Succeeded
```

<span data-ttu-id="dc15d-109">Az áthelyezés gyűjteményben lévő moveresources függőségeinek kiszámítása és érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="dc15d-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="dc15d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc15d-110">PARAMETERS</span></span>

### <span data-ttu-id="dc15d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc15d-111">-AsJob</span></span>
<span data-ttu-id="dc15d-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="dc15d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="dc15d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc15d-113">-DefaultProfile</span></span>
<span data-ttu-id="dc15d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc15d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc15d-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="dc15d-115">-MoveCollectionName</span></span>
<span data-ttu-id="dc15d-116">Az áthelyezés gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="dc15d-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="dc15d-117">-Várva</span><span class="sxs-lookup"><span data-stu-id="dc15d-117">-NoWait</span></span>
<span data-ttu-id="dc15d-118">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="dc15d-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dc15d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc15d-119">-ResourceGroupName</span></span>
<span data-ttu-id="dc15d-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="dc15d-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="dc15d-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc15d-121">-SubscriptionId</span></span>
<span data-ttu-id="dc15d-122">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="dc15d-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="dc15d-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dc15d-123">-Confirm</span></span>
<span data-ttu-id="dc15d-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc15d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc15d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc15d-125">-WhatIf</span></span>
<span data-ttu-id="dc15d-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dc15d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc15d-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc15d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc15d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc15d-128">CommonParameters</span></span>
<span data-ttu-id="dc15d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc15d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc15d-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dc15d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc15d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc15d-131">INPUTS</span></span>

## <span data-ttu-id="dc15d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc15d-132">OUTPUTS</span></span>

### <span data-ttu-id="dc15d-133">Microsoft. Azure. PowerShell. parancsmagok. ResourceMover. modellek. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="dc15d-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="dc15d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc15d-134">NOTES</span></span>

<span data-ttu-id="dc15d-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dc15d-135">ALIASES</span></span>

## <span data-ttu-id="dc15d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc15d-136">RELATED LINKS</span></span>

