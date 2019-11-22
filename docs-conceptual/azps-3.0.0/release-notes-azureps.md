---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: ee3f54e6bc15dbbaeb97cad7463cb1d2e5795e3e
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062139"
---
## <a name="300---november-2019"></a><span data-ttu-id="a5562-103">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="a5562-103">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="a5562-104">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a5562-104">General</span></span>
* <span data-ttu-id="a5562-105">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a5562-105">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a5562-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-106">Az.Accounts</span></span>
* <span data-ttu-id="a5562-107">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="a5562-107">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a5562-108">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a5562-108">Az.Advisor</span></span>
* <span data-ttu-id="a5562-109">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-109">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a5562-110">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a5562-110">Az.Batch</span></span>
* <span data-ttu-id="a5562-111">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="a5562-111">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="a5562-112">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="a5562-112">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="a5562-113">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="a5562-113">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="a5562-114">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="a5562-114">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="a5562-115">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="a5562-115">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="a5562-116">Ezek az **New-AzBatchTask** `-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="a5562-116">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="a5562-117">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="a5562-117">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="a5562-118">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="a5562-118">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="a5562-119">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="a5562-119">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="a5562-120">A `PSApplication` **Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-120">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a5562-121">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="a5562-121">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="a5562-122">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="a5562-122">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="a5562-123">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-123">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a5562-124">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="a5562-124">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="a5562-125">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="a5562-125">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="a5562-126">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-126">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="a5562-127">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-127">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="a5562-128">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a5562-128">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="a5562-129">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-129">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="a5562-130">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="a5562-130">This operation is no longer supported.</span></span>
* <span data-ttu-id="a5562-131">`PSCloudServiceConfiguration` `TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-131">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a5562-132">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-132">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a5562-133">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="a5562-133">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="a5562-134">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="a5562-134">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="a5562-135">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="a5562-135">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="a5562-136">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="a5562-136">New non-verified images are also now returned.</span></span> <span data-ttu-id="a5562-137">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="a5562-137">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="a5562-138">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="a5562-138">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="a5562-139">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="a5562-139">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="a5562-140">Ez a `PSNetworkSecurityGroupRule` `SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="a5562-140">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="a5562-141">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="a5562-141">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="a5562-142">Ezt a `PSTaskContainerSettings` `WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="a5562-142">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="a5562-143">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="a5562-143">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="a5562-144">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="a5562-144">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="a5562-145">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="a5562-145">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="a5562-146">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="a5562-146">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a5562-147">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a5562-147">Az.Cdn</span></span>
* <span data-ttu-id="a5562-148">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="a5562-148">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="a5562-149">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="a5562-149">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-150">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-150">Az.Compute</span></span>
* <span data-ttu-id="a5562-151">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="a5562-151">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="a5562-152">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a5562-152">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="a5562-153">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="a5562-153">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="a5562-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a5562-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="a5562-155">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-155">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a5562-156">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-156">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="a5562-157">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="a5562-157">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="a5562-158">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-158">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="a5562-159">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="a5562-159">Breaking changes</span></span>
    - <span data-ttu-id="a5562-160">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="a5562-160">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="a5562-161">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="a5562-161">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a5562-162">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a5562-162">Az.DataFactory</span></span>
* <span data-ttu-id="a5562-163">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a5562-163">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a5562-164">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-164">Az.DataLakeStore</span></span>
* <span data-ttu-id="a5562-165">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="a5562-165">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="a5562-166">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="a5562-166">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="a5562-167">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="a5562-167">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="a5562-168">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="a5562-168">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="a5562-169">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-169">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="a5562-170">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-170">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a5562-171">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a5562-171">Az.FrontDoor</span></span>
* <span data-ttu-id="a5562-172">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="a5562-172">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a5562-173">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a5562-173">Az.HDInsight</span></span>
* <span data-ttu-id="a5562-174">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-174">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="a5562-175">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="a5562-175">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="a5562-176">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="a5562-176">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="a5562-177">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="a5562-177">Removed five cmdlets:</span></span>
    - <span data-ttu-id="a5562-178">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a5562-178">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a5562-179">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a5562-179">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a5562-180">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a5562-180">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a5562-181">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a5562-181">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="a5562-182">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a5562-182">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="a5562-183">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="a5562-183">Added three cmdlets:</span></span>
    - <span data-ttu-id="a5562-184">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="a5562-184">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a5562-185">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="a5562-185">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a5562-186">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="a5562-186">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="a5562-187">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="a5562-187">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="a5562-188">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="a5562-188">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="a5562-189">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="a5562-189">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="a5562-190">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="a5562-190">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="a5562-191">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="a5562-191">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="a5562-192">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="a5562-192">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="a5562-193">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="a5562-193">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="a5562-194">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a5562-194">Added some scenario test cases.</span></span>
* <span data-ttu-id="a5562-195">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="a5562-195">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a5562-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a5562-196">Az.IotHub</span></span>
* <span data-ttu-id="a5562-197">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="a5562-197">Breaking changes:</span></span>
    - <span data-ttu-id="a5562-198">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="a5562-198">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a5562-199">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-199">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a5562-200">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="a5562-200">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a5562-201">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-201">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a5562-202">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-202">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="a5562-203">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-203">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="a5562-204">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="a5562-204">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="a5562-205">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="a5562-205">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="a5562-206">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="a5562-206">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a5562-207">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-207">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a5562-208">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="a5562-208">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a5562-209">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-209">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-210">Az.RecoveryServices</span></span>
* <span data-ttu-id="a5562-211">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="a5562-211">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="a5562-212">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="a5562-212">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="a5562-213">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="a5562-213">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="a5562-214">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="a5562-214">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="a5562-215">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="a5562-215">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="a5562-216">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="a5562-216">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="a5562-217">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="a5562-217">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="a5562-218">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="a5562-218">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="a5562-219">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="a5562-219">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-220">Az.Resources</span></span>
* <span data-ttu-id="a5562-221">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="a5562-221">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-222">Az.Network</span></span>
* <span data-ttu-id="a5562-223">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="a5562-223">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="a5562-224">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="a5562-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="a5562-225">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-225">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a5562-226">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-226">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a5562-227">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-227">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a5562-228">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-228">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a5562-229">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-229">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a5562-230">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="a5562-230">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="a5562-231">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="a5562-231">New cmdlet:</span></span>
        - <span data-ttu-id="a5562-232">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a5562-232">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="a5562-233">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-233">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="a5562-234">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="a5562-234">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="a5562-235">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="a5562-235">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="a5562-236">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="a5562-236">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="a5562-237">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="a5562-237">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="a5562-238">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="a5562-238">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="a5562-239">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-239">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="a5562-240">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-240">New cmdlets added:</span></span>
        - <span data-ttu-id="a5562-241">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a5562-241">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="a5562-242">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a5562-242">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a5562-243">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a5562-243">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a5562-244">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a5562-244">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a5562-245">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a5562-245">Set-AzVirtualHub</span></span>
* <span data-ttu-id="a5562-246">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-246">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="a5562-247">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-247">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a5562-248">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-248">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a5562-249">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-249">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a5562-250">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-250">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="a5562-251">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-251">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="a5562-252">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-252">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="a5562-253">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-253">New cmdlets added:</span></span>
        - <span data-ttu-id="a5562-254">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-254">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="a5562-255">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-255">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a5562-256">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-256">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a5562-257">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-257">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a5562-258">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-258">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a5562-259">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-259">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a5562-260">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-260">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="a5562-261">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-261">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="a5562-262">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-262">New cmdlets added:</span></span>
        - <span data-ttu-id="a5562-263">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="a5562-263">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="a5562-264">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="a5562-264">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="a5562-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="a5562-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="a5562-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a5562-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="a5562-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="a5562-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="a5562-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5562-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="a5562-269">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-269">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a5562-270">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-270">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="a5562-271">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-271">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="a5562-272">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="a5562-272">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="a5562-273">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-273">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="a5562-274">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-274">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a5562-275">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-275">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="a5562-276">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-276">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="a5562-277">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="a5562-277">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="a5562-278">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="a5562-278">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="a5562-279">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-279">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="a5562-280">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-280">New cmdlets added:</span></span>
        - <span data-ttu-id="a5562-281">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a5562-281">New-AzIpGroup</span></span>
        - <span data-ttu-id="a5562-282">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a5562-282">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="a5562-283">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a5562-283">Get-AzIpGroup</span></span>
        - <span data-ttu-id="a5562-284">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a5562-284">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a5562-285">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a5562-285">Az.ServiceFabric</span></span>
* <span data-ttu-id="a5562-286">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="a5562-286">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-287">Az.Sql</span></span>
* <span data-ttu-id="a5562-288">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="a5562-288">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="a5562-289">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="a5562-289">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="a5562-290">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="a5562-290">Removed deprecated aliases:</span></span>
* <span data-ttu-id="a5562-291">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="a5562-291">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="a5562-292">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="a5562-292">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="a5562-293">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="a5562-293">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a5562-294">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="a5562-294">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="a5562-295">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="a5562-295">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="a5562-296">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="a5562-296">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-297">Az.Storage</span></span>
* <span data-ttu-id="a5562-298">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="a5562-298">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="a5562-299">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5562-299">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a5562-300">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5562-300">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a5562-301">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="a5562-301">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="a5562-302">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a5562-302">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="a5562-303">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a5562-303">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="a5562-304">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="a5562-304">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="a5562-305">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a5562-305">General</span></span>
* <span data-ttu-id="a5562-306">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="a5562-306">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a5562-307">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-307">Az.Accounts</span></span>
* <span data-ttu-id="a5562-308">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="a5562-308">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a5562-309">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5562-309">Az.ApiManagement</span></span>
* <span data-ttu-id="a5562-310">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a5562-310">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="a5562-311">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="a5562-311">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a5562-312">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a5562-312">Az.Automation</span></span>
* <span data-ttu-id="a5562-313">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="a5562-313">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="a5562-314">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a5562-314">Az.Batch</span></span>
* <span data-ttu-id="a5562-315">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="a5562-315">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-316">Az.Compute</span></span>
* <span data-ttu-id="a5562-317">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-317">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a5562-318">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="a5562-318">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="a5562-319">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="a5562-319">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="a5562-320">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="a5562-320">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a5562-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a5562-321">Az.DataFactory</span></span>
* <span data-ttu-id="a5562-322">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="a5562-322">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="a5562-323">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="a5562-323">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="a5562-324">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a5562-324">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a5562-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="a5562-326">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="a5562-326">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a5562-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a5562-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="a5562-328">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a5562-328">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="a5562-329">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a5562-329">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="a5562-330">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="a5562-330">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="a5562-331">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="a5562-331">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a5562-332">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a5562-332">Az.IotHub</span></span>
* <span data-ttu-id="a5562-333">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="a5562-333">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="a5562-334">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5562-334">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="a5562-335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a5562-335">Az.Monitor</span></span>
* <span data-ttu-id="a5562-336">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="a5562-336">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="a5562-337">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="a5562-337">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="a5562-338">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="a5562-338">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="a5562-339">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="a5562-339">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-340">Az.Network</span></span>
* <span data-ttu-id="a5562-341">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="a5562-341">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="a5562-342">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="a5562-342">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="a5562-343">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-343">New cmdlets added:</span></span>
        - <span data-ttu-id="a5562-344">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="a5562-344">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="a5562-345">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-345">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a5562-346">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="a5562-346">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="a5562-347">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-347">Updated cmdlets:</span></span>
        - <span data-ttu-id="a5562-348">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-348">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a5562-349">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-349">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a5562-350">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-350">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a5562-351">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="a5562-351">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="a5562-352">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="a5562-352">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="a5562-353">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="a5562-353">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="a5562-354">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="a5562-354">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a5562-355">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a5562-355">Az.RedisCache</span></span>
* <span data-ttu-id="a5562-356">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="a5562-356">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-357">Az.Sql</span></span>
* <span data-ttu-id="a5562-358">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="a5562-358">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-359">Az.Storage</span></span>
* <span data-ttu-id="a5562-360">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="a5562-360">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="a5562-361">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="a5562-361">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a5562-362">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a5562-362">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="a5562-363">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="a5562-363">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a5562-364">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5562-364">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a5562-365">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a5562-365">Az.StorageSync</span></span>
* <span data-ttu-id="a5562-366">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="a5562-366">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-367">Az.Websites</span></span>
* <span data-ttu-id="a5562-368">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="a5562-368">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="a5562-369">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="a5562-369">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a5562-370">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5562-370">Az.ApiManagement</span></span>
* <span data-ttu-id="a5562-371">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a5562-371">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="a5562-372">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="a5562-372">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="a5562-373">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="a5562-373">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a5562-374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a5562-374">Az.Automation</span></span>
* <span data-ttu-id="a5562-375">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="a5562-375">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="a5562-376">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-376">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="a5562-377">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="a5562-377">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-378">Az.Compute</span></span>
* <span data-ttu-id="a5562-379">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-379">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="a5562-380">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-380">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a5562-381">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="a5562-381">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="a5562-382">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-382">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="a5562-383">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-383">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="a5562-384">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="a5562-384">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="a5562-385">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="a5562-385">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="a5562-386">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-386">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="a5562-387">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-387">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a5562-388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a5562-388">Az.DataFactory</span></span>
* <span data-ttu-id="a5562-389">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="a5562-389">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="a5562-390">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a5562-390">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a5562-391">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a5562-391">Az.HDInsight</span></span>
* <span data-ttu-id="a5562-392">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="a5562-392">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a5562-393">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a5562-393">Az.IotHub</span></span>
* <span data-ttu-id="a5562-394">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="a5562-394">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="a5562-395">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="a5562-395">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="a5562-396">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="a5562-396">New cmdlets are:</span></span>
    - <span data-ttu-id="a5562-397">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a5562-397">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a5562-398">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a5562-398">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a5562-399">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a5562-399">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a5562-400">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a5562-400">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a5562-401">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a5562-401">Az.Monitor</span></span>
* <span data-ttu-id="a5562-402">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="a5562-402">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="a5562-403">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="a5562-403">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="a5562-404">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="a5562-404">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="a5562-405">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="a5562-405">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="a5562-406">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-406">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="a5562-407">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="a5562-407">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="a5562-408">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="a5562-408">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="a5562-409">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="a5562-409">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="a5562-410">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="a5562-410">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a5562-411">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="a5562-411">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="a5562-412">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="a5562-412">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a5562-413">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="a5562-413">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="a5562-414">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-414">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="a5562-415">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="a5562-415">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="a5562-416">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="a5562-416">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="a5562-417">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="a5562-417">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="a5562-418">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="a5562-418">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="a5562-419">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="a5562-419">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="a5562-420">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="a5562-420">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="a5562-421">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="a5562-421">Overall improved help files</span></span>
* <span data-ttu-id="a5562-422">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="a5562-422">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-423">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-423">Az.Network</span></span>
* <span data-ttu-id="a5562-424">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="a5562-424">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="a5562-425">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a5562-425">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="a5562-426">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="a5562-426">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="a5562-427">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="a5562-427">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="a5562-428">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="a5562-428">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="a5562-429">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="a5562-429">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="a5562-430">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="a5562-430">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="a5562-431">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-431">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="a5562-432">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-432">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="a5562-433">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="a5562-433">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="a5562-434">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="a5562-434">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="a5562-435">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="a5562-435">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="a5562-436">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-436">New cmdlets</span></span>
        - <span data-ttu-id="a5562-437">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a5562-437">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="a5562-438">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-438">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="a5562-439">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="a5562-439">Updated cmdlet:</span></span>
        - <span data-ttu-id="a5562-440">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a5562-440">New-VpnSite</span></span>
        - <span data-ttu-id="a5562-441">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a5562-441">Update-VpnSite</span></span>
        - <span data-ttu-id="a5562-442">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-442">New-VpnConnection</span></span>
        - <span data-ttu-id="a5562-443">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-443">Update-VpnConnection</span></span>
* <span data-ttu-id="a5562-444">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="a5562-444">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-445">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-445">Az.RecoveryServices</span></span>
* <span data-ttu-id="a5562-446">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="a5562-446">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="a5562-447">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="a5562-447">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-448">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-448">Az.Resources</span></span>
* <span data-ttu-id="a5562-449">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="a5562-449">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a5562-450">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a5562-450">Az.ServiceFabric</span></span>
* <span data-ttu-id="a5562-451">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="a5562-451">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="a5562-452">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="a5562-452">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="a5562-453">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a5562-453">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a5562-454">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a5562-454">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a5562-455">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a5562-455">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a5562-456">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a5562-456">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="a5562-457">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a5562-457">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a5562-458">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a5562-458">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a5562-459">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a5562-459">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a5562-460">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a5562-460">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a5562-461">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a5562-461">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="a5562-462">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a5562-462">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a5562-463">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a5562-463">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a5562-464">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a5562-464">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a5562-465">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="a5562-465">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="a5562-466">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="a5562-466">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a5562-467">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a5562-467">Az.SignalR</span></span>
* <span data-ttu-id="a5562-468">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-468">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-469">Az.Sql</span></span>
* <span data-ttu-id="a5562-470">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="a5562-470">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="a5562-471">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="a5562-471">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="a5562-472">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a5562-472">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a5562-473">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="a5562-473">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="a5562-474">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="a5562-474">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-475">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-475">Az.Storage</span></span>
* <span data-ttu-id="a5562-476">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="a5562-476">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a5562-477">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-477">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="a5562-478">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a5562-478">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="a5562-479">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a5562-479">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="a5562-480">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-480">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="a5562-481">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a5562-481">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="a5562-482">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="a5562-482">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="a5562-483">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a5562-483">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a5562-484">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a5562-484">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a5562-485">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a5562-485">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a5562-486">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a5562-486">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-487">Az.Websites</span></span>
* <span data-ttu-id="a5562-488">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="a5562-488">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="a5562-489">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="a5562-489">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="a5562-490">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="a5562-490">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="a5562-491">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="a5562-491">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="a5562-492">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a5562-492">General</span></span>
* <span data-ttu-id="a5562-493">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="a5562-493">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a5562-494">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-494">Az.Accounts</span></span>
* <span data-ttu-id="a5562-495">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="a5562-495">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="a5562-496">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a5562-496">Az.Aks</span></span>
* <span data-ttu-id="a5562-497">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="a5562-497">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="a5562-498">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="a5562-498">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a5562-499">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5562-499">Az.ApiManagement</span></span>
* <span data-ttu-id="a5562-500">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="a5562-500">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="a5562-501">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="a5562-501">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="a5562-502">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="a5562-502">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="a5562-503">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="a5562-503">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="a5562-504">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="a5562-504">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a5562-505">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a5562-505">Az.Batch</span></span>
* <span data-ttu-id="a5562-506">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="a5562-506">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a5562-507">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a5562-507">Az.Cdn</span></span>
* <span data-ttu-id="a5562-508">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="a5562-508">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-509">Az.Compute</span></span>
* <span data-ttu-id="a5562-510">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-510">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="a5562-511">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-511">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="a5562-512">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-512">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="a5562-513">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="a5562-513">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="a5562-514">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="a5562-514">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="a5562-515">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-515">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="a5562-516">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="a5562-516">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="a5562-517">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a5562-517">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a5562-518">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a5562-518">Az.DataFactory</span></span>
* <span data-ttu-id="a5562-519">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="a5562-519">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="a5562-520">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a5562-520">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="a5562-521">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="a5562-521">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="a5562-522">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="a5562-522">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a5562-523">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-523">Az.DataLakeStore</span></span>
* <span data-ttu-id="a5562-524">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="a5562-524">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a5562-525">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a5562-525">Az.EventHub</span></span>
* <span data-ttu-id="a5562-526">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a5562-526">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="a5562-527">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="a5562-527">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="a5562-528">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-528">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="a5562-529">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="a5562-529">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="a5562-530">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a5562-530">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a5562-531">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="a5562-531">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a5562-532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a5562-532">Az.Monitor</span></span>
* <span data-ttu-id="a5562-533">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="a5562-533">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-534">Az.Network</span></span>
* <span data-ttu-id="a5562-535">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-535">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="a5562-536">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="a5562-536">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="a5562-537">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="a5562-537">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="a5562-538">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="a5562-538">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="a5562-539">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="a5562-539">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="a5562-540">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="a5562-540">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="a5562-541">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="a5562-541">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a5562-542">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-542">Az.OperationalInsights</span></span>
* <span data-ttu-id="a5562-543">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a5562-543">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="a5562-544">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-544">Added example</span></span>
    - <span data-ttu-id="a5562-545">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="a5562-545">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="a5562-546">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-546">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="a5562-547">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="a5562-547">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-548">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-548">Az.RecoveryServices</span></span>
* <span data-ttu-id="a5562-549">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="a5562-549">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-550">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-550">Az.Resources</span></span>
* <span data-ttu-id="a5562-551">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="a5562-551">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="a5562-552">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-552">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="a5562-553">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="a5562-553">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="a5562-554">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-554">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a5562-555">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a5562-555">Az.ServiceBus</span></span>
* <span data-ttu-id="a5562-556">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a5562-556">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="a5562-557">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="a5562-557">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="a5562-558">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="a5562-558">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="a5562-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a5562-559">Az.ServiceFabric</span></span>
* <span data-ttu-id="a5562-560">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="a5562-560">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="a5562-561">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="a5562-561">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="a5562-562">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="a5562-562">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="a5562-563">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="a5562-563">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="a5562-564">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="a5562-564">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="a5562-565">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="a5562-565">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-566">Az.Sql</span></span>
* <span data-ttu-id="a5562-567">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="a5562-567">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-568">Az.Storage</span></span>
* <span data-ttu-id="a5562-569">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="a5562-569">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="a5562-570">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="a5562-570">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="a5562-571">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a5562-571">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="a5562-572">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a5562-572">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="a5562-573">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="a5562-573">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="a5562-574">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a5562-574">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-575">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-575">Az.Websites</span></span>
* <span data-ttu-id="a5562-576">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="a5562-576">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="a5562-577">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="a5562-577">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a5562-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-578">Az.Accounts</span></span>
* <span data-ttu-id="a5562-579">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="a5562-579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a5562-580">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-580">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a5562-581">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-581">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="a5562-582">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a5562-582">Az.Automation</span></span>
* <span data-ttu-id="a5562-583">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-583">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="a5562-584">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a5562-584">Az.CognitiveServices</span></span>
* <span data-ttu-id="a5562-585">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a5562-585">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-586">Az.Compute</span></span>
* <span data-ttu-id="a5562-587">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="a5562-587">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a5562-588">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a5562-588">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a5562-589">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-589">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="a5562-590">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="a5562-590">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a5562-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a5562-591">Az.DataFactory</span></span>
* <span data-ttu-id="a5562-592">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a5562-592">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="a5562-593">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-593">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a5562-594">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a5562-594">Az.EventHub</span></span>
* <span data-ttu-id="a5562-595">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a5562-595">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a5562-596">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="a5562-596">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a5562-597">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a5562-597">Az.KeyVault</span></span>
* <span data-ttu-id="a5562-598">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="a5562-598">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a5562-599">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a5562-599">Az.LogicApp</span></span>
* <span data-ttu-id="a5562-600">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="a5562-600">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="a5562-601">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="a5562-601">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a5562-602">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a5562-602">Az.ManagedServices</span></span>
* <span data-ttu-id="a5562-603">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-603">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-604">Az.Network</span></span>
* <span data-ttu-id="a5562-605">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-605">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="a5562-606">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-606">New cmdlets</span></span>
        - <span data-ttu-id="a5562-607">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5562-607">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a5562-608">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a5562-608">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a5562-609">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-609">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a5562-610">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-610">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a5562-611">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-611">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a5562-612">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-612">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a5562-613">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="a5562-613">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="a5562-614">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a5562-614">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="a5562-615">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="a5562-615">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="a5562-616">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="a5562-616">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="a5562-617">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-617">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="a5562-618">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-618">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="a5562-619">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="a5562-619">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="a5562-620">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-620">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="a5562-621">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-621">Updated cmdlets</span></span>
        - <span data-ttu-id="a5562-622">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-622">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a5562-623">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-623">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a5562-624">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-624">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a5562-625">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="a5562-625">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a5562-626">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="a5562-626">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="a5562-627">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="a5562-627">Updated cmdlet:</span></span>
        - <span data-ttu-id="a5562-628">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-628">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a5562-629">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-629">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a5562-630">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-630">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="a5562-631">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="a5562-631">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="a5562-632">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="a5562-632">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="a5562-633">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="a5562-633">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a5562-634">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-634">Az.OperationalInsights</span></span>
* <span data-ttu-id="a5562-635">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="a5562-635">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="a5562-636">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="a5562-636">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-637">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-637">Az.RecoveryServices</span></span>
* <span data-ttu-id="a5562-638">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-638">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a5562-639">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-639">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="a5562-640">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-640">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="a5562-641">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-641">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a5562-642">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-642">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="a5562-643">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-643">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a5562-644">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-644">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="a5562-645">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-645">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a5562-646">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-646">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="a5562-647">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-647">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-648">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-648">Az.Resources</span></span>
- <span data-ttu-id="a5562-649">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a5562-649">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="a5562-650">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="a5562-650">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a5562-651">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a5562-651">Az.ServiceBus</span></span>
* <span data-ttu-id="a5562-652">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a5562-652">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a5562-653">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="a5562-653">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-654">Az.Sql</span></span>
* <span data-ttu-id="a5562-655">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-655">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="a5562-656">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-656">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="a5562-657">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="a5562-657">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-658">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-658">Az.Storage</span></span>
* <span data-ttu-id="a5562-659">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="a5562-659">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a5562-660">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a5562-660">Az.StorageSync</span></span>
* <span data-ttu-id="a5562-661">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="a5562-661">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="a5562-662">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="a5562-662">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-663">Az.Websites</span></span>
* <span data-ttu-id="a5562-664">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="a5562-664">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="a5562-665">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-665">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="a5562-666">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-666">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="a5562-667">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="a5562-667">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a5562-668">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-668">Az.Accounts</span></span>
* <span data-ttu-id="a5562-669">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a5562-669">Add support for profile cmdlets</span></span>
* <span data-ttu-id="a5562-670">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a5562-670">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="a5562-671">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="a5562-671">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a5562-672">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a5562-672">Az.Advisor</span></span>
* <span data-ttu-id="a5562-673">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="a5562-673">GA release of Az.Advisor</span></span>
* <span data-ttu-id="a5562-674">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="a5562-674">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a5562-675">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5562-675">Az.ApiManagement</span></span>
* <span data-ttu-id="a5562-676">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="a5562-676">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="a5562-677">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a5562-677">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="a5562-678">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-678">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="a5562-679">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-679">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="a5562-680">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="a5562-680">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="a5562-681">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a5562-681">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="a5562-682">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="a5562-682">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a5562-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a5562-683">Az.Automation</span></span>
* <span data-ttu-id="a5562-684">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="a5562-684">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-685">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-685">Az.Compute</span></span>
* <span data-ttu-id="a5562-686">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-686">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a5562-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a5562-687">Az.DataFactory</span></span>
* <span data-ttu-id="a5562-688">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="a5562-688">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a5562-689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a5562-689">Az.EventGrid</span></span>
* <span data-ttu-id="a5562-690">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a5562-690">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a5562-691">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a5562-691">Az.IotHub</span></span>
* <span data-ttu-id="a5562-692">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a5562-692">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-693">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-693">Az.Network</span></span>
* <span data-ttu-id="a5562-694">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="a5562-694">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="a5562-695">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="a5562-695">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a5562-696">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-696">Az.PolicyInsights</span></span>
* <span data-ttu-id="a5562-697">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a5562-697">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="a5562-698">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="a5562-698">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a5562-699">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-699">Az.OperationalInsights</span></span>
* <span data-ttu-id="a5562-700">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="a5562-700">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="a5562-702">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-702">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-703">Az.Resources</span></span>
    - <span data-ttu-id="a5562-704">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-704">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="a5562-705">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-705">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="a5562-706">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-706">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="a5562-707">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-707">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a5562-708">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a5562-708">Az.ServiceBus</span></span>
* <span data-ttu-id="a5562-709">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="a5562-709">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-710">Az.Sql</span></span>
* <span data-ttu-id="a5562-711">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="a5562-711">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="a5562-712">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="a5562-712">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="a5562-713">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a5562-713">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a5562-714">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a5562-714">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a5562-715">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a5562-715">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a5562-716">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a5562-716">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a5562-717">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a5562-717">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a5562-718">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a5562-718">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="a5562-719">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="a5562-719">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-720">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-720">Az.Storage</span></span>
* <span data-ttu-id="a5562-721">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="a5562-721">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="a5562-722">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a5562-722">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="a5562-723">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="a5562-723">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="a5562-724">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="a5562-724">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="a5562-725">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="a5562-725">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="a5562-726">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5562-726">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a5562-727">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5562-727">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a5562-728">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="a5562-728">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="a5562-729">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a5562-729">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="a5562-730">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a5562-730">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a5562-731">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a5562-731">Az.StorageSync</span></span>
* <span data-ttu-id="a5562-732">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="a5562-732">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="a5562-733">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="a5562-733">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a5562-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-734">Az.Accounts</span></span>
* <span data-ttu-id="a5562-735">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-735">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="a5562-736">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="a5562-736">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="a5562-737">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-737">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="a5562-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a5562-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="a5562-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="a5562-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-740">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-740">Az.Compute</span></span>
* <span data-ttu-id="a5562-741">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="a5562-741">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="a5562-742">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a5562-742">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="a5562-743">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a5562-743">Az.Dns</span></span>
* <span data-ttu-id="a5562-744">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="a5562-744">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a5562-745">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a5562-745">Az.EventGrid</span></span>
* <span data-ttu-id="a5562-746">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="a5562-746">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="a5562-747">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-747">New cmdlets:</span></span>
    - <span data-ttu-id="a5562-748">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a5562-748">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a5562-749">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="a5562-749">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a5562-750">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a5562-750">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a5562-751">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="a5562-751">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="a5562-752">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a5562-752">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a5562-753">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="a5562-753">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a5562-754">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a5562-754">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a5562-755">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-755">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a5562-756">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a5562-756">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a5562-757">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="a5562-757">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="a5562-758">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a5562-758">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a5562-759">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a5562-759">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="a5562-760">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a5562-760">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="a5562-761">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="a5562-761">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="a5562-762">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a5562-762">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a5562-763">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="a5562-763">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="a5562-764">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-764">Updated cmdlets:</span></span>
    - <span data-ttu-id="a5562-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a5562-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="a5562-766">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="a5562-766">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a5562-767">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="a5562-767">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a5562-768">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="a5562-768">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="a5562-769">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="a5562-769">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="a5562-770">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="a5562-770">Event subscription expiration date,</span></span>
            - <span data-ttu-id="a5562-771">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="a5562-771">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="a5562-772">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="a5562-772">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="a5562-773">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="a5562-773">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="a5562-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a5562-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="a5562-775">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="a5562-775">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="a5562-776">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a5562-776">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="a5562-777">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="a5562-777">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="a5562-778">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="a5562-778">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a5562-779">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a5562-779">Az.FrontDoor</span></span>
* <span data-ttu-id="a5562-780">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="a5562-780">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="a5562-781">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="a5562-781">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="a5562-782">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a5562-782">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="a5562-783">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="a5562-783">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-784">Az.Network</span></span>
* <span data-ttu-id="a5562-785">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-785">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="a5562-786">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-786">New cmdlets</span></span>
        - <span data-ttu-id="a5562-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="a5562-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="a5562-788">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-788">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="a5562-789">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-789">New cmdlets</span></span> 
        - <span data-ttu-id="a5562-790">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a5562-790">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="a5562-791">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-791">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="a5562-792">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-792">New cmdlets</span></span> 
        - <span data-ttu-id="a5562-793">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a5562-793">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="a5562-794">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a5562-794">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a5562-795">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a5562-795">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a5562-796">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-796">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="a5562-797">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-797">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a5562-798">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-798">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="a5562-799">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-799">New cmdlets</span></span>
        - <span data-ttu-id="a5562-800">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5562-800">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a5562-801">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5562-801">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a5562-802">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5562-802">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a5562-803">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="a5562-803">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="a5562-804">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="a5562-804">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="a5562-805">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="a5562-805">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="a5562-806">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="a5562-806">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="a5562-807">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-807">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="a5562-808">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-808">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="a5562-809">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="a5562-809">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="a5562-810">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="a5562-810">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="a5562-811">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="a5562-811">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="a5562-812">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-812">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="a5562-813">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="a5562-813">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="a5562-814">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-814">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="a5562-815">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-815">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="a5562-816">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="a5562-816">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="a5562-817">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-817">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="a5562-818">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="a5562-818">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a5562-819">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="a5562-819">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="a5562-820">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="a5562-820">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="a5562-821">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="a5562-821">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="a5562-822">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="a5562-822">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="a5562-823">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-823">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="a5562-824">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-824">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a5562-825">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-825">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a5562-826">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-826">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a5562-827">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-827">Az.OperationalInsights</span></span>
* <span data-ttu-id="a5562-828">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-828">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-829">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-829">Az.Resources</span></span>
* <span data-ttu-id="a5562-830">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="a5562-830">Support for additional Template Export options</span></span>
    - <span data-ttu-id="a5562-831">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-831">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a5562-832">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-832">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a5562-833">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-833">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a5562-834">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a5562-834">Az.ServiceFabric</span></span>
* <span data-ttu-id="a5562-835">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="a5562-835">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-836">Az.Sql</span></span>
* <span data-ttu-id="a5562-837">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="a5562-837">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="a5562-838">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="a5562-838">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="a5562-839">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-839">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="a5562-840">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a5562-840">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a5562-841">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a5562-841">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a5562-842">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a5562-842">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a5562-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a5562-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="a5562-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a5562-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-845">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-845">Az.Storage</span></span>
* <span data-ttu-id="a5562-846">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="a5562-846">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="a5562-847">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5562-847">New-AzStorageAccount</span></span>
* <span data-ttu-id="a5562-848">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="a5562-848">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="a5562-849">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a5562-849">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-850">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-850">Az.Websites</span></span>
* <span data-ttu-id="a5562-851">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="a5562-851">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="a5562-852">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-852">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="a5562-853">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="a5562-853">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="a5562-854">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a5562-854">Az.Cdn</span></span>
* <span data-ttu-id="a5562-855">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="a5562-855">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-856">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-856">Az.Compute</span></span>
* <span data-ttu-id="a5562-857">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="a5562-857">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="a5562-858">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a5562-858">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a5562-859">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a5562-859">Az.EventHub</span></span>
* <span data-ttu-id="a5562-860">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="a5562-860">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="a5562-861">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="a5562-861">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-862">Az.Network</span></span>
* <span data-ttu-id="a5562-863">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="a5562-863">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="a5562-864">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a5562-864">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a5562-865">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-865">Az.PolicyInsights</span></span>
* <span data-ttu-id="a5562-866">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a5562-866">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="a5562-868">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="a5562-868">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a5562-869">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a5562-869">Az.ServiceBus</span></span>
* <span data-ttu-id="a5562-870">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="a5562-870">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a5562-871">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a5562-871">Az.ServiceFabric</span></span>
* <span data-ttu-id="a5562-872">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="a5562-872">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="a5562-873">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="a5562-873">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-874">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-874">Az.Sql</span></span>
* <span data-ttu-id="a5562-875">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="a5562-875">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="a5562-876">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="a5562-876">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a5562-877">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="a5562-877">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="a5562-878">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="a5562-878">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-879">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-879">Az.Websites</span></span>
* <span data-ttu-id="a5562-880">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="a5562-880">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="a5562-881">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="a5562-881">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a5562-882">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5562-882">Az.ApiManagement</span></span>
* <span data-ttu-id="a5562-883">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="a5562-883">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="a5562-884">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="a5562-884">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="a5562-885">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="a5562-885">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="a5562-886">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="a5562-886">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="a5562-887">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="a5562-887">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="a5562-888">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-888">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="a5562-889">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="a5562-889">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="a5562-890">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="a5562-890">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="a5562-891">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-891">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="a5562-892">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="a5562-892">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="a5562-893">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="a5562-893">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="a5562-894">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a5562-894">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="a5562-895">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-895">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="a5562-896">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-896">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="a5562-897">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="a5562-897">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="a5562-898">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="a5562-898">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="a5562-899">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a5562-899">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="a5562-900">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-900">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="a5562-901">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="a5562-901">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="a5562-902">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="a5562-902">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="a5562-903">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-903">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="a5562-904">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="a5562-904">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="a5562-905">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="a5562-905">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="a5562-906">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-906">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="a5562-907">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="a5562-907">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="a5562-908">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="a5562-908">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="a5562-909">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="a5562-909">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="a5562-910">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="a5562-910">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="a5562-911">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="a5562-911">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="a5562-912">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="a5562-912">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="a5562-913">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-913">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="a5562-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="a5562-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="a5562-915">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="a5562-915">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="a5562-916">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-916">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a5562-917">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="a5562-917">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="a5562-918">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="a5562-918">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="a5562-919">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="a5562-919">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="a5562-920">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="a5562-920">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="a5562-921">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="a5562-921">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="a5562-922">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-922">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="a5562-923">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="a5562-923">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a5562-924">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="a5562-924">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a5562-925">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="a5562-925">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="a5562-926">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="a5562-926">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a5562-927">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-927">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a5562-928">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="a5562-928">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a5562-929">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="a5562-929">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="a5562-930">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="a5562-930">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a5562-931">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-931">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="a5562-932">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="a5562-932">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="a5562-933">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="a5562-933">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="a5562-934">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="a5562-934">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="a5562-935">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="a5562-935">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="a5562-936">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-936">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="a5562-937">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="a5562-937">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="a5562-938">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="a5562-938">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="a5562-939">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-939">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a5562-940">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="a5562-940">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a5562-941">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="a5562-941">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a5562-942">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-942">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a5562-943">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-943">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a5562-944">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="a5562-944">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a5562-945">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="a5562-945">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a5562-946">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-946">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a5562-947">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="a5562-947">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="a5562-948">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a5562-948">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="a5562-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="a5562-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="a5562-950">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a5562-950">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="a5562-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="a5562-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="a5562-952">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a5562-952">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="a5562-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="a5562-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="a5562-954">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a5562-954">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="a5562-955">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a5562-955">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="a5562-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="a5562-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="a5562-957">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a5562-957">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="a5562-958">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a5562-958">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="a5562-959">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a5562-959">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a5562-960">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a5562-960">Az.Automation</span></span>
* <span data-ttu-id="a5562-961">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-961">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="a5562-962">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="a5562-962">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="a5562-963">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="a5562-963">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="a5562-964">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="a5562-964">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="a5562-965">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="a5562-965">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="a5562-966">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="a5562-966">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="a5562-967">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="a5562-967">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-968">Az.Compute</span></span>
* <span data-ttu-id="a5562-969">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-969">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="a5562-970">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="a5562-970">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a5562-971">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-971">Az.DataLakeStore</span></span>
* <span data-ttu-id="a5562-972">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="a5562-972">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a5562-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a5562-973">Az.Monitor</span></span>
* <span data-ttu-id="a5562-974">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="a5562-974">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-975">Az.Network</span></span>
* <span data-ttu-id="a5562-976">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="a5562-976">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="a5562-977">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="a5562-977">Updated cmdlet:</span></span>
        - <span data-ttu-id="a5562-978">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a5562-978">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="a5562-979">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a5562-979">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-980">Az.Resources</span></span>
* <span data-ttu-id="a5562-981">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-981">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-982">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-982">Az.Sql</span></span>
* <span data-ttu-id="a5562-983">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="a5562-983">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="a5562-984">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="a5562-984">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a5562-985">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-985">Az.Accounts</span></span>
* <span data-ttu-id="a5562-986">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="a5562-986">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a5562-987">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a5562-987">Az.CognitiveServices</span></span>
* <span data-ttu-id="a5562-988">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="a5562-988">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="a5562-989">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="a5562-989">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-990">Az.Compute</span></span>
* <span data-ttu-id="a5562-991">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="a5562-991">Proximity placement group feature.</span></span>
    - <span data-ttu-id="a5562-992">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a5562-992">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="a5562-993">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-993">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="a5562-994">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-994">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="a5562-995">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="a5562-995">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="a5562-996">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-996">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="a5562-997">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="a5562-997">Breaking changes</span></span>
    - <span data-ttu-id="a5562-998">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="a5562-998">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="a5562-999">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="a5562-999">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a5562-1000">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a5562-1000">Az.DeploymentManager</span></span>
* <span data-ttu-id="a5562-1001">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="a5562-1001">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="a5562-1002">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a5562-1002">Az.Dns</span></span>
* <span data-ttu-id="a5562-1003">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="a5562-1003">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="a5562-1004">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1004">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="a5562-1005">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="a5562-1005">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a5562-1006">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a5562-1006">Az.FrontDoor</span></span>
* <span data-ttu-id="a5562-1007">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="a5562-1007">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="a5562-1008">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="a5562-1008">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="a5562-1009">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a5562-1009">Az.HDInsight</span></span>
* <span data-ttu-id="a5562-1010">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="a5562-1010">Removed two cmdlets:</span></span>
    - <span data-ttu-id="a5562-1011">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a5562-1011">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="a5562-1012">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a5562-1012">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a5562-1013">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="a5562-1013">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a5562-1014">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="a5562-1014">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="a5562-1015">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="a5562-1015">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="a5562-1016">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="a5562-1016">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a5562-1017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a5562-1017">Az.Monitor</span></span>
* <span data-ttu-id="a5562-1018">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="a5562-1018">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="a5562-1019">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a5562-1019">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="a5562-1020">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a5562-1020">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="a5562-1021">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a5562-1021">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="a5562-1022">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a5562-1022">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="a5562-1023">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a5562-1023">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="a5562-1024">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a5562-1024">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="a5562-1025">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a5562-1025">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a5562-1026">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a5562-1026">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a5562-1027">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a5562-1027">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a5562-1028">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a5562-1028">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a5562-1029">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a5562-1029">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a5562-1030">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="a5562-1030">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="a5562-1031">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="a5562-1031">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-1032">Az.Network</span></span>
* <span data-ttu-id="a5562-1033">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-1033">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="a5562-1034">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-1034">New cmdlets</span></span>
        - <span data-ttu-id="a5562-1035">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a5562-1035">New-AzNatGateway</span></span>
        - <span data-ttu-id="a5562-1036">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a5562-1036">Get-AzNatGateway</span></span>
        - <span data-ttu-id="a5562-1037">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a5562-1037">Set-AzNatGateway</span></span>
        - <span data-ttu-id="a5562-1038">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a5562-1038">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="a5562-1039">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-1039">Updated cmdlets</span></span>
        - <span data-ttu-id="a5562-1040">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a5562-1040">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="a5562-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a5562-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="a5562-1042">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a5562-1042">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="a5562-1043">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a5562-1043">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="a5562-1044">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a5562-1044">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a5562-1045">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-1045">Az.PolicyInsights</span></span>
* <span data-ttu-id="a5562-1046">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="a5562-1046">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="a5562-1047">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-1047">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="a5562-1048">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="a5562-1048">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-1049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1049">Az.RecoveryServices</span></span>
* <span data-ttu-id="a5562-1050">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="a5562-1050">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="a5562-1051">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="a5562-1051">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="a5562-1052">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="a5562-1052">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="a5562-1053">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="a5562-1053">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="a5562-1054">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="a5562-1054">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="a5562-1055">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="a5562-1055">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="a5562-1056">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a5562-1056">Az.Relay</span></span>
* <span data-ttu-id="a5562-1057">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="a5562-1057">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a5562-1058">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a5562-1058">Az.ServiceBus</span></span>
* <span data-ttu-id="a5562-1059">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="a5562-1059">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-1060">Az.Storage</span></span>
* <span data-ttu-id="a5562-1061">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="a5562-1061">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="a5562-1062">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="a5562-1062">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="a5562-1063">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="a5562-1063">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="a5562-1064">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5562-1064">New-AzStorageAccount</span></span>
* <span data-ttu-id="a5562-1065">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="a5562-1065">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="a5562-1066">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5562-1066">New-AzStorageAccount</span></span>
    - <span data-ttu-id="a5562-1067">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5562-1067">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="a5562-1068">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5562-1068">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-1069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-1069">Az.Websites</span></span>
* <span data-ttu-id="a5562-1070">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1070">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="a5562-1071">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="a5562-1071">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="a5562-1072">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="a5562-1072">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a5562-1073">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="a5562-1073">Highlights since the last major release</span></span>
* <span data-ttu-id="a5562-1074">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="a5562-1074">General availability of `Az` module</span></span>
* <span data-ttu-id="a5562-1075">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a5562-1075">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a5562-1076">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a5562-1076">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a5562-1077">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1077">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a5562-1078">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1078">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a5562-1079">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1079">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a5562-1080">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1080">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a5562-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-1081">Az.Accounts</span></span>
* <span data-ttu-id="a5562-1082">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-1082">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a5562-1083">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a5562-1083">Az.Batch</span></span>
* <span data-ttu-id="a5562-1084">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1084">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a5562-1085">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a5562-1085">Az.Cdn</span></span>
* <span data-ttu-id="a5562-1086">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1086">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a5562-1087">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1087">Az.CognitiveServices</span></span>
* <span data-ttu-id="a5562-1088">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1088">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-1089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1089">Az.Compute</span></span>
* <span data-ttu-id="a5562-1090">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a5562-1090">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a5562-1091">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1091">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a5562-1092">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a5562-1092">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a5562-1093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a5562-1093">Az.DataFactory</span></span>
* <span data-ttu-id="a5562-1094">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="a5562-1094">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a5562-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-1095">Az.DataLakeStore</span></span>
* <span data-ttu-id="a5562-1096">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1096">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a5562-1097">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a5562-1097">Az.EventGrid</span></span>
* <span data-ttu-id="a5562-1098">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="a5562-1098">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a5562-1099">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a5562-1099">Az.EventHub</span></span>
* <span data-ttu-id="a5562-1100">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="a5562-1100">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="a5562-1101">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a5562-1101">Az.HDInsight</span></span>
* <span data-ttu-id="a5562-1102">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1102">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a5562-1103">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a5562-1103">Az.IotHub</span></span>
* <span data-ttu-id="a5562-1104">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1104">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a5562-1105">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a5562-1105">Az.KeyVault</span></span>
* <span data-ttu-id="a5562-1106">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1106">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a5562-1107">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a5562-1107">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a5562-1108">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a5562-1108">Az.MachineLearning</span></span>
* <span data-ttu-id="a5562-1109">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1109">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a5562-1110">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a5562-1110">Az.Media</span></span>
* <span data-ttu-id="a5562-1111">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1111">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a5562-1112">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a5562-1112">Az.Monitor</span></span>
  * <span data-ttu-id="a5562-1113">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-1113">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a5562-1114">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a5562-1114">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a5562-1115">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a5562-1115">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a5562-1116">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a5562-1116">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a5562-1117">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a5562-1117">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a5562-1118">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a5562-1118">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a5562-1119">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="a5562-1119">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-1120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-1120">Az.Network</span></span>
* <span data-ttu-id="a5562-1121">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a5562-1122">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a5562-1122">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a5562-1123">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a5562-1123">Az.NotificationHubs</span></span>
* <span data-ttu-id="a5562-1124">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1124">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a5562-1125">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-1125">Az.OperationalInsights</span></span>
* <span data-ttu-id="a5562-1126">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a5562-1127">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a5562-1127">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a5562-1128">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-1129">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1129">Az.RecoveryServices</span></span>
* <span data-ttu-id="a5562-1130">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1130">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a5562-1131">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="a5562-1131">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a5562-1132">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="a5562-1132">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a5562-1133">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="a5562-1133">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a5562-1134">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a5562-1134">Az.RedisCache</span></span>
* <span data-ttu-id="a5562-1135">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1136">Az.Resources</span></span>
* <span data-ttu-id="a5562-1137">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a5562-1137">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-1138">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1138">Az.Sql</span></span>
* <span data-ttu-id="a5562-1139">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="a5562-1139">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a5562-1140">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a5562-1141">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="a5562-1141">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a5562-1142">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a5562-1142">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a5562-1143">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="a5562-1143">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a5562-1144">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="a5562-1144">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a5562-1145">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a5562-1145">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-1146">Az.Websites</span></span>
* <span data-ttu-id="a5562-1147">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="a5562-1147">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a5562-1148">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1148">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a5562-1149">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="a5562-1149">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a5562-1150">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="a5562-1150">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a5562-1151">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="a5562-1151">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a5562-1152">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="a5562-1152">Highlights since the last major release</span></span>
* <span data-ttu-id="a5562-1153">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="a5562-1153">General availability of `Az` module</span></span>
* <span data-ttu-id="a5562-1154">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a5562-1154">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a5562-1155">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a5562-1155">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a5562-1156">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1156">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a5562-1157">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1157">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a5562-1158">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1158">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a5562-1159">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1159">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a5562-1160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-1160">Az.Accounts</span></span>
* <span data-ttu-id="a5562-1161">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="a5562-1161">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a5562-1162">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1162">Az.AnalysisServices</span></span>
* <span data-ttu-id="a5562-1163">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a5562-1163">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a5562-1164">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-1164">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a5562-1165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a5562-1165">Az.Automation</span></span>
* <span data-ttu-id="a5562-1166">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="a5562-1166">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a5562-1167">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="a5562-1167">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a5562-1168">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1168">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1169">Az.Compute</span></span>
* <span data-ttu-id="a5562-1170">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1170">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a5562-1171">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="a5562-1171">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="a5562-1172">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a5562-1172">Az.ContainerInstance</span></span>
* <span data-ttu-id="a5562-1173">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="a5562-1173">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a5562-1174">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a5562-1174">Az.DataFactory</span></span>
* <span data-ttu-id="a5562-1175">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="a5562-1175">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a5562-1176">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="a5562-1176">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-1177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1177">Az.Resources</span></span>
* <span data-ttu-id="a5562-1178">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="a5562-1178">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a5562-1179">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1179">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a5562-1180">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="a5562-1180">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a5562-1181">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a5562-1181">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a5562-1182">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-1182">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a5562-1183">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a5562-1183">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1184">Az.Sql</span></span>
* <span data-ttu-id="a5562-1185">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="a5562-1185">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-1186">Az.Storage</span></span>
* <span data-ttu-id="a5562-1187">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="a5562-1187">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a5562-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a5562-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="a5562-1189">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="a5562-1189">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a5562-1190">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a5562-1190">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a5562-1191">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a5562-1191">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a5562-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a5562-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a5562-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a5562-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a5562-1194">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-1194">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a5562-1195">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a5562-1195">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a5562-1196">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a5562-1196">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a5562-1197">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a5562-1197">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a5562-1198">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a5562-1198">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a5562-1199">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="a5562-1199">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a5562-1200">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="a5562-1200">Highlights since the last major release</span></span>
* <span data-ttu-id="a5562-1201">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="a5562-1201">General availability of `Az` module</span></span>
* <span data-ttu-id="a5562-1202">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a5562-1202">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a5562-1203">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a5562-1203">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a5562-1204">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1204">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a5562-1205">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1205">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a5562-1206">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1206">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a5562-1207">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1207">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a5562-1208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a5562-1208">Az.Automation</span></span>
* <span data-ttu-id="a5562-1209">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="a5562-1209">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a5562-1210">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="a5562-1210">Dynamic grouping</span></span>
    * <span data-ttu-id="a5562-1211">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="a5562-1211">Pre-Post script</span></span>
    * <span data-ttu-id="a5562-1212">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="a5562-1212">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-1213">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1213">Az.Compute</span></span>
* <span data-ttu-id="a5562-1214">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1214">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a5562-1215">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="a5562-1215">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a5562-1216">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a5562-1216">Az.KeyVault</span></span>
* <span data-ttu-id="a5562-1217">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1217">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-1218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-1218">Az.Network</span></span>
* <span data-ttu-id="a5562-1219">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1219">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a5562-1220">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-1220">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="a5562-1222">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="a5562-1222">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a5562-1223">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1223">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-1224">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1224">Az.Resources</span></span>
* <span data-ttu-id="a5562-1225">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1225">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a5562-1226">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-1226">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-1227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1227">Az.Sql</span></span>
* <span data-ttu-id="a5562-1228">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="a5562-1228">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-1229">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-1229">Az.Storage</span></span>
* <span data-ttu-id="a5562-1230">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="a5562-1230">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a5562-1231">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a5562-1231">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a5562-1232">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a5562-1232">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a5562-1233">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a5562-1233">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a5562-1234">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a5562-1234">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a5562-1235">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a5562-1235">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a5562-1236">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a5562-1236">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-1237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-1237">Az.Websites</span></span>
* <span data-ttu-id="a5562-1238">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="a5562-1238">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="a5562-1239">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="a5562-1239">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a5562-1240">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-1240">Az.Accounts</span></span>
* <span data-ttu-id="a5562-1241">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="a5562-1241">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a5562-1242">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-1242">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a5562-1243">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a5562-1243">Az.Automation</span></span>
* <span data-ttu-id="a5562-1244">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1244">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a5562-1245">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="a5562-1245">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a5562-1246">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="a5562-1246">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a5562-1247">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a5562-1247">Az.Cdn</span></span>
* <span data-ttu-id="a5562-1248">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="a5562-1248">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-1249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1249">Az.Compute</span></span>
* <span data-ttu-id="a5562-1250">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1250">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a5562-1251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a5562-1251">Az.DataFactory</span></span>
* <span data-ttu-id="a5562-1252">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="a5562-1252">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a5562-1253">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a5562-1253">Az.LogicApp</span></span>
* <span data-ttu-id="a5562-1254">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="a5562-1254">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-1255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-1255">Az.Network</span></span>
* <span data-ttu-id="a5562-1256">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1256">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1257">Az.RecoveryServices</span></span>
* <span data-ttu-id="a5562-1258">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a5562-1258">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a5562-1259">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="a5562-1259">SDK Update</span></span>
* <span data-ttu-id="a5562-1260">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="a5562-1260">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a5562-1261">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1261">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-1262">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1262">Az.Resources</span></span>
* <span data-ttu-id="a5562-1263">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1263">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a5562-1264">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a5562-1264">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a5562-1265">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a5562-1265">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a5562-1266">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a5562-1266">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a5562-1267">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="a5562-1267">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a5562-1268">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a5562-1268">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-1269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1269">Az.Sql</span></span>
* <span data-ttu-id="a5562-1270">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="a5562-1270">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a5562-1271">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="a5562-1271">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-1272">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-1272">Az.Storage</span></span>
* <span data-ttu-id="a5562-1273">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5562-1273">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a5562-1274">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="a5562-1274">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a5562-1275">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1275">Az.AnalysisServices</span></span>
* <span data-ttu-id="a5562-1276">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="a5562-1276">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a5562-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a5562-1277">Az.Automation</span></span>
* <span data-ttu-id="a5562-1278">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-1278">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a5562-1279">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1279">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a5562-1280">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1280">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a5562-1281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1281">Az.CognitiveServices</span></span>
* <span data-ttu-id="a5562-1282">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-1282">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-1283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1283">Az.Compute</span></span>
* <span data-ttu-id="a5562-1284">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="a5562-1284">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a5562-1285">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="a5562-1285">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a5562-1286">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1286">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a5562-1287">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="a5562-1287">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a5562-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="a5562-1289">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="a5562-1289">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a5562-1290">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a5562-1290">Az.EventHub</span></span>
* <span data-ttu-id="a5562-1291">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="a5562-1291">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="a5562-1292">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a5562-1292">Az.KeyVault</span></span>
* <span data-ttu-id="a5562-1293">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="a5562-1293">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a5562-1294">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a5562-1294">Az.LogicApp</span></span>
* <span data-ttu-id="a5562-1295">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="a5562-1295">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a5562-1296">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="a5562-1296">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a5562-1297">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="a5562-1297">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a5562-1298">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a5562-1298">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a5562-1299">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a5562-1299">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a5562-1300">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a5562-1300">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a5562-1301">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a5562-1301">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a5562-1302">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="a5562-1302">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a5562-1303">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5562-1303">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a5562-1304">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5562-1304">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a5562-1305">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5562-1305">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a5562-1306">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5562-1306">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a5562-1307">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="a5562-1307">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a5562-1308">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a5562-1308">Az.Monitor</span></span>
* <span data-ttu-id="a5562-1309">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-1309">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-1310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-1310">Az.Network</span></span>
* <span data-ttu-id="a5562-1311">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="a5562-1311">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a5562-1312">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-1312">Az.OperationalInsights</span></span>
* <span data-ttu-id="a5562-1313">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-1313">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a5562-1314">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="a5562-1314">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="a5562-1315">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="a5562-1315">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="a5562-1316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1316">Az.Resources</span></span>
* <span data-ttu-id="a5562-1317">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a5562-1317">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a5562-1318">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a5562-1318">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a5562-1319">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a5562-1319">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a5562-1320">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="a5562-1320">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-1321">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1321">Az.Sql</span></span>
* <span data-ttu-id="a5562-1322">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-1322">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a5562-1323">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="a5562-1323">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-1324">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-1324">Az.Websites</span></span>
* <span data-ttu-id="a5562-1325">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-1325">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a5562-1326">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="a5562-1326">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a5562-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-1327">Az.Accounts</span></span>
* <span data-ttu-id="a5562-1328">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="a5562-1328">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a5562-1329">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1329">Az.AnalysisServices</span></span>
<span data-ttu-id="a5562-1330">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="a5562-1330">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-1331">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1331">Az.Compute</span></span>
* <span data-ttu-id="a5562-1332">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="a5562-1332">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a5562-1333">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="a5562-1333">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a5562-1334">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="a5562-1334">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-1335">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1335">Az.RecoveryServices</span></span>
<span data-ttu-id="a5562-1336">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="a5562-1336">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-1337">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1337">Az.Resources</span></span>
* <span data-ttu-id="a5562-1338">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-1338">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="a5562-1339">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a5562-1339">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a5562-1340">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="a5562-1340">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="a5562-1341">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a5562-1341">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-1342">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1342">Az.Sql</span></span>
* <span data-ttu-id="a5562-1343">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-1343">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a5562-1344">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="a5562-1344">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a5562-1345">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="a5562-1345">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a5562-1346">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="a5562-1346">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a5562-1347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-1347">Az.Accounts</span></span>
* <span data-ttu-id="a5562-1348">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="a5562-1348">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a5562-1349">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1349">Az.AnalysisServices</span></span>
* <span data-ttu-id="a5562-1350">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="a5562-1350">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-1351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1351">Az.RecoveryServices</span></span>
* <span data-ttu-id="a5562-1352">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="a5562-1352">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a5562-1353">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="a5562-1353">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a5562-1354">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-1354">Az.Accounts</span></span>
* <span data-ttu-id="a5562-1355">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1355">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a5562-1356">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1356">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a5562-1357">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="a5562-1357">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a5562-1358">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a5562-1358">Az.Aks</span></span>
* <span data-ttu-id="a5562-1359">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1359">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a5562-1360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a5562-1360">Az.Automation</span></span>
* <span data-ttu-id="a5562-1361">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="a5562-1361">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a5562-1362">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1362">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a5562-1363">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a5562-1363">Az.Cdn</span></span>
* <span data-ttu-id="a5562-1364">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1364">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-1365">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1365">Az.Compute</span></span>
* <span data-ttu-id="a5562-1366">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="a5562-1366">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a5562-1367">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-1367">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a5562-1368">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-1368">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a5562-1369">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a5562-1369">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a5562-1370">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1370">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a5562-1371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a5562-1371">Az.DataFactory</span></span>
* <span data-ttu-id="a5562-1372">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="a5562-1372">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a5562-1373">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-1373">Az.DataLakeStore</span></span>
* <span data-ttu-id="a5562-1374">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="a5562-1374">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a5562-1375">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a5562-1375">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a5562-1376">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1376">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a5562-1377">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a5562-1377">Az.IotHub</span></span>
* <span data-ttu-id="a5562-1378">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-1378">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a5562-1379">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a5562-1379">Az.KeyVault</span></span>
* <span data-ttu-id="a5562-1380">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1380">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-1381">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-1381">Az.Network</span></span>
* <span data-ttu-id="a5562-1382">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1382">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-1383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1383">Az.Resources</span></span>
* <span data-ttu-id="a5562-1384">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="a5562-1384">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a5562-1385">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="a5562-1385">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a5562-1386">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-1386">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a5562-1387">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a5562-1387">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a5562-1388">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a5562-1388">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a5562-1389">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a5562-1389">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a5562-1390">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a5562-1390">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a5562-1391">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a5562-1391">Az.ServiceFabric</span></span>
* <span data-ttu-id="a5562-1392">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="a5562-1392">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a5562-1393">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-1393">Fix some error messages.</span></span>
* <span data-ttu-id="a5562-1394">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="a5562-1394">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a5562-1395">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="a5562-1395">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a5562-1396">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a5562-1396">Az.SignalR</span></span>
* <span data-ttu-id="a5562-1397">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1397">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1398">Az.Sql</span></span>
* <span data-ttu-id="a5562-1399">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1399">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a5562-1400">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="a5562-1400">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a5562-1401">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="a5562-1401">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a5562-1402">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="a5562-1402">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-1403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-1403">Az.Storage</span></span>
* <span data-ttu-id="a5562-1404">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1404">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a5562-1405">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="a5562-1405">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a5562-1406">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a5562-1406">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a5562-1407">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a5562-1407">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a5562-1408">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a5562-1408">Az.TrafficManager</span></span>
* <span data-ttu-id="a5562-1409">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1409">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-1410">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-1410">Az.Websites</span></span>
* <span data-ttu-id="a5562-1411">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a5562-1411">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a5562-1412">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="a5562-1412">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a5562-1413">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="a5562-1413">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a5562-1414">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="a5562-1414">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a5562-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-1415">Az.Accounts</span></span>
* <span data-ttu-id="a5562-1416">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1416">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-1417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1417">Az.Compute</span></span>
* <span data-ttu-id="a5562-1418">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="a5562-1418">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a5562-1419">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="a5562-1419">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a5562-1420">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="a5562-1420">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a5562-1421">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-1421">Az.DataLakeStore</span></span>
* <span data-ttu-id="a5562-1422">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="a5562-1422">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a5562-1423">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="a5562-1423">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a5562-1424">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a5562-1424">Az.EventGrid</span></span>
* <span data-ttu-id="a5562-1425">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="a5562-1425">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a5562-1426">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="a5562-1426">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a5562-1427">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="a5562-1427">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a5562-1428">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="a5562-1428">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a5562-1429">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="a5562-1429">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a5562-1430">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="a5562-1430">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a5562-1431">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="a5562-1431">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a5562-1432">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="a5562-1432">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a5562-1433">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="a5562-1433">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a5562-1434">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="a5562-1434">Dead letter endpoint.</span></span>
* <span data-ttu-id="a5562-1435">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="a5562-1435">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a5562-1436">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="a5562-1436">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a5562-1437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a5562-1437">Az.IotHub</span></span>
* <span data-ttu-id="a5562-1438">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="a5562-1438">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a5562-1439">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a5562-1439">Az.LogicApp</span></span>
* <span data-ttu-id="a5562-1440">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="a5562-1440">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1441">Az.Resources</span></span>
* <span data-ttu-id="a5562-1442">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="a5562-1442">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a5562-1443">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a5562-1443">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a5562-1444">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="a5562-1444">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a5562-1445">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a5562-1445">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a5562-1446">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1446">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a5562-1447">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a5562-1447">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a5562-1448">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a5562-1448">Az.SignalR</span></span>
* <span data-ttu-id="a5562-1449">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="a5562-1449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1450">Az.Sql</span></span>
* <span data-ttu-id="a5562-1451">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="a5562-1451">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a5562-1452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-1452">Az.Storage</span></span>
* <span data-ttu-id="a5562-1453">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="a5562-1453">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a5562-1454">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a5562-1454">New-AzStorageContext</span></span>
* <span data-ttu-id="a5562-1455">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="a5562-1455">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a5562-1456">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a5562-1456">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-1457">Az.Websites</span></span>
* <span data-ttu-id="a5562-1458">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a5562-1458">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a5562-1459">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="a5562-1459">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a5562-1460">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="a5562-1460">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a5562-1461">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a5562-1461">General</span></span>

- <span data-ttu-id="a5562-1462">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="a5562-1462">General Availability of Az Module</span></span>
- <span data-ttu-id="a5562-1463">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1463">Online help for each module</span></span>
- <span data-ttu-id="a5562-1464">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="a5562-1464">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a5562-1465">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1465">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a5562-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-1466">Az.Accounts</span></span>
- <span data-ttu-id="a5562-1467">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="a5562-1467">Changed from Az.Profile</span></span>
- <span data-ttu-id="a5562-1468">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1468">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a5562-1469">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5562-1469">Az.ApiManagement</span></span>
- <span data-ttu-id="a5562-1470">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="a5562-1470">Fixes for #7002</span></span>
- <span data-ttu-id="a5562-1471">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1471">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a5562-1472">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a5562-1472">Az.Batch</span></span>
- <span data-ttu-id="a5562-1473">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="a5562-1473">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a5562-1474">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="a5562-1474">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a5562-1475">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1475">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a5562-1476">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a5562-1476">Az.Billing</span></span>
- <span data-ttu-id="a5562-1477">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="a5562-1477">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a5562-1478">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1478">Az.CognitivServices</span></span>
- <span data-ttu-id="a5562-1479">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="a5562-1479">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a5562-1480">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="a5562-1480">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a5562-1481">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a5562-1481">Az.ContainerInstance</span></span>
- <span data-ttu-id="a5562-1482">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="a5562-1482">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a5562-1483">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a5562-1483">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a5562-1484">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1484">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a5562-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-1485">Az.DataLakeStore</span></span>
- <span data-ttu-id="a5562-1486">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1486">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a5562-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a5562-1487">Az.Monitor</span></span>
- <span data-ttu-id="a5562-1488">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1488">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a5562-1489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a5562-1489">Az.KeyVault</span></span>
- <span data-ttu-id="a5562-1490">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-1490">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a5562-1491">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a5562-1491">Az.MachineLearning</span></span>
- <span data-ttu-id="a5562-1492">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="a5562-1492">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a5562-1493">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a5562-1493">Az.Media</span></span>
- <span data-ttu-id="a5562-1494">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="a5562-1494">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a5562-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-1495">Az.Network</span></span>
<span data-ttu-id="a5562-1496">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="a5562-1496">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a5562-1497">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a5562-1497">New cmdlets added:</span></span>
        - <span data-ttu-id="a5562-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5562-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a5562-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5562-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a5562-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5562-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a5562-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5562-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a5562-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5562-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a5562-1503">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a5562-1503">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a5562-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a5562-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a5562-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5562-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a5562-1506">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-1506">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a5562-1507">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5562-1507">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a5562-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a5562-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a5562-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a5562-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a5562-1510">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-1510">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a5562-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a5562-1512">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a5562-1512">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a5562-1513">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5562-1513">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a5562-1514">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a5562-1514">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a5562-1515">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a5562-1515">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a5562-1516">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a5562-1516">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a5562-1517">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="a5562-1517">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a5562-1518">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a5562-1519">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-1519">Az.OperationalInsights</span></span>
- <span data-ttu-id="a5562-1520">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1520">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a5562-1521">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a5562-1521">Az.Profile</span></span>
- <span data-ttu-id="a5562-1522">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a5562-1522">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-1523">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1523">Az.RecoveryServices</span></span>
- <span data-ttu-id="a5562-1524">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1524">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a5562-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1525">Az.Resources</span></span>
- <span data-ttu-id="a5562-1526">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1526">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a5562-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a5562-1527">Az.ServiceFabric</span></span>
- <span data-ttu-id="a5562-1528">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a5562-1528">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a5562-1529">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1529">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a5562-1530">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a5562-1530">Az.SIgnalR</span></span>
- <span data-ttu-id="a5562-1531">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="a5562-1531">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a5562-1532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1532">Az.Sql</span></span>
- <span data-ttu-id="a5562-1533">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1533">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a5562-1534">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="a5562-1534">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a5562-1535">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a5562-1536">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-1536">Az.Storage</span></span>
- <span data-ttu-id="a5562-1537">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a5562-1538">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-1538">Az.Websites</span></span>
- <span data-ttu-id="a5562-1539">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a5562-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a5562-1540">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="a5562-1540">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a5562-1541">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a5562-1541">General</span></span>

* <span data-ttu-id="a5562-1542">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-1542">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a5562-1543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1543">Az.Compute</span></span>

* <span data-ttu-id="a5562-1544">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="a5562-1544">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a5562-1545">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-1545">Az.DataLakeStore</span></span>

* <span data-ttu-id="a5562-1546">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="a5562-1546">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a5562-1547">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a5562-1547">Az.FrontDoor</span></span>

* <span data-ttu-id="a5562-1548">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-1548">Fixed some broken links</span></span>
    - <span data-ttu-id="a5562-1549">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="a5562-1549">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a5562-1550">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="a5562-1550">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a5562-1551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1551">Az.RecoveryServices</span></span>

* <span data-ttu-id="a5562-1552">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="a5562-1552">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a5562-1553">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="a5562-1553">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a5562-1554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1554">Az.Resources</span></span>

* <span data-ttu-id="a5562-1555">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-1555">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a5562-1556">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="a5562-1556">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a5562-1557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1557">Az.Sql</span></span>

* <span data-ttu-id="a5562-1558">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="a5562-1558">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a5562-1559">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="a5562-1559">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a5562-1560">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="a5562-1560">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a5562-1561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-1561">Az.Storage</span></span>

* <span data-ttu-id="a5562-1562">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1562">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a5562-1563">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="a5562-1563">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a5562-1564">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a5562-1564">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a5562-1565">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="a5562-1565">Support Static Website configuration</span></span>
    - <span data-ttu-id="a5562-1566">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a5562-1566">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a5562-1567">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a5562-1567">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a5562-1568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-1568">Az.Websites</span></span>

* <span data-ttu-id="a5562-1569">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a5562-1569">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="a5562-1570">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="a5562-1570">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a5562-1571">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="a5562-1571">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a5562-1572">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="a5562-1572">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a5562-1573">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5562-1573">Az.ApiManagement</span></span>
* <span data-ttu-id="a5562-1574">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="a5562-1574">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a5562-1575">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a5562-1575">Az.Automation</span></span>
* <span data-ttu-id="a5562-1576">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="a5562-1576">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a5562-1577">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a5562-1577">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a5562-1578">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a5562-1578">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a5562-1579">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="a5562-1579">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a5562-1580">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="a5562-1580">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a5562-1581">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1581">Az.Compute</span></span>
* <span data-ttu-id="a5562-1582">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="a5562-1582">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a5562-1583">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="a5562-1583">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a5562-1584">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a5562-1584">Az.ContainerInstance</span></span>
* <span data-ttu-id="a5562-1585">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="a5562-1585">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a5562-1586">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a5562-1586">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a5562-1587">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="a5562-1587">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a5562-1588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-1588">Az.Network</span></span>
* <span data-ttu-id="a5562-1589">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="a5562-1589">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a5562-1590">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="a5562-1590">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a5562-1591">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="a5562-1591">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="a5562-1592">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="a5562-1592">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a5562-1593">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a5562-1593">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a5562-1594">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="a5562-1594">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a5562-1595">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="a5562-1595">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a5562-1596">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a5562-1596">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a5562-1597">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="a5562-1597">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a5562-1598">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="a5562-1598">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a5562-1599">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a5562-1599">Az.Relay</span></span>
* <span data-ttu-id="a5562-1600">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1600">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a5562-1601">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1601">Az.Resources</span></span>
* <span data-ttu-id="a5562-1602">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="a5562-1602">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a5562-1603">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="a5562-1603">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a5562-1604">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="a5562-1604">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a5562-1605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a5562-1605">Az.ServiceFabric</span></span>
* <span data-ttu-id="a5562-1606">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-1606">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a5562-1607">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1607">Az.Sql</span></span>
* <span data-ttu-id="a5562-1608">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="a5562-1608">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a5562-1609">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a5562-1609">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a5562-1610">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a5562-1610">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a5562-1611">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a5562-1611">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a5562-1612">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a5562-1612">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a5562-1613">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a5562-1613">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a5562-1614">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a5562-1614">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a5562-1615">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a5562-1615">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a5562-1616">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a5562-1616">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a5562-1617">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="a5562-1617">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a5562-1618">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="a5562-1618">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a5562-1619">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="a5562-1619">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a5562-1620">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a5562-1620">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a5562-1621">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a5562-1621">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a5562-1622">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a5562-1622">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a5562-1623">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a5562-1623">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a5562-1624">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="a5562-1624">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a5562-1625">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="a5562-1625">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a5562-1626">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a5562-1626">General</span></span>
* <span data-ttu-id="a5562-1627">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="a5562-1627">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a5562-1628">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a5562-1628">Az.Profile</span></span>
* <span data-ttu-id="a5562-1629">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="a5562-1629">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a5562-1630">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="a5562-1630">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a5562-1631">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="a5562-1631">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a5562-1632">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="a5562-1632">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a5562-1633">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="a5562-1633">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a5562-1634">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="a5562-1634">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a5562-1635">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="a5562-1635">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a5562-1636">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1636">Az.CognitiveServices</span></span>
* <span data-ttu-id="a5562-1637">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="a5562-1637">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-1638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1638">Az.Compute</span></span>
* <span data-ttu-id="a5562-1639">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="a5562-1639">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a5562-1640">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="a5562-1640">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a5562-1641">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="a5562-1641">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a5562-1642">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-1642">Az.DataLakeStore</span></span>
* <span data-ttu-id="a5562-1643">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="a5562-1643">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a5562-1644">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="a5562-1644">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a5562-1645">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a5562-1645">Az.Insights</span></span>
* <span data-ttu-id="a5562-1646">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="a5562-1646">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a5562-1647">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="a5562-1647">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a5562-1648">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="a5562-1648">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a5562-1649">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="a5562-1649">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-1650">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-1650">Az.Network</span></span>
* <span data-ttu-id="a5562-1651">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="a5562-1651">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a5562-1652">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a5562-1652">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a5562-1653">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a5562-1653">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a5562-1654">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a5562-1654">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a5562-1655">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a5562-1655">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a5562-1656">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a5562-1656">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a5562-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a5562-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a5562-1658">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a5562-1658">Az.PolicyInsights</span></span>
* <span data-ttu-id="a5562-1659">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-1659">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1660">Az.Resources</span></span>
* <span data-ttu-id="a5562-1661">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="a5562-1661">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a5562-1662">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="a5562-1662">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a5562-1663">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a5562-1663">Az.ServiceBus</span></span>
* <span data-ttu-id="a5562-1664">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="a5562-1664">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a5562-1665">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a5562-1665">Az.ServiceFabric</span></span>
* <span data-ttu-id="a5562-1666">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="a5562-1666">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a5562-1667">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="a5562-1667">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a5562-1668">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a5562-1668">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a5562-1669">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a5562-1669">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a5562-1670">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="a5562-1670">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a5562-1671">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="a5562-1671">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a5562-1672">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a5562-1672">Az.Profile</span></span>
* <span data-ttu-id="a5562-1673">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="a5562-1673">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a5562-1674">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="a5562-1674">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-1675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1675">Az.Compute</span></span>
* <span data-ttu-id="a5562-1676">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="a5562-1676">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a5562-1677">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="a5562-1677">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a5562-1678">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a5562-1678">Az.DataLakeStore</span></span>
* <span data-ttu-id="a5562-1679">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="a5562-1679">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a5562-1680">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="a5562-1680">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a5562-1681">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a5562-1681">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a5562-1682">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="a5562-1682">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a5562-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="a5562-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-1684">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-1684">Az.Network</span></span>
* <span data-ttu-id="a5562-1685">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="a5562-1685">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a5562-1686">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="a5562-1686">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1687">Az.Resources</span></span>
* <span data-ttu-id="a5562-1688">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="a5562-1688">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a5562-1689">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="a5562-1689">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a5562-1690">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="a5562-1690">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a5562-1691">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a5562-1691">Azure.Storage</span></span>
* <span data-ttu-id="a5562-1692">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="a5562-1692">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a5562-1693">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a5562-1693">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a5562-1694">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a5562-1694">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a5562-1695">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="a5562-1695">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a5562-1696">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a5562-1696">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="a5562-1697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a5562-1697">Az.CognitiveServices</span></span>
* <span data-ttu-id="a5562-1698">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="a5562-1698">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a5562-1699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a5562-1699">Az.Compute</span></span>
* <span data-ttu-id="a5562-1700">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="a5562-1700">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a5562-1701">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="a5562-1701">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a5562-1702">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="a5562-1702">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a5562-1703">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a5562-1703">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a5562-1704">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="a5562-1704">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a5562-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a5562-1705">Az.Network</span></span>
* <span data-ttu-id="a5562-1706">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="a5562-1706">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a5562-1707">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a5562-1707">new cmdlets added</span></span>
    - <span data-ttu-id="a5562-1708">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a5562-1708">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a5562-1709">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a5562-1709">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a5562-1710">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a5562-1710">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a5562-1711">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a5562-1711">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a5562-1712">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-1712">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a5562-1713">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5562-1713">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a5562-1714">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="a5562-1714">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a5562-1715">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="a5562-1715">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a5562-1716">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="a5562-1716">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a5562-1717">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a5562-1717">Az.RedisCache</span></span>
* <span data-ttu-id="a5562-1718">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="a5562-1718">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a5562-1719">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1719">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a5562-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a5562-1720">Az.Resources</span></span>
* <span data-ttu-id="a5562-1721">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a5562-1721">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a5562-1722">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="a5562-1722">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a5562-1723">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a5562-1723">Az.Sql</span></span>
* <span data-ttu-id="a5562-1724">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="a5562-1724">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a5562-1725">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a5562-1725">Az.Websites</span></span>
* <span data-ttu-id="a5562-1726">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="a5562-1726">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a5562-1727">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="a5562-1727">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a5562-1728">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="a5562-1728">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a5562-1729">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="a5562-1729">Initial Release</span></span>
