---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187548"
---
# <span data-ttu-id="abcdc-101">Az. ResourceMover modul</span><span class="sxs-lookup"><span data-stu-id="abcdc-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="abcdc-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="abcdc-102">Description</span></span>
<span data-ttu-id="abcdc-103">Microsoft Azure PowerShell: ResourceMover parancsmagok</span><span class="sxs-lookup"><span data-stu-id="abcdc-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="abcdc-104">Az. ResourceMover parancsmagok</span><span class="sxs-lookup"><span data-stu-id="abcdc-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="abcdc-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="abcdc-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="abcdc-106">Áthelyezési erőforrás létrehozása vagy frissítése az áthelyezési gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="abcdc-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="abcdc-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="abcdc-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="abcdc-108">Megkapja az áthelyezés gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="abcdc-108">Gets the move collection.</span></span>

### [<span data-ttu-id="abcdc-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="abcdc-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="abcdc-110">Az áthelyezés erőforrást kapja.</span><span class="sxs-lookup"><span data-stu-id="abcdc-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="abcdc-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="abcdc-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="abcdc-112">A feloldatlan függőségek listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="abcdc-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="abcdc-113">Meghívó-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="abcdc-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="abcdc-114">Véglegesíti a kérés törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="abcdc-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="abcdc-115">A véglegesítési művelet az "CommitPending" vagy a "CommitFailed" moveState moveResources lép fel, és a sikeres Befejezés érdekében a moveResource moveState az áttűnést végrehajtja.</span><span class="sxs-lookup"><span data-stu-id="abcdc-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="abcdc-116">Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.</span><span class="sxs-lookup"><span data-stu-id="abcdc-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="abcdc-117">Meghívó-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="abcdc-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="abcdc-118">Elveti a kérés törzsében szereplő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="abcdc-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="abcdc-119">Az elvetési művelet az "CommitPending" vagy a "DiscardFailed" moveState moveResources vált, és a sikeres Befejezés érdekében a moveResource moveState MovePending.</span><span class="sxs-lookup"><span data-stu-id="abcdc-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="abcdc-120">Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.</span><span class="sxs-lookup"><span data-stu-id="abcdc-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="abcdc-121">Meghívó-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="abcdc-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="abcdc-122">Áthelyezi az erőforrások készletét a kérés törzsébe.</span><span class="sxs-lookup"><span data-stu-id="abcdc-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="abcdc-123">Az áthelyezési művelet akkor indul el, ha a moveResources a moveState "MovePending" vagy a "MoveFailed" van, és a sikeres Befejezés érdekében a moveResource moveState átvált a CommitPending.</span><span class="sxs-lookup"><span data-stu-id="abcdc-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="abcdc-124">Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.</span><span class="sxs-lookup"><span data-stu-id="abcdc-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="abcdc-125">Meghívó-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="abcdc-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="abcdc-126">Előkészületeket kezdeményez a kérés törzsében található erőforrások készletére.</span><span class="sxs-lookup"><span data-stu-id="abcdc-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="abcdc-127">Az előkészítési művelet a "PreparePending" vagy a "PrepareFailed" moveState található moveResources, és a sikeres Befejezés érdekében a moveResource moveState MovePending áttűnést hajt végre a.</span><span class="sxs-lookup"><span data-stu-id="abcdc-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="abcdc-128">Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.</span><span class="sxs-lookup"><span data-stu-id="abcdc-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="abcdc-129">Új – AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="abcdc-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="abcdc-130">Áthelyezési gyűjtemény létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="abcdc-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="abcdc-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="abcdc-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="abcdc-132">Az áthelyezési gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="abcdc-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="abcdc-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="abcdc-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="abcdc-134">Áthelyezési erőforrás törlése az áthelyezés gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="abcdc-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="abcdc-135">Feloldás – AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="abcdc-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="abcdc-136">Az áthelyezés gyűjteményben lévő moveResources függőségeinek kiszámítása és érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="abcdc-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

