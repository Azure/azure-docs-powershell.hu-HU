---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: a3d4803fa352c59f826b653b3d0da241608909a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666188"
---
# <span data-ttu-id="e3fcf-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e3fcf-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="e3fcf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fcf-103">Megnyeri a titkot egy kulcs boltozaton.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="e3fcf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3fcf-104">SYNTAX</span></span>

### <span data-ttu-id="e3fcf-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3fcf-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fcf-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="e3fcf-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fcf-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="e3fcf-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fcf-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="e3fcf-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fcf-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="e3fcf-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fcf-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="e3fcf-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fcf-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="e3fcf-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fcf-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="e3fcf-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fcf-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="e3fcf-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3fcf-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3fcf-114">DESCRIPTION</span></span>
<span data-ttu-id="e3fcf-115">A **Get-AzKeyVaultSecret** parancsmag a kulcsok egy fő boltozatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="e3fcf-116">Ez a parancsmag adott titkos vagy minden titkot kap a kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="e3fcf-117">Példák</span><span class="sxs-lookup"><span data-stu-id="e3fcf-117">EXAMPLES</span></span>

### <span data-ttu-id="e3fcf-118">Példa 1: az összes titok jelenlegi verziójának beszerzése a kulcs boltozatára</span><span class="sxs-lookup"><span data-stu-id="e3fcf-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
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

<span data-ttu-id="e3fcf-119">Ez a parancs az összes titok aktuális verzióját a contoso nevű fő boltívben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="e3fcf-120">2. példa: egy adott titok összes verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e3fcf-120">Example 2: Get all versions of a specific secret</span></span>
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

<span data-ttu-id="e3fcf-121">Ez a parancs a contoso nevű secret1 a titkos nevű titkos verzió összes verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="e3fcf-122">3. példa: egy adott titok aktuális verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e3fcf-122">Example 3: Get the current version of a specific secret</span></span>
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

<span data-ttu-id="e3fcf-123">Ez a parancs a contoso nevű secret1 a titkos nevű titkos verzió jelenlegi verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="e3fcf-124">Példa 4: adott titok meghatározott verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e3fcf-124">Example 4: Get a specific version of a specific secret</span></span>
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

<span data-ttu-id="e3fcf-125">Ez a parancs a contoso nevű secret1 a titkos nevű titkos verzió adott verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="e3fcf-126">Példa 5: egy adott titok aktuális verziójának egyszerű szöveges értékének beszerzése</span><span class="sxs-lookup"><span data-stu-id="e3fcf-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is:" $secret.SecretValueText

Secret Value is: P@ssw0rd
```

<span data-ttu-id="e3fcf-127">Ezek a parancsok beolvassák a titkos nevű ITSecret aktuális verzióját, majd megjelenítik az adott titok egyszerű szöveges értékét.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="e3fcf-128">6. példa: a kulcsfájl minden törölt, de el nem távolított titkát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="e3fcf-129">Ez a parancs minden korábban törölt, de nem törölt titkot kap a contoso nevű fő boltozatban.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="e3fcf-130">7. példa: a kulcsfájl által törölt, de meg nem tisztított titkos ITSecret kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="e3fcf-131">Ez a parancs a contoso nevű kulcsfájl "secret1" titkát kapja, amelyet korábban törölt, de nem törölt.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="e3fcf-132">Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt titok ütemezett végleges dátumát.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="e3fcf-133">8. példa: az összes titok jelenlegi verziójának beszerzése a kulcsokba szűréssel</span><span class="sxs-lookup"><span data-stu-id="e3fcf-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
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

<span data-ttu-id="e3fcf-134">Ez a parancs beolvassa a "titok" kezdetű, a contoso nevű "titok" nevű fő boltozat összes titkának aktuális verzióját.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="e3fcf-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3fcf-135">PARAMETERS</span></span>

### <span data-ttu-id="e3fcf-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fcf-136">-DefaultProfile</span></span>
<span data-ttu-id="e3fcf-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e3fcf-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3fcf-138">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="e3fcf-138">-IncludeVersions</span></span>
<span data-ttu-id="e3fcf-139">Azt jelzi, hogy ez a parancsmag minden titkos verziót kap.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-139">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="e3fcf-140">A titok jelenlegi verziója az első a listán.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-140">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="e3fcf-141">Ha ezt a paramétert adja meg, a *nevet* és a *VaultName* paramétereket is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-141">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="e3fcf-142">Ha nem adja meg a *IncludeVersions* paramétert, ez a parancsmag a megadott *néven* a titok aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-142">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="e3fcf-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3fcf-143">-InputObject</span></span>
<span data-ttu-id="e3fcf-144">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-144">KeyVault Object.</span></span>

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

### <span data-ttu-id="e3fcf-145">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e3fcf-145">-InRemovedState</span></span>
<span data-ttu-id="e3fcf-146">Megadja, hogy megjelenjen-e a korábban törölt titok a kimenetben</span><span class="sxs-lookup"><span data-stu-id="e3fcf-146">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="e3fcf-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3fcf-147">-Name</span></span>
<span data-ttu-id="e3fcf-148">A beolvasott titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-148">Specifies the name of the secret to get.</span></span>

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

### <span data-ttu-id="e3fcf-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3fcf-149">-ResourceId</span></span>
<span data-ttu-id="e3fcf-150">A főkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-150">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="e3fcf-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e3fcf-151">-VaultName</span></span>
<span data-ttu-id="e3fcf-152">Annak a fő boltozatnak a neve, amelyhez a titok tartozik.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-152">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="e3fcf-153">Ez a parancsmag a kulcsfájl teljes tartománynevét (FQDN) építi fel a paraméter által megadott név és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-153">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="e3fcf-154">-Verzió</span><span class="sxs-lookup"><span data-stu-id="e3fcf-154">-Version</span></span>
<span data-ttu-id="e3fcf-155">A titkos verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-155">Specifies the secret version.</span></span>
<span data-ttu-id="e3fcf-156">Ez a parancsmag a titkos név, az aktuálisan kijelölt környezet, a titkos név és a titkos verzió alapján építi be a titok teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-156">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="e3fcf-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fcf-157">CommonParameters</span></span>
<span data-ttu-id="e3fcf-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3fcf-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fcf-159">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fcf-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3fcf-160">INPUTS</span></span>

### <span data-ttu-id="e3fcf-161">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e3fcf-162">System. String</span><span class="sxs-lookup"><span data-stu-id="e3fcf-162">System.String</span></span>

## <span data-ttu-id="e3fcf-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3fcf-163">OUTPUTS</span></span>

### <span data-ttu-id="e3fcf-164">Microsoft. Azure. Command. PSKeyVaultSecretIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="e3fcf-165">Microsoft. Azure. Command. PSKeyVaultSecret. models.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="e3fcf-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e3fcf-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="e3fcf-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e3fcf-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="e3fcf-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3fcf-168">NOTES</span></span>

## <span data-ttu-id="e3fcf-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3fcf-169">RELATED LINKS</span></span>

[<span data-ttu-id="e3fcf-170">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e3fcf-170">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="e3fcf-171">Visszavonás – AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="e3fcf-171">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="e3fcf-172">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e3fcf-172">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

