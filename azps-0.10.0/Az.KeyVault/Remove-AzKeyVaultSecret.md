---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: db46a3dd8669d5c8eeeb85aeafc25654faa8c107
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842093"
---
# <span data-ttu-id="704d7-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="704d7-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="704d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="704d7-102">SYNOPSIS</span></span>
<span data-ttu-id="704d7-103">Titkos kulcs törlése a főboltozatról.</span><span class="sxs-lookup"><span data-stu-id="704d7-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="704d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="704d7-104">SYNTAX</span></span>

```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="704d7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="704d7-105">DESCRIPTION</span></span>
<span data-ttu-id="704d7-106">A Remove-AzKeyVaultSecret parancsmag a kulcsfájl titkos kulcsát törli.</span><span class="sxs-lookup"><span data-stu-id="704d7-106">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="704d7-107">Ha a titkot véletlenül töröltük, a titkos kódot helyreállíthatja a felhasználó által a speciális "Recover" engedélyekkel rendelkező felhasználó Undo-AzKeyVaultSecretRemoval használatával.</span><span class="sxs-lookup"><span data-stu-id="704d7-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="704d7-108">A parancsmag értéke magas a **ConfirmImpact** tulajdonság számára.</span><span class="sxs-lookup"><span data-stu-id="704d7-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="704d7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="704d7-109">EXAMPLES</span></span>

### <span data-ttu-id="704d7-110">1. példa: titkos kulcs eltávolítása a főboltozatról</span><span class="sxs-lookup"><span data-stu-id="704d7-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="704d7-111">Ez a parancs eltávolítja a FinanceSecret nevű titkos nevet a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="704d7-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="704d7-112">2. példa: titkos kulcs eltávolítása a felhasználó jóváhagyása nélkül</span><span class="sxs-lookup"><span data-stu-id="704d7-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="704d7-113">Ez a parancs eltávolítja a FinanceSecret nevű titkos nevet a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="704d7-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="704d7-114">A parancs az *erő* és a *megerősítés* paramétert adja meg, ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="704d7-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="704d7-115">3. példa: a törölt titkos elemek végleges kiürítése a Key Vault-ból</span><span class="sxs-lookup"><span data-stu-id="704d7-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="704d7-116">Ebben a parancsban a contoso véglegesen nevű FinanceSecret származó titkos nevű titkos kulcs látható.</span><span class="sxs-lookup"><span data-stu-id="704d7-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="704d7-117">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="704d7-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="704d7-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="704d7-118">PARAMETERS</span></span>

### <span data-ttu-id="704d7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704d7-119">-DefaultProfile</span></span>
<span data-ttu-id="704d7-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="704d7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="704d7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="704d7-121">-Force</span></span>
<span data-ttu-id="704d7-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="704d7-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="704d7-123">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="704d7-123">-InRemovedState</span></span>
<span data-ttu-id="704d7-124">Ha van, eltávolíthatja véglegesen a korábban törölt titkot.</span><span class="sxs-lookup"><span data-stu-id="704d7-124">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="704d7-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="704d7-125">-Name</span></span>
<span data-ttu-id="704d7-126">A titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="704d7-126">Specifies the name of a secret.</span></span>
<span data-ttu-id="704d7-127">Ez a parancsmag a titok teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="704d7-127">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="704d7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="704d7-128">-PassThru</span></span>
<span data-ttu-id="704d7-129">Azt jelzi, hogy ez a parancsmag a **Microsoft. Azure. Command. kulccsal. models. Secret** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="704d7-129">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="704d7-130">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="704d7-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="704d7-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="704d7-131">-VaultName</span></span>
<span data-ttu-id="704d7-132">Annak a fő boltozatnak a neve, amelyhez a titok tartozik.</span><span class="sxs-lookup"><span data-stu-id="704d7-132">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="704d7-133">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="704d7-133">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="704d7-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="704d7-134">-Confirm</span></span>
<span data-ttu-id="704d7-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="704d7-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="704d7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="704d7-136">-WhatIf</span></span>
<span data-ttu-id="704d7-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="704d7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="704d7-138">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="704d7-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="704d7-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="704d7-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="704d7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704d7-140">CommonParameters</span></span>
<span data-ttu-id="704d7-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="704d7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704d7-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="704d7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704d7-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="704d7-143">INPUTS</span></span>

### <span data-ttu-id="704d7-144">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="704d7-144">String</span></span>

## <span data-ttu-id="704d7-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="704d7-145">OUTPUTS</span></span>

### <span data-ttu-id="704d7-146">Microsoft. Azure. Command. DeletedSecret. models.</span><span class="sxs-lookup"><span data-stu-id="704d7-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="704d7-147">Ez a parancsmag csak akkor ad értéket, ha a *PassThru* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="704d7-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="704d7-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="704d7-148">NOTES</span></span>

## <span data-ttu-id="704d7-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="704d7-149">RELATED LINKS</span></span>

[<span data-ttu-id="704d7-150">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="704d7-150">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="704d7-151">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="704d7-151">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="704d7-152">Visszavonás – AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="704d7-152">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

