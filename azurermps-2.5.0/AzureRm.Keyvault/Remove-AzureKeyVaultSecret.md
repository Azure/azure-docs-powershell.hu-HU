---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 56cc6b11c517379f1d13ebe2dbf2cee00f18211b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848210"
---
# <span data-ttu-id="8dc63-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8dc63-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="8dc63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8dc63-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc63-103">Titkos kulcs törlése a főboltozatról.</span><span class="sxs-lookup"><span data-stu-id="8dc63-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dc63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8dc63-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc63-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8dc63-105">DESCRIPTION</span></span>
<span data-ttu-id="8dc63-106">A Remove-AzureKeyVaultSecret parancsmag a kulcsfájl titkos kulcsát törli.</span><span class="sxs-lookup"><span data-stu-id="8dc63-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="8dc63-107">Ha a titkot véletlenül töröltük, a titkos kódot helyreállíthatja a felhasználó által a speciális "Recover" engedélyekkel rendelkező felhasználó Undo-AzureKeyVaultSecretRemoval használatával.</span><span class="sxs-lookup"><span data-stu-id="8dc63-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="8dc63-108">A parancsmag értéke magas a **ConfirmImpact** tulajdonság számára.</span><span class="sxs-lookup"><span data-stu-id="8dc63-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="8dc63-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8dc63-109">EXAMPLES</span></span>

### <span data-ttu-id="8dc63-110">1. példa: titkos kulcs eltávolítása a főboltozatról</span><span class="sxs-lookup"><span data-stu-id="8dc63-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="8dc63-111">Ez a parancs eltávolítja a FinanceSecret nevű titkos nevet a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="8dc63-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="8dc63-112">2. példa: titkos kulcs eltávolítása a felhasználó jóváhagyása nélkül</span><span class="sxs-lookup"><span data-stu-id="8dc63-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="8dc63-113">Ez a parancs eltávolítja a FinanceSecret nevű titkos nevet a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="8dc63-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="8dc63-114">A parancs az *erő* és a *megerősítés* paramétert adja meg, ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8dc63-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8dc63-115">3. példa: a törölt titkos elemek végleges kiürítése a Key Vault-ból</span><span class="sxs-lookup"><span data-stu-id="8dc63-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="8dc63-116">Ebben a parancsban a contoso véglegesen nevű FinanceSecret származó titkos nevű titkos kulcs látható.</span><span class="sxs-lookup"><span data-stu-id="8dc63-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="8dc63-117">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="8dc63-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="8dc63-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8dc63-118">PARAMETERS</span></span>

### <span data-ttu-id="8dc63-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc63-119">-DefaultProfile</span></span>
<span data-ttu-id="8dc63-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8dc63-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dc63-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8dc63-121">-Force</span></span>
<span data-ttu-id="8dc63-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8dc63-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8dc63-123">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8dc63-123">-InRemovedState</span></span>
<span data-ttu-id="8dc63-124">Ha van, eltávolíthatja véglegesen a korábban törölt titkot.</span><span class="sxs-lookup"><span data-stu-id="8dc63-124">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="8dc63-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8dc63-125">-Name</span></span>
<span data-ttu-id="8dc63-126">A titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8dc63-126">Specifies the name of a secret.</span></span>
<span data-ttu-id="8dc63-127">Ez a parancsmag a titok teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="8dc63-127">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="8dc63-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dc63-128">-PassThru</span></span>
<span data-ttu-id="8dc63-129">Azt jelzi, hogy ez a parancsmag a **Microsoft. Azure. Command. kulccsal. models. Secret** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8dc63-129">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="8dc63-130">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8dc63-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8dc63-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8dc63-131">-VaultName</span></span>
<span data-ttu-id="8dc63-132">Annak a fő boltozatnak a neve, amelyhez a titok tartozik.</span><span class="sxs-lookup"><span data-stu-id="8dc63-132">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="8dc63-133">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="8dc63-133">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="8dc63-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8dc63-134">-Confirm</span></span>
<span data-ttu-id="8dc63-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8dc63-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc63-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc63-136">-WhatIf</span></span>
<span data-ttu-id="8dc63-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8dc63-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc63-138">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8dc63-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc63-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8dc63-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc63-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc63-140">CommonParameters</span></span>
<span data-ttu-id="8dc63-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8dc63-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc63-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dc63-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc63-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8dc63-143">INPUTS</span></span>

### <span data-ttu-id="8dc63-144">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="8dc63-144">String</span></span>

## <span data-ttu-id="8dc63-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8dc63-145">OUTPUTS</span></span>

### <span data-ttu-id="8dc63-146">Microsoft. Azure. Command. DeletedSecret. models.</span><span class="sxs-lookup"><span data-stu-id="8dc63-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="8dc63-147">Ez a parancsmag csak akkor ad értéket, ha a *PassThru* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="8dc63-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="8dc63-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8dc63-148">NOTES</span></span>

## <span data-ttu-id="8dc63-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8dc63-149">RELATED LINKS</span></span>

[<span data-ttu-id="8dc63-150">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8dc63-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="8dc63-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8dc63-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="8dc63-152">Visszavonás – AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="8dc63-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

