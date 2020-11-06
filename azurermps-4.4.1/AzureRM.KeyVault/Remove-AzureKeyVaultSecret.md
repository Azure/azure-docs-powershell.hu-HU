---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690300
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: e5ec1e2377b9a1c04fc10ce976bd800227baabed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502700"
---
# <span data-ttu-id="e5697-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e5697-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="e5697-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5697-102">SYNOPSIS</span></span>
<span data-ttu-id="e5697-103">Titkos kulcs törlése a főboltozatról.</span><span class="sxs-lookup"><span data-stu-id="e5697-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5697-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5697-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5697-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5697-105">DESCRIPTION</span></span>
<span data-ttu-id="e5697-106">A Remove-AzureKeyVaultSecret parancsmag a kulcsfájl titkos kulcsát törli.</span><span class="sxs-lookup"><span data-stu-id="e5697-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="e5697-107">Ha a titkot véletlenül töröltük, a titkos kódot helyreállíthatja a felhasználó által a speciális "Recover" engedélyekkel rendelkező felhasználó Undo-AzureKeyVaultSecretRemoval használatával.</span><span class="sxs-lookup"><span data-stu-id="e5697-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="e5697-108">A parancsmag értéke magas a **ConfirmImpact** tulajdonság számára.</span><span class="sxs-lookup"><span data-stu-id="e5697-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="e5697-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e5697-109">EXAMPLES</span></span>

### <span data-ttu-id="e5697-110">1. példa: titkos kulcs eltávolítása a főboltozatról</span><span class="sxs-lookup"><span data-stu-id="e5697-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="e5697-111">Ez a parancs eltávolítja a FinanceSecret nevű titkos nevet a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="e5697-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="e5697-112">2. példa: titkos kulcs eltávolítása a felhasználó jóváhagyása nélkül</span><span class="sxs-lookup"><span data-stu-id="e5697-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="e5697-113">Ez a parancs eltávolítja a FinanceSecret nevű titkos nevet a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="e5697-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="e5697-114">A parancs az *erő* és a *megerősítés* paramétert adja meg, ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5697-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="e5697-115">3. példa: a törölt titkos elemek végleges kiürítése a Key Vault-ból</span><span class="sxs-lookup"><span data-stu-id="e5697-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="e5697-116">Ebben a parancsban a contoso véglegesen nevű FinanceSecret származó titkos nevű titkos kulcs látható.</span><span class="sxs-lookup"><span data-stu-id="e5697-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="e5697-117">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="e5697-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="e5697-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5697-118">PARAMETERS</span></span>

### <span data-ttu-id="e5697-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e5697-119">-Force</span></span>
<span data-ttu-id="e5697-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e5697-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5697-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e5697-121">-InRemovedState</span></span>
<span data-ttu-id="e5697-122">Ha van, eltávolíthatja véglegesen a korábban törölt titkot.</span><span class="sxs-lookup"><span data-stu-id="e5697-122">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="e5697-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5697-123">-Name</span></span>
<span data-ttu-id="e5697-124">A titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5697-124">Specifies the name of a secret.</span></span>
<span data-ttu-id="e5697-125">Ez a parancsmag a titok teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="e5697-125">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5697-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5697-126">-PassThru</span></span>
<span data-ttu-id="e5697-127">Azt jelzi, hogy ez a parancsmag a **Microsoft. Azure. Command. kulccsal. models. Secret** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e5697-127">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="e5697-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e5697-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e5697-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e5697-129">-VaultName</span></span>
<span data-ttu-id="e5697-130">Annak a fő boltozatnak a neve, amelyhez a titok tartozik.</span><span class="sxs-lookup"><span data-stu-id="e5697-130">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="e5697-131">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="e5697-131">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5697-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5697-132">-Confirm</span></span>
<span data-ttu-id="e5697-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5697-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5697-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5697-134">-WhatIf</span></span>
<span data-ttu-id="e5697-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5697-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5697-136">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5697-136">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5697-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5697-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5697-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5697-138">-DefaultProfile</span></span>
<span data-ttu-id="e5697-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5697-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5697-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5697-140">CommonParameters</span></span>
<span data-ttu-id="e5697-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5697-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5697-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5697-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5697-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5697-143">INPUTS</span></span>

### <span data-ttu-id="e5697-144">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="e5697-144">String</span></span>

## <span data-ttu-id="e5697-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5697-145">OUTPUTS</span></span>

### <span data-ttu-id="e5697-146">Microsoft. Azure. Command. DeletedSecret. models.</span><span class="sxs-lookup"><span data-stu-id="e5697-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="e5697-147">Ez a parancsmag csak akkor ad értéket, ha a *PassThru* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5697-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="e5697-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5697-148">NOTES</span></span>

## <span data-ttu-id="e5697-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5697-149">RELATED LINKS</span></span>

[<span data-ttu-id="e5697-150">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e5697-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="e5697-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e5697-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="e5697-152">Visszavonás – AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="e5697-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

