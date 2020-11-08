---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194747"
---
# <span data-ttu-id="ae4aa-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae4aa-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="ae4aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4aa-103">A titkos kulcs attribútumait frissíti a kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="ae4aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae4aa-104">SYNTAX</span></span>

### <span data-ttu-id="ae4aa-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae4aa-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae4aa-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae4aa-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae4aa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae4aa-107">DESCRIPTION</span></span>
<span data-ttu-id="ae4aa-108">Az **Update-AzKeyVaultSecret** parancsmag a titkos kulcsok szerkeszthető attribútumait frissíti a kulcs boltozatakor.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="ae4aa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ae4aa-109">EXAMPLES</span></span>

### <span data-ttu-id="ae4aa-110">Példa 1: a titok attribútumainak módosítása</span><span class="sxs-lookup"><span data-stu-id="ae4aa-110">Example 1: Modify the attributes of a secret</span></span>
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

<span data-ttu-id="ae4aa-111">Az első négy parancs a lejárat, a NotBefore, a címkék és a környezeti típus attribútumait definiálja, valamint az attribútumokat változókban tárolhatja.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="ae4aa-112">A végleges parancs módosította a ContosoVault nevű kulcs boltozatának attribútumait a tárolt változók használatával.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="ae4aa-113">2. példa: a címke és a tartalom típusának törlése titoknak</span><span class="sxs-lookup"><span data-stu-id="ae4aa-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="ae4aa-114">Ez a parancs a contoso nevű fő boltozatban a titkos nevű HR-verzió megadott verziójához tartozó címkéket és tartalomtípust törli.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="ae4aa-115">3. példa: a titok jelenlegi verziójának letiltása, akinek a neve vele kezdődik</span><span class="sxs-lookup"><span data-stu-id="ae4aa-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="ae4aa-116">Az első parancs a contoso karakterlánc értékét a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="ae4aa-117">A második parancs a karakterlánc értékét a $Prefix változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="ae4aa-118">A harmadik parancs az Get-AzKeyVaultSecret parancsmagot használja a megadott kulcsfájl titkainak kinyerésére, majd ezeket a titkokat átadja a **Where-Object** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="ae4aa-119">A **Where-Object** parancsmag kiszűri a karakterrel kezdődő nevek titkát.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="ae4aa-120">A parancs bekapcsolja a szűrőhöz igazodó titkot az Update-AzKeyVaultSecret parancsmaghoz, amely letiltja őket.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="ae4aa-121">4. példa: a ContentType beállítása a titok minden verziójában</span><span class="sxs-lookup"><span data-stu-id="ae4aa-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="ae4aa-122">Az első három parancs a *VaultName* , a *név* és a *ContentType* paraméterben használható karakterlánc-változók definiálását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="ae4aa-123">A negyedik parancs az Get-AzKeyVaultKey parancsmagot használja a megadott kulcsok beolvasására, és a kulcsokat a Update-AzKeyVaultSecret parancsmagba a tartalomtípusok XML-be való beállításához adja.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="ae4aa-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae4aa-124">PARAMETERS</span></span>

### <span data-ttu-id="ae4aa-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="ae4aa-125">-ContentType</span></span>
<span data-ttu-id="ae4aa-126">Secret tartalomtípusa.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-126">Secret's content type.</span></span>
<span data-ttu-id="ae4aa-127">Ha nincs megadva, a titok tartalomtípusának meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="ae4aa-128">A meglévő tartalomtípus-érték eltávolításához adjon meg egy üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="ae4aa-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4aa-129">-DefaultProfile</span></span>
<span data-ttu-id="ae4aa-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae4aa-131">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="ae4aa-131">-Enable</span></span>
<span data-ttu-id="ae4aa-132">Ha van, engedélyezze a titkot, ha az érték igaz.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="ae4aa-133">Titkos érték letiltása, ha az érték hamis.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="ae4aa-134">Ha nem adja meg, akkor a titok engedélyezett/letiltott állapotának meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="ae4aa-135">-Lejár</span><span class="sxs-lookup"><span data-stu-id="ae4aa-135">-Expires</span></span>
<span data-ttu-id="ae4aa-136">A titok lejárati ideje az UTC időpontjában.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="ae4aa-137">Ha nincs megadva, a titok elévülési idejének meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="ae4aa-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae4aa-138">-InputObject</span></span>
<span data-ttu-id="ae4aa-139">Titkos objektum</span><span class="sxs-lookup"><span data-stu-id="ae4aa-139">Secret object</span></span>

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

### <span data-ttu-id="ae4aa-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae4aa-140">-Name</span></span>
<span data-ttu-id="ae4aa-141">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-141">Secret name.</span></span>
<span data-ttu-id="ae4aa-142">A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből és a titkos névvel elkészíti a titkos FQDN-t.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="ae4aa-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="ae4aa-143">-NotBefore</span></span>
<span data-ttu-id="ae4aa-144">Az az UTC-idő, ameddig a titkos kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="ae4aa-145">Ha nincs megadva, a titok NotBefore attribútumának meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="ae4aa-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae4aa-146">-PassThru</span></span>
<span data-ttu-id="ae4aa-147">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="ae4aa-148">Ha ez a kapcsoló van megadva, a titkos objektum visszaadása.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="ae4aa-149">-Címke</span><span class="sxs-lookup"><span data-stu-id="ae4aa-149">-Tag</span></span>
<span data-ttu-id="ae4aa-150">Titkos címkéket jelképező Hashtable</span><span class="sxs-lookup"><span data-stu-id="ae4aa-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="ae4aa-151">Ha nem adja meg, akkor a titkos címke meglévő címkéi változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="ae4aa-152">Címke eltávolítása: üres Hashtable megadásával.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="ae4aa-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ae4aa-153">-VaultName</span></span>
<span data-ttu-id="ae4aa-154">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-154">Vault name.</span></span>
<span data-ttu-id="ae4aa-155">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ae4aa-156">-Verzió</span><span class="sxs-lookup"><span data-stu-id="ae4aa-156">-Version</span></span>
<span data-ttu-id="ae4aa-157">Titkos verzió.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-157">Secret version.</span></span>
<span data-ttu-id="ae4aa-158">A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből, a titkos névvel és a titkos verzióból építi fel a titkos FQDN-t.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

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

### <span data-ttu-id="ae4aa-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae4aa-159">-Confirm</span></span>
<span data-ttu-id="ae4aa-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae4aa-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae4aa-161">-WhatIf</span></span>
<span data-ttu-id="ae4aa-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae4aa-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae4aa-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4aa-164">CommonParameters</span></span>
<span data-ttu-id="ae4aa-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae4aa-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4aa-166">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4aa-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae4aa-167">INPUTS</span></span>

### <span data-ttu-id="ae4aa-168">Microsoft. Azure. Command. PSKeyVaultSecretIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="ae4aa-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae4aa-169">OUTPUTS</span></span>

### <span data-ttu-id="ae4aa-170">Microsoft. Azure. Command. PSKeyVaultSecret. models.</span><span class="sxs-lookup"><span data-stu-id="ae4aa-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="ae4aa-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae4aa-171">NOTES</span></span>

## <span data-ttu-id="ae4aa-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae4aa-172">RELATED LINKS</span></span>
