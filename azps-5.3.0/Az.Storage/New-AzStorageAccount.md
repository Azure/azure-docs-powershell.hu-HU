---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479441"
---
# <span data-ttu-id="85ce1-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85ce1-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="85ce1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="85ce1-103">Tárfiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="85ce1-103">Creates a Storage account.</span></span>

## <span data-ttu-id="85ce1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="85ce1-104">SYNTAX</span></span>

### <span data-ttu-id="85ce1-105">AzureActiveDirectoryDomainServicesForFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="85ce1-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85ce1-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="85ce1-106">ActiveDirectoryDomainServicesForFile</span></span>
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

## <span data-ttu-id="85ce1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="85ce1-107">DESCRIPTION</span></span>
<span data-ttu-id="85ce1-108">A **New-AzStorageAccount** parancsmag létrehoz egy Azure Storage-fiókot.</span><span class="sxs-lookup"><span data-stu-id="85ce1-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="85ce1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="85ce1-109">EXAMPLES</span></span>

### <span data-ttu-id="85ce1-110">1. példa: Tárfiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="85ce1-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="85ce1-111">Ez a parancs tárfiókot hoz létre a MyResourceGroup nevű erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="85ce1-112">2. példa: Blob-tárfiók létrehozása BlobStorage típusú és gyors AccessTier-fiókkal</span><span class="sxs-lookup"><span data-stu-id="85ce1-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="85ce1-113">Ez a parancs létrehoz egy Blob Storage-fiókot, amely a BlobStorage kind és a hot AccessTier segítségével</span><span class="sxs-lookup"><span data-stu-id="85ce1-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="85ce1-114">3. példa: Tárfiók létrehozása a Kind StorageV2 segítségével, valamint identitás létrehozása és hozzárendelése az Azure KeyVaulthoz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="85ce1-115">Ez a parancs létrehoz egy Tárfiókot a Kind StorageV2 segítségével.</span><span class="sxs-lookup"><span data-stu-id="85ce1-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="85ce1-116">Emellett létrehoz és hozzárendel egy identitást, amely a fiókkulcsok Azure KeyVaulton keresztüli kezelésére használható.</span><span class="sxs-lookup"><span data-stu-id="85ce1-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="85ce1-117">4. példa: Tárfiók létrehozása a NetworkRuleSet segítségével a JSON-ból</span><span class="sxs-lookup"><span data-stu-id="85ce1-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="85ce1-118">Ezzel a paranccsal olyan tárfiókot hoz létre, amely a JSON-ból NetworkRuleSet tulajdonságot hoz létre</span><span class="sxs-lookup"><span data-stu-id="85ce1-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="85ce1-119">5. példa: Tárfiók létrehozása engedélyezett Hierarchikus névtér funkcióval.</span><span class="sxs-lookup"><span data-stu-id="85ce1-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="85ce1-120">Ez a parancs egy tárfiókot hoz létre, és a Hierarchikus névtér engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="85ce1-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="85ce1-121">6. példa: Hozzon létre egy tárfiókot az Azure Files AAD DS-hitelesítéssel, és engedélyezze a nagy fájlmegosztást.</span><span class="sxs-lookup"><span data-stu-id="85ce1-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="85ce1-122">Ez a parancs létrehoz egy Tárfiókot az Azure Files AAD DS Authentication segítségével, és engedélyezi a nagy fájlmegosztást.</span><span class="sxs-lookup"><span data-stu-id="85ce1-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="85ce1-123">7. példa: Tárfiók létrehozása a Files Active Directory tartományi szolgáltatás hitelesítésének engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="85ce1-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="85ce1-124">Ez a parancs egy tárolófiókot hoz létre, amely tartalmazza az Active Directory tartományi szolgáltatások hitelesítését.</span><span class="sxs-lookup"><span data-stu-id="85ce1-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="85ce1-125">8. példa: Tárfiók létrehozása a Várólistával és a Táblaszolgáltatással fiókfedő titkosítási kulcsot, valamint infrastruktúra-titkosítás megkövetelése.</span><span class="sxs-lookup"><span data-stu-id="85ce1-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="85ce1-126">Ez a parancs létrehoz egy tárfiókot a Várólistával és a Táblaszolgáltatással, és fiókfüggvényes titkosítási kulcsot használ, és infrastruktúra-titkosítást igényel, így a várólistán és a táblázatban a Blob és a File szolgáltatás ugyanazt a titkosítási kulcsot fogja használni, és a szolgáltatás egy másodlagos titkosítási réteget alkalmaz platform felügyelt kulcsokkal az adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="85ce1-127">Ezután szerezze be a Tárfiók tulajdonságait, és tekintse meg a Várólistás és a Táblaszolgáltatás titkosítási kulcstípusát, valamint a RequireInfrastructureEncryption értéket.</span><span class="sxs-lookup"><span data-stu-id="85ce1-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="85ce1-128">9. példa: Fiók MinimumTlsVersion és AllowBlobPublicAccess létrehozása</span><span class="sxs-lookup"><span data-stu-id="85ce1-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="85ce1-129">A parancs létrehoz egy fiókot a MinimumTlsVersion és az AllowBlobPublicAccess segítségével, majd a létrehozott fiók 2 tulajdonságát mutatja.</span><span class="sxs-lookup"><span data-stu-id="85ce1-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="85ce1-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85ce1-130">PARAMETERS</span></span>

### <span data-ttu-id="85ce1-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="85ce1-131">-AccessTier</span></span>
<span data-ttu-id="85ce1-132">A parancsmag által létrehozott tárfiók hozzáférési rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85ce1-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="85ce1-133">A paraméter elfogadható értékei a következőek: Hot és Cool.</span><span class="sxs-lookup"><span data-stu-id="85ce1-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="85ce1-134">Ha a Kind paraméterhez blobstorage értéket ad meg, meg kell adnia egy értéket az *AccessTier paraméterhez.* </span><span class="sxs-lookup"><span data-stu-id="85ce1-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="85ce1-135">Ha a Kind paraméterhez  tárhelyértéket ad meg, ne adja meg az *AccessTier paramétert.*</span><span class="sxs-lookup"><span data-stu-id="85ce1-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="85ce1-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="85ce1-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="85ce1-137">Az Azure Storage biztonsági azonosítóját (SID) adja meg.</span><span class="sxs-lookup"><span data-stu-id="85ce1-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="85ce1-138">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="85ce1-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="85ce1-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="85ce1-140">A tartomány GUID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="85ce1-140">Specifies the domain GUID.</span></span> <span data-ttu-id="85ce1-141">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="85ce1-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="85ce1-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="85ce1-143">Azt az elsődleges tartományt adja meg, amely esetén az AD DNS-kiszolgáló mérvadó.</span><span class="sxs-lookup"><span data-stu-id="85ce1-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="85ce1-144">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="85ce1-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="85ce1-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="85ce1-146">Megadja a biztonsági azonosítót (SID).</span><span class="sxs-lookup"><span data-stu-id="85ce1-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="85ce1-147">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="85ce1-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="85ce1-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="85ce1-149">A lekért Active Directory-erdőt határozza meg.</span><span class="sxs-lookup"><span data-stu-id="85ce1-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="85ce1-150">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="85ce1-151">-ActiveDirectoryNetNamesDomainName</span><span class="sxs-lookup"><span data-stu-id="85ce1-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="85ce1-152">A Net ROSTS tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85ce1-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="85ce1-153">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="85ce1-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="85ce1-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="85ce1-155">Nyilvános hozzáférés engedélyezése a tárfiók összes blobját vagy tárolóját.</span><span class="sxs-lookup"><span data-stu-id="85ce1-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="85ce1-156">A tulajdonság alapértelmezett értelmezése igaz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="85ce1-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85ce1-157">-AsJob</span></span>
<span data-ttu-id="85ce1-158">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="85ce1-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85ce1-159">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="85ce1-159">-AssignIdentity</span></span>
<span data-ttu-id="85ce1-160">Hozzon létre és rendeljen hozzá egy új tárfiók-identitást ehhez a tárfiókhoz, hogy olyan kulcskezelési szolgáltatásokkal használva használja őket, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="85ce1-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="85ce1-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="85ce1-161">-CustomDomainName</span></span>
<span data-ttu-id="85ce1-162">A Tárfiók egyéni tartományának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85ce1-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="85ce1-163">Az alapértelmezett érték a Tárterület.</span><span class="sxs-lookup"><span data-stu-id="85ce1-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="85ce1-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ce1-164">-DefaultProfile</span></span>
<span data-ttu-id="85ce1-165">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85ce1-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85ce1-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="85ce1-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="85ce1-167">Engedélyezze az Azure Files Active Directory tartományi szolgáltatás hitelesítését a tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="85ce1-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="85ce1-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="85ce1-169">Engedélyezze az Azure Files Azure Active Directory tartományi szolgáltatás hitelesítését a tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="85ce1-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="85ce1-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="85ce1-171">Azt jelzi, hogy a Tárfiók engedélyezi-e a hierarchikus névteret.</span><span class="sxs-lookup"><span data-stu-id="85ce1-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="85ce1-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="85ce1-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="85ce1-173">Azt jelzi, hogy a Tárfiók csak https-forgalmat tesz-e lehetővé.</span><span class="sxs-lookup"><span data-stu-id="85ce1-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="85ce1-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="85ce1-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="85ce1-175">Azt jelzi, hogy a tárfiók támogatja-e az 5 TiB-kapacitásnál nagyobb fájlmegosztásokat.</span><span class="sxs-lookup"><span data-stu-id="85ce1-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="85ce1-176">A fiók engedélyezése után a funkció nem tiltható le.</span><span class="sxs-lookup"><span data-stu-id="85ce1-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="85ce1-177">Jelenleg csak az LRS és a ZRS replikációs típusai támogatottak, ezért a fiókok georedundáns fiókokra konvertálása nem lenne lehetséges.</span><span class="sxs-lookup"><span data-stu-id="85ce1-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="85ce1-178">További információ: https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="85ce1-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="85ce1-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="85ce1-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="85ce1-180">Állítsa be a várólistán lévő titkosítási kulcstípust.</span><span class="sxs-lookup"><span data-stu-id="85ce1-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="85ce1-181">Az alapértelmezett érték a Szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="85ce1-181">The default value is Service.</span></span>
<span data-ttu-id="85ce1-182">-Fiók: A várólistát fiókható titkosítási kulccsal titkosítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="85ce1-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="85ce1-183">-Szolgáltatás: A várólistát a rendszer mindig titkos kulcsokkal Service-Managed titkosítja.</span><span class="sxs-lookup"><span data-stu-id="85ce1-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="85ce1-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="85ce1-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="85ce1-185">Állítsa be a táblázat titkosítási kulcstípusát.</span><span class="sxs-lookup"><span data-stu-id="85ce1-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="85ce1-186">Az alapértelmezett érték a Szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="85ce1-186">The default value is Service.</span></span>
- <span data-ttu-id="85ce1-187">Fiók: A tábla fiókható titkosítási kulccsal lesz titkosítva.</span><span class="sxs-lookup"><span data-stu-id="85ce1-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="85ce1-188">Szolgáltatás: A tábla mindig titkosítva lesz a Service-Managed kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="85ce1-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="85ce1-189">-Kind</span><span class="sxs-lookup"><span data-stu-id="85ce1-189">-Kind</span></span>
<span data-ttu-id="85ce1-190">Meghatározza, hogy a parancsmag milyen típusú tárfiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="85ce1-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="85ce1-191">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="85ce1-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="85ce1-192">Tárterület.</span><span class="sxs-lookup"><span data-stu-id="85ce1-192">Storage.</span></span> <span data-ttu-id="85ce1-193">Általános célú tárfiók, amely támogatja a blobok, táblák, várólisták, fájlok és lemezek tárolását.</span><span class="sxs-lookup"><span data-stu-id="85ce1-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="85ce1-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="85ce1-194">StorageV2.</span></span> <span data-ttu-id="85ce1-195">Általános célú 2-es verzió (GPv2) tárfiók, amely támogatja a blobokat, a táblákat, a várólistákat, a fájlokat és a lemezeket speciális funkciókkal, például adatrétegezéssel.</span><span class="sxs-lookup"><span data-stu-id="85ce1-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="85ce1-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="85ce1-196">BlobStorage.</span></span> <span data-ttu-id="85ce1-197">Blob storage account which supports storage of Blobs only.</span><span class="sxs-lookup"><span data-stu-id="85ce1-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="85ce1-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="85ce1-198">BlockBlobStorage.</span></span> <span data-ttu-id="85ce1-199">Letilthatja a Blob Storage-fiókot, amely csak a blokk blobok tárolását támogatja.</span><span class="sxs-lookup"><span data-stu-id="85ce1-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="85ce1-200">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="85ce1-200">FileStorage.</span></span> <span data-ttu-id="85ce1-201">Fájltárfiók, amely csak a fájlok tárolását támogatja.</span><span class="sxs-lookup"><span data-stu-id="85ce1-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="85ce1-202">Az alapértelmezett érték a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="85ce1-202">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="85ce1-203">-Location</span><span class="sxs-lookup"><span data-stu-id="85ce1-203">-Location</span></span>
<span data-ttu-id="85ce1-204">Megadja a létrehozni szükséges tárfiók helyét.</span><span class="sxs-lookup"><span data-stu-id="85ce1-204">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="85ce1-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="85ce1-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="85ce1-206">A tárterület-kérelmek esetén megengedett minimális TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="85ce1-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="85ce1-207">A tulajdonság alapértelmezett értelmezése a TLS 1.0.</span><span class="sxs-lookup"><span data-stu-id="85ce1-207">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="85ce1-208">-Name</span><span class="sxs-lookup"><span data-stu-id="85ce1-208">-Name</span></span>
<span data-ttu-id="85ce1-209">A létrehozni szükséges tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85ce1-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="85ce1-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="85ce1-210">-NetworkRuleSet</span></span>
<span data-ttu-id="85ce1-211">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazának meghatározására, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé térő szolgáltatások értékeinek beállítására, valamint a megadott szabályoktól különböző kérések kezelésére használható.</span><span class="sxs-lookup"><span data-stu-id="85ce1-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="85ce1-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="85ce1-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="85ce1-213">A szolgáltatás egy másodlagos titkosítási réteget alkalmaz platform felügyelt kulcsokkal a nyugta adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="85ce1-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="85ce1-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85ce1-214">-ResourceGroupName</span></span>
<span data-ttu-id="85ce1-215">Annak az erőforráscsoportnak a neve, amelyhez hozzá kell adni a Tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="85ce1-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="85ce1-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="85ce1-216">-SkuName</span></span>
<span data-ttu-id="85ce1-217">A parancsmag által létrehozott tárfiók termékváltozatnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85ce1-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="85ce1-218">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="85ce1-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="85ce1-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="85ce1-219">Standard_LRS.</span></span> <span data-ttu-id="85ce1-220">Helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="85ce1-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="85ce1-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="85ce1-221">Standard_ZRS.</span></span> <span data-ttu-id="85ce1-222">Zone-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="85ce1-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="85ce1-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="85ce1-223">Standard_GRS.</span></span> <span data-ttu-id="85ce1-224">Georedundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="85ce1-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="85ce1-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="85ce1-225">Standard_RAGRS.</span></span> <span data-ttu-id="85ce1-226">A hozzáférés georedundáns tárterületének olvasása.</span><span class="sxs-lookup"><span data-stu-id="85ce1-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="85ce1-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="85ce1-227">Premium_LRS.</span></span> <span data-ttu-id="85ce1-228">Prémium helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="85ce1-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="85ce1-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="85ce1-229">Premium_ZRS.</span></span> <span data-ttu-id="85ce1-230">Prémium zóna redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="85ce1-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="85ce1-231">Standard_GZRS – Georedundáns zónaredundáns tárolás.</span><span class="sxs-lookup"><span data-stu-id="85ce1-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="85ce1-232">Standard_RAGZRS – Olvassa el a georedundáns zóna-redundáns tárhelyet.</span><span class="sxs-lookup"><span data-stu-id="85ce1-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="85ce1-233">-Tag</span><span class="sxs-lookup"><span data-stu-id="85ce1-233">-Tag</span></span>
<span data-ttu-id="85ce1-234">Kulcsérték-párok a kiszolgálón címkékként beállított kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="85ce1-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="85ce1-235">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="85ce1-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="85ce1-236">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="85ce1-236">-UseSubDomain</span></span>
<span data-ttu-id="85ce1-237">Azt jelzi, hogy engedélyezi-e a CName közvetett érvényesítését.</span><span class="sxs-lookup"><span data-stu-id="85ce1-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="85ce1-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ce1-238">CommonParameters</span></span>
<span data-ttu-id="85ce1-239">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85ce1-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ce1-240">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85ce1-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ce1-241">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85ce1-241">INPUTS</span></span>

### <span data-ttu-id="85ce1-242">System.String</span><span class="sxs-lookup"><span data-stu-id="85ce1-242">System.String</span></span>

## <span data-ttu-id="85ce1-243">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85ce1-243">OUTPUTS</span></span>

### <span data-ttu-id="85ce1-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85ce1-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="85ce1-245">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="85ce1-245">NOTES</span></span>

## <span data-ttu-id="85ce1-246">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85ce1-246">RELATED LINKS</span></span>

[<span data-ttu-id="85ce1-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85ce1-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="85ce1-248">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85ce1-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="85ce1-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85ce1-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
