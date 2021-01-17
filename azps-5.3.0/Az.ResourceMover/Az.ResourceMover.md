---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377886"
---
# <span data-ttu-id="0acda-101">Az.ResourceMover modul</span><span class="sxs-lookup"><span data-stu-id="0acda-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="0acda-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="0acda-102">Description</span></span>
<span data-ttu-id="0acda-103">Microsoft Azure PowerShell: ResourceMover parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0acda-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="0acda-104">Az.ResourceMover parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0acda-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="0acda-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="0acda-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="0acda-106">Létrehozza vagy frissíti az áthelyezési erőforrást az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="0acda-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="0acda-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="0acda-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="0acda-108">Beveszi az áthelyezési gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="0acda-108">Gets the move collection.</span></span>

### [<span data-ttu-id="0acda-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="0acda-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="0acda-110">Az Áthelyezési erőforrást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0acda-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="0acda-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="0acda-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="0acda-112">A nem megoldott függőségek listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0acda-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="0acda-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="0acda-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="0acda-114">A kérelem törzsében szereplő erőforrások halmazának véglegesítésére.</span><span class="sxs-lookup"><span data-stu-id="0acda-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="0acda-115">A véglegesítési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "CommitFailed" műveletben sikeresen befejeződik, és a moveResource moveState áttűnés lekötöttre vált.</span><span class="sxs-lookup"><span data-stu-id="0acda-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="0acda-116">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak ahhoz a művelethez, amely a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="0acda-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="0acda-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="0acda-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="0acda-118">Elveti a kérelem törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="0acda-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="0acda-119">Az elvetési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "DiscardFailed" (Függőben) áthelyezésiForráshelyre vált, és sikeresen befejeződik a moveResource moveState áttűnés a Függőben műveletre.</span><span class="sxs-lookup"><span data-stu-id="0acda-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="0acda-120">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak ahhoz a művelethez, amely a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="0acda-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="0acda-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="0acda-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="0acda-122">Áthelyezi a kérelem törzsében szereplő erőforrások készletét.</span><span class="sxs-lookup"><span data-stu-id="0acda-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="0acda-123">Az áthelyezési művelet akkor indul el, ha a MoveResources a moveState "MovePending" vagy a "MoveFailed" (ÁthelyezésiFailed) művelettel sikeresen befejeződött, és a MoveResource moveState művelet véglegesítésre vált.</span><span class="sxs-lookup"><span data-stu-id="0acda-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="0acda-124">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak ahhoz a művelethez, amely a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="0acda-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="0acda-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="0acda-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="0acda-126">A kérés törzsében szereplő erőforrásokra való felkészülést kezdeményezi.</span><span class="sxs-lookup"><span data-stu-id="0acda-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="0acda-127">Az előkészítési művelet a "PreparePending" vagy a "PrepareFailed" moveState "PrepareFailed" mozgatóforráson van, és sikeresen befejeződik a moveResource moveState áttűnés a Függőben műveletre.</span><span class="sxs-lookup"><span data-stu-id="0acda-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="0acda-128">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak ahhoz a művelethez, amely a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="0acda-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="0acda-129">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="0acda-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="0acda-130">Áthelyezési gyűjteményt hoz létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="0acda-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="0acda-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="0acda-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="0acda-132">Egy áthelyezési gyűjtemény törlése.</span><span class="sxs-lookup"><span data-stu-id="0acda-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="0acda-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="0acda-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="0acda-134">Törli az áthelyezési erőforrást az áthelyezési gyűjteményből.</span><span class="sxs-lookup"><span data-stu-id="0acda-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="0acda-135">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="0acda-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="0acda-136">Kiszámítja, feloldja és ellenőrzi a moveResources függéseket az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="0acda-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

