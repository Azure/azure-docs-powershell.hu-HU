---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181241"
---
# Az. support modul
## Leírás
Az ebben a szakaszban szereplő témakörök az Azure PowerShell-parancsmagok segítségével hozhatják létre és kezelhetik az Azure ügyfélszolgálati jegyeit az Azure Resource Manager (ARM) keretrendszerben. A parancsmagok a Microsoft. Azure. commands. support névtérben találhatók.

## Az. támogatási parancsmagok
### [Get-AzSupportService](Get-AzSupportService.md)
Beolvassa az Azure Services jelenlegi listáját, amelyhez támogatás érhető el. Minden Azure-szolgáltatáshoz tartozik saját kategóriák a probléma besorolásához. Bemutatjuk a szolgáltatás problémás besorolásának aktuális listáját a Get-AzSupportProblemClassification segítségével. A szolgáltatás és a probléma besorolása GLOBÁLISan új támogatási jegyet hozhat létre a New-AzSupportTicket segítségével.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Beolvassa az Azure-szolgáltatás problémás besorolásának aktuális listáját. A szolgáltatás és a probléma besorolása GLOBÁLISan új támogatási jegyet hozhat létre a New-AzSupportTicket segítségével. 

### [Új – AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Segéd-parancsmag a támogatási partnercsoport-objektum létrehozásához. Ezt az objektumot használhatja New-AzSupportTicket parancsmaghoz.

### [Új – AzSupportTicket](New-AzSupportTicket.md)
Új Azure támogatási jegyet hoz létre. Ezt a műveletet az Azure [új támogatási kérés lapjának](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)viselkedése alapján modellezjük.

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
A támogatási jegyek listáját kapja. Teljes támogatási jegyet kaphat a menetjegyek nevével, vagy szűrheti a támogatási jegyeket az *állapot* vagy a *CreatedDate* alapján.

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Frissítse a támogatási jegy súlyosságát, állapotát vagy az ügyfél elérhetőségét.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Kommunikációt kap a támogatási jegyekhez. A támogatási menetjegy-kommunikációt *CreatedDate*   vagy *CommunicationType* is szűrheti. 

### [Új – AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Új ügyfél-kommunikációt ad az Azure támogatási jegyéhez. 



