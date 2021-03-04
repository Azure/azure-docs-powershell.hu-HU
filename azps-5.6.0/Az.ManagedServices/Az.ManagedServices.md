---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 33c6f65e258ee16b0ffb6a4616ffd1c7c5f16c77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924066"
---
# <span data-ttu-id="3c01c-101">Az.ManagedServices modul</span><span class="sxs-lookup"><span data-stu-id="3c01c-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="3c01c-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c01c-102">Description</span></span>
<span data-ttu-id="3c01c-103">Ezt a funkciót a felügyelt szolgáltatók ügyfelei használják.</span><span class="sxs-lookup"><span data-stu-id="3c01c-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="3c01c-104">Az ügyfelek az MSP-nek lehetőséget adnak előfizetésük vagy erőforráscsoportjuk kezelésére.</span><span class="sxs-lookup"><span data-stu-id="3c01c-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="3c01c-105">A hozzáférés megadásán kívül az ügyfél a hozzáférést is eltávolíthatja, vagy megtekintheti a meglévő hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="3c01c-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="3c01c-106">Az MSP-k megtekinthetik azon ügyfelek listáját, akik hozzáférést kaptak az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="3c01c-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="3c01c-107">Ebben a folyamatban két objektum vesz részt: Egy olyan regisztrációs definíció, amely azonosítja az MSP-t és az MSP-felhasználóknak megadott szerepkördefiníciókat.</span><span class="sxs-lookup"><span data-stu-id="3c01c-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="3c01c-108">Az MSP szükség esetén definiálhatja ezt az objektumot egy Felügyelt szolgáltatások piactér használatával, amely Access-hozzárendeléseket kínál, amelyek egy előfizetést társítanak a definícióval.</span><span class="sxs-lookup"><span data-stu-id="3c01c-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="3c01c-109">Az.ManagedServices parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3c01c-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="3c01c-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="3c01c-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="3c01c-111">Egy adott regisztrációs feladatot vagy a regisztrációs feladatok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3c01c-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="3c01c-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="3c01c-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="3c01c-113">Egy adott regisztrációs definíciót vagy a regisztrációs definíciók listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3c01c-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="3c01c-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="3c01c-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="3c01c-115">Regisztrációs feladatot hoz létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="3c01c-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="3c01c-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="3c01c-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="3c01c-117">Regisztrációs definíciót hoz létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="3c01c-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="3c01c-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="3c01c-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="3c01c-119">Eltávolít egy regisztrációs feladatot.</span><span class="sxs-lookup"><span data-stu-id="3c01c-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="3c01c-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="3c01c-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="3c01c-121">Eltávolít egy regisztrációs definíciót.</span><span class="sxs-lookup"><span data-stu-id="3c01c-121">Removes a registration definition.</span></span>
