---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: 0f43535baa284dbe9f7c69aee5a688443172089a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000053"
---
# <span data-ttu-id="c3510-101">Az.ResourceMover modul</span><span class="sxs-lookup"><span data-stu-id="c3510-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="c3510-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3510-102">Description</span></span>
<span data-ttu-id="c3510-103">Microsoft Azure PowerShell: ResourceMover parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c3510-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="c3510-104">Az.ResourceMover parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c3510-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="c3510-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="c3510-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="c3510-106">Létrehozza vagy frissíti az áthelyezési erőforrást az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="c3510-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="c3510-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="c3510-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="c3510-108">Beveszi az áthelyezési gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="c3510-108">Gets the move collection.</span></span>

### [<span data-ttu-id="c3510-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="c3510-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="c3510-110">Az Áthelyezési erőforrást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c3510-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="c3510-111">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="c3510-111">Get-AzResourceMoverRequiredForResources</span></span>](Get-AzResourceMoverRequiredForResources.md)
<span data-ttu-id="c3510-112">Azon áthelyezési erőforrások listája, amelyekhez szükséges a felkarerőforrás.</span><span class="sxs-lookup"><span data-stu-id="c3510-112">List of the move resources for which an arm resource is required for.</span></span>

### [<span data-ttu-id="c3510-113">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="c3510-113">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="c3510-114">A nem megoldott függőségek listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c3510-114">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="c3510-115">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="c3510-115">Invoke-AzResourceMoverBulkRemove</span></span>](Invoke-AzResourceMoverBulkRemove.md)
<span data-ttu-id="c3510-116">Eltávolítja a kérelem törzsében szereplő áthelyezési erőforrások készletét az áthelyezési gyűjteményből.</span><span class="sxs-lookup"><span data-stu-id="c3510-116">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="c3510-117">A veretiont szervizelés szerint kell lefektetni.</span><span class="sxs-lookup"><span data-stu-id="c3510-117">The orchestration is done by service.</span></span>
<span data-ttu-id="c3510-118">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="c3510-118">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="c3510-119">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="c3510-119">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="c3510-120">A kérelem törzsében szereplő erőforrások halmazának véglegesítésére.</span><span class="sxs-lookup"><span data-stu-id="c3510-120">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="c3510-121">A véglegesítési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "CommitFailed" műveletben sikeresen befejeződik, és a moveResource moveState áttűnés lekötöttre vált.</span><span class="sxs-lookup"><span data-stu-id="c3510-121">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="c3510-122">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="c3510-122">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="c3510-123">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="c3510-123">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="c3510-124">Elveti a kérelem törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="c3510-124">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="c3510-125">Az elvetési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "DiscardFailed" (Függőben) áthelyezésiForráshelyre vált, és sikeresen befejeződik a MoveResource moveState áttűnés.</span><span class="sxs-lookup"><span data-stu-id="c3510-125">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="c3510-126">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="c3510-126">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="c3510-127">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="c3510-127">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="c3510-128">Áthelyezi a kérelem törzsében szereplő erőforrások készletét.</span><span class="sxs-lookup"><span data-stu-id="c3510-128">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="c3510-129">Az áthelyezési művelet akkor indul el, ha a MoveResources a moveState "MovePending" vagy a "MoveFailed" (ÁthelyezésiFailed) művelettel sikeresen befejeződött, és a MoveResource moveState művelet véglegesítésre vált.</span><span class="sxs-lookup"><span data-stu-id="c3510-129">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="c3510-130">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="c3510-130">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="c3510-131">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="c3510-131">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="c3510-132">A kérés törzsében szereplő erőforrásokra való felkészülést kezdeményezi.</span><span class="sxs-lookup"><span data-stu-id="c3510-132">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="c3510-133">Az előkészítési művelet a "PreparePending" vagy a "PrepareFailed" moveState "PrepareFailed" moveResources műveleten van, és sikeresen befejeződött a moveResource moveState áttűnés a Függőben műveletre.</span><span class="sxs-lookup"><span data-stu-id="c3510-133">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="c3510-134">Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="c3510-134">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="c3510-135">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="c3510-135">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="c3510-136">Áthelyezési gyűjteményt hoz létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="c3510-136">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="c3510-137">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="c3510-137">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="c3510-138">Egy áthelyezési gyűjtemény törlése.</span><span class="sxs-lookup"><span data-stu-id="c3510-138">Deletes a move collection.</span></span>

### [<span data-ttu-id="c3510-139">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="c3510-139">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="c3510-140">Erőforrás áthelyezése az áthelyezési gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="c3510-140">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="c3510-141">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="c3510-141">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="c3510-142">Kiszámítja, feloldja és ellenőrzi a moveResources függéseket az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="c3510-142">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

