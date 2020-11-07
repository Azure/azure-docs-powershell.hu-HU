---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: edb4c166fbacbf0ee394b10ff475fe90dc00a67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680415"
---
# <span data-ttu-id="fe8b3-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="fe8b3-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="fe8b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe8b3-102">SYNOPSIS</span></span>
<span data-ttu-id="fe8b3-103">A titkos kulcs attribútumait frissíti a kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe8b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe8b3-104">SYNTAX</span></span>

### <span data-ttu-id="fe8b3-105">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="fe8b3-105">Default</span></span>
```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe8b3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fe8b3-106">InputObject</span></span>
```
Set-AzureKeyVaultSecretAttribute [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe8b3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe8b3-107">DESCRIPTION</span></span>
<span data-ttu-id="fe8b3-108">A **set-AzureKeyVaultSecretAttribute** parancsmag a titkos kulcsok szerkeszthető attribútumait frissíti a kulcs boltozatakor.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-108">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="fe8b3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fe8b3-109">EXAMPLES</span></span>

### <span data-ttu-id="fe8b3-110">Példa 1: a titok attribútumainak módosítása</span><span class="sxs-lookup"><span data-stu-id="fe8b3-110">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="fe8b3-111">Az első négy parancs a lejárat, a NotBefore, a címkék és a környezeti típus attribútumait definiálja, valamint az attribútumokat változókban tárolhatja.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="fe8b3-112">A végleges parancs módosította a ContosoVault nevű kulcs boltozatának attribútumait a tárolt változók használatával.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="fe8b3-113">2. példa: a címke és a tartalom típusának törlése titoknak</span><span class="sxs-lookup"><span data-stu-id="fe8b3-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="fe8b3-114">Ez a parancs a contoso nevű fő boltozatban a titkos nevű HR-verzió megadott verziójához tartozó címkéket és tartalomtípust törli.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="fe8b3-115">3. példa: a titok jelenlegi verziójának letiltása, akinek a neve vele kezdődik</span><span class="sxs-lookup"><span data-stu-id="fe8b3-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="fe8b3-116">Az első parancs a contoso karakterlánc értékét a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-116">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="fe8b3-117">A második parancs a karakterlánc értékét a $Prefix változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-117">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="fe8b3-118">A harmadik parancs az Get-AzureKeyVaultSecret parancsmagot használja a megadott kulcsfájl titkainak kinyerésére, majd ezeket a titkokat átadja a **Where-Object** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="fe8b3-119">A **Where-Object** parancsmag kiszűri a karakterrel kezdődő nevek titkát.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="fe8b3-120">A parancs bekapcsolja a szűrőhöz igazodó titkot az Set-AzureKeyVaultSecretAttribute parancsmaghoz, amely letiltja őket.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-120">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="fe8b3-121">4. példa: a ContentType beállítása a titok minden verziójában</span><span class="sxs-lookup"><span data-stu-id="fe8b3-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="fe8b3-122">Az első három parancs a *VaultName* , a *név* és a *ContentType* paraméterben használható karakterlánc-változók definiálását adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="fe8b3-123">A negyedik parancs az Get-AzureKeyVaultKey parancsmagot használja a megadott kulcsok beolvasására, és a kulcsokat a Set-AzureKeyVaultSecretAttribute parancsmagba a tartalomtípusok XML-be való beállításához adja.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="fe8b3-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe8b3-124">PARAMETERS</span></span>

### <span data-ttu-id="fe8b3-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="fe8b3-125">-ContentType</span></span>
<span data-ttu-id="fe8b3-126">A titok tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-126">Specifies the content type of a secret.</span></span> <span data-ttu-id="fe8b3-127">Ha nem adja meg ezt a paramétert, az aktuális titok tartalomtípusa nem változik.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-127">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="fe8b3-128">Ha el szeretné távolítani a meglévő tartalomtípust, adjon meg egy üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-128">To remove the existing content type, specify an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe8b3-129">-DefaultProfile</span></span>
<span data-ttu-id="fe8b3-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fe8b3-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-131">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="fe8b3-131">-Enable</span></span>
<span data-ttu-id="fe8b3-132">Azt jelzi, hogy engedélyezni kell-e a titkot.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-132">Indicates whether to enable a secret.</span></span> <span data-ttu-id="fe8b3-133">A titok engedélyezéséhez $False megadhatja a titkot vagy a $Truet.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-133">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="fe8b3-134">Ha nem adja meg ezt a paramétert, az aktuális titok engedélyezett vagy letiltott állapota nem változik.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-134">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-135">-Lejár</span><span class="sxs-lookup"><span data-stu-id="fe8b3-135">-Expires</span></span>
<span data-ttu-id="fe8b3-136">Itt adhatja meg azt a dátumot és időpontot, amikor a titok lejár.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-136">Specifies the date and time that a secret expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe8b3-137">-InputObject</span></span>
<span data-ttu-id="fe8b3-138">Titkos objektum</span><span class="sxs-lookup"><span data-stu-id="fe8b3-138">Secret object</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fe8b3-139">-Name</span></span>
<span data-ttu-id="fe8b3-140">A titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-140">Specifies the name of a secret.</span></span> <span data-ttu-id="fe8b3-141">Ez a parancsmag a titok teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-141">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-142">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="fe8b3-142">-NotBefore</span></span>
<span data-ttu-id="fe8b3-143">Itt adhatja meg azt a koordinált általános időpontot (UTC), amely előtt a titkos kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-143">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="fe8b3-144">Ha nem adja meg ezt a paramétert, az aktuális titok NotBefore attribútuma nem változik.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-144">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe8b3-145">-PassThru</span></span>
<span data-ttu-id="fe8b3-146">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fe8b3-147">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-147">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="fe8b3-148">-Tag</span></span>
<span data-ttu-id="fe8b3-149">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fe8b3-150">Példa:</span><span class="sxs-lookup"><span data-stu-id="fe8b3-150">For example:</span></span>

<span data-ttu-id="fe8b3-151">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="fe8b3-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fe8b3-152">-VaultName</span></span>
<span data-ttu-id="fe8b3-153">A módosítani kívánt fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-153">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="fe8b3-154">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és az aktuálisan kiválasztott környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-155">-Verzió</span><span class="sxs-lookup"><span data-stu-id="fe8b3-155">-Version</span></span>
<span data-ttu-id="fe8b3-156">A titok verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-156">Specifies the version of a secret.</span></span>
<span data-ttu-id="fe8b3-157">Ez a parancsmag a titkos név, az aktuálisan kijelölt környezet, a titkos név és a titkos verzió alapján építi be a titok teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe8b3-158">-Confirm</span></span>
<span data-ttu-id="fe8b3-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe8b3-160">-WhatIf</span></span>
<span data-ttu-id="fe8b3-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe8b3-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b3-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe8b3-163">CommonParameters</span></span>
<span data-ttu-id="fe8b3-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe8b3-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe8b3-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe8b3-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe8b3-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe8b3-166">INPUTS</span></span>

### <span data-ttu-id="fe8b3-167">Nincs</span><span class="sxs-lookup"><span data-stu-id="fe8b3-167">None</span></span>
<span data-ttu-id="fe8b3-168">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe8b3-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe8b3-169">OUTPUTS</span></span>

### <span data-ttu-id="fe8b3-170">Microsoft. Azure. Command. PSKeyVaultSecret. models.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>
<span data-ttu-id="fe8b3-171">Visszaadja a Microsoft. Azure. Command. kulccsal. models. Secret objektumot, ha a PassThru meg van adva.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-171">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="fe8b3-172">Ellenkező esetben semmit sem ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="fe8b3-172">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="fe8b3-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe8b3-173">NOTES</span></span>

## <span data-ttu-id="fe8b3-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe8b3-174">RELATED LINKS</span></span>

[<span data-ttu-id="fe8b3-175">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fe8b3-175">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="fe8b3-176">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fe8b3-176">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="fe8b3-177">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fe8b3-177">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
