---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 4194899ad20356c8cde68110553495558d3816d5
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2019
ms.locfileid: "93657886"
---
# <span data-ttu-id="284a3-101">AZS. számít. felügyeleti modul</span><span class="sxs-lookup"><span data-stu-id="284a3-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="284a3-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="284a3-102">Description</span></span>
<span data-ttu-id="284a3-103">A AzureStack számítási műveleti moduljának előzetes verziója, amely a számítási kvóták, a platform képei és a virtuálisgép-bővítmények kezelésére szolgáló funkciókat, valamint a felügyelt lemezek áttelepítési feladatait biztosítja a tárterület kiegyensúlyozásához.</span><span class="sxs-lookup"><span data-stu-id="284a3-103">Preview release of the AzureStack Compute operator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="284a3-104">AZS. számítási. rendszergazdai parancsmagok</span><span class="sxs-lookup"><span data-stu-id="284a3-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="284a3-105">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="284a3-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="284a3-106">Virtuális gép platformjának képe egy adott képkonfigurációból.</span><span class="sxs-lookup"><span data-stu-id="284a3-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="284a3-107">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="284a3-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="284a3-108">Új virtuálisgép-kiterjesztési kép létrehozása</span><span class="sxs-lookup"><span data-stu-id="284a3-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="284a3-109">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="284a3-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="284a3-110">Olyan kvótákat ad eredményül, amelyek meghatározzák az objektumok számítási kvótáit.</span><span class="sxs-lookup"><span data-stu-id="284a3-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="284a3-111">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="284a3-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="284a3-112">Azoknak a felügyelt lemezeknek a listáját adja eredményül, amelyek áttelepíthetők a megadott megosztásban.</span><span class="sxs-lookup"><span data-stu-id="284a3-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="284a3-113">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="284a3-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="284a3-114">A felügyelt áttelepítési feladatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="284a3-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="284a3-115">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="284a3-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="284a3-116">A platform képtárházba betöltött virtuális gép képeit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="284a3-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="284a3-117">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="284a3-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="284a3-118">A virtuális gép képkiterjesztéseit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="284a3-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="284a3-119">Új – AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="284a3-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="284a3-120">Új számítási kvóta létrehozása a számítási források korlátozásához.</span><span class="sxs-lookup"><span data-stu-id="284a3-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="284a3-121">Új – AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="284a3-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="284a3-122">Felügyelt áttelepítési feladatot indít át a távtárolású lemezek áttelepítéséhez a megadott célhelyre.</span><span class="sxs-lookup"><span data-stu-id="284a3-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="284a3-123">Új – AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="284a3-123">New-AzsDataDiskObject</span></span>](New-AzsDataDiskObject.md)
<span data-ttu-id="284a3-124">Létrehoz egy adatlemezt, amely egy új virtuális gép platformjának létrehozásakor használatos.</span><span class="sxs-lookup"><span data-stu-id="284a3-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="284a3-125">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="284a3-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="284a3-126">Törli a megadott számítási kvótát.</span><span class="sxs-lookup"><span data-stu-id="284a3-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="284a3-127">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="284a3-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="284a3-128">Törölje a virtuális gép képét a platform képtárházában.</span><span class="sxs-lookup"><span data-stu-id="284a3-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="284a3-129">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="284a3-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="284a3-130">A virtuálisgép-bővítmények lemezképének törlése</span><span class="sxs-lookup"><span data-stu-id="284a3-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="284a3-131">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="284a3-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="284a3-132">Meglévő számítási kvóta frissítése a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="284a3-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="284a3-133">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="284a3-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="284a3-134">Felügyelt áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="284a3-134">Cancel a managed disk migration job.</span></span>

