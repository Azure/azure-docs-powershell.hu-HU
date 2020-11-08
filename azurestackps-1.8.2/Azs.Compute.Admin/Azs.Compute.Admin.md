---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 8b74dd57a85a39403f56840dd0fc54b3f25184f1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016766"
---
# <span data-ttu-id="0f63d-101">AZS. számít. felügyeleti modul</span><span class="sxs-lookup"><span data-stu-id="0f63d-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="0f63d-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f63d-102">Description</span></span>
<span data-ttu-id="0f63d-103">A AzureStack-számítási rendszergazda modul előzetes verziója, amely a számítási kvóták, a platform képei és a virtuálisgép-bővítmények kezelésére szolgáló funkciókat, valamint a felügyelt lemezek áttelepítési feladatait biztosítja a tárterület kiegyensúlyozásához.</span><span class="sxs-lookup"><span data-stu-id="0f63d-103">Preview release of the AzureStack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="0f63d-104">AZS. számítási. rendszergazdai parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0f63d-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="0f63d-105">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="0f63d-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="0f63d-106">Virtuális gép platformjának képe egy adott képkonfigurációból.</span><span class="sxs-lookup"><span data-stu-id="0f63d-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="0f63d-107">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0f63d-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="0f63d-108">Új virtuálisgép-kiterjesztési kép létrehozása</span><span class="sxs-lookup"><span data-stu-id="0f63d-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="0f63d-109">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="0f63d-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="0f63d-110">Olyan kvótákat ad eredményül, amelyek meghatározzák az objektumok számítási kvótáit.</span><span class="sxs-lookup"><span data-stu-id="0f63d-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="0f63d-111">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="0f63d-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="0f63d-112">Azoknak a felügyelt lemezeknek a listáját adja eredményül, amelyek áttelepíthetők a megadott megosztásban.</span><span class="sxs-lookup"><span data-stu-id="0f63d-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="0f63d-113">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0f63d-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="0f63d-114">A felügyelt áttelepítési feladatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0f63d-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="0f63d-115">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="0f63d-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="0f63d-116">A platform képtárházba betöltött virtuális gép képeit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0f63d-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="0f63d-117">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0f63d-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="0f63d-118">A virtuális gép képkiterjesztéseit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0f63d-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="0f63d-119">Új – AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="0f63d-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="0f63d-120">Új számítási kvóta létrehozása a számítási források korlátozásához.</span><span class="sxs-lookup"><span data-stu-id="0f63d-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="0f63d-121">Új – AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0f63d-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="0f63d-122">Felügyelt áttelepítési feladatot indít át a távtárolású lemezek áttelepítéséhez a megadott célhelyre.</span><span class="sxs-lookup"><span data-stu-id="0f63d-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="0f63d-123">Új – DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="0f63d-123">New-DataDiskObject</span></span>](New-DataDiskObject.md)
<span data-ttu-id="0f63d-124">Létrehoz egy adatlemezt, amely egy új virtuális gép platformjának létrehozásakor használatos.</span><span class="sxs-lookup"><span data-stu-id="0f63d-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="0f63d-125">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="0f63d-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="0f63d-126">Törli a megadott számítási kvótát.</span><span class="sxs-lookup"><span data-stu-id="0f63d-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="0f63d-127">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="0f63d-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="0f63d-128">Törölje a virtuális gép képét a platform képtárházában.</span><span class="sxs-lookup"><span data-stu-id="0f63d-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="0f63d-129">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0f63d-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="0f63d-130">A virtuálisgép-bővítmények lemezképének törlése</span><span class="sxs-lookup"><span data-stu-id="0f63d-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="0f63d-131">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="0f63d-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="0f63d-132">Meglévő számítási kvóta frissítése a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="0f63d-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="0f63d-133">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0f63d-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="0f63d-134">Felügyelt áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="0f63d-134">Cancel a managed disk migration job.</span></span>

