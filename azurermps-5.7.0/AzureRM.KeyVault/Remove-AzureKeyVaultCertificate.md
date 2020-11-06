---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 6c8fcc5476ea2defda78ea03cc1acce7b7e3dea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502564"
---
# <span data-ttu-id="77942-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="77942-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="77942-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77942-102">SYNOPSIS</span></span>
<span data-ttu-id="77942-103">Tanúsítvány eltávolítása egy kulcs-boltozatból.</span><span class="sxs-lookup"><span data-stu-id="77942-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77942-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77942-104">SYNTAX</span></span>

### <span data-ttu-id="77942-105">ByVaultNameAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77942-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77942-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="77942-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77942-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="77942-107">DESCRIPTION</span></span>
<span data-ttu-id="77942-108">A **Remove-AzureKeyVaultCertificate** parancsmag eltávolítja a tanúsítványt egy kulcs boltozatról.</span><span class="sxs-lookup"><span data-stu-id="77942-108">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="77942-109">Példák</span><span class="sxs-lookup"><span data-stu-id="77942-109">EXAMPLES</span></span>

### <span data-ttu-id="77942-110">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="77942-110">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="77942-111">Ez a parancs eltávolítja a SelfSigned01 nevű tanúsítványt a ContosoKV01 nevű kulcs-boltozatból.</span><span class="sxs-lookup"><span data-stu-id="77942-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="77942-112">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="77942-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="77942-113">Ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77942-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="77942-114">3. példa: a törölt tanúsítvány végleges kiürítése a kulcs boltozatáról</span><span class="sxs-lookup"><span data-stu-id="77942-114">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="77942-115">Ez a parancs véglegesen eltávolítja a "MyCert" nevű tanúsítványt a "contoso" nevű kulcs boltozatról.</span><span class="sxs-lookup"><span data-stu-id="77942-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="77942-116">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak ebben a kulcsban.</span><span class="sxs-lookup"><span data-stu-id="77942-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="77942-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77942-117">PARAMETERS</span></span>

### <span data-ttu-id="77942-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77942-118">-DefaultProfile</span></span>
<span data-ttu-id="77942-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="77942-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77942-120">-Force</span><span class="sxs-lookup"><span data-stu-id="77942-120">-Force</span></span>
<span data-ttu-id="77942-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="77942-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77942-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77942-122">-InputObject</span></span>
<span data-ttu-id="77942-123">Certificate objektum.</span><span class="sxs-lookup"><span data-stu-id="77942-123">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77942-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="77942-124">-InRemovedState</span></span>
<span data-ttu-id="77942-125">Ha van, eltávolítja a korábban törölt tanúsítványt véglegesen</span><span class="sxs-lookup"><span data-stu-id="77942-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="77942-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77942-126">-Name</span></span>
<span data-ttu-id="77942-127">Annak a tanúsítványnak a nevét adja meg, amelyet a parancsmag a fő boltozattól távolít el.</span><span class="sxs-lookup"><span data-stu-id="77942-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="77942-128">Ez a parancsmag a tanúsítvány teljes tartománynevét (FQDN) építi a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="77942-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77942-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77942-129">-PassThru</span></span>
<span data-ttu-id="77942-130">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="77942-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="77942-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="77942-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="77942-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="77942-132">-VaultName</span></span>
<span data-ttu-id="77942-133">Annak a kulcsnak a neve, amelyből a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="77942-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="77942-134">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="77942-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77942-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77942-135">-Confirm</span></span>
<span data-ttu-id="77942-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77942-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77942-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77942-137">-WhatIf</span></span>
<span data-ttu-id="77942-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77942-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77942-139">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77942-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77942-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77942-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77942-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77942-141">CommonParameters</span></span>
<span data-ttu-id="77942-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77942-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77942-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77942-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77942-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77942-144">INPUTS</span></span>

### <span data-ttu-id="77942-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="77942-145">None</span></span>
<span data-ttu-id="77942-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="77942-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77942-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77942-147">OUTPUTS</span></span>

### <span data-ttu-id="77942-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="77942-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="77942-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77942-149">NOTES</span></span>

## <span data-ttu-id="77942-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77942-150">RELATED LINKS</span></span>

[<span data-ttu-id="77942-151">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="77942-151">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="77942-152">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="77942-152">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="77942-153">Importálás – AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="77942-153">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="77942-154">Visszavonás – AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="77942-154">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)