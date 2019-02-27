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
ms.openlocfilehash: af34497f243ce8f4f718e88312f6ad54eb6ad848
ms.sourcegitcommit: 993db64e68b222acbcfdeef2e81eb3316b160858
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2019
ms.locfileid: "56240519"
---
# <a name="azure-stack-module-170"></a><span data-ttu-id="2622b-103">Azure Stack modul 1.7.0</span><span class="sxs-lookup"><span data-stu-id="2622b-103">Azure Stack Module 1.7.0</span></span>

## <a name="requirements"></a><span data-ttu-id="2622b-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="2622b-104">Requirements:</span></span>
<span data-ttu-id="2622b-105">A minimális támogatott Azure Stack-verzió az 1901-es.</span><span class="sxs-lookup"><span data-stu-id="2622b-105">Minimum supported Azure Stack version is 1901.</span></span>

<span data-ttu-id="2622b-106">Megjegyzés: Ha korábbi verziót használ, telepítse az 1.7.0-s verziót.</span><span class="sxs-lookup"><span data-stu-id="2622b-106">Note: If you are using an earlier version install version 1.7.0</span></span>

## <a name="install"></a><span data-ttu-id="2622b-107">Telepítés</span><span class="sxs-lookup"><span data-stu-id="2622b-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.0
```
## <a name="release-notes"></a><span data-ttu-id="2622b-108">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="2622b-108">Release Notes</span></span>
* <span data-ttu-id="2622b-109">Az 1901-es frissítésben támogatott.</span><span class="sxs-lookup"><span data-stu-id="2622b-109">Supported with 1901 update</span></span>
* <span data-ttu-id="2622b-110">Ez egy kompatibilitástörő változást tartalmazó kiadás.</span><span class="sxs-lookup"><span data-stu-id="2622b-110">This a breaking change release.</span></span> <span data-ttu-id="2622b-111">A kompatibilitástörő változásokkal kapcsolatos részletekért tekintse meg a következőt: https://aka.ms/azspshmigration170.</span><span class="sxs-lookup"><span data-stu-id="2622b-111">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="2622b-112">Azs.Backup.Admin Module \* Kompatibilitástörő változás: Tanúsítványalapú titkosítási mód biztonsági mentésének módosításai.</span><span class="sxs-lookup"><span data-stu-id="2622b-112">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="2622b-113">A tartalomkulcsok támogatása elavult.</span><span class="sxs-lookup"><span data-stu-id="2622b-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="2622b-114">Azs.Fabric.Admin Module       \* Elavulás           \* A Get-AzsInfrastructureVolume elavult, új parancsmag: Get-AzsVolume           \* A Get-AzsStorageSystem elavult, új parancsmag: Get-AzsStorageSubSystem           \* A Get-AzsStoragePool elavult, a StorageSubSystem objektum rendelkezik a kapacitás tulajdonsággal</span><span class="sxs-lookup"><span data-stu-id="2622b-114">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="2622b-115">Azs.Compute.Admin modul           \* Javított hiba: Add-AzsPlatformImage, Get-AzsPlatformImage: A ConvertTo-PlatformImageObject meghívása csak a sikeres útvonalon történik           \* Javított hiba: Add-AzsVmExtension, Get-AzsVmExtension: A ConvertTo-VmExtensionObject meghívása csak a sikeres útvonalon történik</span><span class="sxs-lookup"><span data-stu-id="2622b-115">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="2622b-116">Azs.Storage.Admin Module           \* Javított hiba – Az Új tárterületkvóta megadott értékek hiányában alapértelmezetteket használ.</span><span class="sxs-lookup"><span data-stu-id="2622b-116">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>

