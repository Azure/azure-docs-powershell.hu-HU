---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Kibocsátási megjegyzések

Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.

---

## <a name="600---may-2018"></a>6.0.0 – 2018. május

### <a name="general"></a>Általános kérdések
* A PowerShell 5.0 beállítása mint a modulok minimális függősége

### <a name="azurestorage"></a>Azure.Storage
* Az Azure Storage-blobtárolók neve alapján történő támogatás
    - New-AzureStorageBlobContainer
    - Remove-AzureStorageBlobContainer
    - Set-AzureStorageBlobContent
    - Get-AzureStorageBlobContent
* Probléma kijavítása, amely során bizonyos Storage-parancsmagok hibakimenete nem tartalmazott részletes információt a hibáról

### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Több kompatibilitástörő változás bevezetése
    - További információért tekintse meg a migrálási útmutatót

### <a name="azurermautomation"></a>AzureRM.Automation
* Elavult címkék aliasának eltávolítása a parancsmagokból
    - Set-AzureRmAutomationRunbook

### <a name="azurermbatch"></a>AzureRM.Batch
* Frissült a New-AzureBatchPool dokumentációja, amelyből egy elavult példa el lett távolítva

### <a name="azurermcdn"></a>AzureRM.Cdn
* Több kompatibilitástörő változás bevezetése
    - További információért tekintse meg a migrálási útmutatót

### <a name="azurermcompute"></a>AzureRM.Compute
* A New-AzureRmVm és a New-AzureRmVmss támogatja a paraméterek részletes kimenetét
* A New-AzureRmVm és a New-AzureRmVmss (egyszerű paraméterkészlet) támogatja az identitások meghatározását a virtuális gépek számára felhasználók és (vagy) rendszerek által.
* VMSS Redeploy és PerformMaintenance funkció
    -  Az új -Redeploy és -PerformMaintenance kapcsolóparaméter hozzáadása a Set-AzureRmVmss és Set-AzureRmVmssVM parancshoz
* Az új DisableVMAgent kapcsolóparaméter hozzáadása a Set-AzureRmVMOperatingSystem parancsmaghoz
* A New-AzureRmVm és a New-AzureRmVmss (egyszerű paraméterkészlet) támogatja a Windows 10-rendszerképet.
* Új Repair-AzureRmVmssServiceFabricUpdateDomain parancsmag.
* Több kompatibilitástörő változás bevezetése
    - További információért tekintse meg a migrálási útmutatót
* A Set-AzureRmVmDiskEncryptionExtension az AAD-paramétereket opcionálissá teszi

### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Elavult címkék aliasának eltávolítása a parancsmagokból
    - New-AzureRmDataFactory

### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Az ADF .Net SDK frissítése a 0.7.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:
    - Új végrehajtási paraméterek és kapcsolatkezelő tulajdonságok az ExecuteSSISPackage tevékenységhez
    - A PostgreSql, MySql társított szolgáltatás frissítése teljes kapcsolati karakterlánc használatára, a kiszolgáló, adatbázis, séma, felhasználónév és jelszó használata helyett
    - A séma eltávolítása a DB2 társított szolgáltatásból
    - Sématulajdonság eltávolítása a Teradata társított szolgáltatásból
    - LinkedService, Dataset és CopySource hozzáadása a Responsyshez

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Elavult címkék aliasának eltávolítása a parancsmagokból
    - New-AzureRmDataLakeAnalyticsAccount
    - Set-AzureRmDataLakeAnalyticsAccount

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Új rekurzív Acl-módosítási funkció hozzáadása a következőkhöz: Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl
* Új parancsmag hozzáadása a tartalomösszegzés egy címtárban történő lekéréséhez
* Új parancsmag hozzáadása a lemezhasználat és Acl-memóriakép lekéréséhez
* A Set-AzureRmDataLakeStoreItemAcl logikai érték visszatérési típusának javítása IEnumerable típusra<DataLakeStoreItemAce>
* A Set-AzureRmDataLakeStoreItemAclEntry logikai érték visszatérési típusának javítása IEnumerable típusra<DataLakeStoreItemAce>
* Kompatibilitástörő változások az alábbiakban: Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem

### <a name="azurermdns"></a>AzureRM.Dns
* Több kompatibilitástörő változás bevezetése
    - További információért tekintse meg a migrálási útmutatót

### <a name="azurermeventhub"></a>AzureRM.EventHub
* A parancsmagok súgója frissítve lett a hiányzó példákkal

### <a name="azurerminsights"></a>AzureRM.Insights
* Több kompatibilitástörő változás bevezetése
    - További információért tekintse meg a migrálási útmutatót

### <a name="azurermiothub"></a>AzureRM.IotHub
* Címkék és alapszintű termékváltozat engedélyezése az IoTHub számára

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Átirányítási forgatókönyveket támogató kompatibilitástörő változások
* Az alábbi új parancsmagok hozzáadása: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval és Undo-AzureKeyVaultManagedStorageAccountRemoval

### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Elavult címkék aliasának eltávolítása a parancsmagokból
    - Update-AzureRmMlCommitmentPlan

### <a name="azurermmedia"></a>AzureRM.Media
* Elavult címkék aliasának eltávolítása a parancsmagokból
    - Set-AzureRmMediaService

### <a name="azurermnetwork"></a>AzureRM.Network
* A DDoS-védelem támogatása erőforrás-tervezéshez
* Több kompatibilitástörő változás bevezetése
    - További információért tekintse meg a migrálási útmutatót

### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Több kompatibilitástörő változás bevezetése
    - További információért tekintse meg a migrálási útmutatót

### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Több kompatibilitástörő változás bevezetése
    - További információért tekintse meg a migrálási útmutatót

### <a name="azurermprofile"></a>AzureRM.Profile
* A környezet automatikus mentése alapértelmezés szerint engedélyezve van
* A USGovernmentOperationalInsightsEndpoint és USGovernmentOperationalInsightsEndpointResourceId tulajdonság hozzáadása az USA-beli államigazgatásban használt Azure-környezethez.

### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* A SiteRecovery-forgatókönyvek során használt hitelesítési fejléc javítása

### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Több kompatibilitástörő változás bevezetése
    - További információért tekintse meg a migrálási útmutatót

### <a name="azurermresources"></a>AzureRM.Resources
* Az elavult -AtScopeAndBelow paraméter eltávolítása a Get-AzureRmRoledefinition hívásából
* Hozzárendelések hozzáadása a törölt felhasználókhoz/csoportokhoz/szolgáltatásnevekhez a Get-AzureRmRoleAssignment eredményében
* Scope és ResourceType lapkiegészítő hozzáadása
* Egyszerűsített parancsmag hozzáadása szolgáltatásnevek létrehozásához
* A lekérési és keresési funkció egyesítése a Get-AzureRmResource esetén
* AD-parancsmagok hozzáadása:
  - Remove-AzureRmADGroupMember
  - Get-AzureRmADGroup
  - New-AzureRmADGroup
  - Remove-AzureRmADGroup
  - Remove-AzureRmADUser
  - Update-AzureRmADApplication
  - Update-AzureRmADServicePrincipal
  - Update-AzureRmADUser

### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Az alapértelmezett linuxos rendszerképverzió termékváltozatának frissítése
  - A NewAzureServiceFabricCluster.cs alapértelmezett UbuntuServer1604-termékváltozatának frissítése

### <a name="azurermstorage"></a>AzureRM.Storage
* Több kompatibilitástörő változás bevezetése
    - További információért tekintse meg a migrálási útmutatót

### <a name="azurermwebsites"></a>AzureRM.Websites
* Frissítés a Websites SDK legújabb verziójára
* Új -AssignIdentity és -Httpsonly tulajdonság a Set-AzureRmWebApp és a Set-AzureRmWebAppSlot esetén
* Két új parancsmag hozzáadva: Get-AzureRmWebAppSnapshots és Restore-AzureRmWebAppSnapshot
