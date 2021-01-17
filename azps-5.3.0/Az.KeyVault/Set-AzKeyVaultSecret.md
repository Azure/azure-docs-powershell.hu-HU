---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 0733cf722e26cb52abdb84f7917a78d088f49fd4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467673"
---
# <span data-ttu-id="1089d-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1089d-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="1089d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1089d-102">SYNOPSIS</span></span>
<span data-ttu-id="1089d-103">Titkos kulcsot hoz létre vagy frissítéseket hoz létre egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="1089d-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="1089d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1089d-104">SYNTAX</span></span>

### <span data-ttu-id="1089d-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1089d-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1089d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1089d-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1089d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1089d-107">DESCRIPTION</span></span>
<span data-ttu-id="1089d-108">A **Set-AzKeyVaultSecret** parancsmag létrehoz vagy frissítéseket hoz létre vagy frissítéseket hoz létre egy kulcstárban az Azure-kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="1089d-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="1089d-109">Ha a titkos parancsmag nem létezik, ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1089d-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="1089d-110">Ha a titkos parancsmag már létezik, ez a parancsmag létrehozza a titkos fájl új verzióját.</span><span class="sxs-lookup"><span data-stu-id="1089d-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="1089d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1089d-111">EXAMPLES</span></span>

### <span data-ttu-id="1089d-112">1. példa: A titkos adatok értékének módosítása alapértelmezett attribútumok használatával</span><span class="sxs-lookup"><span data-stu-id="1089d-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

<span data-ttu-id="1089d-113">Az első parancs biztonságos karakterláncgé alakít egy karakterláncot a **ConvertTo-SecureString** parancsmag használatával, majd a karakterláncot a $Secret tárolja.</span><span class="sxs-lookup"><span data-stu-id="1089d-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="1089d-114">További információért írja be a `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="1089d-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="1089d-115">A második parancs módosítja az ITSecret nevű titkos kulcs értékét a Contoso nevű kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="1089d-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="1089d-116">A titkos érték a $Secret.</span><span class="sxs-lookup"><span data-stu-id="1089d-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="1089d-117">2. példa: A titkos adatok értékének módosítása egyéni attribútumok használatával</span><span class="sxs-lookup"><span data-stu-id="1089d-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

<span data-ttu-id="1089d-118">Az első parancs biztonságos karakterláncgé alakít egy karakterláncot a **ConvertTo-SecureString** parancsmag használatával, majd a karakterláncot a $Secret tárolja.</span><span class="sxs-lookup"><span data-stu-id="1089d-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="1089d-119">További információért írja be a `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="1089d-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="1089d-120">A következő parancsok egyéni attribútumokat definiálnak a lejárati dátumhoz, a címkékhez és a környezettípushoz, és az attribútumokat változókban tárolják.</span><span class="sxs-lookup"><span data-stu-id="1089d-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="1089d-121">A végleges parancs módosítja az ITSecret nevű titkos kulcs értékét a Contoso nevű kulcstárban a korábban változóként megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="1089d-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="1089d-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1089d-122">PARAMETERS</span></span>

### <span data-ttu-id="1089d-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="1089d-123">-ContentType</span></span>
<span data-ttu-id="1089d-124">Egy titkos tartalomtípust ad meg.</span><span class="sxs-lookup"><span data-stu-id="1089d-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="1089d-125">A meglévő tartalomtípus törléséhez adjon meg egy üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="1089d-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="1089d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1089d-126">-DefaultProfile</span></span>
<span data-ttu-id="1089d-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1089d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1089d-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="1089d-128">-Disable</span></span>
<span data-ttu-id="1089d-129">Azt jelzi, hogy ez a parancsmag letilt egy titkos füzetet.</span><span class="sxs-lookup"><span data-stu-id="1089d-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="1089d-130">-Lejár</span><span class="sxs-lookup"><span data-stu-id="1089d-130">-Expires</span></span>
<span data-ttu-id="1089d-131">A parancsmag által frissülő titkos objektum **lejárati** idejét adja meg DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="1089d-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="1089d-132">Ez a paraméter egyezményes világidőt (UTC) használ.</span><span class="sxs-lookup"><span data-stu-id="1089d-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1089d-133">**DateTime-objektum** beszerzéséhez használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1089d-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1089d-134">További információért írja be a `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="1089d-134">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1089d-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1089d-135">-InputObject</span></span>
<span data-ttu-id="1089d-136">Titkos objektum</span><span class="sxs-lookup"><span data-stu-id="1089d-136">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1089d-137">-Name</span><span class="sxs-lookup"><span data-stu-id="1089d-137">-Name</span></span>
<span data-ttu-id="1089d-138">A módosítani szükséges titkos elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1089d-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="1089d-139">Ez a parancsmag egy titkos kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcstár neve és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="1089d-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1089d-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="1089d-140">-NotBefore</span></span>
<span data-ttu-id="1089d-141">Azt az időt adja meg **DateTime-objektumként,** amely előtt a titkos elem nem használható.</span><span class="sxs-lookup"><span data-stu-id="1089d-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="1089d-142">Ez a paraméter az UTC-t használja.</span><span class="sxs-lookup"><span data-stu-id="1089d-142">This parameter uses UTC.</span></span> <span data-ttu-id="1089d-143">**DateTime-objektum** beszerzéséhez használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1089d-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1089d-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="1089d-144">-SecretValue</span></span>
<span data-ttu-id="1089d-145">A titkos objektum értékét adja meg **SecureString objektumként.**</span><span class="sxs-lookup"><span data-stu-id="1089d-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="1089d-146">A **SecureString objektum** beszerzéséhez használja a **ConvertTo-SecureString** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1089d-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="1089d-147">További információért írja be a `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="1089d-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1089d-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="1089d-148">-Tag</span></span>
<span data-ttu-id="1089d-149">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="1089d-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1089d-150">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="1089d-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1089d-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1089d-151">-VaultName</span></span>
<span data-ttu-id="1089d-152">Annak a kulcstárnak a nevét adja meg, amelyhez ez a kulcskulcs tartozik.</span><span class="sxs-lookup"><span data-stu-id="1089d-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="1089d-153">Ez a parancsmag egy kulcstár FQDN-ét építi fel a paraméter által megadott név és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="1089d-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1089d-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1089d-154">-Confirm</span></span>
<span data-ttu-id="1089d-155">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1089d-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1089d-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1089d-156">-WhatIf</span></span>
<span data-ttu-id="1089d-157">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1089d-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1089d-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1089d-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1089d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1089d-159">CommonParameters</span></span>
<span data-ttu-id="1089d-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1089d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1089d-161">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1089d-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1089d-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1089d-162">INPUTS</span></span>

### <span data-ttu-id="1089d-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1089d-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="1089d-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1089d-164">OUTPUTS</span></span>

### <span data-ttu-id="1089d-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1089d-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="1089d-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1089d-166">NOTES</span></span>

## <span data-ttu-id="1089d-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1089d-167">RELATED LINKS</span></span>

[<span data-ttu-id="1089d-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1089d-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="1089d-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1089d-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
