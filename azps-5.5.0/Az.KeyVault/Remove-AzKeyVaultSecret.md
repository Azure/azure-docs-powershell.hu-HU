---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 71a0dcebdc889eb8116089eb3c5a5b8379c72b20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209286"
---
# <span data-ttu-id="708db-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="708db-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="708db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="708db-102">SYNOPSIS</span></span>
<span data-ttu-id="708db-103">Egy kulcstárban tárolt titkos kulcsot töröl.</span><span class="sxs-lookup"><span data-stu-id="708db-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="708db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="708db-104">SYNTAX</span></span>

### <span data-ttu-id="708db-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="708db-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="708db-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="708db-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="708db-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="708db-107">DESCRIPTION</span></span>
<span data-ttu-id="708db-108">A Remove-AzKeyVaultSecret parancsmag egy kulcstárban töröl egy titkos adatokat.</span><span class="sxs-lookup"><span data-stu-id="708db-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="708db-109">Ha a titkos adatokat véletlenül törölték, a titkos adatokat Undo-AzKeyVaultSecretRemoval speciális "helyreállítás" engedélyekkel rendelkező felhasználó helyreállíthatja.</span><span class="sxs-lookup"><span data-stu-id="708db-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="708db-110">Ez a parancsmag a **ConfirmImpact** tulajdonság értéke magas.</span><span class="sxs-lookup"><span data-stu-id="708db-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="708db-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="708db-111">EXAMPLES</span></span>

### <span data-ttu-id="708db-112">1. példa: Titkos kulcs eltávolítása egy kulcstárból</span><span class="sxs-lookup"><span data-stu-id="708db-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="708db-113">Ez a parancs eltávolítja a FinanceSecret nevű titkos kulcsot a Contoso nevű kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="708db-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="708db-114">2. példa: Titkos kulcs eltávolítása a kulcstárból a felhasználó jóváhagyása nélkül</span><span class="sxs-lookup"><span data-stu-id="708db-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="708db-115">Ez a parancs eltávolítja a FinanceSecret nevű titkos kulcsot a Contoso nevű kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="708db-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="708db-116">A parancs megadja  az  Kényszerítés és a Megerősítés paramétert, ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="708db-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="708db-117">3. példa: Véglegesen törölt titkos kulcs törlése a kulcstárból</span><span class="sxs-lookup"><span data-stu-id="708db-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="708db-118">Ez a parancs véglegesen eltávolítja a FinanceSecret nevű titkos kulcsot a Contoso nevű kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="708db-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="708db-119">A parancsmag végrehajtatása "végleges végleges" engedélyt igényel, amelynek korábban és explicit módon meg kellett adni a felhasználónak ehhez a kulcstárhoz.</span><span class="sxs-lookup"><span data-stu-id="708db-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="708db-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="708db-120">PARAMETERS</span></span>

### <span data-ttu-id="708db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708db-121">-DefaultProfile</span></span>
<span data-ttu-id="708db-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="708db-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="708db-123">-Force</span><span class="sxs-lookup"><span data-stu-id="708db-123">-Force</span></span>
<span data-ttu-id="708db-124">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="708db-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="708db-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="708db-125">-InputObject</span></span>
<span data-ttu-id="708db-126">Key Vault Secret Object</span><span class="sxs-lookup"><span data-stu-id="708db-126">Key Vault Secret Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="708db-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="708db-127">-InRemovedState</span></span>
<span data-ttu-id="708db-128">Ha van ilyen, véglegesen eltávolítja a korábban törölt titkos adatokat.</span><span class="sxs-lookup"><span data-stu-id="708db-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="708db-129">-Name</span><span class="sxs-lookup"><span data-stu-id="708db-129">-Name</span></span>
<span data-ttu-id="708db-130">Egy titkos elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="708db-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="708db-131">Ez a parancsmag egy titkos kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcstár neve és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="708db-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708db-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="708db-132">-PassThru</span></span>
<span data-ttu-id="708db-133">Azt jelzi, hogy ez a parancsmag **egy Microsoft.Azure.Commands.KeyVault.Models.Secret objektumot** ad vissza.</span><span class="sxs-lookup"><span data-stu-id="708db-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="708db-134">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="708db-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="708db-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="708db-135">-VaultName</span></span>
<span data-ttu-id="708db-136">Annak a kulcstárnak a nevét adja meg, amelyhez a titkos kulcs tartozik.</span><span class="sxs-lookup"><span data-stu-id="708db-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="708db-137">Ez a parancsmag egy kulcstár FQDN-ét építi fel a paraméter által megadott név és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="708db-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708db-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="708db-138">-Confirm</span></span>
<span data-ttu-id="708db-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="708db-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708db-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="708db-140">-WhatIf</span></span>
<span data-ttu-id="708db-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="708db-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="708db-142">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="708db-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="708db-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="708db-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708db-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708db-144">CommonParameters</span></span>
<span data-ttu-id="708db-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="708db-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708db-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="708db-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708db-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="708db-147">INPUTS</span></span>

### <span data-ttu-id="708db-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="708db-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="708db-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="708db-149">OUTPUTS</span></span>

### <span data-ttu-id="708db-150">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="708db-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="708db-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="708db-151">NOTES</span></span>

## <span data-ttu-id="708db-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="708db-152">RELATED LINKS</span></span>

[<span data-ttu-id="708db-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="708db-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="708db-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="708db-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="708db-155">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="708db-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

