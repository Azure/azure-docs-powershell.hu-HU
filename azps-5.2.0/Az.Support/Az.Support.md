---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349085"
---
# <span data-ttu-id="b8bfe-101">Az.Support Module</span><span class="sxs-lookup"><span data-stu-id="b8bfe-101">Az.Support Module</span></span>
## <span data-ttu-id="b8bfe-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8bfe-102">Description</span></span>
<span data-ttu-id="b8bfe-103">A szakasz témakörei azure PowerShell-parancsmagokat tartalmaznak az Azure Resource Manager (ARM) keretrendszerében az Azure támogatási jegyei létrehozásához és kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="b8bfe-104">A parancsmagok a Microsoft.Azure.Commands.Support névterében létezik</span><span class="sxs-lookup"><span data-stu-id="b8bfe-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="b8bfe-105">Az.Support parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b8bfe-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="b8bfe-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="b8bfe-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="b8bfe-107">Azon Azure-szolgáltatások aktuális listáját tartalmazza, amelyekhez elérhető a támogatás.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="b8bfe-108">Mindegyik Azure-szolgáltatás saját kategóriákkal, úgynevezett problémabesorolással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="b8bfe-109">A Szolgáltatás problémabesorolásának aktuális listája a Get-AzSupportProblemClassification segítségével.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="b8bfe-110">A szolgáltatás- és problémabesorolás GUID azonosítóját használva létrehozhat egy új támogatási jegyet a New-AzSupportTicket használatával.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="b8bfe-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="b8bfe-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="b8bfe-112">Egy Azure-szolgáltatás problémabesorolásának aktuális listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="b8bfe-113">A szolgáltatás- és problémabesorolás GUID azonosítóját használva létrehozhat egy új támogatási jegyet a New-AzSupportTicket használatával.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="b8bfe-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="b8bfe-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="b8bfe-115">Támogatási kapcsolatprofil-objektum létrehozásához szükséges súgó parancsmag.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="b8bfe-116">Ezt az objektumot használhatja New-AzSupportTicket parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="b8bfe-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="b8bfe-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="b8bfe-118">Létrehoz egy új Azure támogatási jegyet.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="b8bfe-119">Ezt a műveletet az Azure Új támogatási kérelem lap viselkedése [alapján modelleljuk.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)</span><span class="sxs-lookup"><span data-stu-id="b8bfe-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="b8bfe-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="b8bfe-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="b8bfe-121">A támogatási jegylista lekérte.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-121">Gets the list of support tickets.</span></span> <span data-ttu-id="b8bfe-122">A támogatási jegy teljes adatait a jegy neve alapján kaphatja meg, vagy szűrheti a támogatási jegyeket *az Állapot* vagy a *CreatedDate szerint.*</span><span class="sxs-lookup"><span data-stu-id="b8bfe-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="b8bfe-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="b8bfe-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="b8bfe-124">Frissítheti egy támogatási jegy súlyossági állapotát, állapotát vagy az ügyfél kapcsolatfelvételi adatait.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="b8bfe-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="b8bfe-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="b8bfe-126">Egy támogatási jegy kommunikációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="b8bfe-127">A támogatási jegykommunikációt a *CreatedDate* vagy a CommunicationType segítségével is *szűrheti.*</span><span class="sxs-lookup"><span data-stu-id="b8bfe-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="b8bfe-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="b8bfe-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="b8bfe-129">Új ügyfélkommunikációt ad hozzá egy Azure támogatási jegyhez.</span><span class="sxs-lookup"><span data-stu-id="b8bfe-129">Adds a new customer communication to an Azure support ticket.</span></span> 



