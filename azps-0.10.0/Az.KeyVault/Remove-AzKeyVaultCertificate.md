---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: b2e7264b5c0f54f18e295a86f9abb1cbd51dc4b8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842125"
---
# <span data-ttu-id="6094d-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6094d-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="6094d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6094d-102">SYNOPSIS</span></span>
<span data-ttu-id="6094d-103">Tanúsítvány eltávolítása egy kulcs-boltozatból.</span><span class="sxs-lookup"><span data-stu-id="6094d-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="6094d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6094d-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6094d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6094d-105">DESCRIPTION</span></span>
<span data-ttu-id="6094d-106">A **Remove-AzKeyVaultCertificate** parancsmag eltávolítja a tanúsítványt egy kulcs boltozatról.</span><span class="sxs-lookup"><span data-stu-id="6094d-106">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="6094d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6094d-107">EXAMPLES</span></span>

### <span data-ttu-id="6094d-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6094d-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="6094d-109">Ez a parancs eltávolítja a SelfSigned01 nevű tanúsítványt a ContosoKV01 nevű kulcs-boltozatból.</span><span class="sxs-lookup"><span data-stu-id="6094d-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="6094d-110">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="6094d-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6094d-111">Ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6094d-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="6094d-112">3. példa: a törölt tanúsítvány végleges kiürítése a kulcs boltozatáról</span><span class="sxs-lookup"><span data-stu-id="6094d-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="6094d-113">Ez a parancs véglegesen eltávolítja a "MyCert" nevű tanúsítványt a "contoso" nevű kulcs boltozatról.</span><span class="sxs-lookup"><span data-stu-id="6094d-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="6094d-114">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak ebben a kulcsban.</span><span class="sxs-lookup"><span data-stu-id="6094d-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="6094d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6094d-115">PARAMETERS</span></span>

### <span data-ttu-id="6094d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6094d-116">-DefaultProfile</span></span>
<span data-ttu-id="6094d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6094d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6094d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6094d-118">-Force</span></span>
<span data-ttu-id="6094d-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6094d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6094d-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="6094d-120">-InRemovedState</span></span>
<span data-ttu-id="6094d-121">Ha van, eltávolítja a korábban törölt tanúsítványt véglegesen</span><span class="sxs-lookup"><span data-stu-id="6094d-121">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="6094d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6094d-122">-Name</span></span>
<span data-ttu-id="6094d-123">Annak a tanúsítványnak a nevét adja meg, amelyet a parancsmag a fő boltozattól távolít el.</span><span class="sxs-lookup"><span data-stu-id="6094d-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="6094d-124">Ez a parancsmag a tanúsítvány teljes tartománynevét (FQDN) építi a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="6094d-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6094d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6094d-125">-PassThru</span></span>
<span data-ttu-id="6094d-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6094d-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6094d-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6094d-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6094d-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6094d-128">-VaultName</span></span>
<span data-ttu-id="6094d-129">Annak a kulcsnak a neve, amelyből a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="6094d-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="6094d-130">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="6094d-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="6094d-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6094d-131">-Confirm</span></span>
<span data-ttu-id="6094d-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6094d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6094d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6094d-133">-WhatIf</span></span>
<span data-ttu-id="6094d-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6094d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6094d-135">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6094d-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6094d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6094d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6094d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6094d-137">CommonParameters</span></span>
<span data-ttu-id="6094d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6094d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6094d-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6094d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6094d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6094d-140">INPUTS</span></span>

### <span data-ttu-id="6094d-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="6094d-141">None</span></span>
<span data-ttu-id="6094d-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6094d-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6094d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6094d-143">OUTPUTS</span></span>

### <span data-ttu-id="6094d-144">Microsoft. Azure. Command. CertificateBundle. models.</span><span class="sxs-lookup"><span data-stu-id="6094d-144">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="6094d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6094d-145">NOTES</span></span>

## <span data-ttu-id="6094d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6094d-146">RELATED LINKS</span></span>

[<span data-ttu-id="6094d-147">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6094d-147">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="6094d-148">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6094d-148">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="6094d-149">Importálás – AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6094d-149">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="6094d-150">Visszavonás – AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="6094d-150">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
