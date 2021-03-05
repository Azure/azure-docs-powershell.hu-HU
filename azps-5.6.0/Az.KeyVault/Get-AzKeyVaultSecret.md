---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 361425e7bee88300a196c9ed7ac33fe4db171b8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001414"
---
# <span data-ttu-id="3c469-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3c469-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="3c469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c469-102">SYNOPSIS</span></span>
<span data-ttu-id="3c469-103">Egy kulcstárban rejti el a titkos kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="3c469-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="3c469-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3c469-104">SYNTAX</span></span>

### <span data-ttu-id="3c469-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c469-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c469-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="3c469-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c469-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="3c469-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c469-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="3c469-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c469-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="3c469-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c469-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="3c469-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c469-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="3c469-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c469-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="3c469-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c469-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="3c469-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c469-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3c469-114">DESCRIPTION</span></span>
<span data-ttu-id="3c469-115">A **Get-AzKeyVaultSecret** parancsmag titkosságokat kap egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="3c469-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="3c469-116">Ez a parancsmag egy adott vagy az összes titkos kulcsot kap egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="3c469-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="3c469-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3c469-117">EXAMPLES</span></span>

### <span data-ttu-id="3c469-118">1. példa: Az összes titkos kulcs aktuális verziójának be szereznie egy kulcstárban</span><span class="sxs-lookup"><span data-stu-id="3c469-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
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

<span data-ttu-id="3c469-119">Ez a parancs a Contoso nevű kulcstár összes titka aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3c469-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="3c469-120">2. példa: Egy adott titkos termék összes verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="3c469-120">Example 2: Get all versions of a specific secret</span></span>
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

<span data-ttu-id="3c469-121">Ez a parancs a Contoso nevű kulcstárba bekérte a Titkos1 nevű titkos kulcs összes verzióját.</span><span class="sxs-lookup"><span data-stu-id="3c469-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="3c469-122">3. példa: Adott titkos termék aktuális verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="3c469-122">Example 3: Get the current version of a specific secret</span></span>
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

<span data-ttu-id="3c469-123">Ez a parancs a Contoso nevű kulcstárban megkapja a Titkos1 nevű titkos kulcs aktuális verzióját.</span><span class="sxs-lookup"><span data-stu-id="3c469-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="3c469-124">4. példa: Egy adott titkos termék adott verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="3c469-124">Example 4: Get a specific version of a specific secret</span></span>
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

<span data-ttu-id="3c469-125">Ez a parancs a Contoso nevű kulcstárban a Titkos1 nevű titkos kulcs adott verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3c469-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="3c469-126">5. példa: Adott titkos termék aktuális verziójának egyszerű szöveges értéke</span><span class="sxs-lookup"><span data-stu-id="3c469-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secretText = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -AsPlainText
```

<span data-ttu-id="3c469-127">A parancsmag karakterláncként adja vissza a titkos értéket, `-AsPlainText` ha alkalmazva van.</span><span class="sxs-lookup"><span data-stu-id="3c469-127">The cmdlet returns the secret as a string when `-AsPlainText` is applied.</span></span>

### <span data-ttu-id="3c469-128">6. példa: Szerezze be az ebben a kulcstárban törölt, de nem véglegesen törölt összes titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="3c469-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="3c469-129">Ez a parancs a Contoso nevű kulcstárban megkapja a korábban törölt, de véglegesen nem véglegesen törölt összes titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="3c469-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="3c469-130">7. példa: A kulcstárból törölt, de nem véglegesen törölt titkos ITSecret.</span><span class="sxs-lookup"><span data-stu-id="3c469-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="3c469-131">Ez a parancs a Contoso nevű kulcstárban megkapja a korábban törölt, de nem véglegesen törölt "titkos1" titkos adatokat.</span><span class="sxs-lookup"><span data-stu-id="3c469-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="3c469-132">Ez a parancs metaadatokat, például törlési dátumot és a törölt titkos fájl ütemezett végleges végleges törlésének dátumát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="3c469-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="3c469-133">8. példa: Az összes titkos kulcs aktuális verziójának be szereznie egy kulcstárban szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="3c469-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
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

<span data-ttu-id="3c469-134">Ez a parancs a Contoso nevű kulcstár minden olyan titka aktuális verzióját beveszi, amely a "titkos" kezdetű.</span><span class="sxs-lookup"><span data-stu-id="3c469-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="3c469-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c469-135">PARAMETERS</span></span>

### <span data-ttu-id="3c469-136">-AsPtext</span><span class="sxs-lookup"><span data-stu-id="3c469-136">-AsPlainText</span></span>
<span data-ttu-id="3c469-137">Ha be van állítva, a parancsmag a biztonságos karakterláncban található titkos karakterláncot kimenetként a visszafejtett egyszerű szöveges karakterláncra konvertálja.</span><span class="sxs-lookup"><span data-stu-id="3c469-137">When set, the cmdlet will convert secret in secure string to the decrypted plaintext string as output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, BySecretName, ByInputObjectVaultName, ByInputObjectSecretName, ByResourceIdVaultName, ByResourceIdSecretName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c469-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c469-138">-DefaultProfile</span></span>
<span data-ttu-id="3c469-139">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3c469-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c469-140">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="3c469-140">-IncludeVersions</span></span>
<span data-ttu-id="3c469-141">Azt jelzi, hogy ez a parancsmag egy titkos parancsmag összes verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="3c469-141">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="3c469-142">A titkos adatok aktuális verziója az első a listában.</span><span class="sxs-lookup"><span data-stu-id="3c469-142">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="3c469-143">Ha ezt a paramétert adja meg, a *Name* és *a VaultName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="3c469-143">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="3c469-144">Ha nem adja meg az *IncludeVersions* paramétert, ez a parancsmag a megadott névvel megkapja a titkos fájl aktuális *verzióját.*</span><span class="sxs-lookup"><span data-stu-id="3c469-144">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="3c469-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c469-145">-InputObject</span></span>
<span data-ttu-id="3c469-146">KeyVault objektum.</span><span class="sxs-lookup"><span data-stu-id="3c469-146">KeyVault Object.</span></span>

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

### <span data-ttu-id="3c469-147">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="3c469-147">-InRemovedState</span></span>
<span data-ttu-id="3c469-148">Azt adja meg, hogy a kimenetben meg legyenek-e mutatja a korábban törölt titkos adatokat.</span><span class="sxs-lookup"><span data-stu-id="3c469-148">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="3c469-149">-Name</span><span class="sxs-lookup"><span data-stu-id="3c469-149">-Name</span></span>
<span data-ttu-id="3c469-150">A lekért titkos elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c469-150">Specifies the name of the secret to get.</span></span>

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

### <span data-ttu-id="3c469-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c469-151">-ResourceId</span></span>
<span data-ttu-id="3c469-152">KeyVault-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3c469-152">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="3c469-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3c469-153">-VaultName</span></span>
<span data-ttu-id="3c469-154">Annak a kulcstárnak a nevét adja meg, amelyhez a titkos kulcs tartozik.</span><span class="sxs-lookup"><span data-stu-id="3c469-154">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="3c469-155">Ez a parancsmag egy kulcstár teljes tartománynevét (FQDN) építi fel a paraméter által megadott név és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="3c469-155">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="3c469-156">-Version</span><span class="sxs-lookup"><span data-stu-id="3c469-156">-Version</span></span>
<span data-ttu-id="3c469-157">A titkos verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c469-157">Specifies the secret version.</span></span>
<span data-ttu-id="3c469-158">Ez a parancsmag a kulcstár neve, az aktuálisan kiválasztott környezet, a titkos név és a titkos verzió alapján építi fel egy titkos kulcs teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="3c469-158">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="3c469-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c469-159">CommonParameters</span></span>
<span data-ttu-id="3c469-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c469-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c469-161">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c469-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c469-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c469-162">INPUTS</span></span>

### <span data-ttu-id="3c469-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3c469-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3c469-164">System.String</span><span class="sxs-lookup"><span data-stu-id="3c469-164">System.String</span></span>

## <span data-ttu-id="3c469-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c469-165">OUTPUTS</span></span>

### <span data-ttu-id="3c469-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3c469-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="3c469-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3c469-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="3c469-168">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3c469-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="3c469-169">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3c469-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="3c469-170">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3c469-170">NOTES</span></span>

## <span data-ttu-id="3c469-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c469-171">RELATED LINKS</span></span>

[<span data-ttu-id="3c469-172">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3c469-172">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="3c469-173">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="3c469-173">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="3c469-174">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3c469-174">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

