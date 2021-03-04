---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0a5ccfaec396f4dc79c877da38112a5bfa575e09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939849"
---
# <span data-ttu-id="19f63-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19f63-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="19f63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19f63-102">SYNOPSIS</span></span>
<span data-ttu-id="19f63-103">Tárfiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="19f63-103">Creates a Storage account.</span></span>

## <span data-ttu-id="19f63-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19f63-104">SYNTAX</span></span>

### <span data-ttu-id="19f63-105">AzureActiveDirectoryDomainServicesForFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19f63-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### <span data-ttu-id="19f63-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="19f63-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## <span data-ttu-id="19f63-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19f63-107">DESCRIPTION</span></span>
<span data-ttu-id="19f63-108">A **New-AzStorageAccount** parancsmag létrehoz egy Azure Storage-fiókot.</span><span class="sxs-lookup"><span data-stu-id="19f63-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="19f63-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19f63-109">EXAMPLES</span></span>

### <span data-ttu-id="19f63-110">1. példa: Tárfiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="19f63-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="19f63-111">Ez a parancs tárfiókot hoz létre a MyResourceGroup nevű erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="19f63-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="19f63-112">2. példa: Blob-tárfiók létrehozása BlobStorage típusú és gyors AccessTier-fiókkal</span><span class="sxs-lookup"><span data-stu-id="19f63-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="19f63-113">Ezzel a paranccsal olyan Blob Storage-fiókot hoz létre, amely blobstorage típusú és gyors AccessTier típusú</span><span class="sxs-lookup"><span data-stu-id="19f63-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="19f63-114">3. példa: Tárfiók létrehozása a Kind StorageV2 segítségével, valamint identitás létrehozása és hozzárendelése az Azure KeyVaulthoz.</span><span class="sxs-lookup"><span data-stu-id="19f63-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="19f63-115">Ez a parancs létrehoz egy Tárfiókot a Kind StorageV2 segítségével.</span><span class="sxs-lookup"><span data-stu-id="19f63-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="19f63-116">Emellett létrehoz és hozzárendel egy identitást, amely a fiókkulcsok Azure KeyVaulton keresztüli kezelésére használható.</span><span class="sxs-lookup"><span data-stu-id="19f63-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="19f63-117">4. példa: Tárfiók létrehozása a NetworkRuleSet segítségével a JSON-ból</span><span class="sxs-lookup"><span data-stu-id="19f63-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="19f63-118">Ez a parancs egy Olyan tárfiókot hoz létre, amely a JSON-ból NetworkRuleSet tulajdonságot hoz létre</span><span class="sxs-lookup"><span data-stu-id="19f63-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="19f63-119">5. példa: Tárfiók létrehozása engedélyezett Hierarchikus névtér funkcióval.</span><span class="sxs-lookup"><span data-stu-id="19f63-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="19f63-120">Ez a parancs egy tárfiókot hoz létre, és a Hierarchikus névtér engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="19f63-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="19f63-121">6. példa: Hozzon létre egy tárfiókot az Azure Files AAD DS-hitelesítéssel, és engedélyezze a nagy fájlmegosztást.</span><span class="sxs-lookup"><span data-stu-id="19f63-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="19f63-122">Ez a parancs létrehoz egy Tárfiókot az Azure Files AAD DS Authentication segítségével, és engedélyezi a nagy fájlmegosztást.</span><span class="sxs-lookup"><span data-stu-id="19f63-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="19f63-123">7. példa: Tárfiók létrehozása a Files Active Directory tartományi szolgáltatás hitelesítésének engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="19f63-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="19f63-124">Ez a parancs egy tárolófiókot hoz létre, amely tartalmazza az Active Directory tartományi szolgáltatások hitelesítését.</span><span class="sxs-lookup"><span data-stu-id="19f63-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="19f63-125">8. példa: Tárfiók létrehozása a várólistával és a táblaszolgáltatással fiókfedő titkosítási kulcsot, valamint infrastruktúra-titkosítás megkövetelése.</span><span class="sxs-lookup"><span data-stu-id="19f63-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="19f63-126">Ez a parancs létrehoz egy tárfiókot a Várólistával és a Táblaszolgáltatással, és fiókfüggvényes titkosítási kulcsot használ, és infrastruktúra-titkosítást igényel, így a várólistán és a táblázatban ugyanaz a titkosítási kulcs fog használni a Blob és a Fájl szolgáltatással, és a szolgáltatás egy másodlagos titkosítási réteget alkalmaz platform felügyelt kulcsokkal az adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="19f63-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="19f63-127">Ezután szerezze be a Tárfiók tulajdonságait, és tekintse meg a Várólistás és a Táblaszolgáltatás titkosítási kulcstípusát, valamint a RequireInfrastructureEncryption értéket.</span><span class="sxs-lookup"><span data-stu-id="19f63-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="19f63-128">9. példa: Fiók minimumTlsVersion és AllowBlobPublicAccess létrehozása és a SharedKey Access letiltása</span><span class="sxs-lookup"><span data-stu-id="19f63-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess, and disable SharedKey Access</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
False
```

<span data-ttu-id="19f63-129">A parancs a MinimumTlsVersion, az AllowBlobPublicAccess és a SharedKey hozzáférés letiltása a fiókhoz, majd a létrehozott fiók 3 tulajdonságának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="19f63-129">The command create account with MinimumTlsVersion, AllowBlobPublicAccess, and disable SharedKey access to the account, and then show the the 3 properties of the created account</span></span> 

### <span data-ttu-id="19f63-130">10. példa: Tárfiók létrehozása a RoutingPreference beállítással</span><span class="sxs-lookup"><span data-stu-id="19f63-130">Example 10: Create a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="19f63-131">Ez a parancs létrehoz egy Tárfiókot a RoutingPreference beállítással: a PublishMicrosoftEndpoint és a PublishInternetEndpoint mint true, a RoutingChoice pedig MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="19f63-131">This command creates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint and PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="19f63-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19f63-132">PARAMETERS</span></span>

### <span data-ttu-id="19f63-133">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="19f63-133">-AccessTier</span></span>
<span data-ttu-id="19f63-134">A parancsmag által létrehozott tárfiók hozzáférési rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19f63-134">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="19f63-135">A paraméter elfogadható értékei a következőek: Hot és Cool.</span><span class="sxs-lookup"><span data-stu-id="19f63-135">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="19f63-136">Ha a Kind paraméterhez blobstorage értéket ad meg, meg kell adnia az  *AccessTier paraméter értékét.*</span><span class="sxs-lookup"><span data-stu-id="19f63-136">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="19f63-137">Ha a Kind paraméterhez  tárterületértéket ad meg, ne adja meg az *AccessTier paramétert.*</span><span class="sxs-lookup"><span data-stu-id="19f63-137">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="19f63-138">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="19f63-138">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="19f63-139">Az Azure Storage biztonsági azonosítóját (SID) adja meg.</span><span class="sxs-lookup"><span data-stu-id="19f63-139">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="19f63-140">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="19f63-140">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="19f63-141">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="19f63-141">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="19f63-142">A tartomány GUID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19f63-142">Specifies the domain GUID.</span></span> <span data-ttu-id="19f63-143">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="19f63-143">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="19f63-144">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="19f63-144">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="19f63-145">Azt az elsődleges tartományt adja meg, amely esetén az AD DNS-kiszolgáló mérvadó.</span><span class="sxs-lookup"><span data-stu-id="19f63-145">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="19f63-146">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="19f63-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="19f63-147">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="19f63-147">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="19f63-148">Megadja a biztonsági azonosítót (SID).</span><span class="sxs-lookup"><span data-stu-id="19f63-148">Specifies the security identifier (SID).</span></span> <span data-ttu-id="19f63-149">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="19f63-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="19f63-150">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="19f63-150">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="19f63-151">A lekért Active Directory-erdőt határozza meg.</span><span class="sxs-lookup"><span data-stu-id="19f63-151">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="19f63-152">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="19f63-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="19f63-153">-ActiveDirectoryNetNamesDomainName</span><span class="sxs-lookup"><span data-stu-id="19f63-153">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="19f63-154">A Net ROSTAS tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19f63-154">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="19f63-155">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="19f63-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="19f63-156">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="19f63-156">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="19f63-157">Nyilvános hozzáférés engedélyezése a tárfiók összes blobját vagy tárolóját.</span><span class="sxs-lookup"><span data-stu-id="19f63-157">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="19f63-158">A tulajdonság alapértelmezett értelmezése igaz.</span><span class="sxs-lookup"><span data-stu-id="19f63-158">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="19f63-159">-AllowSharedKeyAccess</span><span class="sxs-lookup"><span data-stu-id="19f63-159">-AllowSharedKeyAccess</span></span>
<span data-ttu-id="19f63-160">Azt jelzi, hogy a tárfiók engedélyezi-e a fiók hozzáférési kulcsával való engedély kérését a Megosztott kulcson keresztül.</span><span class="sxs-lookup"><span data-stu-id="19f63-160">Indicates whether the storage account permits requests to be authorized with the account access key via Shared Key.</span></span> <span data-ttu-id="19f63-161">Ha hamis, akkor minden kérést engedélyezni kell az Azure Active Directory (Azure AD) használatával, beleértve a megosztott hozzáférés-aláírásokat is.</span><span class="sxs-lookup"><span data-stu-id="19f63-161">If false, then all requests, including shared access signatures, must be authorized with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="19f63-162">Az alapértelmezett érték null, amely egyenértékű az igaz értékkel.</span><span class="sxs-lookup"><span data-stu-id="19f63-162">The default value is null, which is equivalent to true.</span></span>

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

### <span data-ttu-id="19f63-163">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19f63-163">-AsJob</span></span>
<span data-ttu-id="19f63-164">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="19f63-164">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19f63-165">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="19f63-165">-AssignIdentity</span></span>
<span data-ttu-id="19f63-166">Hozzon létre és rendeljen hozzá egy új tárfiók-identitást ehhez a tárfiókhoz, hogy olyan kulcskezelési szolgáltatásokkal használva használja őket, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="19f63-166">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="19f63-167">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="19f63-167">-CustomDomainName</span></span>
<span data-ttu-id="19f63-168">A Tárfiók egyéni tartományának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19f63-168">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="19f63-169">Az alapértelmezett érték a Tárterület.</span><span class="sxs-lookup"><span data-stu-id="19f63-169">The default value is Storage.</span></span>

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

### <span data-ttu-id="19f63-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19f63-170">-DefaultProfile</span></span>
<span data-ttu-id="19f63-171">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19f63-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19f63-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="19f63-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="19f63-173">Engedélyezze az Azure Files Active Directory tartományi szolgáltatás hitelesítését a tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="19f63-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="19f63-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="19f63-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="19f63-175">Engedélyezze az Azure Files Azure Active Directory tartományi szolgáltatás hitelesítését a tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="19f63-175">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="19f63-176">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="19f63-176">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="19f63-177">Azt jelzi, hogy a Tárfiók engedélyezi-e a hierarchikus névteret.</span><span class="sxs-lookup"><span data-stu-id="19f63-177">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="19f63-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="19f63-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="19f63-179">Azt jelzi, hogy a Tárfiók csak https-forgalmat tesz-e lehetővé.</span><span class="sxs-lookup"><span data-stu-id="19f63-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="19f63-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="19f63-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="19f63-181">Azt jelzi, hogy a tárfiók támogatja-e az 5 TiB-kapacitásnál nagyobb fájlmegosztásokat.</span><span class="sxs-lookup"><span data-stu-id="19f63-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="19f63-182">A fiók engedélyezése után a funkció nem tiltható le.</span><span class="sxs-lookup"><span data-stu-id="19f63-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="19f63-183">Jelenleg csak az LRS és a ZRS replikációs típusai támogatottak, ezért a fiókok georedundáns fiókokra konvertálása nem lenne lehetséges.</span><span class="sxs-lookup"><span data-stu-id="19f63-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="19f63-184">További információ: https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="19f63-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="19f63-185">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="19f63-185">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="19f63-186">Állítsa be a várólistán lévő titkosítási kulcstípust.</span><span class="sxs-lookup"><span data-stu-id="19f63-186">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="19f63-187">Az alapértelmezett érték a Szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="19f63-187">The default value is Service.</span></span>
<span data-ttu-id="19f63-188">-Fiók: A várólistát fiókható titkosítási kulccsal titkosítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="19f63-188">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="19f63-189">-Szolgáltatás: A várólistát a rendszer mindig titkos kulcsokkal Service-Managed titkosítja.</span><span class="sxs-lookup"><span data-stu-id="19f63-189">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="19f63-190">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="19f63-190">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="19f63-191">Állítsa be a táblázat titkosítási kulcstípusát.</span><span class="sxs-lookup"><span data-stu-id="19f63-191">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="19f63-192">Az alapértelmezett érték a Szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="19f63-192">The default value is Service.</span></span>
- <span data-ttu-id="19f63-193">Fiók: A tábla fiókható titkosítási kulccsal lesz titkosítva.</span><span class="sxs-lookup"><span data-stu-id="19f63-193">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="19f63-194">Szolgáltatás: A tábla mindig titkosítva lesz a Service-Managed kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="19f63-194">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="19f63-195">-Kind</span><span class="sxs-lookup"><span data-stu-id="19f63-195">-Kind</span></span>
<span data-ttu-id="19f63-196">Meghatározza, hogy a parancsmag milyen típusú tárfiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="19f63-196">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="19f63-197">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="19f63-197">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19f63-198">Tárterület.</span><span class="sxs-lookup"><span data-stu-id="19f63-198">Storage.</span></span> <span data-ttu-id="19f63-199">Általános célú tárfiók, amely támogatja a blobok, táblák, várólisták, fájlok és lemezek tárolását.</span><span class="sxs-lookup"><span data-stu-id="19f63-199">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="19f63-200">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="19f63-200">StorageV2.</span></span> <span data-ttu-id="19f63-201">Általános célú 2-es verzió (GPv2) tárfiók, amely támogatja a blobokat, a táblákat, a várólistákat, a fájlokat és a lemezeket speciális funkciókkal, például adatrétegezéssel.</span><span class="sxs-lookup"><span data-stu-id="19f63-201">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="19f63-202">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="19f63-202">BlobStorage.</span></span> <span data-ttu-id="19f63-203">Blob storage account which supports storage of Blobs only.</span><span class="sxs-lookup"><span data-stu-id="19f63-203">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="19f63-204">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="19f63-204">BlockBlobStorage.</span></span> <span data-ttu-id="19f63-205">Letilthatja a Blob Storage-fiókot, amely csak a blokk blobok tárolását támogatja.</span><span class="sxs-lookup"><span data-stu-id="19f63-205">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="19f63-206">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="19f63-206">FileStorage.</span></span> <span data-ttu-id="19f63-207">Fájltárfiók, amely csak a fájlok tárolását támogatja.</span><span class="sxs-lookup"><span data-stu-id="19f63-207">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="19f63-208">Az alapértelmezett érték a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="19f63-208">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="19f63-209">-Location</span><span class="sxs-lookup"><span data-stu-id="19f63-209">-Location</span></span>
<span data-ttu-id="19f63-210">Megadja a létrehozni szükséges tárfiók helyét.</span><span class="sxs-lookup"><span data-stu-id="19f63-210">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="19f63-211">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="19f63-211">-MinimumTlsVersion</span></span>
<span data-ttu-id="19f63-212">A tárterület-kérelmek esetén megengedett minimális TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="19f63-212">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="19f63-213">A tulajdonság alapértelmezett értelmezése a TLS 1.0.</span><span class="sxs-lookup"><span data-stu-id="19f63-213">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="19f63-214">-Name</span><span class="sxs-lookup"><span data-stu-id="19f63-214">-Name</span></span>
<span data-ttu-id="19f63-215">A létrehozni szükséges tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19f63-215">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="19f63-216">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="19f63-216">-NetworkRuleSet</span></span>
<span data-ttu-id="19f63-217">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazának meghatározására, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé térő szolgáltatások értékeinek beállítására, valamint a megadott szabályoktól különböző kérések kezelésére használható.</span><span class="sxs-lookup"><span data-stu-id="19f63-217">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="19f63-218">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="19f63-218">-PublishInternetEndpoint</span></span>
<span data-ttu-id="19f63-219">Azt jelzi, hogy közzé kell-e tenni az internetes útválasztási tárolási végpontokat</span><span class="sxs-lookup"><span data-stu-id="19f63-219">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="19f63-220">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="19f63-220">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="19f63-221">Azt jelzi, hogy közzé kell-e tenni a Microsoft útválasztási tár végpontját</span><span class="sxs-lookup"><span data-stu-id="19f63-221">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="19f63-222">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="19f63-222">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="19f63-223">A szolgáltatás egy másodlagos titkosítási réteget alkalmaz platform felügyelt kulcsokkal a nyugta adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="19f63-223">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="19f63-224">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19f63-224">-ResourceGroupName</span></span>
<span data-ttu-id="19f63-225">Annak az erőforráscsoportnak a nevét adja meg, amelyhez hozzá kell adni a Tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="19f63-225">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="19f63-226">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="19f63-226">-RoutingChoice</span></span>
<span data-ttu-id="19f63-227">Az Útválasztási választási lehetőség a felhasználó által választott hálózati útválasztási típust határozza meg.</span><span class="sxs-lookup"><span data-stu-id="19f63-227">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="19f63-228">Lehetséges értékek: "MicrosoftRouting", "InternetRouting"</span><span class="sxs-lookup"><span data-stu-id="19f63-228">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f63-229">-SkuName</span><span class="sxs-lookup"><span data-stu-id="19f63-229">-SkuName</span></span>
<span data-ttu-id="19f63-230">A parancsmag által létrehozott tárfiók termékváltozatnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19f63-230">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="19f63-231">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="19f63-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19f63-232">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="19f63-232">Standard_LRS.</span></span> <span data-ttu-id="19f63-233">Helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="19f63-233">Locally-redundant storage.</span></span>
- <span data-ttu-id="19f63-234">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="19f63-234">Standard_ZRS.</span></span> <span data-ttu-id="19f63-235">Zone-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="19f63-235">Zone-redundant storage.</span></span>
- <span data-ttu-id="19f63-236">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="19f63-236">Standard_GRS.</span></span> <span data-ttu-id="19f63-237">Georedundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="19f63-237">Geo-redundant storage.</span></span>
- <span data-ttu-id="19f63-238">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="19f63-238">Standard_RAGRS.</span></span> <span data-ttu-id="19f63-239">Georedundáns tárterület olvasása.</span><span class="sxs-lookup"><span data-stu-id="19f63-239">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="19f63-240">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="19f63-240">Premium_LRS.</span></span> <span data-ttu-id="19f63-241">Prémium helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="19f63-241">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="19f63-242">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="19f63-242">Premium_ZRS.</span></span> <span data-ttu-id="19f63-243">Prémium zóna redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="19f63-243">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="19f63-244">Standard_GZRS – Georedundáns zónaredundáns tárolás.</span><span class="sxs-lookup"><span data-stu-id="19f63-244">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="19f63-245">Standard_RAGZRS – Olvassa el a georedundáns zóna-redundáns tárhelyet.</span><span class="sxs-lookup"><span data-stu-id="19f63-245">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="19f63-246">-Tag</span><span class="sxs-lookup"><span data-stu-id="19f63-246">-Tag</span></span>
<span data-ttu-id="19f63-247">Kulcsérték-párok a kiszolgálón címkékként beállított kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="19f63-247">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="19f63-248">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="19f63-248">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="19f63-249">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="19f63-249">-UseSubDomain</span></span>
<span data-ttu-id="19f63-250">Azt jelzi, hogy engedélyezi-e a CName közvetett érvényesítését.</span><span class="sxs-lookup"><span data-stu-id="19f63-250">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="19f63-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f63-251">CommonParameters</span></span>
<span data-ttu-id="19f63-252">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19f63-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f63-253">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19f63-253">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f63-254">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19f63-254">INPUTS</span></span>

### <span data-ttu-id="19f63-255">System.String</span><span class="sxs-lookup"><span data-stu-id="19f63-255">System.String</span></span>

## <span data-ttu-id="19f63-256">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19f63-256">OUTPUTS</span></span>

### <span data-ttu-id="19f63-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19f63-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="19f63-258">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19f63-258">NOTES</span></span>

## <span data-ttu-id="19f63-259">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19f63-259">RELATED LINKS</span></span>

[<span data-ttu-id="19f63-260">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19f63-260">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="19f63-261">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19f63-261">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="19f63-262">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19f63-262">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
