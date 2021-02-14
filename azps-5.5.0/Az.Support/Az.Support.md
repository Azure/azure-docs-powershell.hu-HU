---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150075"
---
# Az.Support Module
## Leírás
A szakasz témakörei azure PowerShell-parancsmagokat tartalmaznak az Azure Resource Manager (ARM) keretrendszerében az Azure támogatási jegyei létrehozásához és kezeléséhez. A parancsmagok a Microsoft.Azure.Commands.Support névterében létezik

## Az.Support parancsmagok
### [Get-AzSupportService](Get-AzSupportService.md)
Azon Azure-szolgáltatások aktuális listáját tartalmazza, amelyekhez elérhető a támogatás. Mindegyik Azure-szolgáltatás saját kategóriákkal, úgynevezett problémabesorolással rendelkezik. A Szolgáltatás problémabesorolásának aktuális listája a Get-AzSupportProblemClassification segítségével. A szolgáltatás- és problémabesorolás GUID azonosítóját használva létrehozhat egy új támogatási jegyet a New-AzSupportTicket használatával.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Egy Azure-szolgáltatás problémabesorolásának aktuális listáját tartalmazza. A szolgáltatás- és problémabesorolás GUID azonosítóját használva létrehozhat egy új támogatási jegyet a New-AzSupportTicket használatával. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Támogatási kapcsolatprofil-objektum létrehozásához szükséges súgó parancsmag. Ezt az objektumot használhatja New-AzSupportTicket parancsmaghoz.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Létrehoz egy új Azure támogatási jegyet. Ezt a műveletet az Azure Új támogatási kérelem lap viselkedése [alapján modelleljuk.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
A támogatási jegylista lekérte. A támogatási jegy teljes adatait a jegy neve alapján kaphatja meg, vagy szűrheti a támogatási jegyeket *az Állapot* vagy a *CreatedDate szerint.*

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Frissítheti egy támogatási jegy súlyossági állapotát, állapotát vagy az ügyfél kapcsolatfelvételi adatait.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Egy támogatási jegy kommunikációját kapja meg. A támogatási jegykommunikációt a *CreatedDate* vagy a CommunicationType segítségével is *szűrheti.* 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Új ügyfélkommunikációt ad hozzá egy Azure támogatási jegyhez. 



