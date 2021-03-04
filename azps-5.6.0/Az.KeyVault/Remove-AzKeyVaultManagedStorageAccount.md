---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ab126ee6bfc6a19f4a3a9997a75a01277437e42d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918873"
---
# <span data-ttu-id="754f7-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="754f7-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="754f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="754f7-102">SYNOPSIS</span></span>
<span data-ttu-id="754f7-103">Eltávolít egy kulcstár által felügyelt Azure Storage-fiókot és az összes hozzá tartozó SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="754f7-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="754f7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="754f7-104">SYNTAX</span></span>

### <span data-ttu-id="754f7-105">ByDefinitionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="754f7-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754f7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="754f7-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="754f7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="754f7-107">DESCRIPTION</span></span>
<span data-ttu-id="754f7-108">Egy Azure-tárfiók társításának megszava a kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="754f7-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="754f7-109">Ez nem távolít el egy Azure-tárfiókot, hanem eltávolítja a fiókkulcsokat az Azure-kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="754f7-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="754f7-110">Az összes társított kulcstár felügyelt TÁROLÓ SAS-definíciója is törlődik.</span><span class="sxs-lookup"><span data-stu-id="754f7-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="754f7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="754f7-111">EXAMPLES</span></span>

### <span data-ttu-id="754f7-112">1. példa: Távolítsa el a kulcstár által felügyelt Azure Storage-fiókot és az összes hozzá tartozó SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="754f7-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="754f7-113">Leállítja az Azure Storage-fiók "mystorageaccount" társítását a myvault kulcstárból, és leállítja a kulcstár kulcskezelését.</span><span class="sxs-lookup"><span data-stu-id="754f7-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="754f7-114">A rendszer nem távolítja el a "mystorageaccount" fiókot.</span><span class="sxs-lookup"><span data-stu-id="754f7-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="754f7-115">Az ezzel a fiókkal társított összes kulcstár által felügyelt TÁROLÓ SAS-definíció el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="754f7-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="754f7-116">2. példa: Felhasználói jóváhagyás nélkül távolítson el egy kulcstár által felügyelt Azure Storage-fiókot és az összes hozzá tartozó SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="754f7-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="754f7-117">Leállítja az Azure Storage-fiók "mystorageaccount" társítását a myvault kulcstárból, és leállítja a kulcstár kulcskezelését.</span><span class="sxs-lookup"><span data-stu-id="754f7-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="754f7-118">A rendszer nem távolítja el a "mystorageaccount" fiókot.</span><span class="sxs-lookup"><span data-stu-id="754f7-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="754f7-119">Az ezzel a fiókkal társított összes kulcstár által felügyelt TÁROLÓ SAS-definíció el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="754f7-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="754f7-120">3. példa: Véglegesen töröljön (véglegesen töröljön) egy kulcstár által felügyelt Azure Storage-fiókot és az összes kapcsolódó SAS-definíciót egy soft-delete-enabled tárolóból.</span><span class="sxs-lookup"><span data-stu-id="754f7-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="754f7-121">A példa feltételezi, hogy a szoftveres törlés engedélyezve van ehhez a tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="754f7-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="754f7-122">Ellenőrizze, hogy ez a helyzet-e a tároló tulajdonságainak vagy a tárolóban egy entitás RecoveryLevel attribútumának vizsgálatával.</span><span class="sxs-lookup"><span data-stu-id="754f7-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="754f7-123">Az első parancsmag leállítja az Azure Storage-fiók "mystorageaccount" társítását a "myvault" kulcstárból, és leállítja a kulcstár kulcskezelését.</span><span class="sxs-lookup"><span data-stu-id="754f7-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="754f7-124">A rendszer nem távolítja el a "mystorageaccount" fiókot.</span><span class="sxs-lookup"><span data-stu-id="754f7-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="754f7-125">Az ezzel a fiókkal társított összes kulcstár által felügyelt TÁROLÓ SAS-definíció el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="754f7-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="754f7-126">A második parancsmag ellenőrzi, hogy a tárfiók törölt, de helyreállítható állapotban van-e.</span><span class="sxs-lookup"><span data-stu-id="754f7-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="754f7-127">Ennek az állapotnak a elérése némi időt igényel, engedélyezze a ~30s-et a próbálkozás előtt.</span><span class="sxs-lookup"><span data-stu-id="754f7-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="754f7-128">A harmadik parancsmag véglegesen eltávolítja a tárfiókot – a helyreállítás már nem lehetséges.</span><span class="sxs-lookup"><span data-stu-id="754f7-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="754f7-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="754f7-129">PARAMETERS</span></span>

### <span data-ttu-id="754f7-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="754f7-130">-AccountName</span></span>
<span data-ttu-id="754f7-131">Key Vault managed storage account name.</span><span class="sxs-lookup"><span data-stu-id="754f7-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="754f7-132">A parancsmag egy felügyelt tárfiók nevének FQDN-ét építi fel a tárolónévből, az aktuálisan kijelölt környezetből és a felügyelt tárfiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="754f7-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754f7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="754f7-133">-DefaultProfile</span></span>
<span data-ttu-id="754f7-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="754f7-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="754f7-135">-Force</span><span class="sxs-lookup"><span data-stu-id="754f7-135">-Force</span></span>
<span data-ttu-id="754f7-136">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="754f7-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="754f7-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="754f7-137">-InputObject</span></span>
<span data-ttu-id="754f7-138">ManagedStorageAccount objektum.</span><span class="sxs-lookup"><span data-stu-id="754f7-138">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="754f7-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="754f7-139">-InRemovedState</span></span>
<span data-ttu-id="754f7-140">Távolítsa el véglegesen a korábban törölt felügyelt tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="754f7-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="754f7-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="754f7-141">-PassThru</span></span>
<span data-ttu-id="754f7-142">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="754f7-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="754f7-143">Ha ez a kapcsoló meg van adva, a parancsmag a törölt felügyelt tárfiókot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="754f7-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="754f7-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="754f7-144">-VaultName</span></span>
<span data-ttu-id="754f7-145">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="754f7-145">Vault name.</span></span>
<span data-ttu-id="754f7-146">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="754f7-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754f7-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="754f7-147">-Confirm</span></span>
<span data-ttu-id="754f7-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="754f7-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="754f7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="754f7-149">-WhatIf</span></span>
<span data-ttu-id="754f7-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="754f7-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="754f7-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="754f7-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="754f7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="754f7-152">CommonParameters</span></span>
<span data-ttu-id="754f7-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="754f7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="754f7-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="754f7-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="754f7-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="754f7-155">INPUTS</span></span>

### <span data-ttu-id="754f7-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="754f7-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="754f7-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="754f7-157">OUTPUTS</span></span>

### <span data-ttu-id="754f7-158">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="754f7-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="754f7-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="754f7-159">NOTES</span></span>

## <span data-ttu-id="754f7-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="754f7-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

