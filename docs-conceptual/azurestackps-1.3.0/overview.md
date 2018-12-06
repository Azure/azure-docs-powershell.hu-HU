---
title: Az Azure Stack Admin PowerShell áttekintése | Microsoft Docs
description: Az Azure Stack Admin PowerShell áttekintése telepítési és konfigurációs utasításokkal.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: fb892daeafb1365ea62324392ac806cf9f3d39cf
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828892"
---
# <a name="azure-stack-module-130"></a>Azure Stack modul 1.3.0

## <a name="requirements"></a>Követelmények:
A minimális támogatott Azure Stack-verzió a 1804-es.

Megjegyzés: korábbi verzió használata esetén az 1.2.11-es verziót telepítse

## <a name="known-issues"></a>Ismert problémák:

- A Riasztás bezárása művelethez az Azure Stack 1803-as verziója szükséges
- Bizonyos Storage-parancsmagokhoz az Azure Stack 1804-es verziója szükséges
- A New-AzsOffer nem teszi lehetővé nyilvános állapotú ajánlatok létrehozását. Utána meg kell hívni a Set-AzsOffer parancsmagot az állapot módosítására.
- Az IP-készleteket nem lehet eltávolítani újratelepítés nélkül

## <a name="breaking-changes"></a>Kompatibilitástörő változások
A 1.2.11-es verzióból migrált összes kompatibilitástörő változást itt találja: https://aka.ms/azspowershellmigration

## <a name="install"></a>Telepítés
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a>Tartalom:
### <a name="azure-bridge"></a>Azure Bridge
Az Azure Stack AzureBridge felügyeleti moduljának előzetes kiadása, amelynek segítségével rendszerképeket tehet közzé az Azure-ból.

### <a name="backup"></a>Backup
A Backup felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:
- Konfigurálhatja a biztonsági másolatok tárolási helyét
- Biztonsági mentéseket hajthat végre
- Listázhatja és visszaállíthatja az elkészült biztonsági másolatokat

### <a name="commerce"></a>Commerce
Az Azure Stack Commerce felügyeleti modul előzetes kiadása, amely lehetővé teszi az összesített adathasználat megtekintését a teljes Azure Stack rendszerben.

### <a name="compute"></a>Compute
Az Azure Stack Compute felügyeleti modul előzetes kiadása, amely a számítási kvóták, platform-rendszerképek és virtuálisgép-bővítmények felügyeletéhez szükséges funkciókat biztosít.

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
