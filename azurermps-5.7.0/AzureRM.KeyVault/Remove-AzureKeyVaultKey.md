---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: 5244ed9a8803be07a46c50a15553a4863f7907d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495340"
---
# <span data-ttu-id="9da35-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9da35-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="9da35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9da35-102">SYNOPSIS</span></span>
<span data-ttu-id="9da35-103">Billentyűt töröl a kulcs boltozatáról.</span><span class="sxs-lookup"><span data-stu-id="9da35-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9da35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9da35-104">SYNTAX</span></span>

### <span data-ttu-id="9da35-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9da35-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9da35-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9da35-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9da35-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9da35-107">DESCRIPTION</span></span>
<span data-ttu-id="9da35-108">A Remove-AzureKeyVaultKey parancsmag egy billentyűt töröl a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="9da35-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="9da35-109">Ha a kulcsot véletlenül töröltük, a kulcs visszaállítható a Undo-AzureKeyVaultKeyRemoval felhasználó által speciális "helyreállítási" engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="9da35-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="9da35-110">A parancsmag értéke magas a **ConfirmImpact** tulajdonság számára.</span><span class="sxs-lookup"><span data-stu-id="9da35-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="9da35-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9da35-111">EXAMPLES</span></span>

### <span data-ttu-id="9da35-112">1. példa: kulcs eltávolítása a főboltozatról</span><span class="sxs-lookup"><span data-stu-id="9da35-112">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="9da35-113">Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="9da35-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="9da35-114">2. példa: kulcs eltávolítása a felhasználó jóváhagyása nélkül</span><span class="sxs-lookup"><span data-stu-id="9da35-114">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="9da35-115">Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="9da35-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="9da35-116">A parancs az *erő* és a *megerősítés* paramétert adja meg, ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9da35-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="9da35-117">3. példa: a törölt billentyűk végleges kiürítése a kulcs boltozatáról</span><span class="sxs-lookup"><span data-stu-id="9da35-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="9da35-118">Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso állandóról.</span><span class="sxs-lookup"><span data-stu-id="9da35-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="9da35-119">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="9da35-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="9da35-120">4. példa: kulcsok eltávolítása a csővezeték-kezelő használatával</span><span class="sxs-lookup"><span data-stu-id="9da35-120">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="9da35-121">Ez a parancs a contoso nevű kulcs-boltozat összes kulcsát beolvassa, és a pipeline operátor segítségével átadja őket a **Where-Object** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="9da35-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9da35-122">Ez a parancsmag átadja azokat a kulcsokat, amelyek $False értékkel rendelkeznek az **engedélyezett** attribútumhoz az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="9da35-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="9da35-123">A parancsmag eltávolítja ezeket a billentyűket.</span><span class="sxs-lookup"><span data-stu-id="9da35-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="9da35-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9da35-124">PARAMETERS</span></span>

### <span data-ttu-id="9da35-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da35-125">-DefaultProfile</span></span>
<span data-ttu-id="9da35-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9da35-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9da35-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9da35-127">-Force</span></span>
<span data-ttu-id="9da35-128">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9da35-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9da35-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9da35-129">-InputObject</span></span>
<span data-ttu-id="9da35-130">Köteg objektum</span><span class="sxs-lookup"><span data-stu-id="9da35-130">KeyBundle Object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9da35-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="9da35-131">-InRemovedState</span></span>
<span data-ttu-id="9da35-132">A korábban törölt kulcs végleges eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9da35-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="9da35-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9da35-133">-Name</span></span>
<span data-ttu-id="9da35-134">Az eltávolítandó kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9da35-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="9da35-135">Ez a parancsmag a kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="9da35-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da35-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9da35-136">-PassThru</span></span>
<span data-ttu-id="9da35-137">Azt jelzi, hogy ez a parancsmag a **Microsoft. Azure. commands.-Vault. models. Bundle** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9da35-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="9da35-138">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9da35-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9da35-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9da35-139">-VaultName</span></span>
<span data-ttu-id="9da35-140">Annak a kulcsnak a nevét adja meg, amelyből el szeretné távolítani a billentyűt.</span><span class="sxs-lookup"><span data-stu-id="9da35-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="9da35-141">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="9da35-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da35-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9da35-142">-Confirm</span></span>
<span data-ttu-id="9da35-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9da35-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9da35-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da35-144">-WhatIf</span></span>
<span data-ttu-id="9da35-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9da35-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9da35-146">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9da35-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9da35-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9da35-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9da35-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da35-148">CommonParameters</span></span>
<span data-ttu-id="9da35-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9da35-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da35-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da35-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da35-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9da35-151">INPUTS</span></span>

### <span data-ttu-id="9da35-152">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="9da35-152">String</span></span>

## <span data-ttu-id="9da35-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9da35-153">OUTPUTS</span></span>

### <span data-ttu-id="9da35-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9da35-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>
<span data-ttu-id="9da35-155">Ez a parancsmag csak akkor ad értéket, ha a *PassThru* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="9da35-155">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="9da35-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9da35-156">NOTES</span></span>

## <span data-ttu-id="9da35-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9da35-157">RELATED LINKS</span></span>

[<span data-ttu-id="9da35-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9da35-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="9da35-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9da35-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="9da35-160">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="9da35-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="9da35-161">Visszavonás – AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="9da35-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

