---
title: Az Azure Stack PowerShell áttekintése | Microsoft Docs
description: Az Azure Stack PowerShell áttekintése telepítési és konfigurációs utasításokkal.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 4b72bbd1bda93767251e0ba3d488f798575d9115
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244313"
---
# <a name="azurerm-module-250"></a>AzureRM 2.5.0-s modul

## <a name="requirements"></a>Követelmények:
A minimális támogatott Azure Stack-verzió a 1904-es.

Megjegyzés: korábbi verzió használata esetén az 1.2.11-es verziót telepítse


## <a name="install"></a>Telepítés
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a>Kibocsátási megjegyzések
* AzureRm.Resources
    * Új Erőforrások modul a 2018-05-01-es API-verzióhoz a 2019-03-01-es hibrid profillal
    * A PolicyDefinition (2016-12-01) és PolicyAssisgment (2017-06-01, előzetes verzió) műveletek továbbra is a régi API-verziókkal futnak
* AzureRm.Compute
    * Új számítási modul a 2017-12-01-es API-verzióhoz.


* Ez a kiadás megegyezik a 2019-03-01-hybrid Azure Stack-specifikus API-profillal
* Minden modul függősége nagyobb vagy egyenlő lett az AzureRM.Profile-modulhoz viszonyítva.
* A modulok által támogatott API-verziók frissítve lettek. 
    * Számítás – 2017-12-30
    * Hálózat – 2017-10-01
    * Tárolás – 2016-01-01
    * Erőforrások – 2018-02-01
    * Kulcstartó – 2016-10-01
    * DNS – 2016-04-01
* A teljes API-verziótérkép az egyes erőforrástípusokhoz megtalálható a következő helyen: https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json.

## <a name="content"></a>Tartalom:
### <a name="azure-bridge"></a>Azure Bridge
Az Azure Stack AzureBridge felügyeleti moduljának előzetes kiadása, amelynek segítségével rendszerképeket tehet közzé az Azure-ból.

### <a name="backup"></a>Backup
A Backup felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:
- Konfigurálhatja a biztonsági másolatok tárolási helyét
- Biztonsági mentéseket hajthat végre
- Listázhatja és visszaállíthatja az elkészült biztonsági másolatokat

### <a name="commerce"></a>Kereskedelem
Az Azure Stack Commerce felügyeleti modul előzetes kiadása, amely lehetővé teszi az összesített adathasználat megtekintését a teljes Azure Stack rendszerben.

### <a name="compute"></a>Compute
Az Azure Stack Compute felügyeleti modul előzetes kiadása, amely a számítási kvóták, platformrendszerképek, felügyelt lemezek és virtuálisgép-bővítmények felügyeletéhez szükséges funkciókat biztosít.

### <a name="fabric"></a>Fabric
Az Azure Stack Fabric felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti és felügyelheti az infrastruktúra-összetevőket:
- Skálázásiegység-csomópontok leállítása, indítása és lekapcsolása
- Skálázásiegység-csomópontok kiürítése és folytatása az FRU-val kapcsolatos tevékenységekhez
- Skálázásiegység-csomópontok javítása
- Infrastruktúra-szerepkör újraindítása
- Infrastruktúra-szerepkörpéldányok leállítása, indítása és lekapcsolása
- Új IP-készletek létrehozása


### <a name="gallery"></a>Katalógus
Az Azure Stack Gallery felügyeleti modul előzetes kiadása, amely a katalóguselemek az Azure Stack-piactéren való felügyeletéhez szükséges funkciókat biztosít.

### <a name="infrastructure-insights"></a>Infrastructure Insights
Az Infrastructure Insights felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:
- Megtekintheti az Azure Stack bélyegző erőforrások állapotát
- Megtekintheti és kezelheti a riasztásokat

### <a name="keyvault"></a>KeyVault
Az Azure Stack KeyVault felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti a KeyVault-kvótákat.

### <a name="network"></a>Network (Hálózat)
A Network felügyeleti modul előzetes kiadása, amely:
- Lehetővé teszi a hálózati kvóták felügyeletét
- Lehetővé teszi a hálózati erőforrások (például nyilvános IP-címek, virtuális hálózatok és terheléselosztók) megtekintését
- Egy parancsmagot biztosít a felügyelet áttekintő megjelenítéséhez

### <a name="storage"></a>Storage
Az Azure Stack Storage felügyeleti modul előzetes kiadása.  Ebben a kiadásban a következő funkcionalitást biztosítjuk:
- Tárhelykvóták kezelése
- Törölt tárolási erőforrások szemétgyűjtése
- Törölt tárfiókok visszaállítása
- Tárolók migrálása megosztások közt
- Az egyéni tároló-összetevőkkel kapcsolatos összetevők megjelenítése
- Használati és teljesítményadatok megtekintése

### <a name="subscription-admin"></a>Subscription Admin
Az Azure Stack Subscription adminisztrációs modul előzetes kiadása.  A modul a következő funkciókat biztosítja a rendszergazdák számára:
- Csomagok és ajánlatok kezelése
- Használati és teljesítményadatok megtekintése
- Az RBAC kezelése

### <a name="subscription"></a>Előfizetés
Az Azure Stack Subscription modul előzetes kiadása.  A modul a következő funkciókat biztosítja a felhasználók számára:
- Előfizetések létrehozása, törlése és frissítése

### <a name="update"></a>Frissítés
Az Azure Stack Update adminisztrációs modul előzetes kiadása.  A modul használatával a rendszergazda:
- Listázhatja és telepítheti az elérhető frissítéseket
- Folytathatja a megszakított frissítéseket
- Megtekintheti a telepített frissítéseket
