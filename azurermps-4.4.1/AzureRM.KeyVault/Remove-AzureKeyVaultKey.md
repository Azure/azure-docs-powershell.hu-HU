---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://go.microsoft.com/fwlink/?LinkId=690299
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: b5f2917da71e8c4539660dbb91dd81f3fb5d7959
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502715"
---
# <span data-ttu-id="ee4cc-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ee4cc-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="ee4cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee4cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4cc-103">Billentyűt töröl a kulcs boltozatáról.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee4cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee4cc-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee4cc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee4cc-105">DESCRIPTION</span></span>
<span data-ttu-id="ee4cc-106">A Remove-AzureKeyVaultKey parancsmag egy billentyűt töröl a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-106">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="ee4cc-107">Ha a kulcsot véletlenül töröltük, a kulcs visszaállítható a Undo-AzureKeyVaultKeyRemoval felhasználó által speciális "helyreállítási" engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-107">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="ee4cc-108">A parancsmag értéke magas a **ConfirmImpact** tulajdonság számára.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="ee4cc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ee4cc-109">EXAMPLES</span></span>

### <span data-ttu-id="ee4cc-110">1. példa: kulcs eltávolítása a főboltozatról</span><span class="sxs-lookup"><span data-stu-id="ee4cc-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="ee4cc-111">Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="ee4cc-112">2. példa: kulcs eltávolítása a felhasználó jóváhagyása nélkül</span><span class="sxs-lookup"><span data-stu-id="ee4cc-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="ee4cc-113">Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso nevű kulcsból.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="ee4cc-114">A parancs az *erő* és a *megerősítés* paramétert adja meg, ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="ee4cc-115">3. példa: a törölt billentyűk végleges kiürítése a kulcs boltozatáról</span><span class="sxs-lookup"><span data-stu-id="ee4cc-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="ee4cc-116">Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso állandóról.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="ee4cc-117">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="ee4cc-118">4. példa: kulcsok eltávolítása a csővezeték-kezelő használatával</span><span class="sxs-lookup"><span data-stu-id="ee4cc-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="ee4cc-119">Ez a parancs a contoso nevű kulcs-boltozat összes kulcsát beolvassa, és a pipeline operátor segítségével átadja őket a **Where-Object** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ee4cc-120">Ez a parancsmag átadja azokat a kulcsokat, amelyek $False értékkel rendelkeznek az **engedélyezett** attribútumhoz az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="ee4cc-121">A parancsmag eltávolítja ezeket a billentyűket.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="ee4cc-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee4cc-122">PARAMETERS</span></span>

### <span data-ttu-id="ee4cc-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ee4cc-123">-Force</span></span>
<span data-ttu-id="ee4cc-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ee4cc-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="ee4cc-125">-InRemovedState</span></span>
<span data-ttu-id="ee4cc-126">A korábban törölt kulcs végleges eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-126">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="ee4cc-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee4cc-127">-Name</span></span>
<span data-ttu-id="ee4cc-128">Az eltávolítandó kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-128">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="ee4cc-129">Ez a parancsmag a kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-129">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee4cc-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee4cc-130">-PassThru</span></span>
<span data-ttu-id="ee4cc-131">Azt jelzi, hogy ez a parancsmag a **Microsoft. Azure. commands.-Vault. models. Bundle** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-131">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="ee4cc-132">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee4cc-133">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ee4cc-133">-VaultName</span></span>
<span data-ttu-id="ee4cc-134">Annak a kulcsnak a nevét adja meg, amelyből el szeretné távolítani a billentyűt.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-134">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="ee4cc-135">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-135">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="ee4cc-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee4cc-136">-Confirm</span></span>
<span data-ttu-id="ee4cc-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee4cc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee4cc-138">-WhatIf</span></span>
<span data-ttu-id="ee4cc-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee4cc-140">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-140">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee4cc-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee4cc-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee4cc-142">-DefaultProfile</span></span>
<span data-ttu-id="ee4cc-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee4cc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4cc-144">CommonParameters</span></span>
<span data-ttu-id="ee4cc-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee4cc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4cc-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee4cc-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4cc-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee4cc-147">INPUTS</span></span>

### <span data-ttu-id="ee4cc-148">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="ee4cc-148">String</span></span>

## <span data-ttu-id="ee4cc-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee4cc-149">OUTPUTS</span></span>

### <span data-ttu-id="ee4cc-150">Microsoft. Azure. Command. DeletedKeyBundle. models.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="ee4cc-151">Ez a parancsmag csak akkor ad értéket, ha a *PassThru* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee4cc-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="ee4cc-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee4cc-152">NOTES</span></span>

## <span data-ttu-id="ee4cc-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee4cc-153">RELATED LINKS</span></span>

[<span data-ttu-id="ee4cc-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ee4cc-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="ee4cc-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ee4cc-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="ee4cc-156">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="ee4cc-156">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="ee4cc-157">Visszavonás – AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="ee4cc-157">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

