---
title: Az AzureRM és az Azure PowerShell Az 1.0.0 közötti összes változás
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 1-es verziójában található kompatibilitástörő változások listáját.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: 6c2d681144fe561e734a247c44046e3dadb78083
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387819"
---
# <a name="breaking-changes-for-az-100"></a>Az Az 1.0.0 kompatibilitástörő változásai

Ez a dokumentum részletes információkat tartalmaz az AzureRM 6.x és az új Az modul 1.x és újabb verziója közötti változásokról. A tartalomjegyzék végigvezeti a teljes migrálási folyamaton, és bemutatja a modulspecifikus módosításokat is, amelyek befolyásolhatják a szkripteket.

Az AzureRM-ből az Az-be történő migrálás megkezdéséhez kapcsolódó általános tanácsokért lásd: [Migrálás megkezdése az AzureRM-ből az Az-be](migrate-from-azurerm-to-az.md).

> [!IMPORTANT]
> Az Az 1.0.0-s és az Az 2.0.0-s verziója között is történtek kompatibilitástörő változások. Az AzureRM-ről Az-re való frissítést ismertető útmutató követése után tekintse meg az [Az 2.0.0 kompatibilitástörő változásait](migrate-az-2.0.0.md) bemutató cikket, amelyből megtudhatja, kell-e további módosításokat végeznie.

## <a name="table-of-contents"></a>Tartalomjegyzék

- [Általános kompatibilitástörő változások](#general-breaking-changes)
  - [A parancsmag főnévi előtagjának változásai](#cmdlet-noun-prefix-changes)
  - [A modul nevének változásai](#module-name-changes)
  - [Eltávolított modulok](#removed-modules)
  - [Windows PowerShell 5.1 és .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [A felhasználói bejelentkezés ideiglenes eltávolítása a PSCredential használatával](#temporary-removal-of-user-login-using-pscredential)
  - [Bejelentkezés alapértelmezett eszközkóddal a webböngészőben megjelenő kérdés helyett](#default-device-code-login-instead-of-web-browser-prompt)
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

Ez a szakasz részletesen bemutatja az Az modul újratervezésének részét képező általános kompatibilitástörő változásokat.

### <a name="cmdlet-noun-prefix-changes"></a>A parancsmag főnévi előtagjának változásai

Az AzureRM modulban a parancsmagok az `AzureRM` vagy az `Azure` főnévi előtagot használták.  Az Az egyszerűsíti és normalizálja a parancsmagok nevét, így minden parancsmag főnévi előtagja „Az” lesz. Például:

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

A következőre módosult:

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

Az új parancsmagokra való áttérés megkönnyítése érdekében az Az két új parancsmagot vezet be: [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) és [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).  Az `Enable-AzureRmAlias` a régebbi parancsmagok nevéhez hoz létre aliasokat az AzureRM-ben, amelyek az újabb Az-parancsmagok nevének felelnek meg. A `-Scope` argumentum és az `Enable-AzureRmAlias` együttes használatával kiválaszthatja, hol legyenek engedélyezve az aliasok.

A következő AzureRM-szkript például:

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Az `Enable-AzureRmAlias` használatával minimális változtatásokkal futtatható:

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Az `Enable-AzureRmAlias -Scope CurrentUser` futtatása engedélyezi az aliasokat az összes megnyitott PowerShell-munkamenetben, így a parancsmag végrehajtása után az ehhez hasonló szkripteket egyáltalán nem kell módosítani:

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

A parancsmagok aliasaival kapcsolatos részletes információért tekintse meg az [Enable-AzureRmAlias referenciáját](/powershell/module/az.accounts/enable-azurermalias).

Amikor készen áll az aliasok letiltására, a `Disable-AzureRmAlias` eltávolítja a létrehozott aliasokat. Részletes információért tekintse meg a [Disable-AzureRmAlias referenciáját](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> Az aliasok letiltásakor győződjön meg arról, hogy _minden_ olyan hatókörnél le lettek tiltva, amelyekhez engedélyezve voltak az aliasok.

### <a name="module-name-changes"></a>A modul nevének változásai

A modul neve a korábbi `AzureRM.*` helyett `Az.*` lett, kivéve a következő modulokban:

| AzureRM modul | Az modul |
|----------------|-----------|
| Azure.Storage | Az.Storage |
| Azure.AnalysisServices | Az.AnalysisServices |
| AzureRM.Profile | Az.Accounts |
| AzureRM.Insights | Az.Monitor |
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |
| AzureRM.Tags | Az.Resources |
| AzureRM.MachineLearningCompute | Az.MachineLearning |
| AzureRM.UsageAggregates | Az.Billing |
| AzureRM.Consumption | Az.Billing |

A modul nevének változása azt jelenti, hogy ha egy szkript a `#Requires` vagy az `Import-Module` használatával tölt be bizonyos modulokat, módosításokat kell végezni az új modul használatához. Azoknál a moduloknál, ahol a parancsmag utótagja nem változott, ez azt jelenti, hogy a modul neve megváltozott, a művelet helyét jelző utótag viszont _nem_.

#### <a name="migrating-requires-and-import-module-statements"></a>#Requires és Import-Module utasítások migrálása

Ha egy szkript `#Requires` vagy `Import-Module` használatával deklarálja egy AzureRM-modultól való függőségét, akkor frissíteni kell az új modulnevek használatára. Például:

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

A következőre kell módosítani:

```azurepowershell-interactive
#Requires -Module Az.Compute
```

`Import-Module` esetében:

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

A következőre kell módosítani:

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Teljesen minősített parancsmaghívások migrálása

Modulhoz minősített parancsmaghívásokat használó szkriptek, például:

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

Úgy kell módosítani, hogy az új modul- és parancsmagneveket használja:

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Moduljegyzék-függőségek migrálása

Amennyiben egy modul AzureRM-modultól való függését egy moduljegyzék (.psd1) fájl fejezi ki, a modul `RequiredModules` szakaszában frissíteni kell a modulok nevét:

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

A következőre kell módosítani:

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Eltávolított modulok

Az alábbi modulok lettek eltávolítva:

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

E szolgáltatások eszközeit már nem támogatja aktívan a rendszer.  Azt javasoljuk ügyfeleinknek, hogy amint lehetséges, térjenek át más szolgáltatások használatára.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 és .NET 4.7.2

Az Az Windows PowerShell 5.1-gyel történő használatához szükséges a .NET-keretrendszer 4.7.2 telepítése. A PowerShell Core 6.x vagy újabb verziójának használatához nincs szükség a .NET-keretrendszerre.

### <a name="temporary-removal-of-user-login-using-pscredential"></a>A felhasználói bejelentkezés ideiglenes eltávolítása a PSCredential használatával

A .NET Standard hitelesítési folyamatának változásai miatt ideiglenesen eltávolítjuk a PSCredential használatával történő felhasználói bejelentkezés lehetőségét. A funkció a Windows PowerShell 5.1 2019. január 15-én megjelenő verziójában válik ismét elérhetővé. Erről részletesen [ebben a GitHub-cikkben](https://github.com/Azure/azure-powershell/issues/7430) olvashat.

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Bejelentkezés alapértelmezett eszközkóddal a webböngészőben megjelenő kérdés helyett

A .NET Standard hitelesítési folyamatának változásai miatt az interaktív bejelentkezések során az eszközről történő bejelentkezés lesz az alapértelmezett bejelentkezési folyamat. A webböngésző-alapú bejelentkezés a Windows PowerShell 5.1 2019. január 15-én megjelenő verziójában válik ismét elérhetővé. Ezt követően a felhasználók a Switch paramétert használva választhatják az eszközről történő bejelentkezést.

## <a name="module-breaking-changes"></a>A modul kompatibilitástörő változásai

Ez a szakasz részletesen bemutatja az egyes modulok és parancsmagok kompatibilitástörő változásait.

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (korábban AzureRM.ApiManagement)

- A következő parancsmagok lettek eltávolítva:
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Ezeket a tulajdonságokat mostantól a **Set-AzApiManagement** parancsmaggal kell beállítani
- A következő tulajdonságok lettek eltávolítva:
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
- A `VmScaleSetVMParameterSet` el lett távolítva az `Add-AzVMDataDisk` parancsmagból, mostantól nem lehet önálló adatlemezt hozzáadni egy ScaleSet-virtuálisgéphez.

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
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  A következőre kell módosítani:
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- A `PSDataLakeStoreAccountBasic` objektum elavult tulajdonságai el lettek távolítva: `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier` és `FirewallAllowAzureIps`.  A `Get-AzDataLakeStoreAccount` által visszaadott `PSDatalakeStoreAccount` értéket használó szkriptek nem hivatkozhatnak ezekre a tulajdonságokra.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (korábban AzureRM.KeyVault)

- A `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` és `PSKeyVaultSecretAttributes` objektum `PurgeDisabled` tulajdonsága el lett távolítva. A szkriptek a jövőben nem hivatkozhatnak a ```PurgeDisabled``` tulajdonságra a feldolgozási döntések során.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (korábban AzureRM.Media)

- A `New-AzMediaService` parancsmag elavult `Tags` tulajdonságaliasa el lett távolítva. A következőt használó szkripteket:
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  A következőre kell módosítani:
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (korábban AzureRM.Insights)

- A `Categories` és a `Timegrains` többes számú paraméternév el lett távolítva. Ezek helyett a `Set-AzDiagnosticSetting` parancsmag egyes számú paraméterneveit kell használni. A következőt használó szkripteket:
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  A következőre kell módosítani:
  ```azurepowershell-interactive
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
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  Úgy kell módosítani, hogy megadjanak egy altípust:
  ```azurepowershell-interactive
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

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Úgy kell módosítani, hogy a kimenetből kérjék le a jelszót:

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (korábban AzureRM.ServiceFabric)

- Módosítottuk a következő parancsmag visszatérési típusait:
  - Az `ApplicationHealthPolicy` típus `ServiceTypeHealthPolicies` tulajdonsága el lett távolítva.
  - Az `ClusterUpgradeDeltaHealthPolicy` típus `ApplicationHealthPolicies` tulajdonsága el lett távolítva.
  - Az `ClusterUpgradePolicy` típus `OverrideUserUpgradePolicy` tulajdonsága el lett távolítva.
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
- A Storage API-metódusok mostantól feladatalapú aszinkron mintát (TAP) használnak az egyidejű API-hívások helyett. Az alábbi példák az új, aszinkron parancsokat mutatják be:

#### <a name="blob-snapshot"></a>Blob-pillanatképek

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

Az:

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a>Megosztási pillanatképek

AzureRM:

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

Az:

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a>Blob helyreállítható törlésének visszavonása

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

Az:

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a>Blobszint beállítása

AzureRM:

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

Az:

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (korábban AzureRM.Websites)

- A `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` és `PSSite` objektum elavult tulajdonságai el lettek távolítva.
