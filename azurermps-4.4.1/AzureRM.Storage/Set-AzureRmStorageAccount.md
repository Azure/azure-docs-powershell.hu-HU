---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 5ca65c09746f6bb9a050c14fe10987702465b484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496791"
---
# <span data-ttu-id="83563-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83563-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="83563-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83563-102">SYNOPSIS</span></span>
<span data-ttu-id="83563-103">Módosítja a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="83563-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83563-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83563-104">SYNTAX</span></span>

### <span data-ttu-id="83563-105">StorageEncryption (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83563-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83563-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="83563-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83563-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="83563-107">DESCRIPTION</span></span>
<span data-ttu-id="83563-108">A **set-AzureRmStorageAccount** parancsmag az Azure Storage-fiókot módosítja.</span><span class="sxs-lookup"><span data-stu-id="83563-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="83563-109">Ezzel a parancsmaggal módosíthatja a fiók típusát, frissítheti az ügyfél tartományát, és beállíthatja a címkéket egy tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="83563-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="83563-110">Példák</span><span class="sxs-lookup"><span data-stu-id="83563-110">EXAMPLES</span></span>

### <span data-ttu-id="83563-111">Példa 1: a tárolási fiók típusának beállítása</span><span class="sxs-lookup"><span data-stu-id="83563-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="83563-112">Ez a parancs a tárterület-típust a Standard_RAGRS értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="83563-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="83563-113">2. példa: egyéni tartomány beállítása tárterület-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="83563-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="83563-114">Ez a parancs egy egyéni tartományt állít be egy tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="83563-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="83563-115">3. példa: a titkosítás engedélyezése a blob-és Fájlszolgáltatások esetén</span><span class="sxs-lookup"><span data-stu-id="83563-115">Example 3: Enable encryption on Blob and File Services</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

<span data-ttu-id="83563-116">Ez a parancs lehetővé teszi a tárterület-titkosítást a blobon és a fájlon egy tároló fiók esetén.</span><span class="sxs-lookup"><span data-stu-id="83563-116">This command enables Storage Service encryption on Blob and File for a Storage account.</span></span>

### <span data-ttu-id="83563-117">4. példa: az Access-Tier értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="83563-117">Example 4: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

<span data-ttu-id="83563-118">A parancs az Access-réteg értékét kihűlni állítja.</span><span class="sxs-lookup"><span data-stu-id="83563-118">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="83563-119">4. példa: egyéni tartomány és címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="83563-119">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="83563-120">A parancs az Access-réteg értékét kihűlni állítja.</span><span class="sxs-lookup"><span data-stu-id="83563-120">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="83563-121">5. példa: a blob-szolgáltatásokhoz tartozó titkosítás engedélyezése a főboltozattal</span><span class="sxs-lookup"><span data-stu-id="83563-121">Example 5: Enable encryption on Blob Services with Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="83563-122">Ez a parancs lehetővé teszi a tárterület-titkosítást a blob-ban egy új, létrehozott főboltozattal.</span><span class="sxs-lookup"><span data-stu-id="83563-122">This command enables Storage Service encryption on Blob with a new created Keyvault.</span></span>

### <span data-ttu-id="83563-123">6. példa: a fájlkezelők titkosítási funkciójának letiltása a "Microsoft. Storage" forráskód beállítással</span><span class="sxs-lookup"><span data-stu-id="83563-123">Example 6: Disable encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

<span data-ttu-id="83563-124">Ez a parancs letiltja a fájlkezelők titkosítását a "Microsoft. Storage" beállítással.</span><span class="sxs-lookup"><span data-stu-id="83563-124">This command disables encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>

## <span data-ttu-id="83563-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83563-125">PARAMETERS</span></span>

### <span data-ttu-id="83563-126">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="83563-126">-AccessTier</span></span>
<span data-ttu-id="83563-127">Annak a tárolási fióknak az Access-rétegét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="83563-127">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="83563-128">A paraméter elfogadható értékei a következők: meleg és hűvös.</span><span class="sxs-lookup"><span data-stu-id="83563-128">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="83563-129">Ha módosítja a hozzáférési szintet, az esetleg további díjakat is eredményezhet.</span><span class="sxs-lookup"><span data-stu-id="83563-129">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="83563-130">További információ: Azure Blob-tároló: Hot and cool Storage Tiers https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="83563-130">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="83563-131">Ha a tárolási fiók típusa tárterület, ne adja meg ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="83563-131">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83563-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="83563-132">-AssignIdentity</span></span>
<span data-ttu-id="83563-133">Új tárolási fiók identitásának létrehozása és hozzárendelése ehhez a tárterülethez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="83563-133">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="83563-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="83563-134">-CustomDomainName</span></span>
<span data-ttu-id="83563-135">Az egyéni tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="83563-135">Specifies the name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83563-136">-DisableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="83563-136">-DisableEncryptionService</span></span>
<span data-ttu-id="83563-137">Azt jelzi, hogy ez a parancsmag letiltja-e a tárterület-titkosítási szolgáltatást a tárterületen.</span><span class="sxs-lookup"><span data-stu-id="83563-137">Indicates whether this cmdlet disables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="83563-138">Az Azure Blob és az Azure file Services támogatott.</span><span class="sxs-lookup"><span data-stu-id="83563-138">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83563-139">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="83563-139">-EnableEncryptionService</span></span>
<span data-ttu-id="83563-140">Azt jelzi, hogy ez a parancsmag engedélyezi-e a tárterület-titkosítási szolgáltatást a tárterületen.</span><span class="sxs-lookup"><span data-stu-id="83563-140">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="83563-141">Az Azure Blob és az Azure file Services támogatott.</span><span class="sxs-lookup"><span data-stu-id="83563-141">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83563-142">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="83563-142">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="83563-143">Azt jelzi, hogy a tárolási fiók csak HTTPS-forgalmat engedélyez-e.</span><span class="sxs-lookup"><span data-stu-id="83563-143">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83563-144">-Force</span><span class="sxs-lookup"><span data-stu-id="83563-144">-Force</span></span>
<span data-ttu-id="83563-145">Ha módosítja a hozzáférési szintet, az esetleg további díjakat is eredményezhet.</span><span class="sxs-lookup"><span data-stu-id="83563-145">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="83563-146">További információ: Azure Blob-tároló: Hot and cool Storage Tiers https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="83563-146">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="83563-147">Ha a tárolási fiók típusa tárterület, ne adja meg ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="83563-147">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="83563-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="83563-148">-InformationAction</span></span>
<span data-ttu-id="83563-149">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="83563-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="83563-150">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="83563-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83563-151">Folytassa</span><span class="sxs-lookup"><span data-stu-id="83563-151">Continue</span></span>
- <span data-ttu-id="83563-152">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="83563-152">Ignore</span></span>
- <span data-ttu-id="83563-153">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="83563-153">Inquire</span></span>
- <span data-ttu-id="83563-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="83563-154">SilentlyContinue</span></span>
- <span data-ttu-id="83563-155">állj</span><span class="sxs-lookup"><span data-stu-id="83563-155">Stop</span></span>
- <span data-ttu-id="83563-156">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="83563-156">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83563-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="83563-157">-InformationVariable</span></span>
<span data-ttu-id="83563-158">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="83563-158">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83563-159">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="83563-159">-KeyName</span></span>
<span data-ttu-id="83563-160">Tárterület-titkosítási forrás</span><span class="sxs-lookup"><span data-stu-id="83563-160">Storage Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="83563-161">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="83563-161">-KeyvaultEncryption</span></span>
<span data-ttu-id="83563-162">Adja meg, hogy a tárterület-titkosítási forrást szeretné-e beállítani a Microsoft. vagy a kiindulási fiókban.</span><span class="sxs-lookup"><span data-stu-id="83563-162">Whether to set Storage Account Encryption KeySource to Microsoft.Keyvault or not.</span></span> <span data-ttu-id="83563-163">Ha a kulcsnév, a verziószám és a KeyvaultUri megadását adja meg, akkor a tárterület-titkosítási forrás is a Microsoft.-boltozatos időjárási értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="83563-163">If you specify KeyName, KeyVersion and KeyvaultUri, Storage Account encryption keySource will also be set to Microsoft.Keyvault weather this parameter is set or not.</span></span>
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

### <span data-ttu-id="83563-164">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="83563-164">-KeyVaultUri</span></span>
<span data-ttu-id="83563-165">Tárterület-titkosítási forrás KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="83563-165">Storage Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="83563-166">-Verzió</span><span class="sxs-lookup"><span data-stu-id="83563-166">-KeyVersion</span></span>
<span data-ttu-id="83563-167">Tárolási fiók titkosítása</span><span class="sxs-lookup"><span data-stu-id="83563-167">Storage Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="83563-168">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83563-168">-Name</span></span>
<span data-ttu-id="83563-169">A módosítani kívánt tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="83563-169">Specifies the name of the Storage account to Modify.</span></span>

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

### <span data-ttu-id="83563-170">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="83563-170">-NetworkRuleSet</span></span>
<span data-ttu-id="83563-171">Tárolási fiók NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="83563-171">Storage Account NetworkRuleSet</span></span>

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

### <span data-ttu-id="83563-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83563-172">-ResourceGroupName</span></span>
<span data-ttu-id="83563-173">Annak az erőforrás-csoportnak a nevét adja meg, amelybe a tárolási fiókot módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="83563-173">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="83563-174">-SkuName</span><span class="sxs-lookup"><span data-stu-id="83563-174">-SkuName</span></span>
<span data-ttu-id="83563-175">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="83563-175">Specifies the SKU name of the storage account.</span></span>
<span data-ttu-id="83563-176">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="83563-176">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83563-177">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="83563-177">Standard_LRS.</span></span>
<span data-ttu-id="83563-178">Helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="83563-178">Locally-redundant storage.</span></span> 
- <span data-ttu-id="83563-179">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="83563-179">Standard_ZRS.</span></span>
<span data-ttu-id="83563-180">Zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="83563-180">Zone-redundant storage.</span></span>
- <span data-ttu-id="83563-181">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="83563-181">Standard_GRS.</span></span>
<span data-ttu-id="83563-182">Geo-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="83563-182">Geo-redundant storage.</span></span> 
- <span data-ttu-id="83563-183">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="83563-183">Standard_RAGRS.</span></span>
<span data-ttu-id="83563-184">Olvassa el az Access geo-redundáns tárterülete című témakört.</span><span class="sxs-lookup"><span data-stu-id="83563-184">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="83563-185">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="83563-185">Premium_LRS.</span></span>
<span data-ttu-id="83563-186">Prémium lokálisan redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="83563-186">Premium locally-redundant storage.</span></span>

<span data-ttu-id="83563-187">A Standard_ZRS és a Premium_LRS típusokat nem lehet más típusú fiókokra módosítani.</span><span class="sxs-lookup"><span data-stu-id="83563-187">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="83563-188">Más típusú fiókokat nem módosíthat Standard_ZRS vagy Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="83563-188">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83563-189">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="83563-189">-StorageEncryption</span></span>
<span data-ttu-id="83563-190">Adja meg, hogy a tárterület-titkosítási forrást szeretné-e beállítani a Microsoft. Storage-ba vagy sem.</span><span class="sxs-lookup"><span data-stu-id="83563-190">Whether to set Storage Account Encryption KeySource to Microsoft.Storage or not.</span></span>

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

### <span data-ttu-id="83563-191">-Címke</span><span class="sxs-lookup"><span data-stu-id="83563-191">-Tag</span></span>
<span data-ttu-id="83563-192">Ha a BlobStorage értékét adja meg az New-AzureRmStorageAccount parancsmag *Kind* paraméteréhez, meg kell adnia a *AccessTier* paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="83563-192">If you specify a value of BlobStorage for the *Kind* parameter of the New-AzureRmStorageAccount cmdlet, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="83563-193">Ha *a tárterület* értékére vonatkozó értéket ad meg, ne adja meg a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="83563-193">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83563-194">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="83563-194">-UseSubDomain</span></span>
<span data-ttu-id="83563-195">Azt jelzi, hogy engedélyezi-e a közvetlen CName érvényesítést.</span><span class="sxs-lookup"><span data-stu-id="83563-195">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83563-196">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83563-196">-Confirm</span></span>
<span data-ttu-id="83563-197">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83563-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83563-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83563-198">-WhatIf</span></span>
<span data-ttu-id="83563-199">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83563-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83563-200">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83563-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83563-201">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83563-201">-DefaultProfile</span></span>
<span data-ttu-id="83563-202">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83563-202">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83563-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83563-203">CommonParameters</span></span>
<span data-ttu-id="83563-204">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83563-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83563-205">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83563-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83563-206">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83563-206">INPUTS</span></span>

## <span data-ttu-id="83563-207">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83563-207">OUTPUTS</span></span>

## <span data-ttu-id="83563-208">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83563-208">NOTES</span></span>

## <span data-ttu-id="83563-209">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83563-209">RELATED LINKS</span></span>

[<span data-ttu-id="83563-210">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83563-210">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="83563-211">Új – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83563-211">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="83563-212">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83563-212">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)


