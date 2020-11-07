---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846341"
---
# <span data-ttu-id="c2c2e-101">Az. support modul</span><span class="sxs-lookup"><span data-stu-id="c2c2e-101">Az.Support Module</span></span>
## <span data-ttu-id="c2c2e-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2c2e-102">Description</span></span>
<span data-ttu-id="c2c2e-103">Az ebben a szakaszban szereplő témakörök az Azure PowerShell-parancsmagok segítségével hozhatják létre és kezelhetik az Azure ügyfélszolgálati jegyeit az Azure Resource Manager (ARM) keretrendszerben.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="c2c2e-104">A parancsmagok a Microsoft. Azure. commands. support névtérben találhatók.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="c2c2e-105">Az. támogatási parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c2c2e-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="c2c2e-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="c2c2e-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="c2c2e-107">Beolvassa az Azure Services jelenlegi listáját, amelyhez támogatás érhető el.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="c2c2e-108">Minden Azure-szolgáltatáshoz tartozik saját kategóriák a probléma besorolásához.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="c2c2e-109">Bemutatjuk a szolgáltatás problémás besorolásának aktuális listáját a Get-AzSupportProblemClassification segítségével.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="c2c2e-110">A szolgáltatás és a probléma besorolása GLOBÁLISan új támogatási jegyet hozhat létre a New-AzSupportTicket segítségével.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="c2c2e-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="c2c2e-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="c2c2e-112">Beolvassa az Azure-szolgáltatás problémás besorolásának aktuális listáját.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="c2c2e-113">A szolgáltatás és a probléma besorolása GLOBÁLISan új támogatási jegyet hozhat létre a New-AzSupportTicket segítségével.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="c2c2e-114">Új – AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="c2c2e-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="c2c2e-115">Segéd-parancsmag a támogatási partnercsoport-objektum létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="c2c2e-116">Ezt az objektumot használhatja New-AzSupportTicket parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="c2c2e-117">Új – AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c2c2e-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="c2c2e-118">Új Azure támogatási jegyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="c2c2e-119">Ezt a műveletet az Azure [új támogatási kérés lapjának](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)viselkedése alapján modellezjük.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="c2c2e-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c2c2e-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="c2c2e-121">A támogatási jegyek listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-121">Gets the list of support tickets.</span></span> <span data-ttu-id="c2c2e-122">Teljes támogatási jegyet kaphat a menetjegyek nevével, vagy szűrheti a támogatási jegyeket az *állapot* vagy a *CreatedDate* alapján.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="c2c2e-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c2c2e-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="c2c2e-124">Frissítse a támogatási jegy súlyosságát, állapotát vagy az ügyfél elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="c2c2e-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="c2c2e-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="c2c2e-126">Kommunikációt kap a támogatási jegyekhez.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="c2c2e-127">A támogatási menetjegy-kommunikációt *CreatedDate*   vagy *CommunicationType* is szűrheti.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="c2c2e-128">Új – AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="c2c2e-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="c2c2e-129">Új ügyfél-kommunikációt ad az Azure támogatási jegyéhez.</span><span class="sxs-lookup"><span data-stu-id="c2c2e-129">Adds a new customer communication to an Azure support ticket.</span></span> 



