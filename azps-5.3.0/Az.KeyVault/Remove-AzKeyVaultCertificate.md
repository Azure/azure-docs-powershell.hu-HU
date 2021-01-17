---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: c6d99fb2b6b568b090cb0ed86277b06fcde28115
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465962"
---
# <span data-ttu-id="2854e-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2854e-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="2854e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2854e-102">SYNOPSIS</span></span>
<span data-ttu-id="2854e-103">Eltávolít egy tanúsítványt egy kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="2854e-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="2854e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2854e-104">SYNTAX</span></span>

### <span data-ttu-id="2854e-105">ByVaultNameAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2854e-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2854e-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="2854e-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2854e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2854e-107">DESCRIPTION</span></span>
<span data-ttu-id="2854e-108">A **Remove-AzKeyVaultCertificate** parancsmag eltávolítja a tanúsítványt a kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="2854e-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="2854e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2854e-109">EXAMPLES</span></span>

### <span data-ttu-id="2854e-110">1. példa: Tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2854e-110">Example 1: Remove a certificate</span></span>
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

<span data-ttu-id="2854e-111">Ez a parancs eltávolítja a SelfSigned01 nevű tanúsítványt a ContosoKV01 nevű kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="2854e-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="2854e-112">Ez a parancs a *Force paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="2854e-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2854e-113">Ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2854e-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="2854e-114">2. példa: A törölt tanúsítvány végleges törlése a kulcstárolóból</span><span class="sxs-lookup"><span data-stu-id="2854e-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="2854e-115">Ez a parancs véglegesen eltávolítja a "MyCert" nevű tanúsítványt a "Contoso" kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="2854e-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="2854e-116">A parancsmag végrehajtatása "végleges végleges" engedélyt igényel, amelyet korábban és kifejezetten a kulcstárban adott meg a felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="2854e-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="2854e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2854e-117">PARAMETERS</span></span>

### <span data-ttu-id="2854e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2854e-118">-DefaultProfile</span></span>
<span data-ttu-id="2854e-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2854e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2854e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2854e-120">-Force</span></span>
<span data-ttu-id="2854e-121">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2854e-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2854e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2854e-122">-InputObject</span></span>
<span data-ttu-id="2854e-123">Tanúsítványobjektum.</span><span class="sxs-lookup"><span data-stu-id="2854e-123">Certificate Object.</span></span>

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

### <span data-ttu-id="2854e-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="2854e-124">-InRemovedState</span></span>
<span data-ttu-id="2854e-125">Ha van ilyen, véglegesen eltávolítja a korábban törölt tanúsítványt</span><span class="sxs-lookup"><span data-stu-id="2854e-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="2854e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2854e-126">-Name</span></span>
<span data-ttu-id="2854e-127">Annak a tanúsítványnak a nevét adja meg, amelyről a parancsmag eltávolítja a kulcstárolót.</span><span class="sxs-lookup"><span data-stu-id="2854e-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="2854e-128">Ez a parancsmag egy tanúsítvány teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcstároló neve és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="2854e-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="2854e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2854e-129">-PassThru</span></span>
<span data-ttu-id="2854e-130">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="2854e-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2854e-131">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2854e-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2854e-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2854e-132">-VaultName</span></span>
<span data-ttu-id="2854e-133">Annak a kulcstárolónak a neve, amelyből a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="2854e-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="2854e-134">Ez a parancsmag egy kulcstár FQDN-ét építi fel a paraméter által megadott név és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="2854e-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="2854e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2854e-135">-Confirm</span></span>
<span data-ttu-id="2854e-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2854e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2854e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2854e-137">-WhatIf</span></span>
<span data-ttu-id="2854e-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2854e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2854e-139">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2854e-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2854e-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2854e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2854e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2854e-141">CommonParameters</span></span>
<span data-ttu-id="2854e-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2854e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2854e-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2854e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2854e-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2854e-144">INPUTS</span></span>

### <span data-ttu-id="2854e-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2854e-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="2854e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2854e-146">OUTPUTS</span></span>

### <span data-ttu-id="2854e-147">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultCertificate eletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2854e-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="2854e-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2854e-148">NOTES</span></span>

## <span data-ttu-id="2854e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2854e-149">RELATED LINKS</span></span>

[<span data-ttu-id="2854e-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2854e-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="2854e-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2854e-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="2854e-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2854e-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="2854e-153">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="2854e-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
