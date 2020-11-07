---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
ms.openlocfilehash: f8463533f8a153b74df1863ba251950f16f9e19a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848178"
---
# <span data-ttu-id="3f26d-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="3f26d-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="3f26d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f26d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f26d-103">A titkos kulcs attribútumait frissíti a kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="3f26d-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f26d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f26d-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f26d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f26d-105">DESCRIPTION</span></span>
<span data-ttu-id="3f26d-106">A **set-AzureKeyVaultSecretAttribute** parancsmag a titkos kulcsok szerkeszthető attribútumait frissíti a kulcs boltozatakor.</span><span class="sxs-lookup"><span data-stu-id="3f26d-106">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="3f26d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3f26d-107">EXAMPLES</span></span>

### <span data-ttu-id="3f26d-108">Példa 1: a titok attribútumainak módosítása</span><span class="sxs-lookup"><span data-stu-id="3f26d-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="3f26d-109">Az első négy parancs a lejárat, a NotBefore, a címkék és a környezeti típus attribútumait definiálja, valamint az attribútumokat változókban tárolhatja.</span><span class="sxs-lookup"><span data-stu-id="3f26d-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="3f26d-110">A végleges parancs módosította a ContosoVault nevű kulcs boltozatának attribútumait a tárolt változók használatával.</span><span class="sxs-lookup"><span data-stu-id="3f26d-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="3f26d-111">2. példa: a címke és a tartalom típusának törlése titoknak</span><span class="sxs-lookup"><span data-stu-id="3f26d-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="3f26d-112">Ez a parancs a contoso nevű fő boltozatban a titkos nevű HR-verzió megadott verziójához tartozó címkéket és tartalomtípust törli.</span><span class="sxs-lookup"><span data-stu-id="3f26d-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="3f26d-113">3. példa: a titok jelenlegi verziójának letiltása, akinek a neve vele kezdődik</span><span class="sxs-lookup"><span data-stu-id="3f26d-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="3f26d-114">Az első parancs a contoso karakterlánc értékét a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3f26d-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="3f26d-115">A második parancs a karakterlánc értékét a $Prefix változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3f26d-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="3f26d-116">A harmadik parancs az Get-AzureKeyVaultSecret parancsmagot használja a megadott kulcsfájl titkainak kinyerésére, majd ezeket a titkokat átadja a **Where-Object** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="3f26d-116">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="3f26d-117">A **Where-Object** parancsmag kiszűri a karakterrel kezdődő nevek titkát.</span><span class="sxs-lookup"><span data-stu-id="3f26d-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="3f26d-118">A parancs bekapcsolja a szűrőhöz igazodó titkot az Set-AzureKeyVaultSecretAttribute parancsmaghoz, amely letiltja őket.</span><span class="sxs-lookup"><span data-stu-id="3f26d-118">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="3f26d-119">4. példa: a ContentType beállítása a titok minden verziójában</span><span class="sxs-lookup"><span data-stu-id="3f26d-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="3f26d-120">Az első három parancs a *VaultName* , a *név* és a *ContentType* paraméterben használható karakterlánc-változók definiálását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f26d-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="3f26d-121">A negyedik parancs az Get-AzureKeyVaultKey parancsmagot használja a megadott kulcsok beolvasására, és a kulcsokat a Set-AzureKeyVaultSecretAttribute parancsmagba a tartalomtípusok XML-be való beállításához adja.</span><span class="sxs-lookup"><span data-stu-id="3f26d-121">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="3f26d-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f26d-122">PARAMETERS</span></span>

### <span data-ttu-id="3f26d-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="3f26d-123">-ContentType</span></span>
<span data-ttu-id="3f26d-124">A titok tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f26d-124">Specifies the content type of a secret.</span></span> <span data-ttu-id="3f26d-125">Ha nem adja meg ezt a paramétert, az aktuális titok tartalomtípusa nem változik.</span><span class="sxs-lookup"><span data-stu-id="3f26d-125">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="3f26d-126">Ha el szeretné távolítani a meglévő tartalomtípust, adjon meg egy üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="3f26d-126">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="3f26d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f26d-127">-DefaultProfile</span></span>
<span data-ttu-id="3f26d-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3f26d-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f26d-129">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="3f26d-129">-Enable</span></span>
<span data-ttu-id="3f26d-130">Azt jelzi, hogy engedélyezni kell-e a titkot.</span><span class="sxs-lookup"><span data-stu-id="3f26d-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="3f26d-131">A titok engedélyezéséhez $False megadhatja a titkot vagy a $Truet.</span><span class="sxs-lookup"><span data-stu-id="3f26d-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="3f26d-132">Ha nem adja meg ezt a paramétert, az aktuális titok engedélyezett vagy letiltott állapota nem változik.</span><span class="sxs-lookup"><span data-stu-id="3f26d-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="3f26d-133">-Lejár</span><span class="sxs-lookup"><span data-stu-id="3f26d-133">-Expires</span></span>
<span data-ttu-id="3f26d-134">Itt adhatja meg azt a dátumot és időpontot, amikor a titok lejár.</span><span class="sxs-lookup"><span data-stu-id="3f26d-134">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="3f26d-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f26d-135">-Name</span></span>
<span data-ttu-id="3f26d-136">A titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f26d-136">Specifies the name of a secret.</span></span> <span data-ttu-id="3f26d-137">Ez a parancsmag a titok teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="3f26d-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f26d-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="3f26d-138">-NotBefore</span></span>
<span data-ttu-id="3f26d-139">Itt adhatja meg azt a koordinált általános időpontot (UTC), amely előtt a titkos kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="3f26d-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="3f26d-140">Ha nem adja meg ezt a paramétert, az aktuális titok NotBefore attribútuma nem változik.</span><span class="sxs-lookup"><span data-stu-id="3f26d-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="3f26d-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f26d-141">-PassThru</span></span>
<span data-ttu-id="3f26d-142">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3f26d-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3f26d-143">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3f26d-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f26d-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="3f26d-144">-Tag</span></span>
<span data-ttu-id="3f26d-145">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3f26d-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3f26d-146">Példa:</span><span class="sxs-lookup"><span data-stu-id="3f26d-146">For example:</span></span>

<span data-ttu-id="3f26d-147">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3f26d-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3f26d-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3f26d-148">-VaultName</span></span>
<span data-ttu-id="3f26d-149">A módosítani kívánt fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f26d-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="3f26d-150">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és az aktuálisan kiválasztott környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="3f26d-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="3f26d-151">-Verzió</span><span class="sxs-lookup"><span data-stu-id="3f26d-151">-Version</span></span>
<span data-ttu-id="3f26d-152">A titok verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f26d-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="3f26d-153">Ez a parancsmag a titkos név, az aktuálisan kijelölt környezet, a titkos név és a titkos verzió alapján építi be a titok teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="3f26d-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="3f26d-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f26d-154">-Confirm</span></span>
<span data-ttu-id="3f26d-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f26d-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f26d-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f26d-156">-WhatIf</span></span>
<span data-ttu-id="3f26d-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f26d-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f26d-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f26d-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f26d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f26d-159">CommonParameters</span></span>
<span data-ttu-id="3f26d-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f26d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f26d-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f26d-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f26d-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f26d-162">INPUTS</span></span>

## <span data-ttu-id="3f26d-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f26d-163">OUTPUTS</span></span>

### <span data-ttu-id="3f26d-164">Microsoft. Azure. Command. kulccsal. modellek. Secret</span><span class="sxs-lookup"><span data-stu-id="3f26d-164">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="3f26d-165">Visszaadja a Microsoft. Azure. Command. kulccsal. models. Secret objektumot, ha a PassThru meg van adva.</span><span class="sxs-lookup"><span data-stu-id="3f26d-165">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="3f26d-166">Ellenkező esetben semmit sem ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3f26d-166">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="3f26d-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f26d-167">NOTES</span></span>

## <span data-ttu-id="3f26d-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f26d-168">RELATED LINKS</span></span>

[<span data-ttu-id="3f26d-169">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3f26d-169">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="3f26d-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3f26d-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="3f26d-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3f26d-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
