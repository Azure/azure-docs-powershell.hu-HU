---
title: Migrálási útmutató az Az 3.0.0-s verziójához
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 3.0-s verziójában található kompatibilitástörő változások listáját.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 641804fc0931d29f082ef7057f610beb75d7550a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856422"
---
# <a name="migration-guide-for-az-300"></a><span data-ttu-id="a1453-103">Migrálási útmutató az Az 3.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="a1453-103">Migration Guide for Az 3.0.0</span></span>

<span data-ttu-id="a1453-104">Ez a dokumentum ismerteti, hogy milyen módosítások történtek az Az 2.0.0-s és 3.0.0-s verziója között</span><span class="sxs-lookup"><span data-stu-id="a1453-104">This document describes the changes between the 2.0.0 and 3.0.0 versions of Az</span></span>

<!-- TOC -->

- [<span data-ttu-id="a1453-105">Migrálási útmutató az Az 3.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="a1453-105">Migration Guide for Az 3.0.0</span></span>](#migration-guide-for-az-300)
  - [<span data-ttu-id="a1453-106">Batch</span><span class="sxs-lookup"><span data-stu-id="a1453-106">Batch</span></span>](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [<span data-ttu-id="a1453-107">Inkompatibilitás az `Az.Resources` korábbi verzióival</span><span class="sxs-lookup"><span data-stu-id="a1453-107">Incompatibility with previous versions of `Az.Resources`</span></span>](#previous-version-incompatibility-with-azresources-module)
  - [<span data-ttu-id="a1453-108">Számítás</span><span class="sxs-lookup"><span data-stu-id="a1453-108">Compute</span></span>](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [<span data-ttu-id="a1453-109">HDInsight</span><span class="sxs-lookup"><span data-stu-id="a1453-109">HDInsight</span></span>](#hdinsight)
    - [`Get-AzHDInsightJobOutput`](#get-azhdinsightjoboutput)
    - [`Add-AzHDInsightConfigValues`](#add-azhdinsightconfigvalues)
    - [`Disable-AzHDInsightMonitoring`](#disable-azhdinsightmonitoring)
    - [`Enable-AzHDInsightMonitoring`](#enable-azhdinsightmonitoring)
    - [`Get-AzHDInsightMonitoring`](#get-azhdinsightmonitoring)
    - [`Get-AzHDInsightProperty`](#get-azhdinsightproperty)
    - [`Grant-AzHDInsightRdpServicesAccess`](#grant-azhdinsightrdpservicesaccess)
    - [`Remove-AzHDInsightCluster`](#remove-azhdinsightcluster)
    - [`Revoke-AzHDInsightRdpServicesAccess`](#revoke-azhdinsightrdpservicesaccess)
    - [`Set-AzHDInsightGatewayCredential`](#set-azhdinsightgatewaycredential)
  - [<span data-ttu-id="a1453-110">IoTHub</span><span class="sxs-lookup"><span data-stu-id="a1453-110">IotHub</span></span>](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [<span data-ttu-id="a1453-111">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a1453-111">RecoveryServices</span></span>](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [<span data-ttu-id="a1453-112">Erőforrások</span><span class="sxs-lookup"><span data-stu-id="a1453-112">Resources</span></span>](#resources)
    - [<span data-ttu-id="a1453-113">Inkompatibilitás az `Az.Batch` korábbi verzióival</span><span class="sxs-lookup"><span data-stu-id="a1453-113">Incompatibility with previous versions of `Az.Batch`</span></span>](#previous-version-incompatibility-with-azbatch-module)
  - [<span data-ttu-id="a1453-114">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a1453-114">ServiceFabric</span></span>](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [<span data-ttu-id="a1453-115">Sql</span><span class="sxs-lookup"><span data-stu-id="a1453-115">Sql</span></span>](#sql)
    - [`Get-AzSqlDatabaseSecureConnectionPolicy`](#get-azsqldatabasesecureconnectionpolicy)
    - [`Get-AzSqlDatabaseIndexRecommendations`](#get-azsqldatabaseindexrecommendations)
    - [`Get-AzSqlDatabaseRestorePoints`](#get-azsqldatabaserestorepoints)
    - [`Get-AzSqlDatabaseAuditing`](#get-azsqldatabaseauditing)
    - [`Set-AzSqlDatabaseAuditing`](#set-azsqldatabaseauditing)
    - [`Get-AzSqlServerAuditing`](#get-azsqlserverauditing)
    - [`Set-AzSqlServerAuditing`](#set-azsqlserverauditing)
    - [`Get-AzSqlServerAdvancedThreatProtectionSettings`](#get-azsqlserveradvancedthreatprotectionsettings)
    - [`Clear-AzSqlServerAdvancedThreatProtectionSettings`](#clear-azsqlserveradvancedthreatprotectionsettings)
    - [`Update-AzSqlServerAdvancedThreatProtectionSettings`](#update-azsqlserveradvancedthreatprotectionsettings)
    - [`Get-AzSqlDatabaseAdvancedThreatProtectionSettings`](#get-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseAdvancedThreatProtectionSettings`](#update-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`](#clear-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseVulnerabilityAssessmentSettings`](#update-azsqldatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlDatabaseVulnerabilityAssessmentSettings`](#get-azsqldatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`](#clear-azsqldatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#update-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#get-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#clear-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceVulnerabilityAssessmentSettings`](#update-azsqlinstancevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceVulnerabilityAssessmentSettings`](#get-azsqlinstancevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceVulnerabilityAssessmentSettings`](#clear-azsqlinstancevulnerabilityassessmentsettings)
    - [`Update-AzSqlServerVulnerabilityAssessmentSettings`](#update-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerVulnerabilityAssessmentSettings`](#get-azsqlservervulnerabilityassessmentsettings)
    - [`Clear-AzSqlServerVulnerabilityAssessmentSettings`](#clear-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerAdvancedThreatProtectionPolicy`](#get-azsqlserveradvancedthreatprotectionpolicy)
    - [`Get-AzSqlServerThreatDetectionPolicy`](#get-azsqlserverthreatdetectionpolicy)
    - [`Remove-AzSqlServerThreatDetectionPolicy`](#remove-azsqlserverthreatdetectionpolicy)
    - [`Set-AzSqlServerThreatDetectionPolicy`](#set-azsqlserverthreatdetectionpolicy)
    - [`Get-AzSqlDatabaseThreatDetectionPolicy`](#get-azsqldatabasethreatdetectionpolicy)
    - [`Set-AzSqlDatabaseThreatDetectionPolicy`](#set-azsqldatabasethreatdetectionpolicy)
    - [`Remove-AzSqlDatabaseThreatDetectionPolicy`](#remove-azsqldatabasethreatdetectionpolicy)

<!-- /TOC -->


## <a name="batch"></a><span data-ttu-id="a1453-116">Batch</span><span class="sxs-lookup"><span data-stu-id="a1453-116">Batch</span></span>

### `Get-AzBatchNodeAgentSku`
- <span data-ttu-id="a1453-117">A `Get-AzBatchNodeAgentSku` el lett távolítva, és a `Get-AzBatchSupportedImage` lépett a helyébe.</span><span class="sxs-lookup"><span data-stu-id="a1453-117">Removed `Get-AzBatchNodeAgentSku` and replaced it with  `Get-AzBatchSupportedImage`.</span></span>
- <span data-ttu-id="a1453-118">A `Get-AzBatchSupportedImage` ugyanazokat az adatokat jeleníti meg, mint a `Get-AzBatchNodeAgentSku`, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="a1453-118">`Get-AzBatchSupportedImage` returns the same data as `Get-AzBatchNodeAgentSku` but in a more friendly format.</span></span>
- <span data-ttu-id="a1453-119">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="a1453-119">New non-verified images are also now returned.</span></span> <span data-ttu-id="a1453-120">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="a1453-120">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-121">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-121">Before</span></span>
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a><span data-ttu-id="a1453-122">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-122">After</span></span>
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a><span data-ttu-id="a1453-123">Az előző verziók inkompatibilitása az Az.Resources modullal</span><span class="sxs-lookup"><span data-stu-id="a1453-123">Previous Version Incompatibility with Az.Resources Module</span></span>
<span data-ttu-id="a1453-124">Az „Az.Batch” modul 2.0.1-es verziója nem kompatibilis az „Az.Resources” modul korábbi verzióival (1.7.0-s vagy korábbi verziók).</span><span class="sxs-lookup"><span data-stu-id="a1453-124">Version 2.0.1 of the ‘Az.Batch’ module is incompatible with earlier versions (version 1.7.0 or earlier) of the ‘Az.Resources’ module.</span></span>  <span data-ttu-id="a1453-125">Ez azt eredményezi, hogy nem lehet importálni az „Az.Resources” modul 1.7.0-s verzióját, ha az „Az.Batch” modul 2.0.1-es verziója importálva van.</span><span class="sxs-lookup"><span data-stu-id="a1453-125">This will result in being unable to import  version 1.7.0 of the ‘Az.Resources’ module when version 2.0.1 of the ‘Az.Batch’ module is imported.</span></span>  <span data-ttu-id="a1453-126">A probléma megoldásához egyszerűen csak frissítse az „Az.Resources” modult az 1.7.1-es vagy újabb verzióra, vagy telepítse az „Az” modul legújabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="a1453-126">To fix this issue, simply update the ‘Az.Resources’ module to version 1.7.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="compute"></a><span data-ttu-id="a1453-127">Számítás</span><span class="sxs-lookup"><span data-stu-id="a1453-127">Compute</span></span>

### `New-AzDiskConfig`
<span data-ttu-id="a1453-128">A `New-AzDiskConfig` esetében a `DiskSizeGB` paraméter helyett az `UploadSizeInBytes` paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="a1453-128">`UploadSizeInBytes` parameter is used instead of `DiskSizeGB` for `New-AzDiskConfig` when CreateOption is Upload</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-129">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-129">Before</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a><span data-ttu-id="a1453-130">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-130">After</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a><span data-ttu-id="a1453-131">HDInsight</span><span class="sxs-lookup"><span data-stu-id="a1453-131">HDInsight</span></span>

### `Get-AzHDInsightJobOutput`
- <span data-ttu-id="a1453-132">Frissült a `Get-AzHDInsightJobOutput` parancsmag, és mostantól támogatja a tárkulcshoz való részletes szerepköralapú hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="a1453-132">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
- <span data-ttu-id="a1453-133">Ez nem érinti a HDInsight-fürt operátor, közreműködő vagy tulajdonos szerepkörrel rendelkező felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="a1453-133">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
- <span data-ttu-id="a1453-134">A csak olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a `DefaultStorageAccountKey` paramétert.</span><span class="sxs-lookup"><span data-stu-id="a1453-134">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-135">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-135">Before</span></span>
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a><span data-ttu-id="a1453-136">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-136">After</span></span>
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
<span data-ttu-id="a1453-137">A `Add-AzHDInsightConfigValue` parancsmag eltávolította az aliast a következőből: `Add-AzHDInsightConfigValues`.</span><span class="sxs-lookup"><span data-stu-id="a1453-137">Cmdlet `Add-AzHDInsightConfigValue` removed alias to `Add-AzHDInsightConfigValues`.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-138">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-138">Before</span></span>
<span data-ttu-id="a1453-139">Elavult alias használata</span><span class="sxs-lookup"><span data-stu-id="a1453-139">Using deprecated alias</span></span>
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a><span data-ttu-id="a1453-140">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-140">After</span></span>
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
<span data-ttu-id="a1453-141">Új `Disable-AzHDInsightMonitoring` parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a1453-141">Added a new `Disable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="a1453-142">A parancsmag használatával letilthatja a monitorozást a HDInsight-fürtökön (a következőket cseréli le: `Disable-AzHDInsightOperationsManagementSuite` és `Disable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="a1453-142">Use this cmdlet to disable monitoring in a HDInsight cluster (replaces `Disable-AzHDInsightOperationsManagementSuite` and `Disable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-143">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-143">Before</span></span>
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="a1453-144">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-144">After</span></span>
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
<span data-ttu-id="a1453-145">Új `Enable-AzHDInsightMonitoring` parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a1453-145">Added a new `Enable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="a1453-146">A parancsmag használatával engedélyezheti a monitorozást a HDInsight-fürtökön (a következőket cseréli le: `Enable-AzHDInsightOperationsManagementSuite` és `Enable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="a1453-146">Use this cmdlet to enable monitoring in a HDInsight cluster (replaces `Enable-AzHDInsightOperationsManagementSuite` and `Enable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-147">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-147">Before</span></span>
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a><span data-ttu-id="a1453-148">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-148">After</span></span>
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
<span data-ttu-id="a1453-149">Új `Get-AzHDInsightMonitoring` parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a1453-149">Added a new `Get-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="a1453-150">A parancsmag használatával lekérheti a monitorozás telepítésének állapotát az Azure HDInsight-fürtökön (a következőket cseréli le: `Get-AzHDInsightOperationsManagementSuite` és `Get-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="a1453-150">Use this cmdlet to get the status of monitoring installation in an Azure HDInsight cluster (replaces `Get-AzHDInsightOperationsManagementSuite` and `Get-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-151">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-151">Before</span></span>
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="a1453-152">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-152">After</span></span>
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
<span data-ttu-id="a1453-153">A `Get-HDInsightProperty` parancsmag eltávolította az aliast a következőből: `Get-AzHDInsightProperties`.</span><span class="sxs-lookup"><span data-stu-id="a1453-153">Cmdlet `Get-HDInsightProperty` removed alias to `Get-AzHDInsightProperties`.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-154">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-154">Before</span></span>
<span data-ttu-id="a1453-155">Elavult alias használata</span><span class="sxs-lookup"><span data-stu-id="a1453-155">Using deprecated alias</span></span>
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a><span data-ttu-id="a1453-156">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-156">After</span></span>
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
<span data-ttu-id="a1453-157">A `Grant-AzHDInsightRdpServicesAccess` és a `Revoke-AzHDInsightRdpServicesAccess` parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="a1453-157">Removed the `Grant-AzHDInsightRdpServicesAccess` and `Revoke-AzHDInsightRdpServicesAccess` cmdlets.</span></span> <span data-ttu-id="a1453-158">Már nincs szükség rájuk, mivel a Windows operációs rendszert használó fürtök nem támogatottak.</span><span class="sxs-lookup"><span data-stu-id="a1453-158">These are no longer necessary because clusters using Windows OS type are not supported.</span></span> <span data-ttu-id="a1453-159">Hozzon létre helyettük egy Linux operációs rendszert használó fürtöt.</span><span class="sxs-lookup"><span data-stu-id="a1453-159">Please create a cluster using Linux OS type instead.</span></span>

### `Remove-AzHDInsightCluster`
<span data-ttu-id="a1453-160">A `Remove-AzHDInsightCluster` kimeneti típusa `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` értékről `bool` értékre változott.</span><span class="sxs-lookup"><span data-stu-id="a1453-160">The output type of `Remove-AzHDInsightCluster` changed from `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` to `bool`.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-161">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-161">Before</span></span>
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a><span data-ttu-id="a1453-162">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-162">After</span></span>
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
<span data-ttu-id="a1453-163">A parancsmag elavult.</span><span class="sxs-lookup"><span data-stu-id="a1453-163">The cmdlet is deprecated.</span></span> <span data-ttu-id="a1453-164">Nincs helyettesítő parancsmag.</span><span class="sxs-lookup"><span data-stu-id="a1453-164">There is no replacement for it.</span></span>

### `Set-AzHDInsightGatewayCredential`
<span data-ttu-id="a1453-165">A `Set-AzHDInsightGatewayCredential` kimeneti típusa `HttpConnectivitySettings` értékről `AzureHDInsightGatewaySettings` értékre változott.</span><span class="sxs-lookup"><span data-stu-id="a1453-165">The output type of `Set-AzHDInsightGatewayCredential` changed from `HttpConnectivitySettings` to `AzureHDInsightGatewaySettings`.</span></span>



## <a name="iothub"></a><span data-ttu-id="a1453-166">IoTHub</span><span class="sxs-lookup"><span data-stu-id="a1453-166">IotHub</span></span>

### `New-AzIotHubImportDevices`
<span data-ttu-id="a1453-167">Ez az alias el lett távolítva, használja helyette a következőt: `New-AzIotHubImportDevice`.</span><span class="sxs-lookup"><span data-stu-id="a1453-167">This alias is removed, please use `New-AzIotHubImportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-168">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-168">Before</span></span>
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a><span data-ttu-id="a1453-169">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-169">After</span></span>
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
<span data-ttu-id="a1453-170">Ez az alias el lett távolítva, használja helyette a következőt: `New-AzIotHubExportDevice`.</span><span class="sxs-lookup"><span data-stu-id="a1453-170">This alias is removed, please use `New-AzIotHubExportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-171">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-171">Before</span></span>
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a><span data-ttu-id="a1453-172">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-172">After</span></span>
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="a1453-173">Az `EventHubEndPointName` paraméter elavult, és nem lehet lecserélni, mivel az IotHub csak egy beépített végpontot tartalmaz („events”), ami kezelni tudja a rendszer- és eszközüzeneteket.</span><span class="sxs-lookup"><span data-stu-id="a1453-173">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-174">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-174">Before</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="a1453-175">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-175">After</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="a1453-176">Az `EventHubEndPointName` paraméter elavult, és nem lehet lecserélni, mivel az IotHub csak egy beépített végpontot tartalmaz („events”), ami kezelni tudja a rendszer- és eszközüzeneteket.</span><span class="sxs-lookup"><span data-stu-id="a1453-176">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-177">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-177">Before</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="a1453-178">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-178">After</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="a1453-179">Az `EventHubEndPointName` paraméter elavult, és nem lehet lecserélni, mivel az IotHub csak egy beépített végpontot tartalmaz („events”), ami kezelni tudja a rendszer- és eszközüzeneteket.</span><span class="sxs-lookup"><span data-stu-id="a1453-179">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-180">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-180">Before</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="a1453-181">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-181">After</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
<span data-ttu-id="a1453-182">Az `OperationsMonitoringProperties` paraméter elavult, és nem lehet lecserélni, mivel az IotHub már nem használ beépített végpontot („operationsMonitoringEvents”).</span><span class="sxs-lookup"><span data-stu-id="a1453-182">Parameter `OperationsMonitoringProperties` is deprecated without being replaced as IotHub is no longer using built-in endpoint("operationsMonitoringEvents").</span></span>



## <a name="recoveryservices"></a><span data-ttu-id="a1453-183">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a1453-183">RecoveryServices</span></span>

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="a1453-184">Az `ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` és `ASRRecoveryPlanGroup.EndGroupActions` el lett távolítva a kimenetből.</span><span class="sxs-lookup"><span data-stu-id="a1453-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `Get-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="a1453-185">Az `ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` és `ASRRecoveryPlanGroup.EndGroupActions` el lett távolítva a kimenetből.</span><span class="sxs-lookup"><span data-stu-id="a1453-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
<span data-ttu-id="a1453-186">Az IncludeDiskId paraméter módosult, és mostantól támogatja az Azure Site Recovery felügyelt lemezeire való közvetlen írást.</span><span class="sxs-lookup"><span data-stu-id="a1453-186">Parameter IncludeDiskId is changed to support directly writing to a managed disk in Azure Site Recovery.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-187">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-187">Before</span></span>
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a><span data-ttu-id="a1453-188">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-188">After</span></span>
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a><span data-ttu-id="a1453-189">Erőforrások</span><span class="sxs-lookup"><span data-stu-id="a1453-189">Resources</span></span>

### <a name="previous-version-incompatibility-with-azbatch-module"></a><span data-ttu-id="a1453-190">Az előző verziók inkompatibilitása az Az.Batch modullal</span><span class="sxs-lookup"><span data-stu-id="a1453-190">Previous Version Incompatibility with Az.Batch Module</span></span>
<span data-ttu-id="a1453-191">Az „Az. Resources” modul 1.7.1-es verziója nem kompatibilis az „Az.Batch” modul korábbi verzióival (1.1.2-es vagy korábbi verziók).</span><span class="sxs-lookup"><span data-stu-id="a1453-191">Version 1.7.1 of the ‘Az.Resources’ module is incompatible with earlier versions (version 1.1.2 or earlier) of the ‘Az.Batch’ module.</span></span>  <span data-ttu-id="a1453-192">Ez azt eredményezi, hogy nem lehet importálni az „Az.Batch” modul 1.1.2-es verzióját, ha az „Az.Resources” modul 1.7.1-es verziója importálva van.</span><span class="sxs-lookup"><span data-stu-id="a1453-192">This will result in being unable to import  version 1.1.2 of the ‘Az.Batch’ module when version 1.7.1 of the ‘Az.Resources’ module is imported.</span></span>  <span data-ttu-id="a1453-193">A probléma megoldásához frissítse az „Az.Batch” modult a 2.0.1-es vagy újabb verzióra, vagy egyszerűen csak telepítse az „Az” modul legújabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="a1453-193">To fix this issue, update the ‘Az.Batch’ module to version 2.0.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="servicefabric"></a><span data-ttu-id="a1453-194">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a1453-194">ServiceFabric</span></span>

### `Add-ServiceFabricApplicationCertificate`
<span data-ttu-id="a1453-195">Az `Add-ServiceFabricApplicationCertificate` el lett távolítva, mivel az `Add-AzVmssSecret` lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="a1453-195">Removed `Add-ServiceFabricApplicationCertificate` as this scenario is covered by `Add-AzVmssSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-196">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-196">Before</span></span>
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a><span data-ttu-id="a1453-197">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-197">After</span></span>
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a><span data-ttu-id="a1453-198">SQL</span><span class="sxs-lookup"><span data-stu-id="a1453-198">Sql</span></span>

### `Get-AzSqlDatabaseSecureConnectionPolicy`
<span data-ttu-id="a1453-199">Vegye figyelembe, hogy a biztonságos kapcsolat elavult, ezért a parancs el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="a1453-199">Note that secure connection is deprecated and so command is removed.</span></span> <span data-ttu-id="a1453-200">A kapcsolati sztringek megtekintéséhez használja az Azure Portal SQL Database paneljét</span><span class="sxs-lookup"><span data-stu-id="a1453-200">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

### `Get-AzSqlDatabaseIndexRecommendations`
<span data-ttu-id="a1453-201">A `Get-AzSqlDatabaseIndexRecommendations` alias el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="a1453-201">`Get-AzSqlDatabaseIndexRecommendations` alias is removed.</span></span> <span data-ttu-id="a1453-202">A `Get-AzSqlDatabaseIndexRecommendation` használható helyette.</span><span class="sxs-lookup"><span data-stu-id="a1453-202">Use `Get-AzSqlDatabaseIndexRecommendation` instead.</span></span>

### `Get-AzSqlDatabaseRestorePoints`
<span data-ttu-id="a1453-203">A `Get-AzSqlDatabaseRestorePoints` alias el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="a1453-203">`Get-AzSqlDatabaseRestorePoints` alias is removed.</span></span> <span data-ttu-id="a1453-204">A `Get-AzSqlDatabaseRestorePoint` használható helyette.</span><span class="sxs-lookup"><span data-stu-id="a1453-204">Use `Get-AzSqlDatabaseRestorePoint` instead.</span></span>

### `Get-AzSqlDatabaseAuditing`
- <span data-ttu-id="a1453-205">A `Get-AzSqlDatabaseAudit` parancsmag lép a parancsmag helyébe.</span><span class="sxs-lookup"><span data-stu-id="a1453-205">The cmdlet `Get-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="a1453-206">A kimeneti típus a meglévő „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” típusról az új „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel” típusra módosul, és eltávolítja az `AuditState` és a `StorageAccountName` tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a1453-206">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removing properties `AuditState` and `StorageAccountName`.</span></span> <span data-ttu-id="a1453-207">és `StorageAccountSubscriptionId`.</span><span class="sxs-lookup"><span data-stu-id="a1453-207">and `StorageAccountSubscriptionId`.</span></span>  <span data-ttu-id="a1453-208">A szkriptek az új `StorageAccountResourceId` tulajdonságból kérhetik le a tárfiókadatokat.</span><span class="sxs-lookup"><span data-stu-id="a1453-208">Scripts can retrieve storage account information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-209">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-209">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="a1453-210">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-210">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlDatabaseAuditing`
- <span data-ttu-id="a1453-211">A `Set-AzSqlDatabaseAudit` parancsmag lép a parancsmag helyébe.</span><span class="sxs-lookup"><span data-stu-id="a1453-211">The cmdlet `Set-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="a1453-212">A kimeneti típus a meglévő „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” típusról az új „bool” típusra módosul</span><span class="sxs-lookup"><span data-stu-id="a1453-212">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-213">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-213">Before</span></span>
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-214">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-214">After</span></span>
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- <span data-ttu-id="a1453-215">A `Get-AzSqlServerAudit` parancsmag lép a parancsmag helyébe.</span><span class="sxs-lookup"><span data-stu-id="a1453-215">The cmdlet `Get-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="a1453-216">A kimeneti típus a meglévő „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” típusról az új „Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel” típusra módosul.</span><span class="sxs-lookup"><span data-stu-id="a1453-216">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span></span>  <span data-ttu-id="a1453-217">Az `AuditState`, `StorageAccountName` és `StorageAccountSubscriptionId` tulajdonságok el lettek távolítva.</span><span class="sxs-lookup"><span data-stu-id="a1453-217">Properties `AuditState`, `StorageAccountName`, and `StorageAccountSubscriptionId` are removed.</span></span>  <span data-ttu-id="a1453-218">A `StorageAccountName` és a `StorageAccountSubscriptionId` tulajdonságot használó szkriptek az új `StorageAccountResourceId` tulajdonságból kérhetik le ezt az információt.</span><span class="sxs-lookup"><span data-stu-id="a1453-218">Scripts that use `StorageAccountName` and `StorageAccountSubscriptionId` proeprties can retrieve this information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-219">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-219">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="a1453-220">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-220">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlServerAuditing`
- <span data-ttu-id="a1453-221">A `Set-AzSqlServerAudit` parancsmag lép a parancsmag helyébe.</span><span class="sxs-lookup"><span data-stu-id="a1453-221">The cmdlet `Set-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="a1453-222">A kimeneti típus a meglévő „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” típusról az új „bool” típusra módosul</span><span class="sxs-lookup"><span data-stu-id="a1453-222">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-223">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-223">Before</span></span>
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a><span data-ttu-id="a1453-224">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-224">After</span></span>
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="a1453-225">A `Get-AzSqlServerAdvancedThreatProtectionSettings` parancsmagot a `Get-AzSqlServerAdvancedThreatProtectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-226">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-226">Before</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="a1453-227">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-227">After</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="a1453-228">A `Clear-AzSqlServerAdvancedThreatProtectionSettings` parancsmagot a `Clear-AzSqlServerAdvancedThreatProtectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-229">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-229">Before</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="a1453-230">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-230">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="a1453-231">A `Update-AzSqlServerAdvancedThreatProtectionSettings` parancsmagot a `Update-AzSqlServerAdvancedThreatProtectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Update-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-232">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-232">Before</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="a1453-233">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-233">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="a1453-234">A `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` parancsmagot a `Get-AzSqlDatabaseAdvancedThreatProtectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-235">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-235">Before</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-236">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-236">After</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="a1453-237">A `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` parancsmagot a `Update-AzSqlDatabaseAdvancedThreatProtectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-238">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-238">Before</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="a1453-239">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-239">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="a1453-240">A `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` parancsmagot a `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-241">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-241">Before</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-242">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-242">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-243">A `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` parancsmagot a `Update-AzSqlDatabaseVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-244">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-244">Before</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="a1453-245">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-245">After</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```


### `Get-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-246">A `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` parancsmagot a `Get-AzSqlDatabaseVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-247">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-247">Before</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-248">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-248">After</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-249">A `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` parancsmagot a `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-250">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-250">Before</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-251">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-251">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-252">A `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` parancsmagot a `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-253">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-253">Before</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="a1453-254">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-254">After</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-255">A `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` parancsmagot a `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-256">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-256">Before</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-257">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-257">After</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-258">A `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` parancsmagot a `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-259">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-259">Before</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-260">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-260">After</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-261">A `Update-AzSqlInstanceVulnerabilityAssessmentSettings` parancsmagot a `Update-AzSqlInstanceVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-262">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-262">Before</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="a1453-263">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-263">After</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-264">A `Get-AzSqlInstanceVulnerabilityAssessmentSettings` parancsmagot a `Get-AzSqlInstanceVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-265">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-265">Before</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-266">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-266">After</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-267">A `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` parancsmagot a `Clear-AzSqlInstanceVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-268">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-268">Before</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-269">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-269">After</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-270">A `Update-AzSqlServerVulnerabilityAssessmentSettings` parancsmagot a `Update-AzSqlServerVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-271">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-271">Before</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="a1453-272">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-272">After</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-273">A `Get-AzSqlServerVulnerabilityAssessmentSettings` parancsmagot a `Get-AzSqlServerVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-274">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-274">Before</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-275">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-275">After</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="a1453-276">A `Clear-AzSqlServerVulnerabilityAssessmentSettings` parancsmagot a `Clear-AzSqlServerVulnerabilityAssessmentSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-277">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-277">Before</span></span>
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-278">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-278">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
<span data-ttu-id="a1453-279">A `Get-AzSqlServerAdvancedThreatProtectionPolicy` parancsmag törölve lett, és nem lépett a helyébe másik parancsmag</span><span class="sxs-lookup"><span data-stu-id="a1453-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` is deleted and no cmdlet is repleaced it</span></span>

### `Get-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="a1453-280">A `Get-AzSqlServerThreatDetectionPolicy` parancsmagot a `Get-AzSqlServerThreatDetectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` is repleaced by `Get-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-281">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-281">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="a1453-282">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-282">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Remove-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="a1453-283">A `Remove-AzSqlServerThreatDetectionPolicy` parancsmagot a `Clear-AzSqlServerThreatDetectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` is repleaced by `Clear-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-284">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-284">Before</span></span>
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="a1453-285">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-285">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="a1453-286">A `Set-AzSqlServerThreatDetectionPolicy` parancsmagot a `Update-AzSqlServerThreatDetectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` is repleaced by `Update-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-287">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-287">Before</span></span>
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="a1453-288">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-288">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="a1453-289">A `Get-AzSqlDatabaseThreatDetectionPolicy` parancsmagot a `Get-AzSqlDatabaseThreatDetectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Get-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-290">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-290">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName   "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="a1453-291">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-291">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"   -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Set-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="a1453-292">A `Set-AzSqlDatabaseThreatDetectionPolicy` parancsmagot a `Update-AzSqlDatabaseThreatDetectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Update-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-293">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-293">Before</span></span>
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="a1453-294">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-294">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="a1453-295">A `Remove-AzSqlDatabaseThreatDetectionPolicy` parancsmagot a `Clear-AzSqlDatabaseThreatDetectionSetting` váltotta fel</span><span class="sxs-lookup"><span data-stu-id="a1453-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Clear-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="a1453-296">Előtte</span><span class="sxs-lookup"><span data-stu-id="a1453-296">Before</span></span>
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="a1453-297">Utána</span><span class="sxs-lookup"><span data-stu-id="a1453-297">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```
