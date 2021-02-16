---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 4a4898645e3f296f861aa9f19a60ea182c112bff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150403"
---
# <span data-ttu-id="442e0-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="442e0-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="442e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="442e0-102">SYNOPSIS</span></span>
<span data-ttu-id="442e0-103">Tárfiókot módosít.</span><span class="sxs-lookup"><span data-stu-id="442e0-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="442e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="442e0-104">SYNTAX</span></span>

### <span data-ttu-id="442e0-105">StorageEncryption (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="442e0-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="442e0-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="442e0-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="442e0-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="442e0-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="442e0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="442e0-108">DESCRIPTION</span></span>
<span data-ttu-id="442e0-109">A **Set-AzStorageAccount** parancsmag módosítja az Azure Storage-fiókot.</span><span class="sxs-lookup"><span data-stu-id="442e0-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="442e0-110">Ezzel a parancsmagkal módosíthatja a fiók típusát, frissíthet egy ügyféltartományt, vagy címkéket állíthat be tárfiókon.</span><span class="sxs-lookup"><span data-stu-id="442e0-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="442e0-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="442e0-111">EXAMPLES</span></span>

### <span data-ttu-id="442e0-112">1. példa: Tárfiók típusának beállítása</span><span class="sxs-lookup"><span data-stu-id="442e0-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="442e0-113">Ezzel a paranccsal a Tárfiók típusát Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="442e0-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="442e0-114">2. példa: Tárfiók egyéni tartományának beállítása</span><span class="sxs-lookup"><span data-stu-id="442e0-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="442e0-115">Ez a parancs egyéni tartományt állít be a Tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="442e0-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="442e0-116">3. példa: A hozzáférési szint értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="442e0-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="442e0-117">A parancs lehűti az Access-szint értékét.</span><span class="sxs-lookup"><span data-stu-id="442e0-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="442e0-118">4. példa: Egyéni tartomány és címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="442e0-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="442e0-119">A parancs beállítja a Tárfiók egyéni tartományát és címkéit.</span><span class="sxs-lookup"><span data-stu-id="442e0-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="442e0-120">5. példa: A Titkosítási kulcsforrás beállítása Keyvaultra</span><span class="sxs-lookup"><span data-stu-id="442e0-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="442e0-121">Ez a parancs beállít egy titkosítási kulcsforrást egy új létrehozott Keyvaulttal.</span><span class="sxs-lookup"><span data-stu-id="442e0-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="442e0-122">6. példa: A Titkosítási kulcsforrás beállítása "Microsoft.Storage" értékre</span><span class="sxs-lookup"><span data-stu-id="442e0-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="442e0-123">Ez a parancs "Microsoft.Storage" titkosítási kulcsforrást ad meg</span><span class="sxs-lookup"><span data-stu-id="442e0-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="442e0-124">7. példa: Tárfiók NetworkRuleSet tulajdonságának beállítása a JSON-nal</span><span class="sxs-lookup"><span data-stu-id="442e0-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="442e0-125">Ez a parancs beállítja egy Tárfiók NetworkRuleSet tulajdonságát JSON-nal</span><span class="sxs-lookup"><span data-stu-id="442e0-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="442e0-126">8. példa: A NetworkRuleSet tulajdonság lekérte tárhelyfiókból, és beállítása másik tárfiókra</span><span class="sxs-lookup"><span data-stu-id="442e0-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="442e0-127">Ez az első parancs a NetworkRuleSet tulajdonságot egy tárfiókból kapja meg, a második pedig egy másik tárfiókra állítja be.</span><span class="sxs-lookup"><span data-stu-id="442e0-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="442e0-128">9. példa: Tárfiók frissítése a Kind "Storage" vagy a "BlobStorage" verzióval "StorageV2" típusú tárfiókra</span><span class="sxs-lookup"><span data-stu-id="442e0-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="442e0-129">A parancs frissíti a tárfiókot Kind "Storage" vagy "BlobStorage" verzióval "StorageV2" típusú tárfiókra.</span><span class="sxs-lookup"><span data-stu-id="442e0-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="442e0-130">10. példa: Tárfiók frissítése az Azure Files AAD DS-hitelesítés engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="442e0-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="442e0-131">A parancs frissíti a tárfiókot az Azure Files AAD DS-hitelesítés engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="442e0-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="442e0-132">11. példa: Tárfiók frissítése a Files Active Directory tartományi szolgáltatás hitelesítésének engedélyezésével, majd a Fájl identitásalapú hitelesítés beállításának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="442e0-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
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

<span data-ttu-id="442e0-133">A parancs frissíti a tárfiókot az Azure Files Active Directory tartományi szolgáltatás hitelesítésének engedélyezésével, majd megjeleníti a Fájl identitásalapú hitelesítés beállítását.</span><span class="sxs-lookup"><span data-stu-id="442e0-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="442e0-134">12. példa: A MinimumTlsVersion és az AllowBlobPublicAccess beállítása</span><span class="sxs-lookup"><span data-stu-id="442e0-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="442e0-135">A parancs beállítja a MinimumTlsVersion és az AllowBlobPublicAccess tulajdonságot, majd a fiók 2 tulajdonságát mutatja.</span><span class="sxs-lookup"><span data-stu-id="442e0-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

### <span data-ttu-id="442e0-136">13. példa: Tárfiók frissítése a RoutingPreference beállítással</span><span class="sxs-lookup"><span data-stu-id="442e0-136">Example 13: Update a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -PublishMicrosoftEndpoint $false -PublishInternetEndpoint $true -RoutingChoice InternetRouting

PS C:\>$account.RoutingPreference

RoutingChoice   PublishMicrosoftEndpoints PublishInternetEndpoints
-------------   ------------------------- ------------------------
InternetRouting                     False                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : 
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="442e0-137">Ez a parancs frissíti a tárfiókot a RoutingPreference beállítással: A PublishMicrosoftEndpoint mint false, a PublishInternetEndpoint mint true, a RoutingChoice pedig MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="442e0-137">This command updates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint as false, PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="442e0-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="442e0-138">PARAMETERS</span></span>

### <span data-ttu-id="442e0-139">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="442e0-139">-AccessTier</span></span>
<span data-ttu-id="442e0-140">A parancsmag által módosított Tárfiók hozzáférési rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="442e0-140">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="442e0-141">A paraméter elfogadható értékei a következőek: Hot és Cool.</span><span class="sxs-lookup"><span data-stu-id="442e0-141">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="442e0-142">Ha módosítja a hozzáférési réteget, az további díjakat eredményezhet.</span><span class="sxs-lookup"><span data-stu-id="442e0-142">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="442e0-143">További információért lásd: [Azure Blob Storage: Hot and cool storage tiers.](http://go.microsoft.com/fwlink/?LinkId=786482)</span><span class="sxs-lookup"><span data-stu-id="442e0-143">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="442e0-144">Ha a Tárfiókban a Kind as StorageV2 vagy a BlobStorage érték van megadva, megadhatja az *AccessTier paramétert.*</span><span class="sxs-lookup"><span data-stu-id="442e0-144">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="442e0-145">Ha a Tárfiókban a Kind as Storage érték van megadva, ne adja meg az *AccessTier paramétert.*</span><span class="sxs-lookup"><span data-stu-id="442e0-145">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="442e0-146">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="442e0-146">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="442e0-147">Az Azure Storage biztonsági azonosítóját (SID) adja meg.</span><span class="sxs-lookup"><span data-stu-id="442e0-147">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="442e0-148">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="442e0-148">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="442e0-149">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="442e0-149">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="442e0-150">A tartomány GUID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="442e0-150">Specifies the domain GUID.</span></span> <span data-ttu-id="442e0-151">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="442e0-151">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="442e0-152">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="442e0-152">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="442e0-153">Azt az elsődleges tartományt adja meg, amely esetén az AD DNS-kiszolgáló mérvadó.</span><span class="sxs-lookup"><span data-stu-id="442e0-153">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="442e0-154">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="442e0-154">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="442e0-155">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="442e0-155">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="442e0-156">Megadja a biztonsági azonosítót (SID).</span><span class="sxs-lookup"><span data-stu-id="442e0-156">Specifies the security identifier (SID).</span></span> <span data-ttu-id="442e0-157">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="442e0-157">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="442e0-158">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="442e0-158">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="442e0-159">A lekért Active Directory-erdőt határozza meg.</span><span class="sxs-lookup"><span data-stu-id="442e0-159">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="442e0-160">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="442e0-160">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="442e0-161">-ActiveDirectoryNetNamesDomainName</span><span class="sxs-lookup"><span data-stu-id="442e0-161">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="442e0-162">A Net ROSTAS tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="442e0-162">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="442e0-163">Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="442e0-163">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="442e0-164">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="442e0-164">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="442e0-165">A tárfiók összes blobja vagy tárolója nyilvános hozzáférésének engedélyezése vagy engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="442e0-165">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="442e0-166">-AsJob</span><span class="sxs-lookup"><span data-stu-id="442e0-166">-AsJob</span></span>
<span data-ttu-id="442e0-167">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="442e0-167">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="442e0-168">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="442e0-168">-AssignIdentity</span></span>
<span data-ttu-id="442e0-169">Hozzon létre és rendeljen hozzá egy új tárfiók-identitást ehhez a tárfiókhoz, hogy olyan kulcskezelési szolgáltatásokkal használva használja őket, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="442e0-169">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="442e0-170">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="442e0-170">-CustomDomainName</span></span>
<span data-ttu-id="442e0-171">Az egyéni tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="442e0-171">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="442e0-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442e0-172">-DefaultProfile</span></span>
<span data-ttu-id="442e0-173">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="442e0-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="442e0-174">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="442e0-174">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="442e0-175">Engedélyezze az Azure Files Active Directory tartományi szolgáltatás hitelesítését a tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="442e0-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="442e0-176">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="442e0-176">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="442e0-177">Engedélyezze az Azure Files Active Directory tartományi szolgáltatás hitelesítését a tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="442e0-177">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="442e0-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="442e0-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="442e0-179">Azt jelzi, hogy a Tárfiók csak https-forgalmat tesz-e lehetővé.</span><span class="sxs-lookup"><span data-stu-id="442e0-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="442e0-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="442e0-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="442e0-181">Azt jelzi, hogy a tárfiók támogatja-e az 5 TiB-kapacitásnál nagyobb fájlmegosztásokat.</span><span class="sxs-lookup"><span data-stu-id="442e0-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="442e0-182">A fiók engedélyezése után a funkció nem tiltható le.</span><span class="sxs-lookup"><span data-stu-id="442e0-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="442e0-183">Jelenleg csak az LRS és a ZRS replikációs típusai támogatottak, ezért a fiókok georedundáns fiókokra történő konvertálása nem lenne lehetséges.</span><span class="sxs-lookup"><span data-stu-id="442e0-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="442e0-184">További információ: https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="442e0-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="442e0-185">-Force</span><span class="sxs-lookup"><span data-stu-id="442e0-185">-Force</span></span>
<span data-ttu-id="442e0-186">A változtatást a Tárfiókba kell átírni.</span><span class="sxs-lookup"><span data-stu-id="442e0-186">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="442e0-187">-KeyName</span><span class="sxs-lookup"><span data-stu-id="442e0-187">-KeyName</span></span>
<span data-ttu-id="442e0-188">Ha a -KeyvaultEncryption segítségével engedélyezi a titkosítást a kulcstárban, adja meg ezzel a beállítással a Kulcsnév tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="442e0-188">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="442e0-189">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="442e0-189">-KeyvaultEncryption</span></span>
<span data-ttu-id="442e0-190">Azt jelzi, hogy a Tárhelyszolgáltatás-titkosítás használata során használni kell-e a Microsoft KeyVaultot a titkosítási kulcsokhoz.</span><span class="sxs-lookup"><span data-stu-id="442e0-190">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="442e0-191">Ha a KeyName, a KeyVersion és a KeyVaultUri mind be van állítva, a KeySource értéke Microsoft.Keyvault lesz, függetlenül attól, hogy be van-e állítva ez a paraméter.</span><span class="sxs-lookup"><span data-stu-id="442e0-191">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="442e0-192">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="442e0-192">-KeyVaultUri</span></span>
<span data-ttu-id="442e0-193">Ha a -KeyvaultEncryption paraméter megadásával használja a kulcstitkosítást, ezzel a beállítással megadhatja a kulcstár URI-ját.</span><span class="sxs-lookup"><span data-stu-id="442e0-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="442e0-194">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="442e0-194">-KeyVersion</span></span>
<span data-ttu-id="442e0-195">Ha a kulcstár titkosítását a -KeyvaultEncryption paraméter megadásával használja, akkor ezzel a beállítással megadhatja az URI-t a kulcsverzióhoz.</span><span class="sxs-lookup"><span data-stu-id="442e0-195">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="442e0-196">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="442e0-196">-MinimumTlsVersion</span></span>
<span data-ttu-id="442e0-197">A tárterület-kérelmekben megengedett minimális TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="442e0-197">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="442e0-198">-Name</span><span class="sxs-lookup"><span data-stu-id="442e0-198">-Name</span></span>
<span data-ttu-id="442e0-199">A módosítani szükséges tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="442e0-199">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="442e0-200">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="442e0-200">-NetworkRuleSet</span></span>
<span data-ttu-id="442e0-201">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazának meghatározására, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé térő szolgáltatások értékeinek beállítására, valamint a megadott szabályoktól különböző kérések kezelésére használható.</span><span class="sxs-lookup"><span data-stu-id="442e0-201">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="442e0-202">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="442e0-202">-PublishInternetEndpoint</span></span>
<span data-ttu-id="442e0-203">Azt jelzi, hogy közzé kell-e tenni az internetes útválasztási tárolási végpontokat</span><span class="sxs-lookup"><span data-stu-id="442e0-203">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="442e0-204">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="442e0-204">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="442e0-205">Azt jelzi, hogy közzé kell-e tenni a Microsoft útválasztási tár végpontját</span><span class="sxs-lookup"><span data-stu-id="442e0-205">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="442e0-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="442e0-206">-ResourceGroupName</span></span>
<span data-ttu-id="442e0-207">Annak az erőforráscsoportnak a nevét adja meg, amelyben módosítani szeretné a Tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="442e0-207">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="442e0-208">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="442e0-208">-RoutingChoice</span></span>
<span data-ttu-id="442e0-209">Az Routing Choice a felhasználó által választott hálózati útválasztási típust határozza meg.</span><span class="sxs-lookup"><span data-stu-id="442e0-209">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="442e0-210">Lehetséges értékek: "MicrosoftRouting", "InternetRouting"</span><span class="sxs-lookup"><span data-stu-id="442e0-210">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

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

### <span data-ttu-id="442e0-211">-SkuName</span><span class="sxs-lookup"><span data-stu-id="442e0-211">-SkuName</span></span>
<span data-ttu-id="442e0-212">A Tárfiók termékváltozatnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="442e0-212">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="442e0-213">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="442e0-213">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="442e0-214">Standard_LRS – Helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="442e0-214">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="442e0-215">Standard_ZRS – Zóna redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="442e0-215">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="442e0-216">Standard_GRS – Georedundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="442e0-216">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="442e0-217">Standard_RAGRS – A hozzáférés georedundáns tárterületének olvasása.</span><span class="sxs-lookup"><span data-stu-id="442e0-217">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="442e0-218">Premium_LRS – Prémium helyi redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="442e0-218">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="442e0-219">Standard_GZRS – Georedundáns zónaredundáns tárolás.</span><span class="sxs-lookup"><span data-stu-id="442e0-219">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="442e0-220">Standard_RAGZRS – Olvassa el a georedundáns zóna-redundáns tárhelyet.</span><span class="sxs-lookup"><span data-stu-id="442e0-220">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="442e0-221">A fióktípusok Standard_ZRS és Premium_LRS más típusú fiókokra nem változtatható.</span><span class="sxs-lookup"><span data-stu-id="442e0-221">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="442e0-222">Más fióktípusokat nem Standard_ZRS vagy Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="442e0-222">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="442e0-223">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="442e0-223">-StorageEncryption</span></span>
<span data-ttu-id="442e0-224">Azt jelzi, hogy a Tárfiók titkosítása a Microsoft által kezelt kulcsok használatára van-e beállítva.</span><span class="sxs-lookup"><span data-stu-id="442e0-224">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="442e0-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="442e0-225">-Tag</span></span>
<span data-ttu-id="442e0-226">Kulcsérték-párok a kiszolgálón címkékként beállított kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="442e0-226">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="442e0-227">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="442e0-227">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="442e0-228">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="442e0-228">-UpgradeToStorageV2</span></span>
<span data-ttu-id="442e0-229">Frissítse a tárfiókok fajtáját a Storage vagy BlobStorage-ból a StorageV2-re.</span><span class="sxs-lookup"><span data-stu-id="442e0-229">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="442e0-230">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="442e0-230">-UseSubDomain</span></span>
<span data-ttu-id="442e0-231">Azt jelzi, hogy engedélyezi-e a CName közvetett érvényesítését.</span><span class="sxs-lookup"><span data-stu-id="442e0-231">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="442e0-232">-Confirm</span><span class="sxs-lookup"><span data-stu-id="442e0-232">-Confirm</span></span>
<span data-ttu-id="442e0-233">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="442e0-233">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="442e0-234">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="442e0-234">-WhatIf</span></span>
<span data-ttu-id="442e0-235">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="442e0-235">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="442e0-236">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="442e0-236">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="442e0-237">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442e0-237">CommonParameters</span></span>
<span data-ttu-id="442e0-238">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="442e0-238">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442e0-239">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="442e0-239">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442e0-240">INPUTS</span><span class="sxs-lookup"><span data-stu-id="442e0-240">INPUTS</span></span>

### <span data-ttu-id="442e0-241">System.String</span><span class="sxs-lookup"><span data-stu-id="442e0-241">System.String</span></span>

### <span data-ttu-id="442e0-242">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="442e0-242">System.Collections.Hashtable</span></span>

## <span data-ttu-id="442e0-243">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="442e0-243">OUTPUTS</span></span>

### <span data-ttu-id="442e0-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="442e0-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="442e0-245">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="442e0-245">NOTES</span></span>

## <span data-ttu-id="442e0-246">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="442e0-246">RELATED LINKS</span></span>

[<span data-ttu-id="442e0-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="442e0-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="442e0-248">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="442e0-248">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="442e0-249">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="442e0-249">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
