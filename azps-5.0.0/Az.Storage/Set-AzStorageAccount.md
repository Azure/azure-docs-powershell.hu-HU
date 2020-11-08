---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185779"
---
# <span data-ttu-id="ad2af-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad2af-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="ad2af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad2af-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2af-103">Módosítja a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="ad2af-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="ad2af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad2af-104">SYNTAX</span></span>

### <span data-ttu-id="ad2af-105">StorageEncryption (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad2af-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad2af-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="ad2af-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad2af-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="ad2af-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2af-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad2af-108">DESCRIPTION</span></span>
<span data-ttu-id="ad2af-109">A **set-AzStorageAccount** parancsmag az Azure Storage-fiókot módosítja.</span><span class="sxs-lookup"><span data-stu-id="ad2af-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="ad2af-110">Ezzel a parancsmaggal módosíthatja a fiók típusát, frissítheti az ügyfél tartományát, és beállíthatja a címkéket egy tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="ad2af-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="ad2af-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ad2af-111">EXAMPLES</span></span>

### <span data-ttu-id="ad2af-112">Példa 1: a tárolási fiók típusának beállítása</span><span class="sxs-lookup"><span data-stu-id="ad2af-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="ad2af-113">Ez a parancs a tárterület-típust a Standard_RAGRS értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="ad2af-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="ad2af-114">2. példa: egyéni tartomány beállítása tárterület-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="ad2af-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="ad2af-115">Ez a parancs egy egyéni tartományt állít be egy tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="ad2af-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="ad2af-116">3. példa: az Access-szint értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="ad2af-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="ad2af-117">A parancs az Access-réteg értékét kihűlni állítja.</span><span class="sxs-lookup"><span data-stu-id="ad2af-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="ad2af-118">4. példa: egyéni tartomány és címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="ad2af-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="ad2af-119">A parancs a tárolási fiók egyéni tartományát és címkéit állítja be.</span><span class="sxs-lookup"><span data-stu-id="ad2af-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="ad2af-120">Példa 5: titkosítási forrás beállítása a következőre</span><span class="sxs-lookup"><span data-stu-id="ad2af-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="ad2af-121">Ez a parancs a titkosító jelforrásokat egy új, új, létrehozott főboltozattal állítja be.</span><span class="sxs-lookup"><span data-stu-id="ad2af-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="ad2af-122">6. példa: a titkosítási forrás beállítása a következőre: "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="ad2af-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="ad2af-123">Ez a parancs a titkosító jelforrást a "Microsoft. Storage" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="ad2af-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="ad2af-124">7. példa: tárolási fiók NetworkRuleSet tulajdonságának beállítása JSON-val</span><span class="sxs-lookup"><span data-stu-id="ad2af-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="ad2af-125">Ez a parancs a JSON-NetworkRuleSet tulajdonságát állítja be.</span><span class="sxs-lookup"><span data-stu-id="ad2af-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="ad2af-126">8. példa: a NetworkRuleSet tulajdonság beolvasása egy tárterület-fiókból, és beállítása másik tárolási fiókra</span><span class="sxs-lookup"><span data-stu-id="ad2af-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="ad2af-127">Ez az első parancs egy tárterület-fiókból kapja a NetworkRuleSet tulajdonságot, és a második parancs másik tárolási fiókra állítja be.</span><span class="sxs-lookup"><span data-stu-id="ad2af-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="ad2af-128">9. példa: a "tárterület" vagy a "BlobStorage" típusú tárolási fiók frissítése "StorageV2" típusú tárterületre</span><span class="sxs-lookup"><span data-stu-id="ad2af-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="ad2af-129">A parancs "tárterület" vagy "BlobStorage" típusú tárterületet frissít a "StorageV2" típusú tárterület-tárolási fiókra.</span><span class="sxs-lookup"><span data-stu-id="ad2af-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="ad2af-130">10. példa: a tárolási fiók frissítése az Azure Files AAD DS-hitelesítés engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="ad2af-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="ad2af-131">A parancs tárolási fiókot frissít az Azure Files AAD DS-hitelesítés engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="ad2af-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="ad2af-132">Példa: a tárterület-fiók frissítése: engedélyezze a fájlok Active Directory tartományi szolgáltatások hitelesítését, majd jelenítse meg a fájl-identitás alapú hitelesítés beállítást</span><span class="sxs-lookup"><span data-stu-id="ad2af-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

<span data-ttu-id="ad2af-133">A parancs frissíti a tárolási fiókot az Azure-fájlok Active Directory tartományi szolgáltatás-hitelesítésének engedélyezésével, majd megjeleníti a fájl-identitás alapú hitelesítés beállítását.</span><span class="sxs-lookup"><span data-stu-id="ad2af-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="ad2af-134">12 példa: a MinimumTlsVersion és a AllowBlobPublicAccess megadása</span><span class="sxs-lookup"><span data-stu-id="ad2af-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="ad2af-135">A parancs beállítja a MinimumTlsVersion és a AllowBlobPublicAccess, majd megjeleníti a fiók 2 tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="ad2af-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

## <span data-ttu-id="ad2af-136">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad2af-136">PARAMETERS</span></span>

### <span data-ttu-id="ad2af-137">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="ad2af-137">-AccessTier</span></span>
<span data-ttu-id="ad2af-138">Annak a tárolási fióknak az Access-rétegét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="ad2af-138">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="ad2af-139">A paraméter elfogadható értékei a következők: meleg és hűvös.</span><span class="sxs-lookup"><span data-stu-id="ad2af-139">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="ad2af-140">Ha módosítja a hozzáférési szintet, az esetleg további díjakat is eredményezhet.</span><span class="sxs-lookup"><span data-stu-id="ad2af-140">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="ad2af-141">További információt az [Azure Blob Storage: Hot and cool Storage Tiers](http://go.microsoft.com/fwlink/?LinkId=786482)című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="ad2af-141">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="ad2af-142">Ha a tárolási fióknak van olyan típusa, mint StorageV2 vagy BlobStorage, megadhatja a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="ad2af-142">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="ad2af-143">Ha a tárolási fióknak van tárterülete, ne adja meg a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="ad2af-143">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="ad2af-144">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="ad2af-144">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="ad2af-145">Az Azure-tárterület biztonsági azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad2af-145">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="ad2af-146">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="ad2af-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ad2af-147">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="ad2af-147">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="ad2af-148">A tartomány GUID-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad2af-148">Specifies the domain GUID.</span></span> <span data-ttu-id="ad2af-149">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="ad2af-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ad2af-150">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="ad2af-150">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="ad2af-151">Annak az elsődleges tartománynak a megadása, amelyhez az AD DNS-kiszolgáló mérvadó.</span><span class="sxs-lookup"><span data-stu-id="ad2af-151">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="ad2af-152">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="ad2af-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ad2af-153">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="ad2af-153">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="ad2af-154">A biztonsági azonosítót (SID) adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad2af-154">Specifies the security identifier (SID).</span></span> <span data-ttu-id="ad2af-155">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="ad2af-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ad2af-156">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="ad2af-156">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="ad2af-157">A beolvasott Active Directory-erdőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad2af-157">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="ad2af-158">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="ad2af-158">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ad2af-159">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="ad2af-159">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="ad2af-160">A NetBIOS-tartománynevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad2af-160">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="ad2af-161">Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="ad2af-161">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ad2af-162">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="ad2af-162">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="ad2af-163">Engedélyezheti vagy letilthatja a nyilvános hozzáférést a tároló fiók minden blobján vagy tárolójában.</span><span class="sxs-lookup"><span data-stu-id="ad2af-163">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="ad2af-164">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad2af-164">-AsJob</span></span>
<span data-ttu-id="ad2af-165">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ad2af-165">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad2af-166">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ad2af-166">-AssignIdentity</span></span>
<span data-ttu-id="ad2af-167">Új tárolási fiók identitásának létrehozása és hozzárendelése ehhez a tárterülethez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="ad2af-167">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ad2af-168">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ad2af-168">-CustomDomainName</span></span>
<span data-ttu-id="ad2af-169">Az egyéni tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad2af-169">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="ad2af-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2af-170">-DefaultProfile</span></span>
<span data-ttu-id="ad2af-171">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad2af-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad2af-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="ad2af-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="ad2af-173">Engedélyezze az Azure-fájlok Active Directory tartományi szolgáltatás-hitelesítését a tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="ad2af-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2af-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="ad2af-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="ad2af-175">Engedélyezze az Azure-fájlok Active Directory tartományi szolgáltatás-hitelesítését a tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="ad2af-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2af-176">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="ad2af-176">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="ad2af-177">Azt jelzi, hogy a tárolási fiók csak HTTPS-forgalmat engedélyez-e.</span><span class="sxs-lookup"><span data-stu-id="ad2af-177">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="ad2af-178">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="ad2af-178">-EnableLargeFileShare</span></span>
<span data-ttu-id="ad2af-179">Azt jelzi, hogy a tárolási fiók támogatja-e az 5 TiB-nál több kapacitással rendelkező nagyméretű fájlmegosztás használatát.</span><span class="sxs-lookup"><span data-stu-id="ad2af-179">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="ad2af-180">Miután a fiók engedélyezve van, a funkció nem tiltható le.</span><span class="sxs-lookup"><span data-stu-id="ad2af-180">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="ad2af-181">Jelenleg csak a LRS és a ZRS replikációs típusai támogatottak, ezért nem lehetett beírni a "geo-redundáns fiókok" konverzióját.</span><span class="sxs-lookup"><span data-stu-id="ad2af-181">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="ad2af-182">További információ https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="ad2af-182">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="ad2af-183">-Force</span><span class="sxs-lookup"><span data-stu-id="ad2af-183">-Force</span></span>
<span data-ttu-id="ad2af-184">Kényszeríti a módosítást a tárolási fiókba.</span><span class="sxs-lookup"><span data-stu-id="ad2af-184">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="ad2af-185">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="ad2af-185">-KeyName</span></span>
<span data-ttu-id="ad2af-186">Ha a KeyvaultEncryption lehetővé teszi a titkosítást a kulcsfájl segítségével, adja meg a kulcsnév tulajdonságot ezzel a beállítással.</span><span class="sxs-lookup"><span data-stu-id="ad2af-186">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2af-187">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="ad2af-187">-KeyvaultEncryption</span></span>
<span data-ttu-id="ad2af-188">Azt jelzi, hogy a Microsoft-billentyűzetet szeretné-e használni a titkosítási kulcsokhoz a tárterület-titkosítási szolgáltatás használatakor.</span><span class="sxs-lookup"><span data-stu-id="ad2af-188">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="ad2af-189">Ha a kulcsnév, a saját verzió és a KeyVaultUri mind készlet, a program a forráskódot a Microsoft. vagy a parancsra állítja be, hogy ez a paraméter be van-e állítva.</span><span class="sxs-lookup"><span data-stu-id="ad2af-189">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2af-190">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="ad2af-190">-KeyVaultUri</span></span>
<span data-ttu-id="ad2af-191">Ha a-KeyvaultEncryption paraméter megadásával használja a Key Vault-titkosítást, ezzel a beállítással megadhatja az URI-azonosítót a kulcs Boltozatához.</span><span class="sxs-lookup"><span data-stu-id="ad2af-191">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2af-192">-Verzió</span><span class="sxs-lookup"><span data-stu-id="ad2af-192">-KeyVersion</span></span>
<span data-ttu-id="ad2af-193">Ha a-KeyvaultEncryption paraméter megadásával használja a Key Vault-titkosítást, akkor ezzel a beállítással megadhatja az URI-azonosító értékét a kulcs verziójában.</span><span class="sxs-lookup"><span data-stu-id="ad2af-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2af-194">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ad2af-194">-MinimumTlsVersion</span></span>
<span data-ttu-id="ad2af-195">A tárolási kérelmeken engedélyezni kívánt minimális TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="ad2af-195">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="ad2af-196">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad2af-196">-Name</span></span>
<span data-ttu-id="ad2af-197">A módosítani kívánt tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad2af-197">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="ad2af-198">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad2af-198">-NetworkRuleSet</span></span>
<span data-ttu-id="ad2af-199">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé tevő, valamint a meghatározott szabályoknak nem megfelelő kérelmek kezelésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="ad2af-199">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="ad2af-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2af-200">-ResourceGroupName</span></span>
<span data-ttu-id="ad2af-201">Annak az erőforrás-csoportnak a nevét adja meg, amelybe a tárolási fiókot módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="ad2af-201">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="ad2af-202">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ad2af-202">-SkuName</span></span>
<span data-ttu-id="ad2af-203">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="ad2af-203">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="ad2af-204">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ad2af-204">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad2af-205">Standard_LRS-lokálisan redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="ad2af-205">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="ad2af-206">Standard_ZRS-zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="ad2af-206">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="ad2af-207">Standard_GRS-geo-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="ad2af-207">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="ad2af-208">Standard_RAGRS-olvasási hozzáférés: Geo-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="ad2af-208">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="ad2af-209">Premium_LRS-prémium helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="ad2af-209">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="ad2af-210">Standard_GZRS-geo-redundáns zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="ad2af-210">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="ad2af-211">Standard_RAGZRS – az Access geo-redundáns zónája – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="ad2af-211">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="ad2af-212">A Standard_ZRS és a Premium_LRS típusokat nem lehet más típusú fiókokra módosítani.</span><span class="sxs-lookup"><span data-stu-id="ad2af-212">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="ad2af-213">Más típusú fiókokat nem módosíthat Standard_ZRS vagy Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="ad2af-213">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2af-214">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="ad2af-214">-StorageEncryption</span></span>
<span data-ttu-id="ad2af-215">Azt jelzi, hogy a tárterület-titkosítás a Microsoft által felügyelt kulcsok használatára van-e beállítva.</span><span class="sxs-lookup"><span data-stu-id="ad2af-215">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2af-216">-Címke</span><span class="sxs-lookup"><span data-stu-id="ad2af-216">-Tag</span></span>
<span data-ttu-id="ad2af-217">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="ad2af-217">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="ad2af-218">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="ad2af-218">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2af-219">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="ad2af-219">-UpgradeToStorageV2</span></span>
<span data-ttu-id="ad2af-220">Frissítse a tárterületet a tárterületről vagy a BlobStorage a StorageV2-ra.</span><span class="sxs-lookup"><span data-stu-id="ad2af-220">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="ad2af-221">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="ad2af-221">-UseSubDomain</span></span>
<span data-ttu-id="ad2af-222">Azt jelzi, hogy engedélyezi-e a közvetlen CName érvényesítést.</span><span class="sxs-lookup"><span data-stu-id="ad2af-222">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="ad2af-223">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad2af-223">-Confirm</span></span>
<span data-ttu-id="ad2af-224">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad2af-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2af-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2af-225">-WhatIf</span></span>
<span data-ttu-id="ad2af-226">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad2af-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad2af-227">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad2af-227">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2af-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2af-228">CommonParameters</span></span>
<span data-ttu-id="ad2af-229">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad2af-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2af-230">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2af-230">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2af-231">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad2af-231">INPUTS</span></span>

### <span data-ttu-id="ad2af-232">System. String</span><span class="sxs-lookup"><span data-stu-id="ad2af-232">System.String</span></span>

### <span data-ttu-id="ad2af-233">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad2af-233">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ad2af-234">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad2af-234">OUTPUTS</span></span>

### <span data-ttu-id="ad2af-235">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad2af-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ad2af-236">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad2af-236">NOTES</span></span>

## <span data-ttu-id="ad2af-237">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad2af-237">RELATED LINKS</span></span>

[<span data-ttu-id="ad2af-238">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad2af-238">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="ad2af-239">Új – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad2af-239">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="ad2af-240">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad2af-240">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
