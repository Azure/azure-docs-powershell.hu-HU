---
Module Name: Az.ManagedServices
Module Guid: d2a8f744-8dcb-4a13-ba80-eb181ff365ad
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.1
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 41d7b3afa19de95b677ff5db18ca38294b8559af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183535"
---
# <span data-ttu-id="618b7-101">Az. ManagedServices modul</span><span class="sxs-lookup"><span data-stu-id="618b7-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="618b7-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="618b7-102">Description</span></span>
<span data-ttu-id="618b7-103">Ezt a szolgáltatást a felügyelt szolgáltatók ügyfelei (MSPs) használják.</span><span class="sxs-lookup"><span data-stu-id="618b7-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="618b7-104">Az ügyfelek hozzáférést biztosítanak az előfizetéséhez.</span><span class="sxs-lookup"><span data-stu-id="618b7-104">Customers give an MSP the ability to manage their subscription.</span></span> <span data-ttu-id="618b7-105">A hozzáférés megadásán kívül az ügyfél is megszüntetheti a hozzáférést vagy megtekintheti a meglévő hozzáférés-delegációkat.</span><span class="sxs-lookup"><span data-stu-id="618b7-105">In addition to granting access, the customer can also remove access or view existing access delegations.</span></span> <span data-ttu-id="618b7-106">A MSPs megtekinthetik azoknak a vevőknek a listáját, akik hozzáférést kaptak az előfizetésekhez.</span><span class="sxs-lookup"><span data-stu-id="618b7-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="618b7-107">Ebben a folyamatban két objektum van: egy olyan regisztrációs definíció, amely azonosítja az MSP-t és a MSP-nek adott szerepkör-definíciókat.</span><span class="sxs-lookup"><span data-stu-id="618b7-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP.</span></span> <span data-ttu-id="618b7-108">Az MSP ezt az objektumot a felügyelt szolgáltatások Piactéren keresztül is megadhatja, amely az előfizetést társítja a definícióval.</span><span class="sxs-lookup"><span data-stu-id="618b7-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="618b7-109">Az. ManagedServices parancsmagok</span><span class="sxs-lookup"><span data-stu-id="618b7-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="618b7-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="618b7-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="618b7-111">A regisztrációs feladatok listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="618b7-111">Gets a list of the registration assignments.</span></span>

### [<span data-ttu-id="618b7-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="618b7-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="618b7-113">A regisztrációs definíciók listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="618b7-113">Gets a list of the registration definitions.</span></span>

### [<span data-ttu-id="618b7-114">Új – AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="618b7-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="618b7-115">Regisztrációs feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="618b7-115">Creates a registration assignment.</span></span>

### [<span data-ttu-id="618b7-116">Új – AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="618b7-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="618b7-117">Regisztrációs definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="618b7-117">Creates a registration definition.</span></span>

### [<span data-ttu-id="618b7-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="618b7-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="618b7-119">Törli a regisztrációs feladatot.</span><span class="sxs-lookup"><span data-stu-id="618b7-119">Deletes the registration assignment.</span></span>

### [<span data-ttu-id="618b7-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="618b7-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="618b7-121">Törli a regisztrációs definíciót.</span><span class="sxs-lookup"><span data-stu-id="618b7-121">Deletes the registration definition.</span></span>

