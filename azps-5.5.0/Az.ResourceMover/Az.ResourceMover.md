---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208550"
---
# Az.ResourceMover modul
## Leírás
Microsoft Azure PowerShell: ResourceMover parancsmagok

## Az.ResourceMover parancsmagok
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Létrehozza vagy frissíti az áthelyezési erőforrást az áthelyezési gyűjteményben.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Beveszi az áthelyezési gyűjteményt.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Az Áthelyezési erőforrást kapja meg.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
A nem megoldott függőségek listáját tartalmazza.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
A kérés törzsében szereplő erőforrások halmazának véglegesítésére.
A véglegesítési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "CommitFailed" műveletben sikeresen befejeződik, és a moveResource moveState áttűnés lekötöttre vált.
Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak ahhoz a művelethez, amely a validateOnly tulajdonság igazra van állítva.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Elveti a kérelem törzsében szereplő erőforrásokat.
Az elvetési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "DiscardFailed" (Függőben) áthelyezésiForráshelyre vált, és sikeresen befejeződik a MoveResource moveState művelet, amely áttűnés függőben van.
Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak ahhoz a művelethez, amely a validateOnly tulajdonság igazra van állítva.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Áthelyezi a kérelem törzsében szereplő erőforrásokat.
Az áthelyezési művelet akkor indul el, ha a moveResources a moveState "MovePending" vagy a "MoveFailed" (ÁthelyezésiFailed) műveletben van, és a moveResource moveState művelet véglegesítésre vált.
Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak ahhoz a művelethez, amely a validateOnly tulajdonság igazra van állítva.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
A kérés törzsében szereplő erőforrásokra való felkészülést kezdeményezi.
Az előkészítési művelet a "PreparePending" vagy a "PrepareFailed" moveState "PrepareFailed" mozgatóforráson van, és sikeresen befejeződik a moveResource moveState áttűnés a Függőben műveletre.
Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak ahhoz a művelethez, amely a validateOnly tulajdonság igazra van állítva.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Áthelyezési gyűjteményt hoz létre vagy frissíti.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Egy áthelyezési gyűjtemény törlése.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Erőforrás áthelyezése az áthelyezési gyűjteményből

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Kiszámítja, feloldja és ellenőrzi a moveResources függéseket az áthelyezési gyűjteményben.

