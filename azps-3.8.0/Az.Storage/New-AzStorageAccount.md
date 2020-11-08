---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c88e56a485f9e42daf229667ab4c07d7a7464578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013146"
---
# <span data-ttu-id="b5fb1-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5fb1-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="b5fb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fb1-103">Tároló fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-103">Creates a Storage account.</span></span>

## <span data-ttu-id="b5fb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5fb1-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5fb1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="b5fb1-106">A **New-AzStorageAccount** parancsmag egy Azure Storage-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="b5fb1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b5fb1-107">EXAMPLES</span></span>

### <span data-ttu-id="b5fb1-108">Példa 1: tárterület-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="b5fb1-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="b5fb1-109">Ez a parancs létrehoz egy tárolási fiókot az erőforráscsoport neve MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="b5fb1-110">2. példa: blob-tároló létrehozása a BlobStorage-féle és a forró AccessTier</span><span class="sxs-lookup"><span data-stu-id="b5fb1-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="b5fb1-111">Ez a parancs olyan blob-tárterületet hoz létre, amely BlobStorage típusú és forró AccessTier</span><span class="sxs-lookup"><span data-stu-id="b5fb1-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="b5fb1-112">3. példa: hozzon létre egy Kind StorageV2 tároló fiókot, és hozzon létre és rendeljen identitást az Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="b5fb1-113">Ez a parancs a Kind StorageV2 létrehoz egy tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="b5fb1-114">Egy identitást hoz létre, és hozzárendel egy olyan identitást, amellyel az Azure-kulccsal kezelheti a fiókok kulcsait.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="b5fb1-115">Példa 4: a NetworkRuleSet származó tárhely-fiók létrehozása a JSON-ról</span><span class="sxs-lookup"><span data-stu-id="b5fb1-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="b5fb1-116">Ez a parancs létrehoz egy olyan tárolási fiókot, amely a NetworkRuleSet tulajdonságot tartalmazza a JSON-ról</span><span class="sxs-lookup"><span data-stu-id="b5fb1-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="b5fb1-117">Példa 5: tárterület-fiók létrehozása a hierarchikus névtér engedélyezve értékkel.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="b5fb1-118">Ez a parancs létrehoz egy olyan tárterület-fiókot, amelyben a hierarchikus névtér engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="b5fb1-119">6. példa: hozzon létre egy tárterületet az Azure-fájlokkal AAD DS-hitelesítéssel, és engedélyezze a nagyméretű fájlok megosztását.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="b5fb1-120">Ez a parancs létrehoz egy olyan tárterület-fiókot, amely Azure-fájlokat AAD a DS-hitelesítéshez, és lehetővé teszi a nagyméretű fájlok megosztását.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-120">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share..</span></span>

### <span data-ttu-id="b5fb1-121">8. példa: tárolási fiók létrehozása várólistával és a táblázat szolgáltatással: a fiók hatókörű titkosítási kulcsát használja.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-121">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account
```

<span data-ttu-id="b5fb1-122">Ez a parancs létrehoz egy tárolási fiókot a várólistával és a táblázat szolgáltatással fiók-hatókörű titkosítási kulccsal, így a várólista és a táblázat ugyanazt a titkosítási kulcsot használja, mint a blob és a file szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-122">This command creates a Storage account with Queue and Table Service use account-scoped encryption key, so Queue and Table will use same encryption key with Blob and File service.</span></span> <span data-ttu-id="b5fb1-123">Ezután kapja meg a tárterület-fiók tulajdonságait, és tekintse meg a várólista és a táblázat szolgáltatás titkosítási típusát.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-123">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service.</span></span>

## <span data-ttu-id="b5fb1-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5fb1-124">PARAMETERS</span></span>

### <span data-ttu-id="b5fb1-125">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="b5fb1-125">-AccessTier</span></span>
<span data-ttu-id="b5fb1-126">A parancsmag által létrehozott tárolási fiók hozzáférési rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-126">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="b5fb1-127">A paraméter elfogadható értékei a következők: meleg és hűvös.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-127">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="b5fb1-128">Ha a BlobStorage értékét adja meg a *Kind* paraméterhez, meg kell adnia a *AccessTier* paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-128">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="b5fb1-129">Ha *a tárterület* értékére vonatkozó értéket ad meg, ne adja meg a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-129">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5fb1-130">-AsJob</span></span>
<span data-ttu-id="b5fb1-131">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b5fb1-131">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b5fb1-132">-AssignIdentity</span></span>
<span data-ttu-id="b5fb1-133">Új tárolási fiók identitásának létrehozása és hozzárendelése ehhez a tárterülethez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-133">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="b5fb1-134">-CustomDomainName</span></span>
<span data-ttu-id="b5fb1-135">A tárolási fiók egyéni tartományának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-135">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="b5fb1-136">Az alapértelmezett érték a tárterület.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-136">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5fb1-137">-DefaultProfile</span></span>
<span data-ttu-id="b5fb1-138">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-139">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="b5fb1-139">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="b5fb1-140">Engedélyezze az Azure-fájlok Azure Active Directory tartományi szolgáltatás általi hitelesítését a tárolási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-140">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-141">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="b5fb1-141">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="b5fb1-142">Azt jelzi, hogy a tárolási fiók engedélyezi-e a hierarchikus névteret.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-142">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-143">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="b5fb1-143">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="b5fb1-144">Azt jelzi, hogy a tárolási fiók csak HTTPS-forgalmat engedélyez-e.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-144">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-145">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="b5fb1-145">-EnableLargeFileShare</span></span>
<span data-ttu-id="b5fb1-146">Azt jelzi, hogy a tárolási fiók támogatja-e az 5 TiB-nál több kapacitással rendelkező nagyméretű fájlmegosztás használatát.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-146">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="b5fb1-147">Miután a fiók engedélyezve van, a funkció nem tiltható le.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-147">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="b5fb1-148">Jelenleg csak a LRS és a ZRS replikációs típusai támogatottak, ezért nem lehetett beírni a "geo-redundáns fiókok" konverzióját.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-148">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="b5fb1-149">További információ https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="b5fb1-149">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-150">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="b5fb1-150">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="b5fb1-151">Állítsa be a várólista titkosítási típusát.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-151">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="b5fb1-152">Az alapértelmezett érték a szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-152">The default value is Service.</span></span>
<span data-ttu-id="b5fb1-153">-Fiók: a várólista a fiók hatókörű titkosítási kulccsal lesz titkosítva.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-153">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="b5fb1-154">-Szolgáltatás: a várólista mindig Service-Managed kulcsokkal lesz titkosítva.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-154">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-155">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="b5fb1-155">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="b5fb1-156">Állítsa be a tábla titkosítási típusát.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-156">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="b5fb1-157">Az alapértelmezett érték a szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-157">The default value is Service.</span></span>
- <span data-ttu-id="b5fb1-158">Fiók: a tábla a fiókhoz tartozó titkosítási kulccsal lesz titkosítva.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-158">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="b5fb1-159">Szolgáltatás: a táblázat Service-Managed billentyűvel mindig titkosítva lesz.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-159">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-160">-Kind</span><span class="sxs-lookup"><span data-stu-id="b5fb1-160">-Kind</span></span>
<span data-ttu-id="b5fb1-161">A parancsmag által létrehozott tárolási fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-161">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="b5fb1-162">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b5fb1-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b5fb1-163">Tárterület.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-163">Storage.</span></span> <span data-ttu-id="b5fb1-164">Általános célú tárolási fiók, amely támogatja a Blobs, a táblázatok, a várólisták, a fájlok és a lemezek tárolását.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-164">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="b5fb1-165">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-165">StorageV2.</span></span> <span data-ttu-id="b5fb1-166">Általános célú 2-es verzió (GPv2) tárterülete, melyen a festékfoltok, a táblázatok, a várólisták, a fájlok és a lemezek a speciális funkciók, például az adatrétegek támogatása.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-166">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="b5fb1-167">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-167">BlobStorage.</span></span> <span data-ttu-id="b5fb1-168">BLOB-tároló fiók, amely támogatja a BLOB-tárolót.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-168">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="b5fb1-169">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-169">BlockBlobStorage.</span></span> <span data-ttu-id="b5fb1-170">A blob-tároló fiók zárolása, amely támogatja a csak blokkos Blobok tárolását.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-170">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="b5fb1-171">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-171">FileStorage.</span></span> <span data-ttu-id="b5fb1-172">A csak a fájlok tárterületét támogató fájl-tároló fiók.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-172">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="b5fb1-173">Az alapértelmezett érték a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-173">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-174">-Hely</span><span class="sxs-lookup"><span data-stu-id="b5fb1-174">-Location</span></span>
<span data-ttu-id="b5fb1-175">A létrehozandó tárterület-fiók helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-175">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-176">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5fb1-176">-Name</span></span>
<span data-ttu-id="b5fb1-177">A létrehozandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-177">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-178">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b5fb1-178">-NetworkRuleSet</span></span>
<span data-ttu-id="b5fb1-179">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé tevő, valamint a meghatározott szabályoknak nem megfelelő kérelmek kezelésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-179">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5fb1-180">-ResourceGroupName</span></span>
<span data-ttu-id="b5fb1-181">Annak az erőforrás-csoportnak a nevét adja meg, amelybe a tárolási fiókot hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-181">Specifies the name of the resource group in which to add the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-182">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b5fb1-182">-SkuName</span></span>
<span data-ttu-id="b5fb1-183">Megadja annak a tárolási fióknak az SKU-nevét, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-183">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="b5fb1-184">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b5fb1-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b5fb1-185">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-185">Standard_LRS.</span></span> <span data-ttu-id="b5fb1-186">Helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-186">Locally-redundant storage.</span></span>
- <span data-ttu-id="b5fb1-187">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-187">Standard_ZRS.</span></span> <span data-ttu-id="b5fb1-188">Zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-188">Zone-redundant storage.</span></span>
- <span data-ttu-id="b5fb1-189">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-189">Standard_GRS.</span></span> <span data-ttu-id="b5fb1-190">Geo-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-190">Geo-redundant storage.</span></span>
- <span data-ttu-id="b5fb1-191">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-191">Standard_RAGRS.</span></span> <span data-ttu-id="b5fb1-192">Olvassa el az Access geo-redundáns tárterülete című témakört.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-192">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="b5fb1-193">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-193">Premium_LRS.</span></span> <span data-ttu-id="b5fb1-194">Prémium lokálisan redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-194">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="b5fb1-195">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-195">Premium_ZRS.</span></span> <span data-ttu-id="b5fb1-196">Prémium zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-196">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="b5fb1-197">Standard_GZRS-geo-redundáns zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-197">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="b5fb1-198">Standard_RAGZRS – az Access geo-redundáns zónája – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-198">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-199">-Címke</span><span class="sxs-lookup"><span data-stu-id="b5fb1-199">-Tag</span></span>
<span data-ttu-id="b5fb1-200">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-200">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="b5fb1-201">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="b5fb1-201">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-202">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="b5fb1-202">-UseSubDomain</span></span>
<span data-ttu-id="b5fb1-203">Azt jelzi, hogy engedélyezi-e a közvetlen CName érvényesítést.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-203">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fb1-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fb1-204">CommonParameters</span></span>
<span data-ttu-id="b5fb1-205">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5fb1-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fb1-206">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fb1-207">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5fb1-207">INPUTS</span></span>

### <span data-ttu-id="b5fb1-208">System. String</span><span class="sxs-lookup"><span data-stu-id="b5fb1-208">System.String</span></span>

## <span data-ttu-id="b5fb1-209">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5fb1-209">OUTPUTS</span></span>

### <span data-ttu-id="b5fb1-210">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5fb1-210">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="b5fb1-211">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5fb1-211">NOTES</span></span>

## <span data-ttu-id="b5fb1-212">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5fb1-212">RELATED LINKS</span></span>

[<span data-ttu-id="b5fb1-213">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5fb1-213">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="b5fb1-214">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5fb1-214">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="b5fb1-215">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5fb1-215">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
