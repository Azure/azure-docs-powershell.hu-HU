---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 18b87f6a83f335958e9c10e392d859ae307e9e87
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361701"
---
# <span data-ttu-id="6a089-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6a089-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="6a089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a089-102">SYNOPSIS</span></span>
<span data-ttu-id="6a089-103">Egy kulcstárban rejti el a titkos kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="6a089-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="6a089-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a089-104">SYNTAX</span></span>

### <span data-ttu-id="6a089-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a089-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a089-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="6a089-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a089-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="6a089-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a089-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="6a089-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a089-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="6a089-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a089-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="6a089-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a089-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="6a089-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a089-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="6a089-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a089-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="6a089-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a089-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a089-114">DESCRIPTION</span></span>
<span data-ttu-id="6a089-115">A **Get-AzKeyVaultSecret** parancsmag titkosságokat kap egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="6a089-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="6a089-116">Ez a parancsmag egy adott vagy az összes titkos kulcsot kap egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="6a089-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="6a089-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a089-117">EXAMPLES</span></span>

### <span data-ttu-id="6a089-118">1. példa: Az összes titkos kulcs aktuális verziójának be szereznie egy kulcstárban</span><span class="sxs-lookup"><span data-stu-id="6a089-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="6a089-119">Ez a parancs a Contoso nevű kulcstár összes titka aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6a089-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="6a089-120">2. példa: Egy adott titkos termék összes verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="6a089-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="6a089-121">Ez a parancs a Contoso nevű kulcstárba bekérte a Titkos1 nevű titkos kulcs összes verzióját.</span><span class="sxs-lookup"><span data-stu-id="6a089-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="6a089-122">3. példa: Adott titkos termék aktuális verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="6a089-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="6a089-123">Ez a parancs a Contoso nevű kulcstárban megkapja a Titkos1 nevű titkos kulcs aktuális verzióját.</span><span class="sxs-lookup"><span data-stu-id="6a089-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="6a089-124">4. példa: Egy adott titkos termék adott verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="6a089-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="6a089-125">Ez a parancs a Contoso nevű kulcstárban a Titkos1 nevű titkos kulcs adott verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6a089-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="6a089-126">5. példa: Adott titkos termék aktuális verziójának egyszerű szöveges értéke</span><span class="sxs-lookup"><span data-stu-id="6a089-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'

# Method 1: requires PowerShell >= 7.0
PS C:\> $secretInPlainText = $secret.SecretValue | ConvertFrom-SecureString -AsPlainText

# Method 2: works on older PowerShell versions
PS C:\> $secretValueText = '';
PS C:\> $ssPtr = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue)
PS C:\> try {
    $secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR($ssPtr)
} finally {
    [System.Runtime.InteropServices.Marshal]::ZeroFreeBSTR($ssPtr)
}

# Method 3: works in ConstrainedLanguage mode
$secretInPlainText = [pscredential]::new("DoesntMatter", $secret.SecretValue).GetNetworkCredential().Password
```

<span data-ttu-id="6a089-127">Ezek a parancsok az ITSecret nevű titkos parancs aktuális verzióját jelenítik meg, majd megjeleníti a titkos érték egyszerű szöveges értékét.</span><span class="sxs-lookup"><span data-stu-id="6a089-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

<span data-ttu-id="6a089-128">(Megjegyzés: használja a 3. módszert, ha PowerShell [ConstrainedLanguage](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_language_modes?view=powershell-7.1#constrained-language-constrained-language)módban dolgozik, például biztonságos/jogosultsággal rendelkező hozzáférésű munkaállomásokon.)</span><span class="sxs-lookup"><span data-stu-id="6a089-128">(Note: use method 3 if you are working in PowerShell [ConstrainedLanguage mode](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_language_modes?view=powershell-7.1#constrained-language-constrained-language), for example, on secure/privileged access workstations.)</span></span>

### <span data-ttu-id="6a089-129">6. példa: Szerezze be az ebben a kulcstárban törölt, de nem véglegesen törölt összes titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="6a089-129">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="6a089-130">Ez a parancs a Contoso nevű kulcstárban megkapja a korábban törölt, de véglegesen nem véglegesen törölt összes titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="6a089-130">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="6a089-131">7. példa: A kulcstárból törölt, de nem véglegesen törölt titkos ITSecret.</span><span class="sxs-lookup"><span data-stu-id="6a089-131">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="6a089-132">Ez a parancs a Contoso nevű kulcstárban megkapja a korábban törölt, de nem véglegesen törölt "titkos1" titkos adatokat.</span><span class="sxs-lookup"><span data-stu-id="6a089-132">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="6a089-133">Ez a parancs metaadatokat, például törlési dátumot és a törölt titkos fájl ütemezett végleges végleges törlésének dátumát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="6a089-133">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="6a089-134">8. példa: Az összes titkos kulcs aktuális verziójának be szereznie egy kulcstárban szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="6a089-134">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name "secret*"

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="6a089-135">Ez a parancs a Contoso nevű kulcstár minden olyan titka aktuális verzióját beveszi, amely a "titkos" kezdetű.</span><span class="sxs-lookup"><span data-stu-id="6a089-135">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="6a089-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a089-136">PARAMETERS</span></span>

### <span data-ttu-id="6a089-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a089-137">-DefaultProfile</span></span>
<span data-ttu-id="6a089-138">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6a089-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a089-139">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="6a089-139">-IncludeVersions</span></span>
<span data-ttu-id="6a089-140">Azt jelzi, hogy ez a parancsmag egy titkos parancsmag összes verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="6a089-140">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="6a089-141">A titkos adatok aktuális verziója az első a listában.</span><span class="sxs-lookup"><span data-stu-id="6a089-141">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="6a089-142">Ha ezt a paramétert adja meg, a *Name* és *a VaultName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="6a089-142">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="6a089-143">Ha nem adja meg az *IncludeVersions* paramétert, ez a parancsmag a megadott névvel megkapja a titkos fájl aktuális *verzióját.*</span><span class="sxs-lookup"><span data-stu-id="6a089-143">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a089-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a089-144">-InputObject</span></span>
<span data-ttu-id="6a089-145">KeyVault objektum.</span><span class="sxs-lookup"><span data-stu-id="6a089-145">KeyVault Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a089-146">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="6a089-146">-InRemovedState</span></span>
<span data-ttu-id="6a089-147">Azt adja meg, hogy a kimenetben meg legyenek-e mutatja a korábban törölt titkos adatokat.</span><span class="sxs-lookup"><span data-stu-id="6a089-147">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a089-148">-Name</span><span class="sxs-lookup"><span data-stu-id="6a089-148">-Name</span></span>
<span data-ttu-id="6a089-149">A lekért titkos elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a089-149">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6a089-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a089-150">-ResourceId</span></span>
<span data-ttu-id="6a089-151">KeyVault-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a089-151">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a089-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6a089-152">-VaultName</span></span>
<span data-ttu-id="6a089-153">Annak a kulcstárnak a nevét adja meg, amelyhez a titkos kulcs tartozik.</span><span class="sxs-lookup"><span data-stu-id="6a089-153">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="6a089-154">Ez a parancsmag egy kulcstár teljes tartománynevét (FQDN) építi fel a paraméter által megadott név és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="6a089-154">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a089-155">-Version</span><span class="sxs-lookup"><span data-stu-id="6a089-155">-Version</span></span>
<span data-ttu-id="6a089-156">A titkos verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a089-156">Specifies the secret version.</span></span>
<span data-ttu-id="6a089-157">Ez a parancsmag a kulcstár neve, az aktuálisan kiválasztott környezet, a titkos név és a titkos verzió alapján építi fel egy titkos kulcs teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="6a089-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a089-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a089-158">CommonParameters</span></span>
<span data-ttu-id="6a089-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a089-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a089-160">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a089-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a089-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a089-161">INPUTS</span></span>

### <span data-ttu-id="6a089-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6a089-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="6a089-163">System.String</span><span class="sxs-lookup"><span data-stu-id="6a089-163">System.String</span></span>

## <span data-ttu-id="6a089-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a089-164">OUTPUTS</span></span>

### <span data-ttu-id="6a089-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6a089-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="6a089-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6a089-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="6a089-167">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6a089-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="6a089-168">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6a089-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="6a089-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a089-169">NOTES</span></span>

## <span data-ttu-id="6a089-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a089-170">RELATED LINKS</span></span>

[<span data-ttu-id="6a089-171">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6a089-171">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="6a089-172">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="6a089-172">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="6a089-173">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6a089-173">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

