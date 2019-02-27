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
# <a name="azure-stack-module-170"></a>Azure Stack modul 1.7.0

## <a name="requirements"></a>Követelmények:
A minimális támogatott Azure Stack-verzió az 1901-es.

Megjegyzés: Ha korábbi verziót használ, telepítse az 1.7.0-s verziót.

## <a name="install"></a>Telepítés
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
## <a name="release-notes"></a>Kibocsátási megjegyzések
* Az 1901-es frissítésben támogatott.
* Ez egy kompatibilitástörő változást tartalmazó kiadás. A kompatibilitástörő változásokkal kapcsolatos részletekért tekintse meg a következőt: https://aka.ms/azspshmigration170.
* Azs.Backup.Admin Module * Kompatibilitástörő változás: Tanúsítványalapú titkosítási mód biztonsági mentésének módosításai. A tartalomkulcsok támogatása elavult.
* Azs.Fabric.Admin Module       * Elavulás           * A Get-AzsInfrastructureVolume elavult, új parancsmag: Get-AzsVolume           * A Get-AzsStorageSystem elavult, új parancsmag: Get-AzsStorageSubSystem           * A Get-AzsStoragePool elavult, a StorageSubSystem objektum rendelkezik a kapacitás tulajdonsággal
* Azs.Compute.Admin modul           * Javított hiba: Add-AzsPlatformImage, Get-AzsPlatformImage: A ConvertTo-PlatformImageObject meghívása csak a sikeres útvonalon történik           * Javított hiba: Add-AzsVmExtension, Get-AzsVmExtension: A ConvertTo-VmExtensionObject meghívása csak a sikeres útvonalon történik
* Azs.Storage.Admin Module           * Javított hiba – Az Új tárterületkvóta megadott értékek hiányában alapértelmezetteket használ.

