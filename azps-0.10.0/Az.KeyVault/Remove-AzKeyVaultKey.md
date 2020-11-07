---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 15470f18e457f31deec66554c955890b52e26e83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842102"
---
# <span data-ttu-id="ae1dc-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ae1dc-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="ae1dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1dc-103">Billentyűt töröl a kulcs boltozatáról.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="ae1dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae1dc-104">SYNTAX</span></span>

```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae1dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae1dc-105">DESCRIPTION</span></span>
<span data-ttu-id="ae1dc-106">A Remove-AzKeyVaultKey parancsmag egy billentyűt töröl a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-106">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="ae1dc-107">Ha a kulcsot véletlenül töröltük, a kulcs visszaállítható a Undo-AzKeyVaultKeyRemoval felhasználó által speciális "helyreállítási" engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-107">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="ae1dc-108">A parancsmag értéke magas a **ConfirmImpact** tulajdonság számára.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="ae1dc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ae1dc-109">EXAMPLES</span></span>

### <span data-ttu-id="ae1dc-110">1. példa: kulcs eltávolítása a főboltozatról</span><span class="sxs-lookup"><span data-stu-id="ae1dc-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="ae1dc-111">Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="ae1dc-112">2. példa: kulcs eltávolítása a felhasználó jóváhagyása nélkül</span><span class="sxs-lookup"><span data-stu-id="ae1dc-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="ae1dc-113">Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="ae1dc-114">A parancs az *erő* és a *megerősítés* paramétert adja meg, ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="ae1dc-115">3. példa: a törölt billentyűk végleges kiürítése a kulcs boltozatáról</span><span class="sxs-lookup"><span data-stu-id="ae1dc-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="ae1dc-116">Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso állandóról.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="ae1dc-117">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="ae1dc-118">4. példa: kulcsok eltávolítása a csővezeték-kezelő használatával</span><span class="sxs-lookup"><span data-stu-id="ae1dc-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="ae1dc-119">Ez a parancs a contoso nevű kulcs-boltozat összes kulcsát beolvassa, és a pipeline operátor segítségével átadja őket a **Where-Object** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ae1dc-120">Ez a parancsmag átadja azokat a kulcsokat, amelyek $False értékkel rendelkeznek az **engedélyezett** attribútumhoz az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="ae1dc-121">A parancsmag eltávolítja ezeket a billentyűket.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="ae1dc-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae1dc-122">PARAMETERS</span></span>

### <span data-ttu-id="ae1dc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae1dc-123">-DefaultProfile</span></span>
<span data-ttu-id="ae1dc-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ae1dc-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae1dc-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ae1dc-125">-Force</span></span>
<span data-ttu-id="ae1dc-126">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ae1dc-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="ae1dc-127">-InRemovedState</span></span>
<span data-ttu-id="ae1dc-128">A korábban törölt kulcs végleges eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-128">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="ae1dc-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae1dc-129">-Name</span></span>
<span data-ttu-id="ae1dc-130">Az eltávolítandó kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-130">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="ae1dc-131">Ez a parancsmag a kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-131">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1dc-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae1dc-132">-PassThru</span></span>
<span data-ttu-id="ae1dc-133">Azt jelzi, hogy ez a parancsmag a **Microsoft. Azure. commands.-Vault. models. Bundle** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="ae1dc-134">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ae1dc-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ae1dc-135">-VaultName</span></span>
<span data-ttu-id="ae1dc-136">Annak a kulcsnak a nevét adja meg, amelyből el szeretné távolítani a billentyűt.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-136">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="ae1dc-137">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="ae1dc-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae1dc-138">-Confirm</span></span>
<span data-ttu-id="ae1dc-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae1dc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae1dc-140">-WhatIf</span></span>
<span data-ttu-id="ae1dc-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae1dc-142">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae1dc-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae1dc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1dc-144">CommonParameters</span></span>
<span data-ttu-id="ae1dc-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae1dc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1dc-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae1dc-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1dc-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae1dc-147">INPUTS</span></span>

### <span data-ttu-id="ae1dc-148">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="ae1dc-148">String</span></span>

## <span data-ttu-id="ae1dc-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae1dc-149">OUTPUTS</span></span>

### <span data-ttu-id="ae1dc-150">Microsoft. Azure. Command. DeletedKeyBundle. models.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="ae1dc-151">Ez a parancsmag csak akkor ad értéket, ha a *PassThru* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae1dc-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="ae1dc-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae1dc-152">NOTES</span></span>

## <span data-ttu-id="ae1dc-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae1dc-153">RELATED LINKS</span></span>

[<span data-ttu-id="ae1dc-154">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ae1dc-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="ae1dc-155">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ae1dc-155">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="ae1dc-156">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="ae1dc-156">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="ae1dc-157">Visszavonás – AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="ae1dc-157">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

