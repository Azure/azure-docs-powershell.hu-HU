---
title: A Microsoft Azure PowerShell Az 1.0.0 kompatibilitástörő változásai
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 1-es verziójában található kompatibilitástörő változások listáját.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153474"
---
# <a name="migration-guide-for-az-100"></a>Migrálási útmutató az Az 1.0.0-s verziójához

Ez a dokumentum ismerteti, hogy milyen módosítások történtek az AzureRM 6.x-es verziói és az Az 1.0.0-s verzió között.

## <a name="table-of-contents"></a>Tartalomjegyzék
- [Általános kompatibilitástörő változások](#general-breaking-changes)
  - [A parancsmag főnévi előtagjának változásai](#cmdlet-noun-prefix-changes)
  - [A modul nevének változásai](#module-name-changes)
  - [Eltávolított modulok](#removed-modules)
  - [Windows PowerShell 5.1 és .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [A felhasználói bejelentkezés ideiglenes eltávolítása a PSCredential használatával](#temporary-removal-of-user-login-using-pscredential)
  - [Bejelentkezés alapértelmezett eszközkóddal a webböngészőben megjelenő kérdés helyett](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [A modul kompatibilitástörő változásai](#module-breaking-changes)
  - [Az.ApiManagement (korábban AzureRM.ApiManagement)](#azapimanagement-previously-azurermapimanagement)
  - [Az.Billing (korábban AzureRM.Billing, AzureRM.Consumption és AzureRM.UsageAggregates)](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [Az.CognitiveServices (korábban AzureRM.CognitiveServices)](#azcognitiveservices-previously-azurermcognitiveservices)
  - [Az.Compute (korábban AzureRM.Compute)](#azcompute-previously-azurermcompute)
  - [Az.DataFactory (korábban AzureRM.DataFactories és AzureRM.DataFactoryV2)](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [Az.DataLakeAnalytics (korábban AzureRM.DataLakeAnalytics)](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [Az.DataLakeStore (korábban AzureRM.DataLakeStore)](#azdatalakestore-previously-azurermdatalakestore)
  - [Az.KeyVault (korábban AzureRM.KeyVault)](#azkeyvault-previously-azurermkeyvault)
  - [Az.Media (korábban AzureRM.Media)](#azmedia-previously-azurermmedia)
  - [Az.Monitor (korábban AzureRM.Insights)](#azmonitor-previously-azurerminsights)
  - [Az.Network (korábban AzureRM.Network)](#aznetwork-previously-azurermnetwork)
  - [Az.OperationalInsights (korábban AzureRM.OperationalInsights)](#azoperationalinsights-previously-azurermoperationalinsights)
  - [Az.RecoveryServices (korábban AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup és AzureRM.RecoveryServices.SiteRecovery)](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [Az.Resources (korábban AzureRM.Resources)](#azresources-previously-azurermresources)
  - [Az.ServiceFabric (korábban AzureRM.ServiceFabric)](#azservicefabric-previously-azurermservicefabric)
  - [Az.Sql (korábban AzureRM.Sql)](#azsql-previously-azurermsql)
  - [Az.Storage (korábban Azure.Storage és AzureRM.Storage)](#azstorage-previously-azurestorage-and-azurermstorage)
  - [Az.Websites (korábban AzureRM.Websites)](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a>Általános kompatibilitástörő változások
### <a name="cmdlet-noun-prefix-changes"></a>A parancsmag főnévi előtagjának változásai
Az AzureRM-ben a parancsmagok az „AzureRM” vagy az „Azure” főnévi előtagot használják.  Az Az egyszerűsíti és normalizálja a parancsmagok nevét, így minden parancsmag főnévi előtagja „Az” lesz. Például:
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

A következőre módosult:
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

Az új parancsmagokra való áttérés megkönnyítése érdekében az Az két új parancsmagot (```Enable-AzureRmAlias``` és ```Disable-AzureRmAlias```) tartalmaz.  Az ```Enable-AzureRmAlias``` az újabb Az-parancsmagok nevéhez aliasokat hoz létre a korábbi AzureRM-parancsmagok nevéből.  A parancsmag lehetővé teszi aliasok létrehozását az aktuális munkamenetben, vagy akár több munkamenet során, a felhasználói vagy a gépprofil váltása után. 

A következő AzureRM-szkript például:
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Az ```Enable-AzureRmAlias``` használatával minimális változtatásokkal futtatható:
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Az ```Enable-AzureRmAlias -Scope CurrentUser``` futtatása elérhetővé teszi az aliasokat minden megnyitott PowerShell-munkamenetben, így a parancsmag végrehajtása után az ehhez hasonló szkripteket egyáltalán nem kell módosítani:
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

A parancsmagok aliasaival kapcsolatos részletes információkért futtassa a ```Get-Help -Online Enable-AzureRmAlias``` parancsot a PowerShell-parancssorból.

A ```Disable-AzureRmAlias``` eltávolítja az ```Enable-AzureRmAlias``` által létrehozott AzureRM-parancsmagaliasokat.  Részletes információkért futtassa a ```Get-Help -Online Disable-AzureRmAlias``` parancsot a PowerShell-parancssorból.

### <a name="module-name-changes"></a>A modul nevének változásai
- A modul neve a korábbi `AzureRM.*` helyett `Az.*` lett, kivéve a következő modulokban:
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

A modul nevének változása azt jelenti, hogy ha egy szkript a ```#Requires``` vagy az ```Import-Module``` használatával tölt be bizonyos modulokat, módosításokat kell végezni az új modul használatához.

#### <a name="migrating-requires-statements"></a>#Requires-utasítások migrálása
Amennyiben egy szkript a #Requires használatával deklarálja függőségét egy AzureRM-modultól, frissíteni kell azt az új modulnevekkel.
```powershell
#Requires -Module AzureRM.Compute
```

A következőre kell módosítani:
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a>Import-Module-utasítások migrálása
Amennyiben egy szkript az ```Import-Module``` használatával tölt be AzureRM-modulokat, frissíteni kell azt az új modulnevekkel.
```powershell
Import-Module -Name AzureRM.Compute
```

A következőre kell módosítani:
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Teljesen minősített parancsmaghívások migrálása
Modulhoz minősített parancsmaghívásokat használó szkriptek, például:
```powershell
AzureRM.Compute\Get-AzureRmVM
```

Úgy kell módosítani, hogy az új modul- és parancsmagneveket használja
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Moduljegyzék-függőségek migrálása
Amennyiben egy modul AzureRM-modultól való függését egy moduljegyzék (.psd1) fájl fejezi ki, a modul „RequiredModules” szakaszában frissíteni kell a modulok nevét.

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

A következőre kell módosítani:

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Eltávolított modulok
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

E szolgáltatások eszközállománya már nem aktívan támogatott.  Azt javasoljuk ügyfeleinknek, hogy amint lehetséges, térjenek át más szolgáltatások használatára.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 és .NET 4.7.2
- Az Az Windows PowerShell 5.1-gyel történő használatához szükséges a .NET 4.7.2 telepítése. Az Az PowerShell Core-ral történő használatához ugyanakkor nem szükséges a .NET 4.7.2 megléte. 

### <a name="temporary-removal-of-user-login-using-pscredential"></a>A felhasználói bejelentkezés ideiglenes eltávolítása a PSCredential használatával
- A .NET Standard hitelesítési folyamatának változásai miatt ideiglenesen eltávolítjuk a PSCredential használatával történő felhasználói bejelentkezés lehetőségét. A funkció a Windows PowerShell 5.1 2019. január 15-én megjelenő verziójában válik ismét elérhetővé. Erről részletesen [ebben a cikkben](https://github.com/Azure/azure-powershell/issues/7430) írtunk.

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Bejelentkezés alapértelmezett eszközkóddal a webböngészőben megjelenő kérdés helyett
- A .NET Standard hitelesítési folyamatának változásai miatt az interaktív bejelentkezések során az eszközről történő bejelentkezés lesz az alapértelmezett bejelentkezési folyamat. A webböngésző-alapú bejelentkezés a Windows PowerShell 5.1 2019. január 15-én megjelenő verziójában válik ismét elérhetővé. Ezt követően a felhasználók a Switch paramétert használva választhatják az eszközről történő bejelentkezést.

## <a name="module-breaking-changes"></a>A modul kompatibilitástörő változásai

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (korábban AzureRM.ApiManagement)
- A következő parancsmagok el lettek távolítva:
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Ezeket a tulajdonságokat mostantól a **Set-AzApiManagement** parancsmaggal kell beállítani.
- A következő tulajdonságok el lettek távolítva
  - A `PsApiManagementHostnameConfiguration` típus `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` és `ScmHostnameConfiguration` tulajdonsága el lett távolítva a `PsApiManagementContext`ből. Ezek helyett a `PsApiManagementCustomHostNameConfiguration` típus `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` és `ScmCustomHostnameConfiguration` tulajdonságát használja.
  - A `StaticIPs` tulajdonság el lett távolítva a PsApiManagementContextből. Két új tulajdonságra lett osztva: ez a `PublicIPAddresses` és a `PrivateIPAddresses`.
  - A kötelező `Location` tulajdonság el lett távolítva a New-AzureApiManagementVirtualNetwork parancsmagból.

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a>Az.Billing (korábban AzureRM.Billing, AzureRM.Consumption és AzureRM.UsageAggregates)
- A `Get-AzConsumptionUsageDetail` parancsmag `InvoiceName` paramétere el lett távolítva.  A szkripteknek a számlák készítéséhez más identitásparamétereket kell használniuk.

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a>Az.CognitiveServices (korábban AzureRM.CognitiveServices)
- A `Get-AzCognitiveServicesAccountSkus` parancsmag `GetSkusWithAccountParamSetName` paramétere el lett távolítva.  A termékváltozatokat a fiók típusa és helye alapján lehet lekérdezni a ResourceGroupName és a fiók nevének használata helyett.

### <a name="azcompute-previously-azurermcompute"></a>Az.Compute (korábban AzureRM.Compute)
- A `PSVirtualMachine` és `PSVirtualMachineScaleSet` objektum `Identity` tulajdonsága mostantól nem tartalmazza az `IdentityIds` azonosítókat. A szkriptek a jövőben nem veszik figyelembe a mező értékét a feldolgozási döntések során.
- A `PSVirtualMachineScaleSetVM` objektum `InstanceView` tulajdonságának típusa `VirtualMachineInstanceView` helyett `VirtualMachineScaleSetVMInstanceView` lett.
- Az `UpgradePolicy` tulajdonság `AutoOSUpgradePolicy` és `AutomaticOSUpgrade` tulajdonsága el lett távolítva.
- A `PSSnapshotUpdate` objektum `Sku` tulajdonságának típusa `DiskSku` helyett `SnapshotSku` lett.
- Az `Add-AzVMDataDisk` parancsmagból el lett távolítva a `VmScaleSetVMParameterSet`. Mostantól nem lehet önálló adatlemezt hozzáadni egy ScaleSet-virtuálisgéphez.

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a>Az.DataFactory (korábban AzureRM.DataFactories és AzureRM.DataFactoryV2)
- A `New-AzDataFactoryEncryptValue` parancsmagban kötelezővé vált a `GatewayName` paraméter használata.
- A `New-AzDataFactoryGatewayKey` parancsmag el lett távolítva.
- A `Get-AzDataFactoryV2ActivityRun` parancsmag `LinkedServiceName` paramétere el lett távolítva. A szkriptek a jövőben nem veszik figyelembe a mező értékét a feldolgozási döntések során.

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a>Az.DataLakeAnalytics (korábban AzureRM.DataLakeAnalytics)
- El lettek távolítva a következő elavult parancsmagok: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, és `Set-AzDataLakeAnalyticsCatalogSecret`

### <a name="azdatalakestore-previously-azurermdatalakestore"></a>Az.DataLakeStore (korábban AzureRM.DataLakeStore)
- A következő parancsmagok `Encoding` paraméterének típusa `FileSystemCmdletProviderEncoding` helyett `System.Text.Encoding` lett. Ez a módosítás eltávolítja a `String` és `Oem` kódolási értéket. Az összes egyéb korábbi kódolási érték elérhető marad.
  - New-AzureRmDataLakeStoreItem
  - Add-AzureRmDataLakeStoreItemContent
  - Get-AzureRmDataLakeStoreItemContent
- A `New-AzDataLakeStoreAccount` és `Set-AzDataLakeStoreAccount` parancsmag elavult `Tags` tulajdonságaliasa el lett távolítva.

  A következőt használó szkripteket:
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  A következőre kell módosítani:
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- A ```PSDataLakeStoreAccountBasic``` objektum elavult tulajdonságai el lettek távolítva: ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier``` és ```FirewallAllowAzureIps```.  A ```Get-AzDataLakeStoreAccount``` által visszaadott ```PSDatalakeStoreAccount``` értéket használó szkriptek nem hivatkozhatnak ezekre a tulajdonságokra.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (korábban AzureRM.KeyVault)
- A `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` és `PSKeyVaultSecretAttributes` objektum `PurgeDisabled` tulajdonsága el lett távolítva. A szkriptek a jövőben nem hivatkozhatnak a ```PurgeDisabled``` tulajdonságra a feldolgozási döntések során.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (korábban AzureRM.Media)
- A `New-AzMediaService` parancsmag elavult `Tags` tulajdonságaliasa el lett távolítva. A következőt használó szkripteket:
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  A következőre kell módosítani:
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (korábban AzureRM.Insights)
- A `Categories` és a `Timegrains` többes számú paraméternév el lett távolítva. Ezek helyett a `Set-AzDiagnosticSetting` parancsmag egyes számú paraméterneveit kell használni. A következőt használó szkripteket:
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  A következőre kell módosítani:
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (korábban AzureRM.Network)
- A `Get-AzServiceEndpointPolicyDefinition` parancsmag elavult `ResourceId` paramétere el lett távolítva.
- A `PSVirtualNetwork` objektum elavult `EnableVmProtection` tulajdonsága el lett távolítva.
- Az elavult `Set-AzVirtualNetworkGatewayVpnClientConfig` parancsmag el lett távolítva.
  
A szkriptek a jövőben nem hozhatnak feldolgozási döntéseket e mezők értéke alapján.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (korábban AzureRM.OperationalInsights)
- A `Get-AzOperationalInsightsDataSource` alapértelmezett paraméterkészlete el lett távolítva. Mostantól a `ByWorkspaceNameByKind` az alapértelmezett paraméterkészlet.

  Azokat a szkripteket, amelyek a következő használatával listázták az adatforrásokat:
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  Úgy kell módosítani, hogy megadjanak egy altípust:
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a>Az.RecoveryServices (korábban AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup és AzureRM.RecoveryServices.SiteRecovery)
- A `New/Set-AzRecoveryServicesAsrPolicy` parancsmag `Encryption` paramétere el lett távolítva.
- A `TargetStorageAccountName` paraméter megadása mostantól kötelező a `Restore-AzRecoveryServicesBackupItem` parancsmag felügyeltlemez-visszaállítási műveleteihez.
- A `Restore-AzRecoveryServicesBackupItem` parancsmag `StorageAccountName` és `StorageAccountResourceGroupName` paramétere el lett távolítva.
- A `Get-AzRecoveryServicesBackupContainer` parancsmag `Name` paramétere el lett távolítva

### <a name="azresources-previously-azurermresources"></a>Az.Resources (korábban AzureRM.Resources)
- A `New/Set-AzPolicyAssignment` parancsmag `Sku` paramétere el lett távolítva.
- A `New-AzADServicePrincipal` és `New-AzADSpCredential` parancsmag `Password` paramétere el lett távolítva. A jelszavak létrehozása automatikusan történik, a korábban jelszót biztosító szkripteket:
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Úgy kell módosítani, hogy a jelszót a kimenetből kérjék le:
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (korábban AzureRM.ServiceFabric)
- Módosítottuk a következő parancsmag visszatérési típusait:
  - Az `ApplicationHealthPolicy` típus `SerivceTypeHealthPolicies` tulajdonsága el lett távolítva.
  - A `ClusterUpgradeDeltaHealthPolicy` típus `ApplicationHealthPolicies` tulajdonsága el lett távolítva.
  - A `ClusterUpgradePolicy` típus `OverrideUserUpgradePolicy` tulajdonsága el lett távolítva.
  - Ezek a módosítások a következő parancsmagokat érintik:
    - Add-AzServiceFabricClientCertificate
    - Add-AzServiceFabricClusterCertificate
    - Add-AzServiceFabricNode
    - Add-AzServiceFabricNodeType
    - Get-AzServiceFabricCluster
    - Remove-AzServiceFabricClientCertificate
    - Remove-AzServiceFabricClusterCertificate
    - Remove-AzServiceFabricNode
    - Remove-AzServiceFabricNodeType
    - Remove-AzServiceFabricSetting
    - Set-AzServiceFabricSetting
    - Set-AzServiceFabricUpgradeType
    - Update-AzServiceFabricDurability
    - Update-AzServiceFabricReliability

### <a name="azsql-previously-azurermsql"></a>Az.Sql (korábban AzureRM.Sql)
- A `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` parancsmag `State` és `ResourceId` paramétere el lett távolítva.
- A következő, elavult parancsmagok el lettek távolítva: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing` és `Remove-AzSqlServerAuditing`.
- A `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` parancsmag elavult `Current` paramétere el lett távolítva.
- A `Get-AzSqlServerServiceObjective` parancsmag elavult `DatabaseName` paramétere el lett távolítva.
- A `Set-AzSqlDatabaseDataMaskingPolicy` parancsmag elavult `PrivilegedLogin` paramétere el lett távolítva.

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a>Az.Storage (korábban Azure.Storage és AzureRM.Storage)
- Annak érdekében, hogy létre lehessen hozni egy Oauth Storage-környezetet pusztán a tárfiók nevét használva, az új alapértelmezett paraméterkészlet a következő: `OAuthParameterSet`
  - Például: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`
- A `Get-AzStorageUsage` parancsmagban kötelezővé vált a `Location` paraméter használata.
- A Storage API-metódusok mostantól feladatalapú aszinkron mintát (TAP) használnak az egyidejű API-hívások helyett.
#### <a name="1-blob-snapshot"></a>1. Blob-pillanatképek
##### <a name="before"></a>Előtte:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a>Utána:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a>2. Megosztási pillanatképek
##### <a name="before"></a>Előtte:
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a>Utána:
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a>3. Blob helyreállítható törlésének visszavonása
##### <a name="before"></a>Előtte:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a>Utána:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a>4. Blobszint beállítása
##### <a name="before"></a>Előtte:
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a>Utána:
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (korábban AzureRM.Websites)
- A `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` és `PSSite` objektum elavult tulajdonságai el lettek távolítva.