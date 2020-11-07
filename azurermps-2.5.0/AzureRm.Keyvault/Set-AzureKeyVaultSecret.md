---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 0c482d3fd4e2e02221799ea72e61eacc80ff9e2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849985"
---
# <span data-ttu-id="0e520-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e520-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="0e520-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e520-102">SYNOPSIS</span></span>
<span data-ttu-id="0e520-103">Titkos kulcsot hoz létre vagy frissít a főboltozatban.</span><span class="sxs-lookup"><span data-stu-id="0e520-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e520-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e520-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e520-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e520-105">DESCRIPTION</span></span>
<span data-ttu-id="0e520-106">A **set-AzureKeyVaultSecret** parancsmag az Azure Key Vault-ban hoz létre vagy frissít egy titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="0e520-106">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="0e520-107">Ha a titok nem létezik, akkor ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0e520-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="0e520-108">Ha a titok már létezik, ez a parancsmag a titok új verzióját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0e520-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="0e520-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0e520-109">EXAMPLES</span></span>

### <span data-ttu-id="0e520-110">Példa 1: a titok értékének módosítása alapértelmezett attribútumokkal</span><span class="sxs-lookup"><span data-stu-id="0e520-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="0e520-111">Az első parancs a karakterláncot egy biztonságos karakterláncba a **ConvertTo-SecureString** parancsmag használatával konvertálja, majd a karakterláncot a $Secret változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0e520-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="0e520-112">További információért írja be a következőt: `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="0e520-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="0e520-113">A második parancs módosította a contoso nevű ITSecret titkos nevű kulcs értékét.</span><span class="sxs-lookup"><span data-stu-id="0e520-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="0e520-114">A titkos érték a $Secretban tárolt érték lesz.</span><span class="sxs-lookup"><span data-stu-id="0e520-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="0e520-115">2. példa: a titok értékének módosítása egyéni attribútumok használatával</span><span class="sxs-lookup"><span data-stu-id="0e520-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="0e520-116">Az első parancs a karakterláncot egy biztonságos karakterláncba a **ConvertTo-SecureString** parancsmag használatával konvertálja, majd a karakterláncot a $Secret változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0e520-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="0e520-117">További információért írja be a következőt: `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="0e520-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="0e520-118">A következő parancsok a lejárat, a címkék és a környezeti típus egyéni attribútumait határozzák meg, és a változókban tárolják az attribútumokat.</span><span class="sxs-lookup"><span data-stu-id="0e520-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="0e520-119">A végleges parancs módosítja a contoso nevű ITSecret titkos nevű kulcsának értékeit a korábban változóként megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="0e520-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="0e520-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e520-120">PARAMETERS</span></span>

### <span data-ttu-id="0e520-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="0e520-121">-ContentType</span></span>
<span data-ttu-id="0e520-122">A titok tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e520-122">Specifies the content type of a secret.</span></span>
<span data-ttu-id="0e520-123">Ha törölni szeretné a meglévő tartalomtípust, adjon meg egy üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="0e520-123">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="0e520-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e520-124">-DefaultProfile</span></span>
<span data-ttu-id="0e520-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0e520-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e520-126">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="0e520-126">-Disable</span></span>
<span data-ttu-id="0e520-127">Jelzi, hogy ez a parancsmag letiltja a titkot.</span><span class="sxs-lookup"><span data-stu-id="0e520-127">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="0e520-128">-Lejár</span><span class="sxs-lookup"><span data-stu-id="0e520-128">-Expires</span></span>
<span data-ttu-id="0e520-129">A lejárati idő **datetime** objektumként adja meg az adott parancsmag által frissített titkot.</span><span class="sxs-lookup"><span data-stu-id="0e520-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="0e520-130">Ez a paraméter koordinált univerzális időpontot (UTC) használ.</span><span class="sxs-lookup"><span data-stu-id="0e520-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="0e520-131">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0e520-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0e520-132">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0e520-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="0e520-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0e520-133">-Name</span></span>
<span data-ttu-id="0e520-134">A módosítandó titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e520-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="0e520-135">Ez a parancsmag a titok teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="0e520-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="0e520-136">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="0e520-136">-NotBefore</span></span>
<span data-ttu-id="0e520-137">Itt adhatja meg az időt **datetime** objektumként, amely előtt a titok nem használható.</span><span class="sxs-lookup"><span data-stu-id="0e520-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="0e520-138">Ez a paraméter az UTC-t használja.</span><span class="sxs-lookup"><span data-stu-id="0e520-138">This parameter uses UTC.</span></span> <span data-ttu-id="0e520-139">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0e520-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="0e520-140">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="0e520-140">-SecretValue</span></span>
<span data-ttu-id="0e520-141">A titok **SecureString** -objektumként való értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e520-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="0e520-142">**SecureString** objektum beolvasásához használja a **ConvertTo-SecureString** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0e520-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="0e520-143">További információért írja be a következőt: `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="0e520-143">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e520-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="0e520-144">-Tag</span></span>
<span data-ttu-id="0e520-145">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="0e520-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0e520-146">Példa:</span><span class="sxs-lookup"><span data-stu-id="0e520-146">For example:</span></span>

<span data-ttu-id="0e520-147">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="0e520-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0e520-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0e520-148">-VaultName</span></span>
<span data-ttu-id="0e520-149">Annak a kulcsnak a neve, amelyhez a titok tartozik.</span><span class="sxs-lookup"><span data-stu-id="0e520-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="0e520-150">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="0e520-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="0e520-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0e520-151">-Confirm</span></span>
<span data-ttu-id="0e520-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0e520-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e520-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e520-153">-WhatIf</span></span>
<span data-ttu-id="0e520-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0e520-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e520-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e520-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e520-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e520-156">CommonParameters</span></span>
<span data-ttu-id="0e520-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e520-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e520-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e520-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e520-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e520-159">INPUTS</span></span>

## <span data-ttu-id="0e520-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e520-160">OUTPUTS</span></span>

### <span data-ttu-id="0e520-161">Microsoft. Azure. Command. kulccsal. modellek. Secret</span><span class="sxs-lookup"><span data-stu-id="0e520-161">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="0e520-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e520-162">NOTES</span></span>

## <span data-ttu-id="0e520-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e520-163">RELATED LINKS</span></span>

[<span data-ttu-id="0e520-164">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e520-164">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="0e520-165">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e520-165">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
