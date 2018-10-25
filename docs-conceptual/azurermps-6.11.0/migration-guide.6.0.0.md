---
title: A Microsoft Azure PowerShell 6.0.0 kompatibilitástörő változásai
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell 6-os verziójában található kompatibilitástörő változások listáját.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 8b7b1422ba2881ca172e65dba61d4c4808cca7de
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/25/2018
ms.locfileid: "50000878"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>A Microsoft Azure PowerShell 6.0.0 kompatibilitástörő változásai

Ez a dokumentum egyrészt értesítőül szolgál a használhatatlanná tévő változtatásokról, másrészt egy migrálási útmutató az Azure PowerShell-parancsmagok felhasználóinak. Minden szakasz tárgyalja a használhatatlanná tévő változások okát, valamint a legkisebb ellenállással járó migrálási módot is. A körülmények részletesebb leírásáért tekintse meg az egyes változásokhoz tartozó lekérési kérelmeket.

## <a name="table-of-contents"></a>Tartalomjegyzék

- [Általános kompatibilitástörő változások](#general-breaking-changes)
    - [PowerShell minimálisan szükséges verziója: 5.0](#minimum-powershell-version-required-bumped-to-50)
    - [Környezet automatikus mentése alapértelmezés szerint engedélyezve](#context-autosave-enabled-by-default)
    - [A Tags alias eltávolítása](#removal-of-tags-alias)
- [Az AzureRM.Compute-parancsmagok kompatibilitástörő változásai](#breaking-changes-to-azurermcompute-cmdlets)
- [Az AzureRM.DataLakeStore-parancsmagok kompatibilitástörő változásai](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [Az AzureRM.Dns-parancsmagok kompatibilitástörő változásai](#breaking-changes-to-azurermdns-cmdlets)
- [Az AzureRM.Insights-parancsmagok kompatibilitástörő változásai](#breaking-changes-to-azurerminsights-cmdlets)
- [Az AzureRM.KeyVault-parancsmagok kompatibilitástörő változásai](#breaking-changes-to-azurermkeyvault-cmdlets)
- [Az AzureRM.Network-parancsmagok kompatibilitástörő változásai](#breaking-changes-to-azurermnetwork-cmdlets)
- [Az AzureRM.RedisCache-parancsmagok kompatibilitástörő változásai](#breaking-changes-to-azurermrediscache-cmdlets)
- [Az AzureRM.Resources-parancsmagok kompatibilitástörő változásai](#breaking-changes-to-azurermresources-cmdlets)
- [Az AzureRM.Storage-parancsmagok kompatibilitástörő változásai](#breaking-changes-to-azurermstorage-cmdlets)
- [Eltávolított modulok](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>Általános kompatibilitástörő változások

### <a name="minimum-powershell-version-required-bumped-to-50"></a>PowerShell minimálisan szükséges verziója: 5.0

Korábban az Azure PowerShellnek _legalább_ a PowerShell 3.0-s verziójára volt szüksége bármely parancsmag futtatásához. A továbbiakban ez a követelmény a PowerShell 5.0-s verziójára változik. A PowerShell 5.0-s verziójára történő frissítéssel kapcsolatos információkért lásd [ezt a táblázatot](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

### <a name="context-autosave-enabled-by-default"></a>Környezet alapértelmezés szerinti automatikus mentése

A környezet automatikus mentése azon Azure-beli bejelentkezési adatok tárolását jelenti, amelyek a PowerShell új és eltérő munkamenetei között használhatók. A környezet automatikus mentéséről további információt [ebben a dokumentumban](https://docs.microsoft.com/powershell/azure/context-persistence) talál.

A környezet automatikus mentése le volt tiltva korábban alapértelmezés szerint le volt tiltva, ami azt jelentette, hogy a felhasználó Azure-beli hitelesítési adatait nem tárolta a rendszer a munkamenetek között, amíg a környezetmegőrzést engedélyező `Enable-AzureRmContextAutosave` parancsmag nem lett futtatva. Ezután a környezet automatikus mentése alapértelmezés szerint engedélyezve lesz, ami azt jelenti, hogy a _környezet automatikus mentésére vonatkozó beállításokkal nem rendelkező felhasználók_ esetén a környezet a következő bejelentkezéstől kezdve lesz tárolva. Ezt a funkciót a `Disable-AzureRmContextAutosave` parancsmag használatával lehet felülbírálni.

_Megjegyzés:_ A változás nem érinti azokat a felhasználókat, akik korábban letiltották a környezet automatikus mentését, vagy engedélyezték azt, és rendelkeznek meglévő környezettel

### <a name="removal-of-tags-alias"></a>A Tags alias eltávolítása

A `Tag` paraméter `Tags` aliasa több parancsmag esetén is el lett távolítva. Az alábbi lista tartalmazza az érintett modulokat (és a hozzájuk tartozó parancsmagokat):

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>Az AzureRM.Compute-parancsmagok kompatibilitástörő változásai

**Egyéb**
- A `PSDisk` és `PSSnapshot` típus beágyazott termékváltozat-tulajdonsága `StandardLRS` és `PremiumLRS` értékről `Standard_LRS` és `Premium_LRS` értékre változott

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- A `PSVirtualMachine`, `PSVirtualMachineScaleSet` és `PSImage` típus beágyazott tárfióktípus-tulajdonsága `StandardLRS` és `PremiumLRS` értékről `Standard_LRS` és `Premium_LRS` értékre változott

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**
- A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

**Add-AzureRmVMDataDisk**
- A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

**Add-AzureRmVmssDataDisk**
- A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

**New-AzureRmAvailabilitySet**
- A `Managed` paraméter el lett távolítva, és helyébe a `Sku` lépett

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- A `SkuName` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

**New-AzureRmDiskUpdateConfig**
- A `SkuName` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

**New-AzureRmSnapshotConfig**
- A `SkuName` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

**New-AzureRmSnapshotUpdateConfig**
- A `SkuName` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

**Set-AzureRmImageOsDisk**
- A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

**Set-AzureRmVMAEMExtension**
- A `DisableWAD` paraméter el lett távolítva
    -  A Microsoft Azure Diagnostics alapértelmezés szerint le van tiltva

**Set-AzureRmVMDataDisk**
- A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

**Set-AzureRmVMOSDisk**
- A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

**Set-AzureRmVmssStorageProfile**
- A `ManagedDisk` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

**Update-AzureRmVmss**
- A `ManagedDiskStorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>Az AzureRM.DataLakeStore-parancsmagok kompatibilitástörő változásai

**Export-AzureRmDataLakeStoreItem**
- A `PerFileThreadCount` és a `ConcurrentFileCount` paraméter el lett távolítva. A továbbiakban a `Concurrency` paramétert használhatja

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- A `PerFileThreadCount` és a `ConcurrentFileCount` paraméter el lett távolítva. A továbbiakban a `Concurrency` paramétert használhatja

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- A `Clean` paraméter el lett távolítva

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>Az AzureRM.Dns-parancsmagok kompatibilitástörő változásai

**New-AzureRmDnsRecordSet**
- A `Force` paraméter el lett távolítva

**Remove-AzureRmDnsRecordSet**
- A `Force` paraméter el lett távolítva

**Remove-AzureRmDnsZone**
- A `Force` paraméter el lett távolítva

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>Az AzureRM.Insights-parancsmagok kompatibilitástörő változásai

**Add-AzureRmAutoscaleSetting**
- A `AutoscaleProfiles` és `Notifications` paraméteralias el lett távolítva

**Add-AzureRmLogProfile**
- A `Categories` és `Locations` paraméteralias el lett távolítva

**Add-AzureRmMetricAlertRule**
- A `Actions` paraméteralias el lett távolítva

**Add-AzureRmWebtestAlertRule**
- A `Actions` paraméteralias el lett távolítva

**Get-AzureRmLog**
- A `MaxRecords` és `MaxEvents` paraméteralias el lett távolítva

**Get-AzureRmMetricDefinition**
- A `MetricNames` paraméteralias el lett távolítva

**New-AzureRmAlertRuleEmail**
- A `CustomEmails` és `SendToServiceOwners` paraméteralias el lett távolítva

**New-AzureRmAlertRuleWebhook**
- A `Properties` paraméteralias el lett távolítva

**New-AzureRmAutoscaleNotification**
- A `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` és `Webhooks` paraméteralias el lett távolítva

**New-AzureRmAutoscaleProfile**
- A `Rules`, `ScheduleDays`, `ScheduleHours` és `ScheduleMinutes` paraméteralias el lett távolítva

**New-AzureRmAutoscaleWebhook**
- A `Properties` paraméteralias el lett távolítva

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>Az AzureRM.KeyVault-parancsmagok kompatibilitástörő változásai

**Add-AzureKeyVaultCertificate**
- A `CertificatePolicy` paraméter használata kötelezővé vált.

**Set-AzureKeyVaultManagedStorageSasDefinition**
- A parancsmag többé már nem fogad olyan paramétereket, amelyek a hozzáférési jogkivonatot határozzák meg. Ehelyett a parancsmag lecseréli az olyan kifejezett jogkivonat-paramétereket, mint a `Service` és a `Permissions` egy általános `TemplateUri` paraméterre, amely egy máshol (valószínűleg Storage PowerShell-parancsmagokkal vagy a Storage-dokumentáció alapján manuálisan) meghatározott hozzáférési mintajogkivonatnak feleltethető meg. A parancsmag megőrzi a `ValidityPeriod` paramétert.

Az Azure Storage megosztott hozzáférési jogkivonatok létrehozásával kapcsolatos további információiért tekintse meg az alábbi dokumentációs oldalakat:
- [SAS-szolgáltatás létrehozása] (https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)
- [SAS-fiók létrehozása] (https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

**Set-AzureKeyVaultCertificateIssuer**
- A `IssuerProvider` paraméter használata kötelezővé vált.

**Undo-AzureKeyVaultCertificateRemoval**
- A parancsmag kimenete `CertificateBundle` értékről `PSKeyVaultCertificate` értékre változott.

**Undo-AzureRmKeyVaultRemoval**
- A `ResourceGroupName` el lett távolítva az `InputObject` paraméterkészletből, és ehelyett az `InputObject` paraméter `ResourceId` tulajdonságából lesz származtatva.

**Set-AzureRmKeyVaultAccessPolicy**
- Az `all` engedély el lett távolítva a `PermissionsToKeys`, `PermissionsToSecrets` és `PermissionsToCertificates` esetén.

**Általános**
- A `ValueFromPipelineByPropertyName` tulajdonság el lett távolítva az összes olyan parancsmagból, ahol az `InputObject` általi átirányítás engedélyezve volt.  Az érintett parancsmagok az alábbiak:
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- A `ConfirmImpact`-szintek el lettek távolítva az összes parancsmagból.  Az érintett parancsmagok az alábbiak:
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- Az `IKeyVaultDataServiceClient` frissítve lett, ezáltal az összes tanúsítványművelet PS-típust ad vissza SDK-típus helyett. Az érintett műveletek közé tartoznak az alábbiak:
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>Az AzureRM.Network-parancsmagok kompatibilitástörő változásai


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- A `ProbeEnabled` paraméter el lett távolítva

**Add-AzureRmVirtualNetworkPeering**
- A `AlloowGatewayTransit` paraméteralias el lett távolítva

**New-AzureRmApplicationGatewayBackendHttpSettings**
- A `ProbeEnabled` paraméter el lett távolítva

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- A `ProbeEnabled` paraméter el lett távolítva

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>Az AzureRM.RedisCache-parancsmagok kompatibilitástörő változásai

**New-AzureRmRedisCache**
- A `Subnet` és `VirtualNetwork` paraméter el lett távolítva, és a helyükbe a `SubnetId` lépett
- A `RedisVersion` paraméter el lett távolítva
- A `MaxMemoryPolicy` paraméter el lett távolítva, és helyébe a `RedisConfiguration` lépett

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- A `MaxMemoryPolicy` paraméter el lett távolítva, és helyébe a `RedisConfiguration` lépett

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>Az AzureRM.Resources-parancsmagok kompatibilitástörő változásai

**Find-AzureRmResource**
- A parancsmag el lett távolítva, és a funkcióit mostantól a `Get-AzureRmResource` teszi elérhetővé

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- A parancsmag el lett távolítva, és a funkcióit mostantól a `Get-AzureRmResourceGroup` teszi elérhetővé

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

**Get-AzureRmRoleDefinition**
- Az `AtScopeAndBelow` paraméter el lett távolítva.

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>Az AzureRM.Storage-parancsmagok kompatibilitástörő változásai

**New-AzureRmStorageAccount**
- A `EnableEncryptionService` paraméter el lett távolítva

**Set-AzureRmStorageAccount**
- Az `EnableEncryptionService` és a `DisableEncryptionService` paraméter el lett távolítva

## <a name="removed-modules"></a>Eltávolított modulok

### `AzureRM.ServerManagement`

A Server Management Tools szolgáltatás a [múlt évben ki lett vezetve](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), ezért az SMT megfelelő modulja, az `AzureRM.ServerManagement` el lett távolítva az `AzureRM`-ből, és a továbbiakban nem lesz érhető.

### `AzureRM.SiteRecovery`

A `AzureRM.SiteRecovery` modult felváltja az `AzureRM.RecoveryServices.SiteRecovery`, ami az `AzureRM.SiteRecovery` modul bővebb tulajdonságokkal rendelkező változata, és új, a korábbiak működését biztosító parancsmagokkal rendelkezik. A régi parancsmagok az újakba történő leképezésének listáját az alábbiakban találja:

| Elavult parancsmag                                        | Egyenértékű parancsmag                                                | Aliasok                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
