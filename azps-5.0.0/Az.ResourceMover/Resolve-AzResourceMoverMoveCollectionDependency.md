---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187546"
---
# <span data-ttu-id="9e73e-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="9e73e-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="9e73e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e73e-102">SYNOPSIS</span></span>
<span data-ttu-id="9e73e-103">Az áthelyezés gyűjteményben lévő moveResources függőségeinek kiszámítása és érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="9e73e-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="9e73e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e73e-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9e73e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e73e-105">DESCRIPTION</span></span>
<span data-ttu-id="9e73e-106">Az áthelyezés gyűjteményben lévő moveResources függőségeinek kiszámítása és érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="9e73e-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="9e73e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e73e-107">EXAMPLES</span></span>

### <span data-ttu-id="9e73e-108">1. példa: kiszámítja, megoldja és validálja a moveresources az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="9e73e-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
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

<span data-ttu-id="9e73e-109">Az áthelyezés gyűjteményben lévő moveresources függőségeinek kiszámítása és érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="9e73e-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="9e73e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e73e-110">PARAMETERS</span></span>

### <span data-ttu-id="9e73e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e73e-111">-AsJob</span></span>
<span data-ttu-id="9e73e-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="9e73e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9e73e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e73e-113">-DefaultProfile</span></span>
<span data-ttu-id="9e73e-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e73e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e73e-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="9e73e-115">-MoveCollectionName</span></span>
<span data-ttu-id="9e73e-116">Az áthelyezés gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="9e73e-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="9e73e-117">-Várva</span><span class="sxs-lookup"><span data-stu-id="9e73e-117">-NoWait</span></span>
<span data-ttu-id="9e73e-118">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="9e73e-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9e73e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e73e-119">-ResourceGroupName</span></span>
<span data-ttu-id="9e73e-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9e73e-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="9e73e-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e73e-121">-SubscriptionId</span></span>
<span data-ttu-id="9e73e-122">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="9e73e-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="9e73e-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9e73e-123">-Confirm</span></span>
<span data-ttu-id="9e73e-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e73e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e73e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e73e-125">-WhatIf</span></span>
<span data-ttu-id="9e73e-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9e73e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e73e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e73e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e73e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e73e-128">CommonParameters</span></span>
<span data-ttu-id="9e73e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e73e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e73e-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9e73e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e73e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e73e-131">INPUTS</span></span>

## <span data-ttu-id="9e73e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e73e-132">OUTPUTS</span></span>

### <span data-ttu-id="9e73e-133">Microsoft. Azure. PowerShell. parancsmagok. ResourceMover. modellek. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="9e73e-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="9e73e-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e73e-134">NOTES</span></span>

<span data-ttu-id="9e73e-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9e73e-135">ALIASES</span></span>

## <span data-ttu-id="9e73e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e73e-136">RELATED LINKS</span></span>

