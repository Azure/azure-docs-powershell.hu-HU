---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: ca6bc95d0da6e9793b2bb26ab12362bb74d9212a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011223"
---
# <span data-ttu-id="f61c5-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f61c5-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="f61c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f61c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f61c5-103">Módosítja a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="f61c5-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="f61c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f61c5-104">SYNTAX</span></span>

### <span data-ttu-id="f61c5-105">StorageEncryption (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f61c5-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f61c5-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="f61c5-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f61c5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f61c5-107">DESCRIPTION</span></span>
<span data-ttu-id="f61c5-108">A **set-AzStorageAccount** parancsmag az Azure Storage-fiókot módosítja.</span><span class="sxs-lookup"><span data-stu-id="f61c5-108">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="f61c5-109">Ezzel a parancsmaggal módosíthatja a fiók típusát, frissítheti az ügyfél tartományát, és beállíthatja a címkéket egy tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="f61c5-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="f61c5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f61c5-110">EXAMPLES</span></span>

### <span data-ttu-id="f61c5-111">Példa 1: a tárolási fiók típusának beállítása</span><span class="sxs-lookup"><span data-stu-id="f61c5-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="f61c5-112">Ez a parancs a tárterület-típust a Standard_RAGRS értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="f61c5-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="f61c5-113">2. példa: egyéni tartomány beállítása tárterület-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="f61c5-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="f61c5-114">Ez a parancs egy egyéni tartományt állít be egy tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f61c5-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="f61c5-115">3. példa: az Access-szint értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="f61c5-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="f61c5-116">A parancs az Access-réteg értékét kihűlni állítja.</span><span class="sxs-lookup"><span data-stu-id="f61c5-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="f61c5-117">4. példa: egyéni tartomány és címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="f61c5-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="f61c5-118">A parancs a tárolási fiók egyéni tartományát és címkéit állítja be.</span><span class="sxs-lookup"><span data-stu-id="f61c5-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="f61c5-119">Példa 5: titkosítási forrás beállítása a következőre</span><span class="sxs-lookup"><span data-stu-id="f61c5-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="f61c5-120">Ez a parancs a titkosító jelforrásokat egy új, új, létrehozott főboltozattal állítja be.</span><span class="sxs-lookup"><span data-stu-id="f61c5-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="f61c5-121">6. példa: a titkosítási forrás beállítása a következőre: "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="f61c5-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="f61c5-122">Ez a parancs a titkosító jelforrást a "Microsoft. Storage" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="f61c5-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="f61c5-123">7. példa: tárolási fiók NetworkRuleSet tulajdonságának beállítása JSON-val</span><span class="sxs-lookup"><span data-stu-id="f61c5-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="f61c5-124">Ez a parancs a JSON-NetworkRuleSet tulajdonságát állítja be.</span><span class="sxs-lookup"><span data-stu-id="f61c5-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="f61c5-125">8. példa: a NetworkRuleSet tulajdonság beolvasása egy tárterület-fiókból, és beállítása másik tárolási fiókra</span><span class="sxs-lookup"><span data-stu-id="f61c5-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="f61c5-126">Ez az első parancs egy tárterület-fiókból kapja a NetworkRuleSet tulajdonságot, és a második parancs másik tárolási fiókra állítja be.</span><span class="sxs-lookup"><span data-stu-id="f61c5-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="f61c5-127">9. példa: a "tárterület" vagy a "BlobStorage" típusú tárolási fiók frissítése "StorageV2" típusú tárterületre</span><span class="sxs-lookup"><span data-stu-id="f61c5-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="f61c5-128">A parancs "tárterület" vagy "BlobStorage" típusú tárterületet frissít a "StorageV2" típusú tárterület-tárolási fiókra.</span><span class="sxs-lookup"><span data-stu-id="f61c5-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="f61c5-129">10. példa: a tárolási fiók frissítése az Azure Files AAD DS-hitelesítés engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="f61c5-129">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true
```

<span data-ttu-id="f61c5-130">A parancs tárolási fiókot frissít az Azure Files AAD DS-hitelesítés engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="f61c5-130">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

## <span data-ttu-id="f61c5-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f61c5-131">PARAMETERS</span></span>

### <span data-ttu-id="f61c5-132">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="f61c5-132">-AccessTier</span></span>
<span data-ttu-id="f61c5-133">Annak a tárolási fióknak az Access-rétegét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f61c5-133">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="f61c5-134">A paraméter elfogadható értékei a következők: meleg és hűvös.</span><span class="sxs-lookup"><span data-stu-id="f61c5-134">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="f61c5-135">Ha módosítja a hozzáférési szintet, az esetleg további díjakat is eredményezhet.</span><span class="sxs-lookup"><span data-stu-id="f61c5-135">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="f61c5-136">További információt az [Azure Blob Storage: Hot and cool Storage Tiers](http://go.microsoft.com/fwlink/?LinkId=786482)című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="f61c5-136">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="f61c5-137">Ha a tárolási fióknak van olyan típusa, mint StorageV2 vagy BlobStorage, megadhatja a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="f61c5-137">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="f61c5-138">Ha a tárolási fióknak van tárterülete, ne adja meg a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="f61c5-138">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="f61c5-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f61c5-139">-AsJob</span></span>
<span data-ttu-id="f61c5-140">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f61c5-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f61c5-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f61c5-141">-AssignIdentity</span></span>
<span data-ttu-id="f61c5-142">Új tárolási fiók identitásának létrehozása és hozzárendelése ehhez a tárterülethez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="f61c5-142">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="f61c5-143">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="f61c5-143">-CustomDomainName</span></span>
<span data-ttu-id="f61c5-144">Az egyéni tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f61c5-144">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="f61c5-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f61c5-145">-DefaultProfile</span></span>
<span data-ttu-id="f61c5-146">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f61c5-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f61c5-147">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="f61c5-147">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="f61c5-148">Engedélyezze az Azure-fájlok Azure Active Directory tartományi szolgáltatás általi hitelesítését a tárolási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f61c5-148">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="f61c5-149">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="f61c5-149">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="f61c5-150">Azt jelzi, hogy a tárolási fiók csak HTTPS-forgalmat engedélyez-e.</span><span class="sxs-lookup"><span data-stu-id="f61c5-150">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="f61c5-151">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="f61c5-151">-EnableLargeFileShare</span></span>
<span data-ttu-id="f61c5-152">Azt jelzi, hogy a tárolási fiók támogatja-e az 5 TiB-nál több kapacitással rendelkező nagyméretű fájlmegosztás használatát.</span><span class="sxs-lookup"><span data-stu-id="f61c5-152">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="f61c5-153">Miután a fiók engedélyezve van, a funkció nem tiltható le.</span><span class="sxs-lookup"><span data-stu-id="f61c5-153">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="f61c5-154">Jelenleg csak a LRS és a ZRS replikációs típusai támogatottak, ezért nem lehetett beírni a "geo-redundáns fiókok" konverzióját.</span><span class="sxs-lookup"><span data-stu-id="f61c5-154">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="f61c5-155">További információ https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="f61c5-155">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="f61c5-156">-Force</span><span class="sxs-lookup"><span data-stu-id="f61c5-156">-Force</span></span>
<span data-ttu-id="f61c5-157">Kényszeríti a módosítást a tárolási fiókba.</span><span class="sxs-lookup"><span data-stu-id="f61c5-157">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="f61c5-158">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="f61c5-158">-KeyName</span></span>
<span data-ttu-id="f61c5-159">Ha a KeyvaultEncryption lehetővé teszi a titkosítást a kulcsfájl segítségével, adja meg a kulcsnév tulajdonságot ezzel a beállítással.</span><span class="sxs-lookup"><span data-stu-id="f61c5-159">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="f61c5-160">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="f61c5-160">-KeyvaultEncryption</span></span>
<span data-ttu-id="f61c5-161">Azt jelzi, hogy a Microsoft-billentyűzetet szeretné-e használni a titkosítási kulcsokhoz a tárterület-titkosítási szolgáltatás használatakor.</span><span class="sxs-lookup"><span data-stu-id="f61c5-161">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="f61c5-162">Ha a kulcsnév, a saját verzió és a KeyVaultUri mind készlet, a program a forráskódot a Microsoft. vagy a parancsra állítja be, hogy ez a paraméter be van-e állítva.</span><span class="sxs-lookup"><span data-stu-id="f61c5-162">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="f61c5-163">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="f61c5-163">-KeyVaultUri</span></span>
<span data-ttu-id="f61c5-164">Ha a-KeyvaultEncryption paraméter megadásával használja a Key Vault-titkosítást, ezzel a beállítással megadhatja az URI-azonosítót a kulcs Boltozatához.</span><span class="sxs-lookup"><span data-stu-id="f61c5-164">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="f61c5-165">-Verzió</span><span class="sxs-lookup"><span data-stu-id="f61c5-165">-KeyVersion</span></span>
<span data-ttu-id="f61c5-166">Ha a-KeyvaultEncryption paraméter megadásával használja a Key Vault-titkosítást, akkor ezzel a beállítással megadhatja az URI-azonosító értékét a kulcs verziójában.</span><span class="sxs-lookup"><span data-stu-id="f61c5-166">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="f61c5-167">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f61c5-167">-Name</span></span>
<span data-ttu-id="f61c5-168">A módosítani kívánt tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f61c5-168">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="f61c5-169">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f61c5-169">-NetworkRuleSet</span></span>
<span data-ttu-id="f61c5-170">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé tevő, valamint a meghatározott szabályoknak nem megfelelő kérelmek kezelésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f61c5-170">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="f61c5-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f61c5-171">-ResourceGroupName</span></span>
<span data-ttu-id="f61c5-172">Annak az erőforrás-csoportnak a nevét adja meg, amelybe a tárolási fiókot módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="f61c5-172">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="f61c5-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f61c5-173">-SkuName</span></span>
<span data-ttu-id="f61c5-174">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="f61c5-174">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="f61c5-175">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f61c5-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f61c5-176">Standard_LRS-lokálisan redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="f61c5-176">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="f61c5-177">Standard_ZRS-zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="f61c5-177">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="f61c5-178">Standard_GRS-geo-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="f61c5-178">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="f61c5-179">Standard_RAGRS-olvasási hozzáférés: Geo-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="f61c5-179">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="f61c5-180">Premium_LRS-prémium helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="f61c5-180">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="f61c5-181">Standard_GZRS-geo-redundáns zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="f61c5-181">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="f61c5-182">Standard_RAGZRS – az Access geo-redundáns zónája – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="f61c5-182">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="f61c5-183">A Standard_ZRS és a Premium_LRS típusokat nem lehet más típusú fiókokra módosítani.</span><span class="sxs-lookup"><span data-stu-id="f61c5-183">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="f61c5-184">Más típusú fiókokat nem módosíthat Standard_ZRS vagy Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="f61c5-184">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="f61c5-185">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="f61c5-185">-StorageEncryption</span></span>
<span data-ttu-id="f61c5-186">Azt jelzi, hogy a tárterület-titkosítás a Microsoft által felügyelt kulcsok használatára van-e beállítva.</span><span class="sxs-lookup"><span data-stu-id="f61c5-186">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="f61c5-187">-Címke</span><span class="sxs-lookup"><span data-stu-id="f61c5-187">-Tag</span></span>
<span data-ttu-id="f61c5-188">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="f61c5-188">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="f61c5-189">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="f61c5-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f61c5-190">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="f61c5-190">-UpgradeToStorageV2</span></span>
<span data-ttu-id="f61c5-191">Frissítse a tárterületet a tárterületről vagy a BlobStorage a StorageV2-ra.</span><span class="sxs-lookup"><span data-stu-id="f61c5-191">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="f61c5-192">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="f61c5-192">-UseSubDomain</span></span>
<span data-ttu-id="f61c5-193">Azt jelzi, hogy engedélyezi-e a közvetlen CName érvényesítést.</span><span class="sxs-lookup"><span data-stu-id="f61c5-193">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="f61c5-194">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f61c5-194">-Confirm</span></span>
<span data-ttu-id="f61c5-195">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f61c5-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f61c5-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f61c5-196">-WhatIf</span></span>
<span data-ttu-id="f61c5-197">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f61c5-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f61c5-198">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f61c5-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f61c5-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f61c5-199">CommonParameters</span></span>
<span data-ttu-id="f61c5-200">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f61c5-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f61c5-201">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f61c5-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f61c5-202">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f61c5-202">INPUTS</span></span>

### <span data-ttu-id="f61c5-203">System. String</span><span class="sxs-lookup"><span data-stu-id="f61c5-203">System.String</span></span>

### <span data-ttu-id="f61c5-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f61c5-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f61c5-205">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f61c5-205">OUTPUTS</span></span>

### <span data-ttu-id="f61c5-206">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f61c5-206">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f61c5-207">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f61c5-207">NOTES</span></span>

## <span data-ttu-id="f61c5-208">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f61c5-208">RELATED LINKS</span></span>

[<span data-ttu-id="f61c5-209">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f61c5-209">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="f61c5-210">Új – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f61c5-210">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="f61c5-211">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f61c5-211">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
