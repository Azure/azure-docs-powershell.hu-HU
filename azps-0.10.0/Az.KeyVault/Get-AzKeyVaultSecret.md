---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: b14e97ba09cba70a9ec571b2fbf1273de7157930
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843889"
---
# <span data-ttu-id="a0773-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a0773-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="a0773-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0773-102">SYNOPSIS</span></span>
<span data-ttu-id="a0773-103">Megnyeri a titkot egy kulcs boltozaton.</span><span class="sxs-lookup"><span data-stu-id="a0773-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="a0773-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0773-104">SYNTAX</span></span>

### <span data-ttu-id="a0773-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0773-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0773-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="a0773-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0773-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="a0773-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0773-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="a0773-108">ByDeletedSecrets</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0773-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0773-109">DESCRIPTION</span></span>
<span data-ttu-id="a0773-110">A **Get-AzKeyVaultSecret** parancsmag a kulcsok egy fő boltozatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0773-110">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="a0773-111">Ez a parancsmag adott titkos vagy minden titkot kap a kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="a0773-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="a0773-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a0773-112">EXAMPLES</span></span>

### <span data-ttu-id="a0773-113">Példa 1: az összes titok jelenlegi verziójának beszerzése a kulcs boltozatára</span><span class="sxs-lookup"><span data-stu-id="a0773-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="a0773-114">Ez a parancs az összes titok aktuális verzióját a contoso nevű fő boltívben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0773-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="a0773-115">2. példa: egy adott titok összes verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0773-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="a0773-116">Ez a parancs a contoso nevű ITSecret a titkos nevű titkos verzió összes verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="a0773-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="a0773-117">3. példa: egy adott titok aktuális verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0773-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="a0773-118">Ez a parancs a contoso nevű ITSecret a titkos nevű titkos verzió jelenlegi verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0773-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="a0773-119">Példa 4: adott titok meghatározott verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0773-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="a0773-120">Ez a parancs a contoso nevű ITSecret a titkos nevű titkos verzió adott verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0773-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="a0773-121">Példa 5: egy adott titok aktuális verziójának egyszerű szöveges értékének beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0773-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="a0773-122">Ezek a parancsok beolvassák a titkos nevű ITSecret aktuális verzióját, majd megjelenítik az adott titok egyszerű szöveges értékét.</span><span class="sxs-lookup"><span data-stu-id="a0773-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="a0773-123">6. példa: a kulcsfájl minden törölt, de el nem távolított titkát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="a0773-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="a0773-124">Ez a parancs minden korábban törölt, de nem törölt titkot kap a contoso nevű fő boltozatban.</span><span class="sxs-lookup"><span data-stu-id="a0773-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="a0773-125">7. példa: a kulcsfájl által törölt, de meg nem tisztított titkos ITSecret kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0773-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="a0773-126">Ez a parancs a contoso nevű kulcsfájl által korábban törölt, de el nem távolított titkos ITSecret kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0773-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="a0773-127">Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt titok ütemezett végleges dátumát.</span><span class="sxs-lookup"><span data-stu-id="a0773-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="a0773-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0773-128">PARAMETERS</span></span>

### <span data-ttu-id="a0773-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0773-129">-DefaultProfile</span></span>
<span data-ttu-id="a0773-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a0773-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0773-131">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="a0773-131">-IncludeVersions</span></span>
<span data-ttu-id="a0773-132">Azt jelzi, hogy ez a parancsmag minden titkos verziót kap.</span><span class="sxs-lookup"><span data-stu-id="a0773-132">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="a0773-133">A titok jelenlegi verziója az első a listán.</span><span class="sxs-lookup"><span data-stu-id="a0773-133">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="a0773-134">Ha ezt a paramétert adja meg, a *nevet* és a *VaultName* paramétereket is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="a0773-134">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="a0773-135">Ha nem adja meg a *IncludeVersions* paramétert, ez a parancsmag a megadott *néven* a titok aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0773-135">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0773-136">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a0773-136">-InRemovedState</span></span>
<span data-ttu-id="a0773-137">Megadja, hogy megjelenjen-e a korábban törölt titok a kimenetben</span><span class="sxs-lookup"><span data-stu-id="a0773-137">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0773-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0773-138">-Name</span></span>
<span data-ttu-id="a0773-139">A beolvasott titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0773-139">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0773-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a0773-140">-VaultName</span></span>
<span data-ttu-id="a0773-141">Annak a fő boltozatnak a neve, amelyhez a titok tartozik.</span><span class="sxs-lookup"><span data-stu-id="a0773-141">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="a0773-142">Ez a parancsmag a kulcsfájl teljes tartománynevét (FQDN) építi fel a paraméter által megadott név és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="a0773-142">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0773-143">-Verzió</span><span class="sxs-lookup"><span data-stu-id="a0773-143">-Version</span></span>
<span data-ttu-id="a0773-144">A titkos verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0773-144">Specifies the secret version.</span></span>
<span data-ttu-id="a0773-145">Ez a parancsmag a titkos név, az aktuálisan kijelölt környezet, a titkos név és a titkos verzió alapján építi be a titok teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="a0773-145">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0773-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0773-146">CommonParameters</span></span>
<span data-ttu-id="a0773-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0773-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0773-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0773-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0773-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0773-149">INPUTS</span></span>

### <span data-ttu-id="a0773-150">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="a0773-150">String</span></span>

## <span data-ttu-id="a0773-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0773-151">OUTPUTS</span></span>

### <span data-ttu-id="a0773-152">Lista<Microsoft. Azure. commands. SecretIdentityItem. models.>, Microsoft. Azure. commands.-Vault. models. Secret, List<Microsoft. Azure. Command. DeletedSecret. DeletedSecretIdentityItem>, Microsoft. Azure. Command.</span><span class="sxs-lookup"><span data-stu-id="a0773-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="a0773-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0773-153">NOTES</span></span>

## <span data-ttu-id="a0773-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0773-154">RELATED LINKS</span></span>

[<span data-ttu-id="a0773-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a0773-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="a0773-156">Visszavonás – AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="a0773-156">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="a0773-157">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a0773-157">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

