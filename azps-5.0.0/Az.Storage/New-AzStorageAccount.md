---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187189"
---
# <span data-ttu-id="da48f-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="da48f-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="da48f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da48f-102">SYNOPSIS</span></span>
<span data-ttu-id="da48f-103">Tároló fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="da48f-103">Creates a Storage account.</span></span>

## <span data-ttu-id="da48f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da48f-104">SYNTAX</span></span>

### <span data-ttu-id="da48f-105">AzureActiveDirectoryDomainServicesForFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da48f-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da48f-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="da48f-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da48f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="da48f-107">DESCRIPTION</span></span>
<span data-ttu-id="da48f-108">A **New-AzStorageAccount** parancsmag egy Azure Storage-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="da48f-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="da48f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="da48f-109">EXAMPLES</span></span>

### <span data-ttu-id="da48f-110">Példa 1: tárterület-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="da48f-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="da48f-111">Ez a parancs létrehoz egy tárolási fiókot az erőforráscsoport neve MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="da48f-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="da48f-112">2. példa: blob-tároló létrehozása a BlobStorage-féle és a forró AccessTier</span><span class="sxs-lookup"><span data-stu-id="da48f-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="da48f-113">Ez a parancs olyan blob-tárterületet hoz létre, amely BlobStorage típusú és forró AccessTier</span><span class="sxs-lookup"><span data-stu-id="da48f-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="da48f-114">3. példa: hozzon létre egy Kind StorageV2 tároló fiókot, és hozzon létre és rendeljen identitást az Azure.</span><span class="sxs-lookup"><span data-stu-id="da48f-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="da48f-115">Ez a parancs a Kind StorageV2 létrehoz egy tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="da48f-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="da48f-116">Egy identitást hoz létre, és hozzárendel egy olyan identitást, amellyel az Azure-kulccsal kezelheti a fiókok kulcsait.</span><span class="sxs-lookup"><span data-stu-id="da48f-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="da48f-117">Példa 4: a NetworkRuleSet származó tárhely-fiók létrehozása a JSON-ról</span><span class="sxs-lookup"><span data-stu-id="da48f-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="da48f-118">Ez a parancs létrehoz egy olyan tárolási fiókot, amely a NetworkRuleSet tulajdonságot tartalmazza a JSON-ról</span><span class="sxs-lookup"><span data-stu-id="da48f-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="da48f-119">Példa 5: tárterület-fiók létrehozása a hierarchikus névtér engedélyezve értékkel.</span><span class="sxs-lookup"><span data-stu-id="da48f-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="da48f-120">Ez a parancs létrehoz egy olyan tárterület-fiókot, amelyben a hierarchikus névtér engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="da48f-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="da48f-121">6. példa: hozzon létre egy tárterületet az Azure-fájlokkal AAD DS-hitelesítéssel, és engedélyezze a nagyméretű fájlok megosztását.</span><span class="sxs-lookup"><span data-stu-id="da48f-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="da48f-122">Ez a parancs létrehoz egy olyan tárterület-fiókot, amely Azure-fájlokat AAD a DS-hitelesítéshez, és lehetővé teszi a nagyméretű fájlok megosztását.</span><span class="sxs-lookup"><span data-stu-id="da48f-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="da48f-123">7. példa: hozzon létre egy tárolási fiókot, és engedélyezze a fájlok Active Directory tartományi szolgáltatás hitelesítését.</span><span class="sxs-lookup"><span data-stu-id="da48f-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="da48f-124">Ez a parancs létrehoz egy tárolási fiókot withenable-fájlok Active Directory tartományi szolgáltatás-hitelesítéssel.</span><span class="sxs-lookup"><span data-stu-id="da48f-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="da48f-125">8. példa: a várólista-és a táblázat-szolgáltatási tárterület létrehozásakor fiók-hatókörű titkosítási kulccsal kell rendelkezniük, és infrastrukturális titkosítást kell használniuk.</span><span class="sxs-lookup"><span data-stu-id="da48f-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

<span data-ttu-id="da48f-126">Ez a parancs létrehoz egy tárolási fiókot a várólistával és a táblázat szolgáltatással, és a fiók hatókörű titkosítási kulcsát használja, és infrastruktúra-titkosítást igényel, ezért a várólista és a táblázat ugyanazzal a titkosítási kulccsal fog rendelkezni, mint a blob és a fájlkezelő, valamint a szolgáltatás a többszintű adatok platformon kezelt kulcsait alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="da48f-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="da48f-127">Ezután kapja meg a tárolási fiók tulajdonságait, és tekintse meg a várólista és a táblázat szolgáltatás titkosítási típusát, valamint a RequireInfrastructureEncryption értékét.</span><span class="sxs-lookup"><span data-stu-id="da48f-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="da48f-128">9. példa: fiók MinimumTlsVersion és AllowBlobPublicAccess létrehozása</span><span class="sxs-lookup"><span data-stu-id="da48f-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="da48f-129">A parancs létrehoz egy fiókot a MinimumTlsVersion és a AllowBlobPublicAccess, majd megjeleníti a létrehozott fiók 2 tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="da48f-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="da48f-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da48f-130">PARAMETERS</span></span>

### <span data-ttu-id="da48f-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="da48f-131">-AccessTier</span></span>
<span data-ttu-id="da48f-132">A parancsmag által létrehozott tárolási fiók hozzáférési rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da48f-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="da48f-133">A paraméter elfogadható értékei a következők: meleg és hűvös.</span><span class="sxs-lookup"><span data-stu-id="da48f-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="da48f-134">Ha a BlobStorage értékét adja meg a *Kind* paraméterhez, meg kell adnia a *AccessTier* paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="da48f-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="da48f-135">Ha *a tárterület* értékére vonatkozó értéket ad meg, ne adja meg a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="da48f-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="da48f-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="da48f-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="da48f-137">Az Azure-tárterület biztonsági azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="da48f-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="da48f-138">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="da48f-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="da48f-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="da48f-140">A tartomány GUID-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="da48f-140">Specifies the domain GUID.</span></span> <span data-ttu-id="da48f-141">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="da48f-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="da48f-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="da48f-143">Annak az elsődleges tartománynak a megadása, amelyhez az AD DNS-kiszolgáló mérvadó.</span><span class="sxs-lookup"><span data-stu-id="da48f-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="da48f-144">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="da48f-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="da48f-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="da48f-146">A biztonsági azonosítót (SID) adja meg.</span><span class="sxs-lookup"><span data-stu-id="da48f-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="da48f-147">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="da48f-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="da48f-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="da48f-149">A beolvasott Active Directory-erdőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="da48f-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="da48f-150">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="da48f-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-151">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="da48f-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="da48f-152">A NetBIOS-tartománynevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="da48f-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="da48f-153">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="da48f-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="da48f-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="da48f-155">Engedélyezze a nyilvános hozzáférést a tárterülethez tartozó összes blobhoz vagy tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="da48f-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="da48f-156">A tulajdonság alapértelmezett értelmezése igaz.</span><span class="sxs-lookup"><span data-stu-id="da48f-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="da48f-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da48f-157">-AsJob</span></span>
<span data-ttu-id="da48f-158">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="da48f-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da48f-159">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="da48f-159">-AssignIdentity</span></span>
<span data-ttu-id="da48f-160">Új tárolási fiók identitásának létrehozása és hozzárendelése ehhez a tárterülethez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="da48f-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="da48f-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="da48f-161">-CustomDomainName</span></span>
<span data-ttu-id="da48f-162">A tárolási fiók egyéni tartományának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da48f-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="da48f-163">Az alapértelmezett érték a tárterület.</span><span class="sxs-lookup"><span data-stu-id="da48f-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="da48f-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da48f-164">-DefaultProfile</span></span>
<span data-ttu-id="da48f-165">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da48f-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da48f-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="da48f-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="da48f-167">Engedélyezze az Azure-fájlok Active Directory tartományi szolgáltatás-hitelesítését a tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="da48f-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="da48f-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="da48f-169">Engedélyezze az Azure-fájlok Azure Active Directory tartományi szolgáltatás általi hitelesítését a tárolási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="da48f-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="da48f-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="da48f-171">Azt jelzi, hogy a tárolási fiók engedélyezi-e a hierarchikus névteret.</span><span class="sxs-lookup"><span data-stu-id="da48f-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="da48f-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="da48f-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="da48f-173">Azt jelzi, hogy a tárolási fiók csak HTTPS-forgalmat engedélyez-e.</span><span class="sxs-lookup"><span data-stu-id="da48f-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="da48f-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="da48f-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="da48f-175">Azt jelzi, hogy a tárolási fiók támogatja-e az 5 TiB-nál több kapacitással rendelkező nagyméretű fájlmegosztás használatát.</span><span class="sxs-lookup"><span data-stu-id="da48f-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="da48f-176">Miután a fiók engedélyezve van, a funkció nem tiltható le.</span><span class="sxs-lookup"><span data-stu-id="da48f-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="da48f-177">Jelenleg csak a LRS és a ZRS replikációs típusai támogatottak, ezért nem lehetett beírni a "geo-redundáns fiókok" konverzióját.</span><span class="sxs-lookup"><span data-stu-id="da48f-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="da48f-178">További információ https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="da48f-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="da48f-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="da48f-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="da48f-180">Állítsa be a várólista titkosítási típusát.</span><span class="sxs-lookup"><span data-stu-id="da48f-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="da48f-181">Az alapértelmezett érték a szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="da48f-181">The default value is Service.</span></span>
<span data-ttu-id="da48f-182">-Fiók: a várólista a fiók hatókörű titkosítási kulccsal lesz titkosítva.</span><span class="sxs-lookup"><span data-stu-id="da48f-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="da48f-183">-Szolgáltatás: a várólista mindig Service-Managed kulcsokkal lesz titkosítva.</span><span class="sxs-lookup"><span data-stu-id="da48f-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="da48f-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="da48f-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="da48f-185">Állítsa be a tábla titkosítási típusát.</span><span class="sxs-lookup"><span data-stu-id="da48f-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="da48f-186">Az alapértelmezett érték a szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="da48f-186">The default value is Service.</span></span>
- <span data-ttu-id="da48f-187">Fiók: a tábla a fiókhoz tartozó titkosítási kulccsal lesz titkosítva.</span><span class="sxs-lookup"><span data-stu-id="da48f-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="da48f-188">Szolgáltatás: a táblázat Service-Managed billentyűvel mindig titkosítva lesz.</span><span class="sxs-lookup"><span data-stu-id="da48f-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="da48f-189">-Kind</span><span class="sxs-lookup"><span data-stu-id="da48f-189">-Kind</span></span>
<span data-ttu-id="da48f-190">A parancsmag által létrehozott tárolási fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="da48f-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="da48f-191">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="da48f-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da48f-192">Tárterület.</span><span class="sxs-lookup"><span data-stu-id="da48f-192">Storage.</span></span> <span data-ttu-id="da48f-193">Általános célú tárolási fiók, amely támogatja a Blobs, a táblázatok, a várólisták, a fájlok és a lemezek tárolását.</span><span class="sxs-lookup"><span data-stu-id="da48f-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="da48f-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="da48f-194">StorageV2.</span></span> <span data-ttu-id="da48f-195">Általános célú 2-es verzió (GPv2) tárterülete, melyen a festékfoltok, a táblázatok, a várólisták, a fájlok és a lemezek a speciális funkciók, például az adatrétegek támogatása.</span><span class="sxs-lookup"><span data-stu-id="da48f-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="da48f-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="da48f-196">BlobStorage.</span></span> <span data-ttu-id="da48f-197">BLOB-tároló fiók, amely támogatja a BLOB-tárolót.</span><span class="sxs-lookup"><span data-stu-id="da48f-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="da48f-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="da48f-198">BlockBlobStorage.</span></span> <span data-ttu-id="da48f-199">A blob-tároló fiók zárolása, amely támogatja a csak blokkos Blobok tárolását.</span><span class="sxs-lookup"><span data-stu-id="da48f-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="da48f-200">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="da48f-200">FileStorage.</span></span> <span data-ttu-id="da48f-201">A csak a fájlok tárterületét támogató fájl-tároló fiók.</span><span class="sxs-lookup"><span data-stu-id="da48f-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="da48f-202">Az alapértelmezett érték a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="da48f-202">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-203">-Hely</span><span class="sxs-lookup"><span data-stu-id="da48f-203">-Location</span></span>
<span data-ttu-id="da48f-204">A létrehozandó tárterület-fiók helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da48f-204">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="da48f-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="da48f-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="da48f-206">A tárolási kérelmeken engedélyezni kívánt minimális TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="da48f-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="da48f-207">Az alapértelmezett értelmezés a TLS 1,0 tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="da48f-207">The default interpretation is TLS 1.0 for this property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-208">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da48f-208">-Name</span></span>
<span data-ttu-id="da48f-209">A létrehozandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da48f-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="da48f-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="da48f-210">-NetworkRuleSet</span></span>
<span data-ttu-id="da48f-211">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé tevő, valamint a meghatározott szabályoknak nem megfelelő kérelmek kezelésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="da48f-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="da48f-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="da48f-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="da48f-213">A szolgáltatás másodlagos titkosítási réteget alkalmaz a REST-alapú adatok platformon kezelt kulcsaival.</span><span class="sxs-lookup"><span data-stu-id="da48f-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="da48f-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da48f-214">-ResourceGroupName</span></span>
<span data-ttu-id="da48f-215">Annak az erőforrás-csoportnak a nevét adja meg, amelybe a tárolási fiókot hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="da48f-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="da48f-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="da48f-216">-SkuName</span></span>
<span data-ttu-id="da48f-217">Megadja annak a tárolási fióknak az SKU-nevét, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="da48f-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="da48f-218">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="da48f-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da48f-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="da48f-219">Standard_LRS.</span></span> <span data-ttu-id="da48f-220">Helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="da48f-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="da48f-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="da48f-221">Standard_ZRS.</span></span> <span data-ttu-id="da48f-222">Zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="da48f-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="da48f-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="da48f-223">Standard_GRS.</span></span> <span data-ttu-id="da48f-224">Geo-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="da48f-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="da48f-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="da48f-225">Standard_RAGRS.</span></span> <span data-ttu-id="da48f-226">Olvassa el az Access geo-redundáns tárterülete című témakört.</span><span class="sxs-lookup"><span data-stu-id="da48f-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="da48f-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="da48f-227">Premium_LRS.</span></span> <span data-ttu-id="da48f-228">Prémium lokálisan redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="da48f-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="da48f-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="da48f-229">Premium_ZRS.</span></span> <span data-ttu-id="da48f-230">Prémium zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="da48f-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="da48f-231">Standard_GZRS-geo-redundáns zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="da48f-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="da48f-232">Standard_RAGZRS – az Access geo-redundáns zónája – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="da48f-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="da48f-233">-Címke</span><span class="sxs-lookup"><span data-stu-id="da48f-233">-Tag</span></span>
<span data-ttu-id="da48f-234">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="da48f-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="da48f-235">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="da48f-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="da48f-236">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="da48f-236">-UseSubDomain</span></span>
<span data-ttu-id="da48f-237">Azt jelzi, hogy engedélyezi-e a közvetlen CName érvényesítést.</span><span class="sxs-lookup"><span data-stu-id="da48f-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="da48f-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da48f-238">CommonParameters</span></span>
<span data-ttu-id="da48f-239">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da48f-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da48f-240">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da48f-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da48f-241">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da48f-241">INPUTS</span></span>

### <span data-ttu-id="da48f-242">System. String</span><span class="sxs-lookup"><span data-stu-id="da48f-242">System.String</span></span>

## <span data-ttu-id="da48f-243">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da48f-243">OUTPUTS</span></span>

### <span data-ttu-id="da48f-244">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="da48f-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="da48f-245">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da48f-245">NOTES</span></span>

## <span data-ttu-id="da48f-246">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da48f-246">RELATED LINKS</span></span>

[<span data-ttu-id="da48f-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="da48f-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="da48f-248">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="da48f-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="da48f-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="da48f-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)