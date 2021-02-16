---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0e1243765064717c6e0030b437c07a176a232f44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163003"
---
# <span data-ttu-id="cd9f4-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd9f4-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="cd9f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9f4-103">Tárfiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-103">Creates a Storage account.</span></span>

## <span data-ttu-id="cd9f4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd9f4-104">SYNTAX</span></span>

### <span data-ttu-id="cd9f4-105">AzureActiveDirectoryDomainServicesForFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd9f4-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### <span data-ttu-id="cd9f4-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="cd9f4-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## <span data-ttu-id="cd9f4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd9f4-107">DESCRIPTION</span></span>
<span data-ttu-id="cd9f4-108">A **New-AzStorageAccount** parancsmag létrehoz egy Azure Storage-fiókot.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="cd9f4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd9f4-109">EXAMPLES</span></span>

### <span data-ttu-id="cd9f4-110">1. példa: Tárfiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="cd9f4-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="cd9f4-111">Ez a parancs tárfiókot hoz létre a MyResourceGroup nevű erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="cd9f4-112">2. példa: Blob-tárfiók létrehozása BlobStorage típusú és gyors AccessTier-fiókkal</span><span class="sxs-lookup"><span data-stu-id="cd9f4-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="cd9f4-113">Ezzel a paranccsal olyan Blob Storage-fiókot hoz létre, amely blobstorage típusú és gyors AccessTier típusú</span><span class="sxs-lookup"><span data-stu-id="cd9f4-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="cd9f4-114">3. példa: Tárfiók létrehozása a Kind StorageV2 segítségével, valamint identitás létrehozása és hozzárendelése az Azure KeyVaulthoz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="cd9f4-115">Ez a parancs létrehoz egy Tárfiókot a Kind StorageV2 segítségével.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="cd9f4-116">Emellett létrehoz és hozzárendel egy identitást, amely a fiókkulcsok Azure KeyVaulton keresztüli kezelésére használható.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="cd9f4-117">4. példa: Tárfiók létrehozása a NetworkRuleSet segítségével a JSON-ból</span><span class="sxs-lookup"><span data-stu-id="cd9f4-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="cd9f4-118">Ezzel a paranccsal olyan tárfiókot hoz létre, amely a JSON-ból NetworkRuleSet tulajdonságot hoz létre</span><span class="sxs-lookup"><span data-stu-id="cd9f4-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="cd9f4-119">5. példa: Tárfiók létrehozása engedélyezett Hierarchikus névtér funkcióval.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="cd9f4-120">Ez a parancs egy tárfiókot hoz létre, és a Hierarchikus névtér engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="cd9f4-121">6. példa: Hozzon létre egy tárfiókot az Azure Files AAD DS-hitelesítéssel, és engedélyezze a nagy fájlmegosztást.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="cd9f4-122">Ez a parancs létrehoz egy Tárfiókot az Azure Files AAD DS Authentication segítségével, és engedélyezi a nagy fájlmegosztást.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="cd9f4-123">7. példa: Tárfiók létrehozása a Files Active Directory tartományi szolgáltatás hitelesítésének engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="cd9f4-124">Ez a parancs egy tárolófiókot hoz létre, amely tartalmazza az Active Directory tartományi szolgáltatások hitelesítését.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="cd9f4-125">8. példa: Tárfiók létrehozása a várólistával és a táblaszolgáltatással fiókfedő titkosítási kulcsot, valamint infrastruktúra-titkosítás megkövetelése.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="cd9f4-126">Ez a parancs létrehoz egy tárfiókot a Várólistával és a Táblaszolgáltatással, és fiókfüggvényes titkosítási kulcsot használ, és infrastruktúra-titkosítást igényel, így a várólistán és a táblázatban a Blob és a File szolgáltatás ugyanazt a titkosítási kulcsot fogja használni, és a szolgáltatás egy másodlagos titkosítási réteget alkalmaz platform felügyelt kulcsokkal az adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="cd9f4-127">Ezután szerezze be a Tárfiók tulajdonságait, és tekintse meg a Várólistás és a Táblaszolgáltatás titkosítási kulcstípusát, valamint a RequireInfrastructureEncryption értéket.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="cd9f4-128">9. példa: Fiók MinimumTlsVersion és AllowBlobPublicAccess létrehozása</span><span class="sxs-lookup"><span data-stu-id="cd9f4-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="cd9f4-129">A parancs létrehoz egy fiókot a MinimumTlsVersion és az AllowBlobPublicAccess segítségével, majd a létrehozott fiók 2 tulajdonságát mutatja</span><span class="sxs-lookup"><span data-stu-id="cd9f4-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

### <span data-ttu-id="cd9f4-130">10. példa: Tárfiók létrehozása a RoutingPreference beállítással</span><span class="sxs-lookup"><span data-stu-id="cd9f4-130">Example 10: Create a Storage account with RoutingPreference setting</span></span>
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

<span data-ttu-id="cd9f4-131">Ez a parancs létrehoz egy Tárfiókot a RoutingPreference beállítással: a PublishMicrosoftEndpoint és a PublishInternetEndpoint mint true, a RoutingChoice pedig MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-131">This command creates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint and PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="cd9f4-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd9f4-132">PARAMETERS</span></span>

### <span data-ttu-id="cd9f4-133">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="cd9f4-133">-AccessTier</span></span>
<span data-ttu-id="cd9f4-134">A parancsmag által létrehozott tárfiók hozzáférési rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-134">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="cd9f4-135">A paraméter elfogadható értékei a következőek: Hot és Cool.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-135">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="cd9f4-136">Ha a Kind paraméterhez blobstorage értéket ad meg, meg kell adnia egy értéket az *AccessTier paraméterhez.* </span><span class="sxs-lookup"><span data-stu-id="cd9f4-136">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="cd9f4-137">Ha a Kind paraméterhez  tárterületértéket ad meg, ne adja meg az *AccessTier paramétert.*</span><span class="sxs-lookup"><span data-stu-id="cd9f4-137">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="cd9f4-138">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="cd9f4-138">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="cd9f4-139">Az Azure Storage biztonsági azonosítóját (SID) adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-139">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="cd9f4-140">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-140">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="cd9f4-141">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="cd9f4-141">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="cd9f4-142">A tartomány GUID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-142">Specifies the domain GUID.</span></span> <span data-ttu-id="cd9f4-143">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-143">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="cd9f4-144">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="cd9f4-144">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="cd9f4-145">Azt az elsődleges tartományt adja meg, amely esetén az AD DNS-kiszolgáló mérvadó.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-145">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="cd9f4-146">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="cd9f4-147">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="cd9f4-147">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="cd9f4-148">Megadja a biztonsági azonosítót (SID).</span><span class="sxs-lookup"><span data-stu-id="cd9f4-148">Specifies the security identifier (SID).</span></span> <span data-ttu-id="cd9f4-149">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="cd9f4-150">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="cd9f4-150">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="cd9f4-151">A lekért Active Directory-erdőt határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-151">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="cd9f4-152">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="cd9f4-153">-ActiveDirectoryNetNamesDomainName</span><span class="sxs-lookup"><span data-stu-id="cd9f4-153">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="cd9f4-154">A Net ROSTAS tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-154">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="cd9f4-155">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="cd9f4-156">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="cd9f4-156">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="cd9f4-157">Nyilvános hozzáférés engedélyezése a tárfiók összes blobját vagy tárolóját.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-157">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="cd9f4-158">A tulajdonság alapértelmezett értelmezése igaz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-158">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="cd9f4-159">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd9f4-159">-AsJob</span></span>
<span data-ttu-id="cd9f4-160">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cd9f4-160">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd9f4-161">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="cd9f4-161">-AssignIdentity</span></span>
<span data-ttu-id="cd9f4-162">Hozzon létre és rendeljen hozzá egy új tárfiók-identitást ehhez a tárfiókhoz, hogy olyan kulcskezelési szolgáltatásokkal használva használja őket, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-162">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="cd9f4-163">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="cd9f4-163">-CustomDomainName</span></span>
<span data-ttu-id="cd9f4-164">A Tárfiók egyéni tartományának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-164">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="cd9f4-165">Az alapértelmezett érték a Tárterület.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-165">The default value is Storage.</span></span>

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

### <span data-ttu-id="cd9f4-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9f4-166">-DefaultProfile</span></span>
<span data-ttu-id="cd9f4-167">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-167">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd9f4-168">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="cd9f4-168">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="cd9f4-169">Engedélyezze az Azure Files Active Directory tartományi szolgáltatás hitelesítését a tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-169">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="cd9f4-170">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="cd9f4-170">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="cd9f4-171">Engedélyezze az Azure Files Azure Active Directory tartományi szolgáltatás hitelesítését a tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-171">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="cd9f4-172">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="cd9f4-172">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="cd9f4-173">Azt jelzi, hogy a Tárfiók engedélyezi-e a hierarchikus névteret.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-173">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="cd9f4-174">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="cd9f4-174">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="cd9f4-175">Azt jelzi, hogy a Tárfiók csak https-forgalmat tesz-e lehetővé.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-175">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="cd9f4-176">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="cd9f4-176">-EnableLargeFileShare</span></span>
<span data-ttu-id="cd9f4-177">Azt jelzi, hogy a tárfiók támogatja-e az 5 TiB-kapacitásnál nagyobb fájlmegosztásokat.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-177">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="cd9f4-178">A fiók engedélyezése után a funkció nem tiltható le.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-178">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="cd9f4-179">Jelenleg csak az LRS és a ZRS replikációs típusai támogatottak, ezért a fiókok georedundáns fiókokra konvertálása nem lenne lehetséges.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-179">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="cd9f4-180">További információ: https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="cd9f4-180">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="cd9f4-181">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="cd9f4-181">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="cd9f4-182">Állítsa be a titkosítási kulcstípust a várólistához.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-182">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="cd9f4-183">Az alapértelmezett érték a Szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-183">The default value is Service.</span></span>
<span data-ttu-id="cd9f4-184">-Fiók: A várólistát fiókható titkosítási kulccsal titkosítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-184">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="cd9f4-185">-Szolgáltatás: A várólistát a rendszer mindig titkos kulcsokkal Service-Managed titkosítja.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-185">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="cd9f4-186">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="cd9f4-186">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="cd9f4-187">Állítsa be a táblázat titkosítási kulcstípusát.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-187">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="cd9f4-188">Az alapértelmezett érték a Szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-188">The default value is Service.</span></span>
- <span data-ttu-id="cd9f4-189">Fiók: A tábla fiókható titkosítási kulccsal lesz titkosítva.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-189">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="cd9f4-190">Szolgáltatás: A tábla mindig titkosítva lesz a Service-Managed kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-190">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="cd9f4-191">-Kind</span><span class="sxs-lookup"><span data-stu-id="cd9f4-191">-Kind</span></span>
<span data-ttu-id="cd9f4-192">Meghatározza, hogy a parancsmag milyen típusú tárfiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-192">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="cd9f4-193">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="cd9f4-193">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cd9f4-194">Tárterület.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-194">Storage.</span></span> <span data-ttu-id="cd9f4-195">Általános célú tárfiók, amely támogatja a blobok, táblák, várólisták, fájlok és lemezek tárolását.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-195">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="cd9f4-196">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-196">StorageV2.</span></span> <span data-ttu-id="cd9f4-197">Általános célú 2-es verzió (GPv2) tárfiók, amely támogatja a blobokat, a táblákat, a várólistákat, a fájlokat és a lemezeket speciális funkciókkal, például adatrétegezéssel.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-197">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="cd9f4-198">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-198">BlobStorage.</span></span> <span data-ttu-id="cd9f4-199">Blob storage account which supports storage of Blobs only.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-199">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="cd9f4-200">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-200">BlockBlobStorage.</span></span> <span data-ttu-id="cd9f4-201">Blokk blob storage account which supports storage of Block Blobs only.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-201">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="cd9f4-202">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-202">FileStorage.</span></span> <span data-ttu-id="cd9f4-203">Fájltároló fiók, amely csak a fájlok tárolását támogatja.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-203">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="cd9f4-204">Az alapértelmezett érték a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-204">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="cd9f4-205">-Location</span><span class="sxs-lookup"><span data-stu-id="cd9f4-205">-Location</span></span>
<span data-ttu-id="cd9f4-206">Megadja a létrehozni szükséges tárfiók helyét.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-206">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="cd9f4-207">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="cd9f4-207">-MinimumTlsVersion</span></span>
<span data-ttu-id="cd9f4-208">A tárterület-kérelmekben megengedett minimális TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-208">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="cd9f4-209">A tulajdonság alapértelmezett értelmezése a TLS 1.0.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-209">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="cd9f4-210">-Name</span><span class="sxs-lookup"><span data-stu-id="cd9f4-210">-Name</span></span>
<span data-ttu-id="cd9f4-211">A létrehozni szükséges tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-211">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="cd9f4-212">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd9f4-212">-NetworkRuleSet</span></span>
<span data-ttu-id="cd9f4-213">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazának meghatározására, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé térő szolgáltatások értékeinek beállítására, valamint a megadott szabályoktól különböző kérések kezelésére használható.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-213">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="cd9f4-214">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd9f4-214">-PublishInternetEndpoint</span></span>
<span data-ttu-id="cd9f4-215">Azt jelzi, hogy közzé kell-e tenni az internetes útválasztási tárolási végpontokat</span><span class="sxs-lookup"><span data-stu-id="cd9f4-215">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="cd9f4-216">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd9f4-216">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="cd9f4-217">Azt jelzi, hogy közzé kell-e tenni a Microsoft útválasztási tár végpontját</span><span class="sxs-lookup"><span data-stu-id="cd9f4-217">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="cd9f4-218">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd9f4-218">-ResourceGroupName</span></span>
<span data-ttu-id="cd9f4-219">Annak az erőforráscsoportnak a neve, amelyhez hozzá kell adni a Tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-219">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="cd9f4-220">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="cd9f4-220">-RoutingChoice</span></span>
<span data-ttu-id="cd9f4-221">Az Routing Choice a felhasználó által választott hálózati útválasztási típust határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-221">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="cd9f4-222">Lehetséges értékek: "MicrosoftRouting", "InternetRouting"</span><span class="sxs-lookup"><span data-stu-id="cd9f4-222">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

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

### <span data-ttu-id="cd9f4-223">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cd9f4-223">-SkuName</span></span>
<span data-ttu-id="cd9f4-224">A parancsmag által létrehozott tárfiók termékváltozatnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-224">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="cd9f4-225">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="cd9f4-225">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cd9f4-226">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-226">Standard_LRS.</span></span> <span data-ttu-id="cd9f4-227">Helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-227">Locally-redundant storage.</span></span>
- <span data-ttu-id="cd9f4-228">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-228">Standard_ZRS.</span></span> <span data-ttu-id="cd9f4-229">Zone-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-229">Zone-redundant storage.</span></span>
- <span data-ttu-id="cd9f4-230">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-230">Standard_GRS.</span></span> <span data-ttu-id="cd9f4-231">Georedundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-231">Geo-redundant storage.</span></span>
- <span data-ttu-id="cd9f4-232">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-232">Standard_RAGRS.</span></span> <span data-ttu-id="cd9f4-233">A hozzáférés georedundáns tárterületének olvasása.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-233">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="cd9f4-234">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-234">Premium_LRS.</span></span> <span data-ttu-id="cd9f4-235">Prémium helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-235">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="cd9f4-236">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-236">Premium_ZRS.</span></span> <span data-ttu-id="cd9f4-237">Prémium zóna redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-237">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="cd9f4-238">Standard_GZRS – Georedundáns zónaredundáns tárolás.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-238">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="cd9f4-239">Standard_RAGZRS – Olvassa el a georedundáns zóna-redundáns tárhelyet.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-239">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="cd9f4-240">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd9f4-240">-Tag</span></span>
<span data-ttu-id="cd9f4-241">Kulcsérték-párok a kiszolgálón címkékként beállított kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-241">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="cd9f4-242">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="cd9f4-242">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cd9f4-243">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="cd9f4-243">-UseSubDomain</span></span>
<span data-ttu-id="cd9f4-244">Azt jelzi, hogy engedélyezi-e a CName közvetett érvényesítését.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-244">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="cd9f4-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9f4-245">CommonParameters</span></span>
<span data-ttu-id="cd9f4-246">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd9f4-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9f4-247">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9f4-247">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9f4-248">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd9f4-248">INPUTS</span></span>

### <span data-ttu-id="cd9f4-249">System.String</span><span class="sxs-lookup"><span data-stu-id="cd9f4-249">System.String</span></span>

## <span data-ttu-id="cd9f4-250">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd9f4-250">OUTPUTS</span></span>

### <span data-ttu-id="cd9f4-251">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd9f4-251">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="cd9f4-252">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd9f4-252">NOTES</span></span>

## <span data-ttu-id="cd9f4-253">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd9f4-253">RELATED LINKS</span></span>

[<span data-ttu-id="cd9f4-254">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd9f4-254">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="cd9f4-255">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd9f4-255">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="cd9f4-256">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd9f4-256">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
