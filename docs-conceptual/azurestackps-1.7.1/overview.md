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
ms.openlocfilehash: 6568dc4e6c51e8f250aad2c4dd765c065fe6a8bf
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/18/2019
ms.locfileid: "58808060"
---
# <a name="azure-stack-module-171"></a>Azure Stack 1.7.1-es modul

## <a name="requirements"></a>Követelmények:

A minimális támogatott Azure Stack-verzió az 1901-es.

Megjegyzés: Az Azure Stack korábbi verzióiért tekintse meg a következőt: [Az Azure Stack PowerShell telepítése](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Telepítés

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a>Kibocsátási megjegyzések

* Az 1901-es frissítésben támogatott.
* Ez egy kompatibilitástörő változást tartalmazó kiadás. A kompatibilitástörő változásokkal kapcsolatos részletekért tekintse meg a következőt: <https://aka.ms/azspshmigration170>.
* Azs.Backup.Admin Module * Kompatibilitástörő változás: Tanúsítványalapú titkosítási mód biztonsági mentésének módosításai. A tartalomkulcsok támogatása elavult.
* Azs.Fabric.Admin Module       * Elavulás           * A Get-AzsInfrastructureVolume elavult, új parancsmag: Get-AzsVolume           * A Get-AzsStorageSystem elavult, új parancsmag: Get-AzsStorageSubSystem           * A Get-AzsStoragePool elavult, a StorageSubSystem objektum rendelkezik a kapacitás tulajdonsággal
* Azs.Compute.Admin modul           * Javított hiba: Add-AzsPlatformImage, Get-AzsPlatformImage: A ConvertTo-PlatformImageObject meghívása csak a sikeres útvonalon történik           * Javított hiba: Add-AzsVmExtension, Get-AzsVmExtension: A ConvertTo-VmExtensionObject meghívása csak a sikeres útvonalon történik
* Azs.Storage.Admin Module           * Javított hiba – Az Új tárterületkvóta megadott értékek hiányában alapértelmezetteket használ.
