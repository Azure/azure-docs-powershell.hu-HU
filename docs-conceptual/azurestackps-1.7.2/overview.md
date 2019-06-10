---
title: Az Azure Stack Admin PowerShell áttekintése | Microsoft Docs
description: Az Azure Stack Admin PowerShell áttekintése telepítési és konfigurációs utasításokkal.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855788"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="fcd94-103">Azure Stack 1.7.2-es modul</span><span class="sxs-lookup"><span data-stu-id="fcd94-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd94-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="fcd94-104">Requirements:</span></span>

<span data-ttu-id="fcd94-105">A minimális támogatott Azure Stack-verzió a 1904-es.</span><span class="sxs-lookup"><span data-stu-id="fcd94-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="fcd94-106">Megjegyzés: Az Azure Stack korábbi verzióiért tekintse meg a következőt: [Az Azure Stack PowerShell telepítése](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="fcd94-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install-powershell-for-azure-stack"></a><span data-ttu-id="fcd94-107">A PowerShell telepítése az Azure Stackhez</span><span class="sxs-lookup"><span data-stu-id="fcd94-107">Install PowerShell for Azure Stack</span></span>

<span data-ttu-id="fcd94-108">A telepítés három lépésből áll:</span><span class="sxs-lookup"><span data-stu-id="fcd94-108">Installation has three steps:</span></span>

1. <span data-ttu-id="fcd94-109">Az Azure Stack PowerShell telepítése az Azure Stack verziójától függően</span><span class="sxs-lookup"><span data-stu-id="fcd94-109">Install Azure Stack PowerShell depending on your version of Azure Stack</span></span>
2. <span data-ttu-id="fcd94-110">További tárolási szolgáltatások engedélyezése</span><span class="sxs-lookup"><span data-stu-id="fcd94-110">Enable additional storage features</span></span>
3. <span data-ttu-id="fcd94-111">A PowerShell telepítésének megerősítése</span><span class="sxs-lookup"><span data-stu-id="fcd94-111">Confirm the installation of PowerShell</span></span>

### <a name="install-azure-stack-powershell"></a><span data-ttu-id="fcd94-112">Az Azure Stack PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="fcd94-112">Install Azure Stack PowerShell</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a><span data-ttu-id="fcd94-113">További tárolási szolgáltatások engedélyezése</span><span class="sxs-lookup"><span data-stu-id="fcd94-113">Enable additional storage features</span></span>

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a><span data-ttu-id="fcd94-114">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="fcd94-114">Release Notes</span></span>

* <span data-ttu-id="fcd94-115">Az 1904-es frissítésben támogatott</span><span class="sxs-lookup"><span data-stu-id="fcd94-115">Supported with 1904 update</span></span>
* <span data-ttu-id="fcd94-116">Ez egy kompatibilitástörő változást tartalmazó kiadás.</span><span class="sxs-lookup"><span data-stu-id="fcd94-116">This a breaking change release.</span></span> <span data-ttu-id="fcd94-117">A kompatibilitástörő változásokkal kapcsolatos részletekért tekintse meg a következőt: <https://aka.ms/azspshmigration170>.</span><span class="sxs-lookup"><span data-stu-id="fcd94-117">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="fcd94-118">Azs.Backup.Admin Module \* Kompatibilitástörő változás: Tanúsítványalapú titkosítási mód biztonsági mentésének módosításai.</span><span class="sxs-lookup"><span data-stu-id="fcd94-118">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="fcd94-119">A tartalomkulcsok támogatása elavult.</span><span class="sxs-lookup"><span data-stu-id="fcd94-119">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="fcd94-120">Azs.Fabric.Admin Module       \* Elavulás           \* A Get-AzsInfrastructureVolume elavult, új parancsmag: Get-AzsVolume           \* A Get-AzsStorageSystem elavult, új parancsmag: Get-AzsStorageSubSystem           \* A Get-AzsStoragePool elavult, a StorageSubSystem objektum rendelkezik a kapacitás tulajdonsággal</span><span class="sxs-lookup"><span data-stu-id="fcd94-120">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="fcd94-121">Azs.Compute.Admin modul           \* Javított hiba: Add-AzsPlatformImage, Get-AzsPlatformImage: A ConvertTo-PlatformImageObject meghívása csak a sikeres útvonalon történik           \* Javított hiba: Add-AzsVmExtension, Get-AzsVmExtension: A ConvertTo-VmExtensionObject meghívása csak a sikeres útvonalon történik</span><span class="sxs-lookup"><span data-stu-id="fcd94-121">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="fcd94-122">Azs.Storage.Admin Module           \* Javított hiba – Az Új tárterületkvóta megadott értékek hiányában alapértelmezetteket használ.</span><span class="sxs-lookup"><span data-stu-id="fcd94-122">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
