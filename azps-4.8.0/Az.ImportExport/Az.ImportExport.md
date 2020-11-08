---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182753"
---
# <span data-ttu-id="4c8d0-101">Az. ImportExport modul</span><span class="sxs-lookup"><span data-stu-id="4c8d0-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="4c8d0-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c8d0-102">Description</span></span>
<span data-ttu-id="4c8d0-103">Microsoft Azure PowerShell: ImportExport parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4c8d0-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="4c8d0-104">Az. ImportExport parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4c8d0-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="4c8d0-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4c8d0-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="4c8d0-106">Információt kap egy meglévő feladatról.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="4c8d0-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="4c8d0-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="4c8d0-108">A megadott feladat összes meghajtójának BitLocker-kulcsait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="4c8d0-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="4c8d0-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="4c8d0-110">Egy olyan hely részleteit számítja ki, amelybe az importálási vagy exportálási feladathoz kapcsolódó lemezeket szállíthatja.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="4c8d0-111">A hely egy Azure-terület.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="4c8d0-112">Új – AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4c8d0-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="4c8d0-113">Új feladatot hoz létre, vagy egy meglévő feladatot frissít a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="4c8d0-114">Új – AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="4c8d0-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="4c8d0-115">Hozzon létre egy DriverList-objektumot a ImportExport-hoz.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="4c8d0-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4c8d0-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="4c8d0-117">Egy meglévő feladat törlése</span><span class="sxs-lookup"><span data-stu-id="4c8d0-117">Deletes an existing job.</span></span>
<span data-ttu-id="4c8d0-118">Csak a létrehozó vagy a Befejezett állapotú feladatok törölhetők.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="4c8d0-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4c8d0-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="4c8d0-120">A feladatok bizonyos tulajdonságait frissíti.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="4c8d0-121">Ezt a műveletet felhívhatja az importálási/exportálási szolgáltatás értesítésére, hogy az importálási vagy exportálási feladatot tartalmazó merevlemezek a Microsoft-adatközpontba lettek szállítva.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="4c8d0-122">A meglévő feladatok visszavonására is használható.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-122">It can also be used to cancel an existing job.</span></span>

