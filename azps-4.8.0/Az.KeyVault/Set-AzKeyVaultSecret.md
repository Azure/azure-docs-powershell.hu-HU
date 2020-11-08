---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 0733cf722e26cb52abdb84f7917a78d088f49fd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181885"
---
# <span data-ttu-id="6cdca-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6cdca-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="6cdca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cdca-102">SYNOPSIS</span></span>
<span data-ttu-id="6cdca-103">Titkos kulcsot hoz létre vagy frissít a főboltozatban.</span><span class="sxs-lookup"><span data-stu-id="6cdca-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="6cdca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cdca-104">SYNTAX</span></span>

### <span data-ttu-id="6cdca-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cdca-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cdca-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6cdca-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cdca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cdca-107">DESCRIPTION</span></span>
<span data-ttu-id="6cdca-108">A **set-AzKeyVaultSecret** parancsmag az Azure Key Vault-ban hoz létre vagy frissít egy titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="6cdca-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="6cdca-109">Ha a titok nem létezik, akkor ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6cdca-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="6cdca-110">Ha a titok már létezik, ez a parancsmag a titok új verzióját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6cdca-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="6cdca-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6cdca-111">EXAMPLES</span></span>

### <span data-ttu-id="6cdca-112">Példa 1: a titok értékének módosítása alapértelmezett attribútumokkal</span><span class="sxs-lookup"><span data-stu-id="6cdca-112">Example 1: Modify the value of a secret using default attributes</span></span>
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

<span data-ttu-id="6cdca-113">Az első parancs a karakterláncot egy biztonságos karakterláncba a **ConvertTo-SecureString** parancsmag használatával konvertálja, majd a karakterláncot a $Secret változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6cdca-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="6cdca-114">További információért írja be a következőt: `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="6cdca-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="6cdca-115">A második parancs módosította a contoso nevű ITSecret titkos nevű kulcs értékét.</span><span class="sxs-lookup"><span data-stu-id="6cdca-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="6cdca-116">A titkos érték a $Secretban tárolt érték lesz.</span><span class="sxs-lookup"><span data-stu-id="6cdca-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="6cdca-117">2. példa: a titok értékének módosítása egyéni attribútumok használatával</span><span class="sxs-lookup"><span data-stu-id="6cdca-117">Example 2: Modify the value of a secret using custom attributes</span></span>
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

<span data-ttu-id="6cdca-118">Az első parancs a karakterláncot egy biztonságos karakterláncba a **ConvertTo-SecureString** parancsmag használatával konvertálja, majd a karakterláncot a $Secret változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6cdca-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="6cdca-119">További információért írja be a következőt: `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="6cdca-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="6cdca-120">A következő parancsok a lejárat, a címkék és a környezeti típus egyéni attribútumait határozzák meg, és a változókban tárolják az attribútumokat.</span><span class="sxs-lookup"><span data-stu-id="6cdca-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="6cdca-121">A végleges parancs módosítja a contoso nevű ITSecret titkos nevű kulcsának értékeit a korábban változóként megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="6cdca-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="6cdca-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cdca-122">PARAMETERS</span></span>

### <span data-ttu-id="6cdca-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="6cdca-123">-ContentType</span></span>
<span data-ttu-id="6cdca-124">A titok tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cdca-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="6cdca-125">Ha törölni szeretné a meglévő tartalomtípust, adjon meg egy üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="6cdca-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="6cdca-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cdca-126">-DefaultProfile</span></span>
<span data-ttu-id="6cdca-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6cdca-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cdca-128">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="6cdca-128">-Disable</span></span>
<span data-ttu-id="6cdca-129">Jelzi, hogy ez a parancsmag letiltja a titkot.</span><span class="sxs-lookup"><span data-stu-id="6cdca-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="6cdca-130">-Lejár</span><span class="sxs-lookup"><span data-stu-id="6cdca-130">-Expires</span></span>
<span data-ttu-id="6cdca-131">A lejárati idő **datetime** objektumként adja meg az adott parancsmag által frissített titkot.</span><span class="sxs-lookup"><span data-stu-id="6cdca-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="6cdca-132">Ez a paraméter koordinált univerzális időpontot (UTC) használ.</span><span class="sxs-lookup"><span data-stu-id="6cdca-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="6cdca-133">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6cdca-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="6cdca-134">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6cdca-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="6cdca-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cdca-135">-InputObject</span></span>
<span data-ttu-id="6cdca-136">Titkos objektum</span><span class="sxs-lookup"><span data-stu-id="6cdca-136">Secret object</span></span>

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

### <span data-ttu-id="6cdca-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6cdca-137">-Name</span></span>
<span data-ttu-id="6cdca-138">A módosítandó titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cdca-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="6cdca-139">Ez a parancsmag a titok teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="6cdca-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="6cdca-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="6cdca-140">-NotBefore</span></span>
<span data-ttu-id="6cdca-141">Itt adhatja meg az időt **datetime** objektumként, amely előtt a titok nem használható.</span><span class="sxs-lookup"><span data-stu-id="6cdca-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="6cdca-142">Ez a paraméter az UTC-t használja.</span><span class="sxs-lookup"><span data-stu-id="6cdca-142">This parameter uses UTC.</span></span> <span data-ttu-id="6cdca-143">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6cdca-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="6cdca-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="6cdca-144">-SecretValue</span></span>
<span data-ttu-id="6cdca-145">A titok **SecureString** -objektumként való értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cdca-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="6cdca-146">**SecureString** objektum beolvasásához használja a **ConvertTo-SecureString** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6cdca-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="6cdca-147">További információért írja be a következőt: `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="6cdca-147">For more information, type `Get-Help
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

### <span data-ttu-id="6cdca-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="6cdca-148">-Tag</span></span>
<span data-ttu-id="6cdca-149">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="6cdca-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6cdca-150">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="6cdca-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6cdca-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6cdca-151">-VaultName</span></span>
<span data-ttu-id="6cdca-152">Annak a kulcsnak a neve, amelyhez a titok tartozik.</span><span class="sxs-lookup"><span data-stu-id="6cdca-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="6cdca-153">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="6cdca-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="6cdca-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6cdca-154">-Confirm</span></span>
<span data-ttu-id="6cdca-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6cdca-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cdca-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cdca-156">-WhatIf</span></span>
<span data-ttu-id="6cdca-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6cdca-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cdca-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cdca-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cdca-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cdca-159">CommonParameters</span></span>
<span data-ttu-id="6cdca-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cdca-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cdca-161">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6cdca-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cdca-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cdca-162">INPUTS</span></span>

### <span data-ttu-id="6cdca-163">Microsoft. Azure. Command. PSKeyVaultSecretIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="6cdca-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="6cdca-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cdca-164">OUTPUTS</span></span>

### <span data-ttu-id="6cdca-165">Microsoft. Azure. Command. PSKeyVaultSecret. models.</span><span class="sxs-lookup"><span data-stu-id="6cdca-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="6cdca-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cdca-166">NOTES</span></span>

## <span data-ttu-id="6cdca-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cdca-167">RELATED LINKS</span></span>

[<span data-ttu-id="6cdca-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6cdca-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="6cdca-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6cdca-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
