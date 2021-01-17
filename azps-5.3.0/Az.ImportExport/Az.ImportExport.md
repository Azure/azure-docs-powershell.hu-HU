---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480280"
---
# <span data-ttu-id="3f264-101">Az.ImportExport modul</span><span class="sxs-lookup"><span data-stu-id="3f264-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="3f264-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f264-102">Description</span></span>
<span data-ttu-id="3f264-103">Microsoft Azure PowerShell: ImportExport parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3f264-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="3f264-104">Az.ImportExport parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3f264-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="3f264-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="3f264-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="3f264-106">Információkat kap egy meglévő feladatról.</span><span class="sxs-lookup"><span data-stu-id="3f264-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="3f264-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="3f264-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="3f264-108">A megadott feladatban található összes meghajtó BitLocker-kulcsait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3f264-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="3f264-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="3f264-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="3f264-110">Az importálási vagy exportálási feladathoz társított lemezeket tartalmazó hely adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="3f264-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="3f264-111">A hely egy Azure-régió.</span><span class="sxs-lookup"><span data-stu-id="3f264-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="3f264-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="3f264-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="3f264-113">Új feladatot hoz létre, vagy frissíti a megadott előfizetésben meglévő feladatot.</span><span class="sxs-lookup"><span data-stu-id="3f264-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="3f264-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="3f264-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="3f264-115">Hozzon létre egy DriverList-objektumot az ImportExporthoz.</span><span class="sxs-lookup"><span data-stu-id="3f264-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="3f264-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="3f264-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="3f264-117">Töröl egy meglévő feladatot.</span><span class="sxs-lookup"><span data-stu-id="3f264-117">Deletes an existing job.</span></span>
<span data-ttu-id="3f264-118">Csak a Létrehozás vagy a Kész államban törölt feladatok törölhetők.</span><span class="sxs-lookup"><span data-stu-id="3f264-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="3f264-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="3f264-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="3f264-120">Frissíti egy feladat adott tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="3f264-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="3f264-121">Ezt a műveletet felhívva értesítheti az Importálás/exportálás szolgáltatást, hogy az importálási vagy exportálási feladatot tartalmazó merevlemezek a Microsoft adatközpontba került.</span><span class="sxs-lookup"><span data-stu-id="3f264-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="3f264-122">Egy meglévő feladat megszakítása is használható.</span><span class="sxs-lookup"><span data-stu-id="3f264-122">It can also be used to cancel an existing job.</span></span>

