---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181948"
---
# Az. ResourceMover modul
## Leírás
Microsoft Azure PowerShell: ResourceMover parancsmagok

## Az. ResourceMover parancsmagok
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Áthelyezési erőforrás létrehozása vagy frissítése az áthelyezési gyűjteményben.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Megkapja az áthelyezés gyűjteményt.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Az áthelyezés erőforrást kapja.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
A feloldatlan függőségek listáját kapja.

### [Meghívó-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Véglegesíti a kérés törzsében szereplő erőforrásokat.
A véglegesítési művelet az "CommitPending" vagy a "CommitFailed" moveState moveResources lép fel, és a sikeres Befejezés érdekében a moveResource moveState az áttűnést végrehajtja.
Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.

### [Meghívó-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Elveti a kérés törzsében szereplő erőforrásokat.
Az elvetési művelet az "CommitPending" vagy a "DiscardFailed" moveState moveResources vált, és a sikeres Befejezés érdekében a moveResource moveState MovePending.
Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.

### [Meghívó-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Áthelyezi az erőforrások készletét a kérés törzsébe.
Az áthelyezési művelet akkor indul el, ha a moveResources a moveState "MovePending" vagy a "MoveFailed" van, és a sikeres Befejezés érdekében a moveResource moveState átvált a CommitPending.
Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.

### [Meghívó-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Előkészületeket kezdeményez a kérés törzsében található erőforrások készletére.
Az előkészítési művelet a "PreparePending" vagy a "PrepareFailed" moveState található moveResources, és a sikeres Befejezés érdekében a moveResource moveState MovePending áttűnést hajt végre a.
Ha támogatást szeretne a felhasználónak az előfeltételhez, az ügyfél felhívhatja a műveletet a validateOnly tulajdonság értéke True értékre.

### [Új – AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Áthelyezési gyűjtemény létrehozása vagy frissítése

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Az áthelyezési gyűjtemény törlése

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Áthelyezési erőforrás törlése az áthelyezés gyűjteményből

### [Feloldás – AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Az áthelyezés gyűjteményben lévő moveResources függőségeinek kiszámítása és érvényesítése.

