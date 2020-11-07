---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: 3e2da64d467d71721255afa12211530e7c0d9f08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666175"
---
# <span data-ttu-id="aabea-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="aabea-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="aabea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aabea-102">SYNOPSIS</span></span>
<span data-ttu-id="aabea-103">Tanúsítvány eltávolítása egy kulcs-boltozatból.</span><span class="sxs-lookup"><span data-stu-id="aabea-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="aabea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aabea-104">SYNTAX</span></span>

### <span data-ttu-id="aabea-105">ByVaultNameAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aabea-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aabea-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="aabea-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aabea-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aabea-107">DESCRIPTION</span></span>
<span data-ttu-id="aabea-108">A **Remove-AzKeyVaultCertificate** parancsmag eltávolítja a tanúsítványt egy kulcs boltozatról.</span><span class="sxs-lookup"><span data-stu-id="aabea-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="aabea-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aabea-109">EXAMPLES</span></span>

### <span data-ttu-id="aabea-110">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aabea-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       4/11/2018 4:28:39 PM

                     [Not After]
                       10/11/2018 4:38:39 PM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contosokv01.vault.azure.net:443/keys/selfsigned01/968c3920884a435abf8faea11f565456
SecretId           : https://contosokv01.vault.azure.net:443/secrets/selfsigned01/968c3920884a435abf8faea11f565456
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Purgeable
ScheduledPurgeDate :
DeletedDate        :
Enabled            : True
Expires            : 10/11/2018 11:38:39 PM
NotBefore          : 4/11/2018 11:28:39 PM
Created            : 4/11/2018 11:38:39 PM
Updated            : 4/11/2018 11:38:39 PM
Tags               :
VaultName          : ContosoKV01
Name               : SelfSigned01
Version            : 968c3920884a435abf8faea11f565456
Id                 : https://contosokv01.vault.azure.net:443/certificates/selfsigned01/968c3920884a435abf8faea11f565456
```

<span data-ttu-id="aabea-111">Ez a parancs eltávolítja a SelfSigned01 nevű tanúsítványt a ContosoKV01 nevű kulcs-boltozatból.</span><span class="sxs-lookup"><span data-stu-id="aabea-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="aabea-112">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabea-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="aabea-113">Ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aabea-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="aabea-114">2. példa: a törölt tanúsítvány végleges kiürítése a kulcs boltozatáról</span><span class="sxs-lookup"><span data-stu-id="aabea-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="aabea-115">Ez a parancs véglegesen eltávolítja a "MyCert" nevű tanúsítványt a "contoso" nevű kulcs boltozatról.</span><span class="sxs-lookup"><span data-stu-id="aabea-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="aabea-116">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak ebben a kulcsban.</span><span class="sxs-lookup"><span data-stu-id="aabea-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="aabea-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aabea-117">PARAMETERS</span></span>

### <span data-ttu-id="aabea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aabea-118">-DefaultProfile</span></span>
<span data-ttu-id="aabea-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aabea-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aabea-120">-Force</span><span class="sxs-lookup"><span data-stu-id="aabea-120">-Force</span></span>
<span data-ttu-id="aabea-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="aabea-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aabea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aabea-122">-InputObject</span></span>
<span data-ttu-id="aabea-123">Certificate objektum.</span><span class="sxs-lookup"><span data-stu-id="aabea-123">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="aabea-124">-InRemovedState</span></span>
<span data-ttu-id="aabea-125">Ha van, eltávolítja a korábban törölt tanúsítványt véglegesen</span><span class="sxs-lookup"><span data-stu-id="aabea-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="aabea-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aabea-126">-Name</span></span>
<span data-ttu-id="aabea-127">Annak a tanúsítványnak a nevét adja meg, amelyet a parancsmag a fő boltozattól távolít el.</span><span class="sxs-lookup"><span data-stu-id="aabea-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="aabea-128">Ez a parancsmag a tanúsítvány teljes tartománynevét (FQDN) építi a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="aabea-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aabea-129">-PassThru</span></span>
<span data-ttu-id="aabea-130">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="aabea-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aabea-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="aabea-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aabea-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="aabea-132">-VaultName</span></span>
<span data-ttu-id="aabea-133">Annak a kulcsnak a neve, amelyből a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="aabea-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="aabea-134">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="aabea-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aabea-135">-Confirm</span></span>
<span data-ttu-id="aabea-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aabea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aabea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aabea-137">-WhatIf</span></span>
<span data-ttu-id="aabea-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aabea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aabea-139">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aabea-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aabea-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aabea-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aabea-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabea-141">CommonParameters</span></span>
<span data-ttu-id="aabea-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aabea-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabea-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aabea-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabea-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aabea-144">INPUTS</span></span>

### <span data-ttu-id="aabea-145">Microsoft. Azure. Command. PSKeyVaultCertificateIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="aabea-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="aabea-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aabea-146">OUTPUTS</span></span>

### <span data-ttu-id="aabea-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="aabea-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="aabea-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aabea-148">NOTES</span></span>

## <span data-ttu-id="aabea-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aabea-149">RELATED LINKS</span></span>

[<span data-ttu-id="aabea-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="aabea-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="aabea-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="aabea-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="aabea-152">Importálás – AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="aabea-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="aabea-153">Visszavonás – AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="aabea-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
