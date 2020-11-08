---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181725"
---
# <span data-ttu-id="496be-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="496be-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="496be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="496be-102">SYNOPSIS</span></span>
<span data-ttu-id="496be-103">A felügyelt Azure Storage-fiók és az összes társított biztonsági társítási definíció eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="496be-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="496be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="496be-104">SYNTAX</span></span>

### <span data-ttu-id="496be-105">ByDefinitionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="496be-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496be-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="496be-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="496be-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="496be-107">DESCRIPTION</span></span>
<span data-ttu-id="496be-108">Az Azure Storage-fiók társítása a Key Vault-ról</span><span class="sxs-lookup"><span data-stu-id="496be-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="496be-109">Ez a művelet nem távolítja el az Azure-tárterületet, de eltávolítja a fiók kulcsait az Azure Key Vault által felügyelt fiókból.</span><span class="sxs-lookup"><span data-stu-id="496be-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="496be-110">Az összes társított kulcs boltozata: a biztonsági társítások definíciója is törlődik.</span><span class="sxs-lookup"><span data-stu-id="496be-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="496be-111">Példák</span><span class="sxs-lookup"><span data-stu-id="496be-111">EXAMPLES</span></span>

### <span data-ttu-id="496be-112">1. példa: távolítsa el a fontos Vault Managed Azure Storage-fiókot és az összes társított biztonsági társítási definíciót.</span><span class="sxs-lookup"><span data-stu-id="496be-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
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

<span data-ttu-id="496be-113">Az Azure-tárterület "mystorageaccount"-fiókjának társítása a Key Vault "myvault", és a kulcsfájl leállítása a kulcsok kezeléséről.</span><span class="sxs-lookup"><span data-stu-id="496be-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="496be-114">Nem törlődik a "mystorageaccount" fiók.</span><span class="sxs-lookup"><span data-stu-id="496be-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="496be-115">A program eltávolítja a fiókkal társított összes fontos boltíves tárolót.</span><span class="sxs-lookup"><span data-stu-id="496be-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="496be-116">2. példa: távolítsa el a fontos Vault Managed Azure Storage-fiókot és az összes társított biztonsági társítási definíciót felhasználó megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="496be-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
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

<span data-ttu-id="496be-117">Az Azure-tárterület "mystorageaccount"-fiókjának társítása a Key Vault "myvault", és a kulcsfájl leállítása a kulcsok kezeléséről.</span><span class="sxs-lookup"><span data-stu-id="496be-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="496be-118">Nem törlődik a "mystorageaccount" fiók.</span><span class="sxs-lookup"><span data-stu-id="496be-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="496be-119">A program eltávolítja a fiókkal társított összes fontos boltíves tárolót.</span><span class="sxs-lookup"><span data-stu-id="496be-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="496be-120">3. példa: a fontos, az Azure által felügyelt fő tároló-fiók és az összes társított biztonsági társítási definíció végleges törlése (kiürítése).</span><span class="sxs-lookup"><span data-stu-id="496be-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="496be-121">A példa feltételezi, hogy a boltozathoz engedélyezve van a finom törlés.</span><span class="sxs-lookup"><span data-stu-id="496be-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="496be-122">Ellenőrizze, hogy ez-e a helyzet a boltozat tulajdonságainak vagy a RecoveryLevel attribútumának a boltozatban való vizsgálatával.</span><span class="sxs-lookup"><span data-stu-id="496be-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="496be-123">Az első parancsmag az Azure-tárterület "mystorageaccount"-fiókját nem társítja a "myvault" kulccsal, és a kulcs-boltozatot leállítja a kulcsok kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="496be-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="496be-124">Nem törlődik a "mystorageaccount" fiók.</span><span class="sxs-lookup"><span data-stu-id="496be-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="496be-125">A program eltávolítja a fiókkal társított összes fontos boltíves tárolót.</span><span class="sxs-lookup"><span data-stu-id="496be-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="496be-126">A második parancsmag azt ellenőrzi, hogy a tárolási fiók törölt, de helyreállítható állapotban van-e.</span><span class="sxs-lookup"><span data-stu-id="496be-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="496be-127">Ha elérte ezt az állapotot, akkor szükség lehet némi időre, kérjük, hogy próbálkozzon a ~ 30-as évekkel.</span><span class="sxs-lookup"><span data-stu-id="496be-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="496be-128">A harmadik parancsmag véglegesen eltávolítja a tárterület-helyreállítási fiókot, a továbbiakban nem lesz lehetséges.</span><span class="sxs-lookup"><span data-stu-id="496be-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="496be-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="496be-129">PARAMETERS</span></span>

### <span data-ttu-id="496be-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="496be-130">-AccountName</span></span>
<span data-ttu-id="496be-131">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="496be-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="496be-132">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="496be-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="496be-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496be-133">-DefaultProfile</span></span>
<span data-ttu-id="496be-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="496be-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="496be-135">-Force</span><span class="sxs-lookup"><span data-stu-id="496be-135">-Force</span></span>
<span data-ttu-id="496be-136">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="496be-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="496be-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="496be-137">-InputObject</span></span>
<span data-ttu-id="496be-138">ManagedStorageAccount objektum</span><span class="sxs-lookup"><span data-stu-id="496be-138">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="496be-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="496be-139">-InRemovedState</span></span>
<span data-ttu-id="496be-140">Véglegesen eltávolítja a korábban törölt távtárolású tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="496be-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="496be-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="496be-141">-PassThru</span></span>
<span data-ttu-id="496be-142">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="496be-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="496be-143">Ha meg van adva ez a kapcsoló, akkor a parancsmag a törölt tárterület-fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="496be-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="496be-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="496be-144">-VaultName</span></span>
<span data-ttu-id="496be-145">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="496be-145">Vault name.</span></span>
<span data-ttu-id="496be-146">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="496be-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="496be-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="496be-147">-Confirm</span></span>
<span data-ttu-id="496be-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="496be-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="496be-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="496be-149">-WhatIf</span></span>
<span data-ttu-id="496be-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="496be-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="496be-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="496be-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="496be-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496be-152">CommonParameters</span></span>
<span data-ttu-id="496be-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="496be-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496be-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="496be-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496be-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="496be-155">INPUTS</span></span>

### <span data-ttu-id="496be-156">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccountIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="496be-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="496be-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="496be-157">OUTPUTS</span></span>

### <span data-ttu-id="496be-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="496be-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="496be-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="496be-159">NOTES</span></span>

## <span data-ttu-id="496be-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="496be-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

