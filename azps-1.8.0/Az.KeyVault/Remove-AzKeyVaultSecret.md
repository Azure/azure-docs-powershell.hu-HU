---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 2c52d6cbd5a3e027baf41959d28816f63062b046
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835670"
---
# <span data-ttu-id="f7a8c-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f7a8c-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="f7a8c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a8c-103">Titkos kulcs törlése a főboltozatról.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="f7a8c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7a8c-104">SYNTAX</span></span>

### <span data-ttu-id="f7a8c-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7a8c-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7a8c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f7a8c-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7a8c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7a8c-107">DESCRIPTION</span></span>
<span data-ttu-id="f7a8c-108">A Remove-AzKeyVaultSecret parancsmag a kulcsfájl titkos kulcsát törli.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="f7a8c-109">Ha a titkot véletlenül töröltük, a titkos kódot helyreállíthatja a felhasználó által a speciális "Recover" engedélyekkel rendelkező felhasználó Undo-AzKeyVaultSecretRemoval használatával.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="f7a8c-110">A parancsmag értéke magas a **ConfirmImpact** tulajdonság számára.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="f7a8c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f7a8c-111">EXAMPLES</span></span>

### <span data-ttu-id="f7a8c-112">1. példa: titkos kulcs eltávolítása a főboltozatról</span><span class="sxs-lookup"><span data-stu-id="f7a8c-112">Example 1: Remove a secret from a key vault</span></span>
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

<span data-ttu-id="f7a8c-113">Ez a parancs eltávolítja a FinanceSecret nevű titkos nevet a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="f7a8c-114">2. példa: titkos kulcs eltávolítása a felhasználó jóváhagyása nélkül</span><span class="sxs-lookup"><span data-stu-id="f7a8c-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
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

<span data-ttu-id="f7a8c-115">Ez a parancs eltávolítja a FinanceSecret nevű titkos nevet a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="f7a8c-116">A parancs az *erő* és a *megerősítés* paramétert adja meg, ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="f7a8c-117">3. példa: a törölt titkos elemek végleges kiürítése a Key Vault-ból</span><span class="sxs-lookup"><span data-stu-id="f7a8c-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="f7a8c-118">Ebben a parancsban a contoso véglegesen nevű FinanceSecret származó titkos nevű titkos kulcs látható.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="f7a8c-119">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="f7a8c-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7a8c-120">PARAMETERS</span></span>

### <span data-ttu-id="f7a8c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a8c-121">-DefaultProfile</span></span>
<span data-ttu-id="f7a8c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f7a8c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7a8c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f7a8c-123">-Force</span></span>
<span data-ttu-id="f7a8c-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f7a8c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7a8c-125">-InputObject</span></span>
<span data-ttu-id="f7a8c-126">A Key Vault titkos objektuma</span><span class="sxs-lookup"><span data-stu-id="f7a8c-126">Key Vault Secret Object</span></span>

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

### <span data-ttu-id="f7a8c-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f7a8c-127">-InRemovedState</span></span>
<span data-ttu-id="f7a8c-128">Ha van, eltávolíthatja véglegesen a korábban törölt titkot.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="f7a8c-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7a8c-129">-Name</span></span>
<span data-ttu-id="f7a8c-130">A titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="f7a8c-131">Ez a parancsmag a titok teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="f7a8c-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7a8c-132">-PassThru</span></span>
<span data-ttu-id="f7a8c-133">Azt jelzi, hogy ez a parancsmag a **Microsoft. Azure. Command. kulccsal. models. Secret** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="f7a8c-134">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f7a8c-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f7a8c-135">-VaultName</span></span>
<span data-ttu-id="f7a8c-136">Annak a fő boltozatnak a neve, amelyhez a titok tartozik.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="f7a8c-137">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="f7a8c-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7a8c-138">-Confirm</span></span>
<span data-ttu-id="f7a8c-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7a8c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7a8c-140">-WhatIf</span></span>
<span data-ttu-id="f7a8c-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7a8c-142">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7a8c-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7a8c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a8c-144">CommonParameters</span></span>
<span data-ttu-id="f7a8c-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7a8c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a8c-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7a8c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a8c-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7a8c-147">INPUTS</span></span>

### <span data-ttu-id="f7a8c-148">Microsoft. Azure. Command. PSKeyVaultSecretIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="f7a8c-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="f7a8c-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7a8c-149">OUTPUTS</span></span>

### <span data-ttu-id="f7a8c-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f7a8c-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="f7a8c-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7a8c-151">NOTES</span></span>

## <span data-ttu-id="f7a8c-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7a8c-152">RELATED LINKS</span></span>

[<span data-ttu-id="f7a8c-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f7a8c-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="f7a8c-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f7a8c-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="f7a8c-155">Visszavonás – AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="f7a8c-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

