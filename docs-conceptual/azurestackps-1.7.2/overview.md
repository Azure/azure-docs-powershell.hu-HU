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
# <a name="azure-stack-module-172"></a>Azure Stack 1.7.2-es modul

## <a name="requirements"></a>Követelmények:

A minimális támogatott Azure Stack-verzió a 1904-es.

Megjegyzés: Az Azure Stack korábbi verzióiért tekintse meg a következőt: [Az Azure Stack PowerShell telepítése](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install-powershell-for-azure-stack"></a>A PowerShell telepítése az Azure Stackhez

A telepítés három lépésből áll:

1. Az Azure Stack PowerShell telepítése az Azure Stack verziójától függően
2. További tárolási szolgáltatások engedélyezése
3. A PowerShell telepítésének megerősítése

### <a name="install-azure-stack-powershell"></a>Az Azure Stack PowerShell telepítése

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

### <a name="enable-additional-storage-features"></a>További tárolási szolgáltatások engedélyezése

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

## <a name="release-notes"></a>Kibocsátási megjegyzések

* Az 1904-es frissítésben támogatott
* Ez egy kompatibilitástörő változást tartalmazó kiadás. A kompatibilitástörő változásokkal kapcsolatos részletekért tekintse meg a következőt: <https://aka.ms/azspshmigration170>.
* Azs.Backup.Admin Module * Kompatibilitástörő változás: Tanúsítványalapú titkosítási mód biztonsági mentésének módosításai. A tartalomkulcsok támogatása elavult.
* Azs.Fabric.Admin Module       * Elavulás           * A Get-AzsInfrastructureVolume elavult, új parancsmag: Get-AzsVolume           * A Get-AzsStorageSystem elavult, új parancsmag: Get-AzsStorageSubSystem           * A Get-AzsStoragePool elavult, a StorageSubSystem objektum rendelkezik a kapacitás tulajdonsággal
* Azs.Compute.Admin modul           * Javított hiba: Add-AzsPlatformImage, Get-AzsPlatformImage: A ConvertTo-PlatformImageObject meghívása csak a sikeres útvonalon történik           * Javított hiba: Add-AzsVmExtension, Get-AzsVmExtension: A ConvertTo-VmExtensionObject meghívása csak a sikeres útvonalon történik
* Azs.Storage.Admin Module           * Javított hiba – Az Új tárterületkvóta megadott értékek hiányában alapértelmezetteket használ.
