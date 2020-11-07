---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 662304cff991da0d9ffe9d946e63bc94ba51e4a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848241"
---
# <span data-ttu-id="413bf-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="413bf-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="413bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="413bf-102">SYNOPSIS</span></span>
<span data-ttu-id="413bf-103">Tanúsítvány eltávolítása egy kulcs-boltozatból.</span><span class="sxs-lookup"><span data-stu-id="413bf-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="413bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="413bf-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="413bf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="413bf-105">DESCRIPTION</span></span>
<span data-ttu-id="413bf-106">A **Remove-AzureKeyVaultCertificate** parancsmag eltávolítja a tanúsítványt egy kulcs boltozatról.</span><span class="sxs-lookup"><span data-stu-id="413bf-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="413bf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="413bf-107">EXAMPLES</span></span>

### <span data-ttu-id="413bf-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="413bf-108">Example 1: Remove a certificate</span></span>
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

<span data-ttu-id="413bf-109">Ez a parancs eltávolítja a SelfSigned01 nevű tanúsítványt a ContosoKV01 nevű kulcs-boltozatból.</span><span class="sxs-lookup"><span data-stu-id="413bf-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="413bf-110">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="413bf-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="413bf-111">Ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="413bf-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="413bf-112">3. példa: a törölt tanúsítvány végleges kiürítése a kulcs boltozatáról</span><span class="sxs-lookup"><span data-stu-id="413bf-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="413bf-113">Ez a parancs véglegesen eltávolítja a "MyCert" nevű tanúsítványt a "contoso" nevű kulcs boltozatról.</span><span class="sxs-lookup"><span data-stu-id="413bf-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="413bf-114">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak ebben a kulcsban.</span><span class="sxs-lookup"><span data-stu-id="413bf-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="413bf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="413bf-115">PARAMETERS</span></span>

### <span data-ttu-id="413bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413bf-116">-DefaultProfile</span></span>
<span data-ttu-id="413bf-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="413bf-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="413bf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="413bf-118">-Force</span></span>
<span data-ttu-id="413bf-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="413bf-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="413bf-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="413bf-120">-InRemovedState</span></span>
<span data-ttu-id="413bf-121">Ha van, eltávolítja a korábban törölt tanúsítványt véglegesen</span><span class="sxs-lookup"><span data-stu-id="413bf-121">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="413bf-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="413bf-122">-Name</span></span>
<span data-ttu-id="413bf-123">Annak a tanúsítványnak a nevét adja meg, amelyet a parancsmag a fő boltozattól távolít el.</span><span class="sxs-lookup"><span data-stu-id="413bf-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="413bf-124">Ez a parancsmag a tanúsítvány teljes tartománynevét (FQDN) építi a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="413bf-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="413bf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="413bf-125">-PassThru</span></span>
<span data-ttu-id="413bf-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="413bf-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="413bf-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="413bf-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="413bf-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="413bf-128">-VaultName</span></span>
<span data-ttu-id="413bf-129">Annak a kulcsnak a neve, amelyből a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="413bf-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="413bf-130">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="413bf-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="413bf-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="413bf-131">-Confirm</span></span>
<span data-ttu-id="413bf-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="413bf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="413bf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="413bf-133">-WhatIf</span></span>
<span data-ttu-id="413bf-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="413bf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="413bf-135">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="413bf-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="413bf-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="413bf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="413bf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413bf-137">CommonParameters</span></span>
<span data-ttu-id="413bf-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="413bf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413bf-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413bf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413bf-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="413bf-140">INPUTS</span></span>

## <span data-ttu-id="413bf-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="413bf-141">OUTPUTS</span></span>

### <span data-ttu-id="413bf-142">Microsoft. Azure. Command. CertificateBundle. models.</span><span class="sxs-lookup"><span data-stu-id="413bf-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="413bf-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="413bf-143">NOTES</span></span>

## <span data-ttu-id="413bf-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="413bf-144">RELATED LINKS</span></span>

[<span data-ttu-id="413bf-145">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="413bf-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="413bf-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="413bf-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="413bf-147">Importálás – AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="413bf-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="413bf-148">Visszavonás – AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="413bf-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
