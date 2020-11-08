---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185289"
---
# <span data-ttu-id="fcda4-101">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fcda4-101">Remove-AzManagedHsmKey</span></span>

## <span data-ttu-id="fcda4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcda4-102">SYNOPSIS</span></span>
<span data-ttu-id="fcda4-103">Egy felügyelt HSM kulcsának törlése</span><span class="sxs-lookup"><span data-stu-id="fcda4-103">Deletes a key in a managed HSM.</span></span>

## <span data-ttu-id="fcda4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcda4-104">SYNTAX</span></span>

### <span data-ttu-id="fcda4-105">RemoveByKeyNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fcda4-105">RemoveByKeyNameParameterSet (Default)</span></span>
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcda4-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcda4-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcda4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcda4-107">DESCRIPTION</span></span>
<span data-ttu-id="fcda4-108">A Remove-AzManagedHsmKey parancsmag a felügyelt HSM-beli kulcsokat törli.</span><span class="sxs-lookup"><span data-stu-id="fcda4-108">The Remove-AzManagedHsmKey cmdlet deletes a key in a managed HSM.</span></span>
<span data-ttu-id="fcda4-109">Ha a kulcsot véletlenül töröltük, a kulcs visszaállítható a Undo-AzManagedHsmKeyRemoval felhasználó által speciális "helyreállítási" engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="fcda4-109">If the key was accidentally deleted the key can be recovered using Undo-AzManagedHsmKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="fcda4-110">A parancsmag értéke magas a **ConfirmImpact** tulajdonság számára.</span><span class="sxs-lookup"><span data-stu-id="fcda4-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="fcda4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fcda4-111">EXAMPLES</span></span>

### <span data-ttu-id="fcda4-112">1. példa: kulcs eltávolítása a felügyelt HSM-ből</span><span class="sxs-lookup"><span data-stu-id="fcda4-112">Example 1: Remove a key from a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="fcda4-113">Ez a parancs eltávolítja a testkey nevű kulcsot a testmhsm nevű felügyelt HSM-ből.</span><span class="sxs-lookup"><span data-stu-id="fcda4-113">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="fcda4-114">2. példa: kulcs eltávolítása a felhasználó jóváhagyása nélkül</span><span class="sxs-lookup"><span data-stu-id="fcda4-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

<span data-ttu-id="fcda4-115">Ez a parancs eltávolítja a testkey nevű kulcsot a testmhsm nevű felügyelt HSM-ből.</span><span class="sxs-lookup"><span data-stu-id="fcda4-115">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>
<span data-ttu-id="fcda4-116">A parancs az *erő* paramétert adja meg, ezért a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fcda4-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="fcda4-117">3. példa: törölt kulcsok végleges törlése a felügyelt HSM-ből</span><span class="sxs-lookup"><span data-stu-id="fcda4-117">Example 3: Purge a deleted key from the managed HSM permanently</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

<span data-ttu-id="fcda4-118">Ez a parancs eltávolítja a testkey nevű kulcsot véglegesen a testmhsm nevű felügyelt HSM-ből.</span><span class="sxs-lookup"><span data-stu-id="fcda4-118">This command removes the key named testkey from the managed HSM named testmhsm permanently.</span></span>
<span data-ttu-id="fcda4-119">A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak a felügyelt HSM számára.</span><span class="sxs-lookup"><span data-stu-id="fcda4-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this managed HSM.</span></span>

### <span data-ttu-id="fcda4-120">4. példa: kulcsok eltávolítása a csővezeték-kezelő használatával</span><span class="sxs-lookup"><span data-stu-id="fcda4-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

<span data-ttu-id="fcda4-121">Ez a parancs a testmhsm nevű felügyelt HSM összes kulcsát beolvassa, és a csővezeték-kezelő segítségével átadja őket a **Where-Object** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="fcda4-121">This command gets all the keys in the managed HSM named testmhsm and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fcda4-122">Ez a parancsmag átadja azokat a kulcsokat, amelyek $False értékkel rendelkeznek az **engedélyezett** attribútumhoz az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fcda4-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="fcda4-123">A parancsmag eltávolítja ezeket a billentyűket.</span><span class="sxs-lookup"><span data-stu-id="fcda4-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="fcda4-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcda4-124">PARAMETERS</span></span>

### <span data-ttu-id="fcda4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcda4-125">-DefaultProfile</span></span>
<span data-ttu-id="fcda4-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcda4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcda4-127">-Force</span><span class="sxs-lookup"><span data-stu-id="fcda4-127">-Force</span></span>
<span data-ttu-id="fcda4-128">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fcda4-128">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fcda4-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="fcda4-129">-HsmName</span></span>
<span data-ttu-id="fcda4-130">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="fcda4-130">HSM name.</span></span> <span data-ttu-id="fcda4-131">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="fcda4-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcda4-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcda4-132">-InputObject</span></span>
<span data-ttu-id="fcda4-133">Fő objektum</span><span class="sxs-lookup"><span data-stu-id="fcda4-133">Key Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcda4-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="fcda4-134">-InRemovedState</span></span>
<span data-ttu-id="fcda4-135">A korábban törölt kulcs végleges eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="fcda4-135">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="fcda4-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fcda4-136">-Name</span></span>
<span data-ttu-id="fcda4-137">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="fcda4-137">Key name.</span></span>
<span data-ttu-id="fcda4-138">Parancsmag: a felügyelt HSM-név, az aktuálisan kijelölt környezet és a kulcsnév alapján egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="fcda4-138">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcda4-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcda4-139">-PassThru</span></span>
<span data-ttu-id="fcda4-140">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="fcda4-140">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fcda4-141">Ha meg van adva ez a kapcsoló, a parancsmag a törölt kulcs objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fcda4-141">If this switch is specified, the cmdlet returns the key object that was deleted.</span></span>

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

### <span data-ttu-id="fcda4-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fcda4-142">-Confirm</span></span>
<span data-ttu-id="fcda4-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fcda4-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcda4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcda4-144">-WhatIf</span></span>
<span data-ttu-id="fcda4-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fcda4-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcda4-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fcda4-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcda4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcda4-147">CommonParameters</span></span>
<span data-ttu-id="fcda4-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcda4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcda4-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fcda4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcda4-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcda4-150">INPUTS</span></span>

### <span data-ttu-id="fcda4-151">Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="fcda4-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="fcda4-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcda4-152">OUTPUTS</span></span>

### <span data-ttu-id="fcda4-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fcda4-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="fcda4-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcda4-154">NOTES</span></span>

## <span data-ttu-id="fcda4-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcda4-155">RELATED LINKS</span></span>

[<span data-ttu-id="fcda4-156">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fcda4-156">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="fcda4-157">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fcda4-157">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="fcda4-158">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fcda4-158">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="fcda4-159">Visszavonás – AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="fcda4-159">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="fcda4-160">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fcda4-160">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="fcda4-161">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fcda4-161">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)