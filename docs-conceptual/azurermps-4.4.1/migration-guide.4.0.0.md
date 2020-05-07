---
title: A Microsoft Azure PowerShell 4.0.0 használhatatlanná tévő változásai
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell 4-es verziójában található kompatibilitástörő változások listáját.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 2f61e41b701dfc263df18064f6ac2cc4c6e4021e
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "67863555"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a>A Microsoft Azure PowerShell 4.0.0 használhatatlanná tévő változásai

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Ez a dokumentum egyrészt értesítőül szolgál a használhatatlanná tévő változtatásokról, másrészt egy migrálási útmutató az Azure PowerShell-parancsmagok felhasználóinak. Minden szakasz tárgyalja a használhatatlanná tévő változások okát, valamint a legkisebb ellenállással járó migrálási módot is. A körülmények részletesebb leírásáért tekintse meg az egyes változásokhoz tartozó lekérési kérelmeket.

## <a name="table-of-contents"></a>Tartalomjegyzék

- [A Compute-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-compute-cmdlets)
- [Az EventHub-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-eventhub-cmdlets)
- [Az Insights-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-insights-cmdlets)
- [A Network-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-network-cmdlets)
- [A ServiceBus-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-servicebus-cmdlets)
- [Az SQL-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-sql-cmdlets)
- [A Storage-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-storage-cmdlets)
- [A Profile-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a>A Compute-parancsmagok használhatatlanná tévő változásai

A kiadás a következő kimeneti típusokat érinti:

### <a name="psvirtualmachine"></a>PSVirtualMachine
- A `DataDiskNames` objektum `NetworkInterfaceIDs` és `PSVirtualMachine` legfelsőbb szintű tulajdonságai el lettek távolítva a kimenettípusból. Ezek a tulajdonságok eddig is elérhetőek voltak a `StorageProfile` objektum `NetworkProfile` és `PSVirtualMachine` tulajdonságaiban, és ezentúl csak innen lehet hozzájuk férni.
- A módosítás a következő parancsmagokat érinti:
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell-interactive
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Az EventHub-parancsmagok használhatatlanná tévő változásai

A kiadás a következő parancsmagokat érinti:

### <a name="get-azurermeventhubnamespace"></a>Get-AzureRmEventHubNamespace
- A `ResourceGroupName` tulajdonság el lett távolítva a `NamespaceAttributes` kimenettípusból.

### <a name="new-azurermeventhubnamespace"></a>New-AzureRmEventHubNamespace
- A `ResourceGroupName` tulajdonság el lett távolítva a `NamespaceAttributes` kimenettípusból.

## <a name="breaking-changes-to-insights-cmdlets"></a>Az Insights-parancsmagok használhatatlanná tévő változásai

A kiadás a következő parancsmagokat érinti:
    
### <a name="get-azurermusage"></a>Get-AzureRmUsage
- Ez a parancsmag elavult.

### <a name="remove-azurermalertrule"></a>Remove-AzureRmAlertRule
- A parancsmag kimenete (korábban egy egyetlen objektumból álló lista) egy objektumra módosult; ez az objektum tartalmazza a kérés azonosítóját és az állapotkódot.
    
```powershell-interactive
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a>Add-AzureRmLogAlertRule
- Ez a parancsmag elavult.
    
### <a name="get-azurermalertrule"></a>Get-AzureRmAlertRule
- A parancsmag kimenetének (egy objektumlistának) az összes eleme egybe lett simítva, azaz a rendszer az objektumokat az `{ Id, Location, Name, Tags, Properties }` struktúra helyett az `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` struktúrával adja vissza, amely magában foglalja egy Azure-erőforrás, valamint egy AlertRuleResource összes legfelsőbb szintű tulajdonságát.
    
```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a>Get-AzureRmAutoscaleSetting
- Az `AutoscaleSettingResourceName` mező elavult, mivel az értéke mindig megegyezik a `Name` mező értékével.

```powershell-interactive
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a>Remove-AzureRmLogProfile
- A parancsmag kimenete `Boolean` értékről egy `RequestId` és `StatusCode` tulajdonságot tartalmazó objektumra módosul.

```powershell-interactive
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a>Add-AzureRmLogProfile
- A parancsmag kimenete egy olyan objektumra módosul, amely tartalmazza a kérés azonosítóját és az állapotkódot, valamint a frissített vagy újonnan létrehozott erőforrást.
    
```powershell-interactive
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a>Set-AzureRmDiagnosticSettings
- A parancs új nevet kap: `Update-AzureRmDiagnosticSettings`

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a>A Network-parancsmagok használhatatlanná tévő változásai

A kiadás a következő parancsmagokat érinti:

### <a name="new-azurermvirtualnetworkgatewayconnection"></a>New-AzureRmVirtualNetworkGatewayConnection
- Az `EnableBgp` paraméter értéke `boolean` helyett `string` lett

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>A ServiceBus-parancsmagok használhatatlanná tévő változásai

A kiadás a következő parancsmagokat érinti:

### <a name="get-azurermservicebusnamespace"></a>Get-AzureRmServiceBusNamespace
- A `ResourceGroupName` tulajdonság el lett távolítva a `NamespaceAttributes` kimenettípusból.

### <a name="new-azurermservicebusnamespace"></a>New-AzureRmServiceBusNamespace

- A `ResourceGroupName` tulajdonság el lett távolítva a `NamespaceAttributes` kimenettípusból.

## <a name="breaking-changes-to-sql-cmdlets"></a>Az SQL-parancsmagok használhatatlanná tévő változásai

A kiadás a következő parancsmagokat érinti:

### <a name="new-azurermsqldatabasefailovergroup"></a>New-AzureRmSqlDatabaseFailoverGroup
- A `Tag` paraméter el lett távolítva
- A `GracePeriodWithDataLossHour` paraméter új nevet kapott: `GracePeriodWithDataLossHours`

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a>Set-AzureRmSqlDatabaseFailoverGroup
- A `Tag` paraméter el lett távolítva
- A `GracePeriodWithDataLossHour` paraméter új nevet kapott: `GracePeriodWithDataLossHours`

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a>Add-AzureRmSqlDatabaseToFailoverGroup
- A `Tag` paraméter el lett távolítva

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a>Remove-AzureRmSqlDatabaseFromFailoverGroup
- A `Tag` paraméter el lett távolítva

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a>Remove-AzureRmSqlDatabaseFailoverGroup
- A `PartnerResourceGroupName` paraméter el lett távolítva
- A `PartnerServerName` paraméter el lett távolítva

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a>Set-AzureRmSqlDatabaseThreatDetectionPolicy
- A `Usage_Anomaly` érték már nem érvényes az `ExcludedDetectionType` paraméterhez

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a>Set-AzureRmSqlServerThreatDetectionPolicy
- A `Usage_Anomaly` érték már nem érvényes az `ExcludedDetectionType` paraméterhez

## <a name="breaking-changes-to-storage-cmdlets"></a>A Storage-parancsmagok használhatatlanná tévő változásai

A kiadás a következő kimenettípus-tulajdonságokat érinti:

### <a name="azurestorageblobicloudblobserviceclient"></a>AzureStorageBlob.ICloudBlob.ServiceClient
- A következő tulajdonságok lettek eltávolítva a típusból (_megjegyzés_: ezek továbbra is megtalálhatók a `DefaultRequestOptions` tulajdonság alatt):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- A módosítás a következő parancsmagokat érinti:
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a>AzureStorageContainer.CloudBlobContainer.ServiceClient
- A következő tulajdonságok lettek eltávolítva a típusból (_megjegyzés_: ezek továbbra is megtalálhatók a `DefaultRequestOptions` tulajdonság alatt):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- A módosítás a következő parancsmagokat érinti:
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a>AzureStorageQueue.CloudQueue.ServiceClient
- A következő tulajdonságok lettek eltávolítva a típusból (_megjegyzés_: ezek továbbra is megtalálhatók a `DefaultRequestOptions` tulajdonság alatt):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- A módosítás a következő parancsmagokat érinti:
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a>AzureStorageTable.CloudTable.ServiceClient
- A következő tulajdonságok lettek eltávolítva a típusból (_megjegyzés_: ezek továbbra is megtalálhatók a `DefaultRequestOptions` tulajdonság alatt):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- A módosítás a következő parancsmagokat érinti:
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell-interactive
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a>A profilparancsmagok használhatatlanná tévő változásai

A kiadás a következő parancsmagokat és a parancsmagok következő kimeneti típusait érintette:

### <a name="add-azurermaccount-breaking-changes"></a>Az Add-AzureRmAccount használhatatlanná tévő változásai

- Az ```EnvironmentName``` paraméter el lett távolítva, és az ```Environment``` lépett a helyébe. Az ```Environment``` most már egy sztringet vesz fel egy ```AzureEnvironment``` objektum helyett.

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a>A Select-AzureRmProfile új nevet kapott: Import-AzureRmContext

A ```Select-AzureRmProfile``` új nevet kapott: ```Import-AzureRmContext```

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a>A Save-AzureRmProfile új nevet kapott: Save-AzureRmContext

A ```Save-AzureRmProfile``` új nevet kapott: ```Save-AzureRmContext```

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a>A PSAzureContext típusú kimenet használhatatlanná tévő változásai

- A ```TokenCache``` tulajdonság olyan típusra módosult, amely ```IAzureTokenCache``` elemet implementál ```byte[]``` helyett

```powershell-interactive
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a>A PSAzureAccount típusú kimenet használhatatlanná tévő változásai

- A ```AccountType``` tulajdonság a következőre módosult: ```Type```

```powershell-interactive
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a>A PSAzureSubscription típusú kimenet használhatatlanná tévő változásai
- A ```SubscriptionId``` tulajdonság a következőre módosult: ```Id```

```powershell-interactive
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- A ```SubscriptionName``` tulajdonság a következőre módosult: ```Name```

```powershell-interactive
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a>A PSAzureTenant típusú kimenet használhatatlanná tévő változásai

- A ```TenantId``` tulajdonság a következőre módosult: ```Id```

```powershell-interactive
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- A ```Domain``` tulajdonság a következőre módosult: ```Directory```

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
