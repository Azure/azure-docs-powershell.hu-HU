---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 9a40eae86b60afb5e04dd6a6074b60e82731578f
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854630"
---
# <a name="release-notes"></a>Kibocsátási megjegyzések

Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.

## <a name="version-170"></a>1.7.0-ás verzió

* **A -Force, –Confirm és $ConfirmPreference paraméterek viselkedésének módosítása minden parancsmag esetében. Ezt a megvalósítást azért módosítottuk, hogy megfeleljen a PowerShell irányelveinek. A legtöbb parancsmag esetében ez a Force paraméter eltávolítását, valamint a ShouldProcess adatkérés kihagyását jelenti. A felhasználóknak továbbá bele kell foglalniuk a következő paramétert a PowerShell-szkriptjeikbe: -Confirm:$false.** A módosítások a következő problémákat érintik:
  - A –WhatIf funkció megvalósításának javítása, amely lehetővé teszi a felhasználók számára, hogy bármilyen tényleges módosítás nélkül megállapíthassák egy parancsmag vagy szkript hatásait
  - Az adatkérés vezérlése egy az egész munkamenetre kiterjedő $ConfirmPreference paraméter használatával, így a rendszer a végrehajtandó módosítás hatásai alapján szólítja fel a felhasználót (a parancsmag ConfirmImpact beállításában jelentett módon)
  - A megerősítési felszólítások parancsmag-specifikus vezérlése a –Confirm paraméter használatával
  - A ShouldContinue és a –Force paraméterek konzisztens használata az összes parancsmagra vonatkozóan, valamint csak azon műveletek esetében, amelyekhez szükség van a felhasználó visszajelzésére a módosítások speciális jellege miatt (pl. rejtett fájlok törlése)
  - Konzisztencia más PowerShell-parancsmagokkal annak érdekében, hogy a PowerShell-szkriptek használatának más parancsmagokból származó ismerete azonnal alkalmazható legyen az Azure PowerShell-parancsmagok esetében.

**Vegye figyelembe, hogy ha *minden esetben mellőzni szeretne minden adatkérést*, az Azure PowerShell-parancsmagok két paraméter megadását követelik meg:**
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* Azure Compute
  - Set-AzureRmVMADDomainExtension
  - Get-AzureRmVMADDomainExtension
  - -Redeploy paraméter a Restart-AzureVM parancsmag esetében
  - -Validate paraméter a Move-AzureService, Move-AzureStorageAccount és Move-AzureVirtualNetwork parancsmagok esetében
  - A név- és verzióparaméterek továbbra is választhatók a bővítményparancsmagok esetében.
  - A New-AzureVM paraméter a virtuálisgép-objektumtól kaphatja meg a licenctípust.
* Azure Storage
  - A Tags paraméter nevének módosítása a Tag névre, valamint a Tags paraméteralias hozzáadása
    + New-AzureRmStorageAccount
    + Set-AzureRmStorageAccount
* Azure Network-hálózat
  - Új parancsmag hozzáadása a virtuális hálózatok közötti társviszony létesítéséhez
* Azure Redis Cache
  - Új parancsmag hozzáadása a Reset-AzureRmRedisCache parancsmag esetében
  - Új parancsmag hozzáadása a Export-AzureRmRedisCache parancsmag esetében
  - Új parancsmag hozzáadása a Import-AzureRmRedisCache parancsmag esetében
  - A New-AzureRmRedisCache parancsmag módosítása, hogy tartalmazza a vNet paramétermódosítását
* Azure SQL DB Backup/Restore
  - Parancsmagok a hosszú távú adatmegőrzés céljából készített biztonsági mentésekhez
  - Get-AzureRmSqlServerBackupLongTermRetentionVault
  - Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Set-AzureRmSqlServerBackupLongTermRetentionVault
  - Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - A Restore-AzureRmSqlDatabase parancsmag mostantól támogatja a törölt adatbázisok időponthoz kötött visszaállítását
  - A Restore-AzureRmSqlDatabase mostantól támogatja a hosszú távú adatmegőrzés céljából készített biztonsági mentésekből történő helyreállítást
* Azure LogicApp
  - LogicApp integrációs fiókok parancsmagjainak hozzáadása
  - Get-AzureRmIntegrationAccountAgreement
  - Get-AzureRmIntegrationAccountCallbackUrl
  - Get-AzureRmIntegrationAccountCertificate
  - Get-AzureRmIntegrationAccount
  - Get-AzureRmIntegrationAccountMap
  - Get-AzureRmIntegrationAccountPartner
  - Get-AzureRmIntegrationAccountSchema
  - New-AzureRmIntegrationAccountAgreement
  - New-AzureRmIntegrationAccountCertificate
  - New-AzureRmIntegrationAccount
  - New-AzureRmIntegrationAccountMap
  - New-AzureRmIntegrationAccountPartner
  - New-AzureRmIntegrationAccountSchema
  - Remove-AzureRmIntegrationAccountAgreement
  - Remove-AzureRmIntegrationAccountCertificate
  - Remove-AzureRmIntegrationAccount
  - Remove-AzureRmIntegrationAccountMap
  - Remove-AzureRmIntegrationAccountPartner
  - Remove-AzureRmIntegrationAccountSchema
  - Set-AzureRmIntegrationAccountAgreement
  - Set-AzureRmIntegrationAccountCertificate
  - Set-AzureRmIntegrationAccount
  - Set-AzureRmIntegrationAccountMap
  - Set-AzureRmIntegrationAccountPartner
  - Set-AzureRmIntegrationAccountSchema
* Azure Data Lake Store
  - A fájl- és mappafeltöltések, illetve -letöltések teljesítményének jelentős mértékű javítása.
  - Ez magában foglalja a paraméternevek kismértékű módosítását a letöltések, valamint két új paraméter bevezetését a feltöltések esetében:
    + NumThreads -> PerFileThreadCount – Az egyetlen fájlban használandó szálak számát jelöli
    + ConcurrentFileCount – A mappafeltöltés/-letöltés esetében a párhuzamosan feltölteni/letölteni kívánt fájlok számát jelöli.
  - Az alapértelmezett szálkezelési értékek úgy lett kialakítva, hogy jobb általános teljesítményt biztosítsanak a legtöbb fájlméret esetében. Ha a teljesítmény nem felel meg az elvárásnak, a fenti értékek az igényeknek megfelelően módosíthatók.
* Azure Data Lake Analytics
  - A Get-AzureRMDataLakeAnalyticsDataSource parancsmag mostantól az összes adatforrást visszaadja, ha argumentumok nélkül hívják meg.
  - Ez a változtatás továbbá az adatforrás típusára vonatkozó paramétert is eltávolítja a parancsmagból.
  - A változtatás eredményeképp a rendszer egy új objektumot ad vissza a listaművelet esetében, amely a következő tulajdonságokkal rendelkezik:
    + Type – Az adatforrás típusa
    + Name – Az adatforrás neve
    + IsDefault – Az értéke igaz, ha ez a fiók alapértelmezett adatforrása
  - A Get-AzureRMDataLakeAnalyticsJob parancsmag javítása bizonyos dátum-/időeltolási értékek listázásakor, a submittedBefore és submittedAfter paraméterekre történő szűrés esetén.
* Web Apps
  - A Swap-AzureRmWebAppSlot parancsmag hozzáadása a normál felcserélés és a felcserélés előnézettel műveletek esetében
  - A Set-AzureRmWebAppSlot parancsmag kiterjesztése az automatikus felcserélés támogatásához
* Azure API Management
  - Az Azure API Management telepítési parancsmagjainak javítása az AzureChinaCloud esetében.
  - A Set-AzureRmApiManagementTenantGitAccess parancsmag eltávolítása, mivel a Git-hozzáférés alapértelmezés szerint engedélyezve van.
* Azure Recovery Services Backup
  - Az Azure SQL számítási feladatok támogatása
  - A titkosított Azure virtuális gépek biztonsági mentésének és helyreállításának támogatása
  - Backup-AzureRmRecoveryServicesBackupItem – Opcionális adatmegőrzési idő funkció hozzáadása a helyreállítási pontok esetében
  - Kisebb, szűréssel kapcsolatos hibák javítása a Get-AzureRmRecoveryServicesBackupContainer és Get-AzureRmRecoveryServicesBackupItem parancsmagok esetében
* Azure Automation
  - A Get-AzureRmAutomationHybridWorkerGroup parancsmag hozzáadása
