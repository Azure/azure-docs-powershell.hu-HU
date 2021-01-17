---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469506"
---
# <span data-ttu-id="87f75-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="87f75-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="87f75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87f75-102">SYNOPSIS</span></span>
<span data-ttu-id="87f75-103">Frissíti egy titkos kulcs attribútumát egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="87f75-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="87f75-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87f75-104">SYNTAX</span></span>

### <span data-ttu-id="87f75-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87f75-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87f75-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="87f75-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87f75-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87f75-107">DESCRIPTION</span></span>
<span data-ttu-id="87f75-108">Az **Update-AzKeyVaultSecret** parancsmag frissíti egy kulcstárban található titkos kulcs szerkeszthető attribútumát.</span><span class="sxs-lookup"><span data-stu-id="87f75-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="87f75-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87f75-109">EXAMPLES</span></span>

### <span data-ttu-id="87f75-110">1. példa: Egy titkos attribútum módosítása</span><span class="sxs-lookup"><span data-stu-id="87f75-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

<span data-ttu-id="87f75-111">Az első négy parancs attribútumokat definiál a lejárati dátumhoz, a NotBefore dátumhoz, a címkékhez és a környezettípushoz, és az attribútumokat változókban tárolja.</span><span class="sxs-lookup"><span data-stu-id="87f75-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="87f75-112">A végleges parancs módosítja a ContosoVault nevű kulcstárolóban a HR nevű kulcs attribútumát a tárolt változók használatával.</span><span class="sxs-lookup"><span data-stu-id="87f75-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="87f75-113">2. példa: Titkos címkék és tartalomtípus törlése</span><span class="sxs-lookup"><span data-stu-id="87f75-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="87f75-114">Ez a parancs törli a Contoso nevű kulcstárban található HR nevű titkos fájl adott verziójának címkéit és tartalomtípusát.</span><span class="sxs-lookup"><span data-stu-id="87f75-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="87f75-115">3. példa: A titkos kulcsok aktuális verziójának letiltása, amelynek a neve IT-val kezdődik</span><span class="sxs-lookup"><span data-stu-id="87f75-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="87f75-116">Az első parancs a Contoso karakterláncértéket tárolja a $Vault változóban.</span><span class="sxs-lookup"><span data-stu-id="87f75-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="87f75-117">A második parancs az IT karakterlánc értékét tárolja a $Prefix változóban.</span><span class="sxs-lookup"><span data-stu-id="87f75-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="87f75-118">A harmadik parancs a Get-AzKeyVaultSecret parancsmag segítségével begyűjte a megadott kulcstárban található titkosságokat, majd átadja ezeket a titkosságokat a **Where-Object** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="87f75-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="87f75-119">A **Where-Object** parancsmag az IT karakterekkel kezdődik nevek titkos karaktereit szűri.</span><span class="sxs-lookup"><span data-stu-id="87f75-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="87f75-120">A parancs a szűrőnek a szűrőnek megfelelő titkosságokat a Update-AzKeyVaultSecret el, ami letiltja őket.</span><span class="sxs-lookup"><span data-stu-id="87f75-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="87f75-121">4. példa: A ContentType beállítása egy titkos fájl minden verziójához</span><span class="sxs-lookup"><span data-stu-id="87f75-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="87f75-122">Az első három parancs karakterlánc-változókat definiál a *VaultName,* a *Name* és a *ContentType paraméterhez.*</span><span class="sxs-lookup"><span data-stu-id="87f75-122">The first three commands define string variables to use for the *VaultName*, *Name*, and *ContentType* parameters.</span></span> <span data-ttu-id="87f75-123">A negyedik parancs a Get-AzKeyVaultKey parancsmag segítségével beszereti a megadott kulcsokat, és a Update-AzKeyVaultSecret-parancsmag kulcsait az XML-re állíthatja.</span><span class="sxs-lookup"><span data-stu-id="87f75-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="87f75-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87f75-124">PARAMETERS</span></span>

### <span data-ttu-id="87f75-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="87f75-125">-ContentType</span></span>
<span data-ttu-id="87f75-126">A Secret tartalomtípusa.</span><span class="sxs-lookup"><span data-stu-id="87f75-126">Secret's content type.</span></span>
<span data-ttu-id="87f75-127">Ha nincs megadva, a titkos fájl tartalomtípusának meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="87f75-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="87f75-128">Távolítsa el a meglévő tartalomtípus értékét egy üres karakterlánc megadásával.</span><span class="sxs-lookup"><span data-stu-id="87f75-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="87f75-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f75-129">-DefaultProfile</span></span>
<span data-ttu-id="87f75-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87f75-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87f75-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="87f75-131">-Enable</span></span>
<span data-ttu-id="87f75-132">Ha jelen van, engedélyezzen egy titkos értéket, ha az érték igaz.</span><span class="sxs-lookup"><span data-stu-id="87f75-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="87f75-133">Tiltsa le a titkos adatokat, ha az érték hamis.</span><span class="sxs-lookup"><span data-stu-id="87f75-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="87f75-134">Ha nincs megadva, a titkos fájl engedélyezett/letiltott állapotának meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="87f75-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="87f75-135">-Lejár</span><span class="sxs-lookup"><span data-stu-id="87f75-135">-Expires</span></span>
<span data-ttu-id="87f75-136">A titkos idő lejárati ideje az UTC-ben.</span><span class="sxs-lookup"><span data-stu-id="87f75-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="87f75-137">Ha nincs megadva, a titkos kulcs lejárati időének meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="87f75-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="87f75-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87f75-138">-InputObject</span></span>
<span data-ttu-id="87f75-139">Titkos objektum</span><span class="sxs-lookup"><span data-stu-id="87f75-139">Secret object</span></span>

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

### <span data-ttu-id="87f75-140">-Name</span><span class="sxs-lookup"><span data-stu-id="87f75-140">-Name</span></span>
<span data-ttu-id="87f75-141">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="87f75-141">Secret name.</span></span>
<span data-ttu-id="87f75-142">A parancsmag a tárolónévből ( jelenleg kijelölt környezetből és titkos névből ) egy titkos kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="87f75-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="87f75-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="87f75-143">-NotBefore</span></span>
<span data-ttu-id="87f75-144">Az a UTC-idő, amely előtt a titkos adatok nem használhatók.</span><span class="sxs-lookup"><span data-stu-id="87f75-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="87f75-145">Ha nincs megadva, a titkos attribútum NotBefore attribútumának meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="87f75-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="87f75-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87f75-146">-PassThru</span></span>
<span data-ttu-id="87f75-147">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="87f75-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="87f75-148">Ha ez a kapcsoló meg van adva, a Secret objektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="87f75-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="87f75-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="87f75-149">-Tag</span></span>
<span data-ttu-id="87f75-150">Titkos címkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="87f75-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="87f75-151">Ha nincs megadva, a titkos kód meglévő címkéi változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="87f75-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="87f75-152">Címke eltávolítása üres hashtable megadásával.</span><span class="sxs-lookup"><span data-stu-id="87f75-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="87f75-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="87f75-153">-VaultName</span></span>
<span data-ttu-id="87f75-154">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="87f75-154">Vault name.</span></span>
<span data-ttu-id="87f75-155">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="87f75-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="87f75-156">-Version</span><span class="sxs-lookup"><span data-stu-id="87f75-156">-Version</span></span>
<span data-ttu-id="87f75-157">Titkos verzió.</span><span class="sxs-lookup"><span data-stu-id="87f75-157">Secret version.</span></span>
<span data-ttu-id="87f75-158">A parancsmag a tároló nevéből, az aktuálisan kijelölt környezetből, a titkos névből és a titkos verzióból építi fel egy titkos név teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="87f75-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f75-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87f75-159">-Confirm</span></span>
<span data-ttu-id="87f75-160">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="87f75-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87f75-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87f75-161">-WhatIf</span></span>
<span data-ttu-id="87f75-162">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="87f75-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87f75-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87f75-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87f75-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f75-164">CommonParameters</span></span>
<span data-ttu-id="87f75-165">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87f75-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f75-166">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87f75-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f75-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87f75-167">INPUTS</span></span>

### <span data-ttu-id="87f75-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="87f75-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="87f75-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87f75-169">OUTPUTS</span></span>

### <span data-ttu-id="87f75-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="87f75-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="87f75-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87f75-171">NOTES</span></span>

## <span data-ttu-id="87f75-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87f75-172">RELATED LINKS</span></span>
