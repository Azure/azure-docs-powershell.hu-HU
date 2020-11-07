---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: a6f16c4ef9012f7aaf5216e0cfb24edf65ce9f4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848978"
---
# <span data-ttu-id="3f4aa-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f4aa-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="3f4aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4aa-103">Módosítja a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f4aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f4aa-104">SYNTAX</span></span>

### <span data-ttu-id="3f4aa-105">StorageEncryption (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f4aa-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4aa-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="3f4aa-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f4aa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f4aa-107">DESCRIPTION</span></span>
<span data-ttu-id="3f4aa-108">A **set-AzureRmStorageAccount** parancsmag az Azure Storage-fiókot módosítja.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="3f4aa-109">Ezzel a parancsmaggal módosíthatja a fiók típusát, frissítheti az ügyfél tartományát, és beállíthatja a címkéket egy tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="3f4aa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3f4aa-110">EXAMPLES</span></span>

### <span data-ttu-id="3f4aa-111">Példa 1: a tárolási fiók típusának beállítása</span><span class="sxs-lookup"><span data-stu-id="3f4aa-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="3f4aa-112">Ez a parancs a tárterület-típust a Standard_RAGRS értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="3f4aa-113">2. példa: egyéni tartomány beállítása tárterület-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="3f4aa-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="3f4aa-114">Ez a parancs egy egyéni tartományt állít be egy tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="3f4aa-115">3. példa: az Access-szint értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="3f4aa-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="3f4aa-116">A parancs az Access-réteg értékét kihűlni állítja.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="3f4aa-117">4. példa: egyéni tartomány és címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="3f4aa-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="3f4aa-118">A parancs a tárolási fiók egyéni tartományát és címkéit állítja be.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="3f4aa-119">Példa 5: titkosítási forrás beállítása a következőre</span><span class="sxs-lookup"><span data-stu-id="3f4aa-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="3f4aa-120">Ez a parancs a titkosító jelforrásokat egy új, új, létrehozott főboltozattal állítja be.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="3f4aa-121">6. példa: a titkosítási forrás beállítása a következőre: "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="3f4aa-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="3f4aa-122">Ez a parancs a titkosító jelforrást a "Microsoft. Storage" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="3f4aa-123">7. példa: tárolási fiók NetworkRuleSet tulajdonságának beállítása JSON-val</span><span class="sxs-lookup"><span data-stu-id="3f4aa-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="3f4aa-124">Ez a parancs a JSON-NetworkRuleSet tulajdonságát állítja be.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="3f4aa-125">8. példa: a NetworkRuleSet tulajdonság beolvasása egy tárterület-fiókból, és beállítása másik tárolási fiókra</span><span class="sxs-lookup"><span data-stu-id="3f4aa-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="3f4aa-126">Ez az első parancs egy tárterület-fiókból kapja a NetworkRuleSet tulajdonságot, és a második parancs másik tárolási fiókra állítja be.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="3f4aa-127">9. példa: a "tárterület" vagy a "BlobStorage" típusú tárolási fiók frissítése "StorageV2" típusú tárterületre</span><span class="sxs-lookup"><span data-stu-id="3f4aa-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="3f4aa-128">A parancs "tárterület" vagy "BlobStorage" típusú tárterületet frissít a "StorageV2" típusú tárterület-tárolási fiókra.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

## <span data-ttu-id="3f4aa-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f4aa-129">PARAMETERS</span></span>

### <span data-ttu-id="3f4aa-130">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="3f4aa-130">-AccessTier</span></span>
<span data-ttu-id="3f4aa-131">Annak a tárolási fióknak az Access-rétegét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-131">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="3f4aa-132">A paraméter elfogadható értékei a következők: meleg és hűvös.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-132">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="3f4aa-133">Ha módosítja a hozzáférési szintet, az esetleg további díjakat is eredményezhet.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-133">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="3f4aa-134">További információt az [Azure Blob Storage: Hot and cool Storage Tiers](https://go.microsoft.com/fwlink/?LinkId=786482)című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-134">For more information, see [Azure Blob Storage: Hot and cool storage tiers](https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="3f4aa-135">Ha a tárolási fióknak van olyan típusa, mint StorageV2 vagy BlobStorage, megadhatja a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-135">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="3f4aa-136">Ha a tárolási fióknak van tárterülete, ne adja meg a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-136">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="3f4aa-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f4aa-137">-AsJob</span></span>
<span data-ttu-id="3f4aa-138">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3f4aa-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f4aa-139">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3f4aa-139">-AssignIdentity</span></span>
<span data-ttu-id="3f4aa-140">Új tárolási fiók identitásának létrehozása és hozzárendelése ehhez a tárterülethez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-140">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3f4aa-141">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="3f4aa-141">-CustomDomainName</span></span>
<span data-ttu-id="3f4aa-142">Az egyéni tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-142">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="3f4aa-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4aa-143">-DefaultProfile</span></span>
<span data-ttu-id="3f4aa-144">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f4aa-145">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="3f4aa-145">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="3f4aa-146">Azt jelzi, hogy a tárolási fiók csak HTTPS-forgalmat engedélyez-e.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-146">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="3f4aa-147">-Force</span><span class="sxs-lookup"><span data-stu-id="3f4aa-147">-Force</span></span>
<span data-ttu-id="3f4aa-148">Kényszeríti a módosítást a tárolási fiókba.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-148">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="3f4aa-149">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="3f4aa-149">-KeyName</span></span>
<span data-ttu-id="3f4aa-150">Ha a KeyvaultEncryption lehetővé teszi a titkosítást a kulcsfájl segítségével, adja meg a kulcsnév tulajdonságot ezzel a beállítással.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-150">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="3f4aa-151">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="3f4aa-151">-KeyvaultEncryption</span></span>
<span data-ttu-id="3f4aa-152">Azt jelzi, hogy a Microsoft-billentyűzetet szeretné-e használni a titkosítási kulcsokhoz a tárterület-titkosítási szolgáltatás használatakor.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-152">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="3f4aa-153">Ha a kulcsnév, a saját verzió és a KeyVaultUri mind készlet, a program a forráskódot a Microsoft. vagy a parancsra állítja be, hogy ez a paraméter be van-e állítva.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-153">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="3f4aa-154">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="3f4aa-154">-KeyVaultUri</span></span>
<span data-ttu-id="3f4aa-155">Ha a-KeyvaultEncryption paraméter megadásával használja a Key Vault-titkosítást, ezzel a beállítással megadhatja az URI-azonosítót a kulcs Boltozatához.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-155">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="3f4aa-156">-Verzió</span><span class="sxs-lookup"><span data-stu-id="3f4aa-156">-KeyVersion</span></span>
<span data-ttu-id="3f4aa-157">Ha a-KeyvaultEncryption paraméter megadásával használja a Key Vault-titkosítást, akkor ezzel a beállítással megadhatja az URI-azonosító értékét a kulcs verziójában.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-157">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="3f4aa-158">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f4aa-158">-Name</span></span>
<span data-ttu-id="3f4aa-159">A módosítani kívánt tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-159">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="3f4aa-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f4aa-160">-NetworkRuleSet</span></span>
<span data-ttu-id="3f4aa-161">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé tevő, valamint a meghatározott szabályoknak nem megfelelő kérelmek kezelésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="3f4aa-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4aa-162">-ResourceGroupName</span></span>
<span data-ttu-id="3f4aa-163">Annak az erőforrás-csoportnak a nevét adja meg, amelybe a tárolási fiókot módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-163">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="3f4aa-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3f4aa-164">-SkuName</span></span>
<span data-ttu-id="3f4aa-165">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-165">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="3f4aa-166">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3f4aa-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3f4aa-167">Standard_LRS-lokálisan redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-167">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="3f4aa-168">Standard_ZRS-zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-168">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="3f4aa-169">Standard_GRS-geo-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-169">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="3f4aa-170">Standard_RAGRS-olvasási hozzáférés: Geo-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-170">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="3f4aa-171">Premium_LRS-prémium helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-171">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="3f4aa-172">A Standard_ZRS és a Premium_LRS típusokat nem lehet más típusú fiókokra módosítani.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-172">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="3f4aa-173">Más típusú fiókokat nem módosíthat Standard_ZRS vagy Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-173">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4aa-174">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="3f4aa-174">-StorageEncryption</span></span>
<span data-ttu-id="3f4aa-175">Azt jelzi, hogy a tárterület-titkosítás a Microsoft által felügyelt kulcsok használatára van-e beállítva.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-175">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="3f4aa-176">-Címke</span><span class="sxs-lookup"><span data-stu-id="3f4aa-176">-Tag</span></span>
<span data-ttu-id="3f4aa-177">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-177">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="3f4aa-178">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3f4aa-178">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3f4aa-179">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="3f4aa-179">-UpgradeToStorageV2</span></span>
<span data-ttu-id="3f4aa-180">Frissítse a tárterületet a tárterületről vagy a BlobStorage a StorageV2-ra.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-180">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="3f4aa-181">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="3f4aa-181">-UseSubDomain</span></span>
<span data-ttu-id="3f4aa-182">Azt jelzi, hogy engedélyezi-e a közvetlen CName érvényesítést.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-182">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="3f4aa-183">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f4aa-183">-Confirm</span></span>
<span data-ttu-id="3f4aa-184">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f4aa-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4aa-185">-WhatIf</span></span>
<span data-ttu-id="3f4aa-186">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f4aa-187">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f4aa-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f4aa-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4aa-188">CommonParameters</span></span>
<span data-ttu-id="3f4aa-189">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f4aa-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4aa-190">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f4aa-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4aa-191">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f4aa-191">INPUTS</span></span>

### <span data-ttu-id="3f4aa-192">System. String</span><span class="sxs-lookup"><span data-stu-id="3f4aa-192">System.String</span></span>

### <span data-ttu-id="3f4aa-193">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3f4aa-193">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3f4aa-194">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f4aa-194">System.Boolean</span></span>

## <span data-ttu-id="3f4aa-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f4aa-195">OUTPUTS</span></span>

### <span data-ttu-id="3f4aa-196">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f4aa-196">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="3f4aa-197">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f4aa-197">NOTES</span></span>

## <span data-ttu-id="3f4aa-198">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f4aa-198">RELATED LINKS</span></span>

[<span data-ttu-id="3f4aa-199">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f4aa-199">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="3f4aa-200">Új – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f4aa-200">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="3f4aa-201">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f4aa-201">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)
