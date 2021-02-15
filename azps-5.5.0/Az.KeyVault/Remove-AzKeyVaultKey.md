---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: e78b6729061efe5a83f31bd25b9e542c09627ca3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152770"
---
# <span data-ttu-id="8574c-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8574c-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="8574c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8574c-102">SYNOPSIS</span></span>
<span data-ttu-id="8574c-103">Kulcs törlése a kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="8574c-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="8574c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8574c-104">SYNTAX</span></span>

### <span data-ttu-id="8574c-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8574c-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8574c-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="8574c-106">HsmByVaultName</span></span>
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8574c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8574c-107">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8574c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8574c-108">DESCRIPTION</span></span>
<span data-ttu-id="8574c-109">A Remove-AzKeyVaultKey parancsmag törli a kulcsot a kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="8574c-109">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="8574c-110">Ha a kulcsot véletlenül törölték, a kulcsot a speciális "helyreállításUndo-AzKeyVaultKeyRemoval engedéllyel rendelkező felhasználó helyreállíthatja.</span><span class="sxs-lookup"><span data-stu-id="8574c-110">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="8574c-111">Ez a parancsmag a **ConfirmImpact** tulajdonság értéke magas.</span><span class="sxs-lookup"><span data-stu-id="8574c-111">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="8574c-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8574c-112">EXAMPLES</span></span>

### <span data-ttu-id="8574c-113">1. példa: Kulcs eltávolítása egy kulcstárból</span><span class="sxs-lookup"><span data-stu-id="8574c-113">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="8574c-114">Ez a parancs eltávolítja az ITSoftware nevű kulcsot a Contoso nevű kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="8574c-114">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="8574c-115">2. példa: Kulcs eltávolítása a felhasználó jóváhagyása nélkül</span><span class="sxs-lookup"><span data-stu-id="8574c-115">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="8574c-116">Ez a parancs eltávolítja az ITSoftware nevű kulcsot a Contoso nevű kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="8574c-116">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="8574c-117">A parancs megadja a *Force* paramétert, ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8574c-117">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8574c-118">3. példa: Törölt kulcs végleges törlése a kulcstárból</span><span class="sxs-lookup"><span data-stu-id="8574c-118">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="8574c-119">Ez a parancs véglegesen eltávolítja az ITSoftware nevű kulcsot a Contoso nevű kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="8574c-119">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="8574c-120">A parancsmag végrehajtatása "végleges végleges" engedélyt igényel, amelynek korábban és explicit módon meg kellett adni a felhasználónak ehhez a kulcstárhoz.</span><span class="sxs-lookup"><span data-stu-id="8574c-120">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="8574c-121">4. példa: Kulcsok eltávolítása a folyamat műveleti operátorával</span><span class="sxs-lookup"><span data-stu-id="8574c-121">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="8574c-122">Ez a parancs begyűjte a Contoso nevű kulcstár összes kulcsát, és átadja őket a **Where-Object** parancsmagnak a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="8574c-122">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8574c-123">Ez a parancsmag átadja az Engedélyezett $False értékkel  rendelkező kulcsokat az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="8574c-123">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="8574c-124">Ez a parancsmag eltávolítja ezeket a kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="8574c-124">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="8574c-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8574c-125">PARAMETERS</span></span>

### <span data-ttu-id="8574c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8574c-126">-DefaultProfile</span></span>
<span data-ttu-id="8574c-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8574c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8574c-128">-Force</span><span class="sxs-lookup"><span data-stu-id="8574c-128">-Force</span></span>
<span data-ttu-id="8574c-129">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="8574c-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8574c-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="8574c-130">-HsmName</span></span>
<span data-ttu-id="8574c-131">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="8574c-131">HSM name.</span></span> <span data-ttu-id="8574c-132">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="8574c-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8574c-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8574c-133">-InputObject</span></span>
<span data-ttu-id="8574c-134">KeyBundle objektum</span><span class="sxs-lookup"><span data-stu-id="8574c-134">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8574c-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8574c-135">-InRemovedState</span></span>
<span data-ttu-id="8574c-136">Távolítsa el véglegesen a korábban törölt kulcsot.</span><span class="sxs-lookup"><span data-stu-id="8574c-136">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="8574c-137">-Name</span><span class="sxs-lookup"><span data-stu-id="8574c-137">-Name</span></span>
<span data-ttu-id="8574c-138">Az eltávolítható kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="8574c-138">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="8574c-139">Ez a parancsmag egy kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcstár neve és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="8574c-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8574c-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8574c-140">-PassThru</span></span>
<span data-ttu-id="8574c-141">Azt jelzi, hogy ez a parancsmag **egy Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey objektumot ad** vissza.</span><span class="sxs-lookup"><span data-stu-id="8574c-141">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="8574c-142">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8574c-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8574c-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8574c-143">-VaultName</span></span>
<span data-ttu-id="8574c-144">Annak a kulcstárnak a nevét adja meg, amelyből el szeretné távolítani a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="8574c-144">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="8574c-145">Ez a parancsmag egy kulcstár FQDN-ét építi fel a paraméter által megadott név és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="8574c-145">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8574c-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8574c-146">-Confirm</span></span>
<span data-ttu-id="8574c-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8574c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8574c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8574c-148">-WhatIf</span></span>
<span data-ttu-id="8574c-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8574c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8574c-150">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8574c-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8574c-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8574c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8574c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8574c-152">CommonParameters</span></span>
<span data-ttu-id="8574c-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8574c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8574c-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8574c-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8574c-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8574c-155">INPUTS</span></span>

### <span data-ttu-id="8574c-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8574c-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="8574c-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8574c-157">OUTPUTS</span></span>

### <span data-ttu-id="8574c-158">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultKey billentyű</span><span class="sxs-lookup"><span data-stu-id="8574c-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="8574c-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8574c-159">NOTES</span></span>

## <span data-ttu-id="8574c-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8574c-160">RELATED LINKS</span></span>

[<span data-ttu-id="8574c-161">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8574c-161">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="8574c-162">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8574c-162">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="8574c-163">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="8574c-163">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="8574c-164">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="8574c-164">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

