---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187692"
---
# <span data-ttu-id="5283e-101">Az. ManagedServices modul</span><span class="sxs-lookup"><span data-stu-id="5283e-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="5283e-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="5283e-102">Description</span></span>
<span data-ttu-id="5283e-103">Ezt a szolgáltatást a felügyelt szolgáltatók ügyfelei (MSPs) használják.</span><span class="sxs-lookup"><span data-stu-id="5283e-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="5283e-104">Az ügyfelek hozzáférést biztosítanak az előfizetéshez vagy az erőforráscsoport kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="5283e-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="5283e-105">A hozzáférés megadásán kívül az ügyfél is megszüntetheti a hozzáférést, vagy megtekintheti a meglévőket.</span><span class="sxs-lookup"><span data-stu-id="5283e-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="5283e-106">A MSPs megtekinthetik azoknak a vevőknek a listáját, akik hozzáférést kaptak az előfizetésekhez.</span><span class="sxs-lookup"><span data-stu-id="5283e-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="5283e-107">Ebben a folyamatban két objektum van: egy olyan regisztrációs definíció, amely azonosítja az MSP-t, valamint az MSP-felhasználóknak biztosított szerepkör-definíciókat.</span><span class="sxs-lookup"><span data-stu-id="5283e-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="5283e-108">Az MSP ezt az objektumot a felügyelt szolgáltatások Piactéren keresztül is megadhatja, amely az előfizetést társítja a definícióval.</span><span class="sxs-lookup"><span data-stu-id="5283e-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="5283e-109">Az. ManagedServices parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5283e-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="5283e-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="5283e-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="5283e-111">Egy bizonyos regisztrációs feladatot vagy a regisztrációs feladatok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5283e-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="5283e-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="5283e-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="5283e-113">Beolvassa a regisztráció definícióját vagy a regisztrációs definíciók listáját.</span><span class="sxs-lookup"><span data-stu-id="5283e-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="5283e-114">Új – AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="5283e-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="5283e-115">Regisztrációs feladatot hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="5283e-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="5283e-116">Új – AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="5283e-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="5283e-117">Regisztrációs definíciót hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="5283e-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="5283e-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="5283e-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="5283e-119">A regisztrációs feladat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="5283e-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="5283e-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="5283e-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="5283e-121">A regisztrációs definíció eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="5283e-121">Removes a registration definition.</span></span>
