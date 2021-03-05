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

### [Get-AzResourceMoverRequiredForResources](Get-AzResourceMoverRequiredForResources.md)
Azon áthelyezési erőforrások listája, amelyekhez szükséges a felkarerőforrás.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
A nem megoldott függőségek listáját tartalmazza.

### [Invoke-AzResourceMoverBulkRemove](Invoke-AzResourceMoverBulkRemove.md)
Eltávolítja a kérelem törzsében szereplő áthelyezési erőforrások készletét az áthelyezési gyűjteményből.
A veretiont szervizelés szerint kell lefektetni.
Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
A kérelem törzsében szereplő erőforrások halmazának véglegesítésére.
A véglegesítési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "CommitFailed" műveletben sikeresen befejeződik, és a moveResource moveState áttűnés lekötöttre vált.
Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Elveti a kérelem törzsében szereplő erőforrásokat.
Az elvetési művelet akkor indul el, amikor a moveResources a moveState "CommitPending" vagy a "DiscardFailed" (Függőben) áthelyezésiForráshelyre vált, és sikeresen befejeződik a MoveResource moveState áttűnés.
Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Áthelyezi a kérelem törzsében szereplő erőforrások készletét.
Az áthelyezési művelet akkor indul el, ha a MoveResources a moveState "MovePending" vagy a "MoveFailed" (ÁthelyezésiFailed) művelettel sikeresen befejeződött, és a MoveResource moveState művelet véglegesítésre vált.
Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
A kérés törzsében szereplő erőforrásokra való felkészülést kezdeményezi.
Az előkészítési művelet a "PreparePending" vagy a "PrepareFailed" moveState "PrepareFailed" moveResources műveleten van, és sikeresen befejeződött a moveResource moveState áttűnés a Függőben műveletre.
Annak érdekében, hogy az ügyfél előfeltételként segítséget nyújt a felhasználónak a művelet végrehajtásához, a validateOnly tulajdonság igazra van állítva.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Áthelyezési gyűjteményt hoz létre vagy frissíti.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Egy áthelyezési gyűjtemény törlése.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Erőforrás áthelyezése az áthelyezési gyűjteményből

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Kiszámítja, feloldja és ellenőrzi a moveResources függéseket az áthelyezési gyűjteményben.

