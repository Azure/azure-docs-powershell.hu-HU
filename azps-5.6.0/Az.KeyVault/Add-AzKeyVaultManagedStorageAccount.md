---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 05c744050cc377eda01e309fb30122f83b9a8f5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007862"
---
# <span data-ttu-id="4c2c6-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c2c6-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="4c2c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c2c6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c2c6-103">Hozzáad egy meglévő Azure Storage-fiókot a megadott kulcstárolóhoz, hogy kulcsait a kulcstár szolgáltatás kezelnie kell.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="4c2c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4c2c6-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c2c6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4c2c6-105">DESCRIPTION</span></span>
<span data-ttu-id="4c2c6-106">Beállítja a meglévő Azure Storage-fiókot a kulcstárolóval ahhoz, hogy a tárfiók kulcskulcsait a kulcstár kezelnie kell.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="4c2c6-107">A tárfióknak már léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-107">The Storage Account must already exist.</span></span> <span data-ttu-id="4c2c6-108">A tárbillentyűk soha nem fedik fel a hívók számára.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="4c2c6-109">A kulcstár automatikusan újragenerálja és átváltja az aktív kulcsot a időszak alapján.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="4c2c6-110">A funkció áttekintését az [Azure Key Vault felügyelt tárfiókja – a PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) használatával is áttekintheti.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="4c2c6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4c2c6-111">EXAMPLES</span></span>

### <span data-ttu-id="4c2c6-112">1. példa: Azure-tárfiók beállítása a kulcstárolóval a kulcsok kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="4c2c6-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="4c2c6-113">Beállítja a kulcstárolóval egy tárfiókot, hogy a kulcstár kezelnie kell a kulcstárat.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="4c2c6-114">Az aktív kulcskészlet a "kulcs1".</span><span class="sxs-lookup"><span data-stu-id="4c2c6-114">The active key set is 'key1'.</span></span> <span data-ttu-id="4c2c6-115">Ezt a kulcsot használjuk a sas tokenek létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="4c2c6-116">A kulcstár a parancs időtartama után újra létrehozza a "key2" kulcsot, és aktív kulcsként beállítja azt.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="4c2c6-117">Ez az automatikus folyamat a "kulcs1" és a "kulcs2" között folytatódik, 90 napos eltéréssel.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="4c2c6-118">2. példa: Klasszikus Azure Storage-fiók beállítása a kulcstárolóval a kulcsok kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="4c2c6-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myvault/providers/Microsoft.Cl
                      assicStorage/storageAccounts/mystorageaccount
Active Key Name     : Primary
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="4c2c6-119">Klasszikus tárfiókot állít be a kulcstárolóval, hogy a kulcstár kezelnie kell a kulcstárat.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="4c2c6-120">Az aktív kulcskészlet az "Elsődleges".</span><span class="sxs-lookup"><span data-stu-id="4c2c6-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="4c2c6-121">Ezt a kulcsot használjuk a sas tokenek létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="4c2c6-122">A kulcstár a parancs időtartama után újra létrehozza a "Másodlagos" kulcsot, és aktív kulcsként beállítja azt.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="4c2c6-123">Ez az automatikus folyamat az "Elsődleges" és a "Másodlagos" között folytatódik, 90 napos eltéréssel.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="4c2c6-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c2c6-124">PARAMETERS</span></span>

### <span data-ttu-id="4c2c6-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4c2c6-125">-AccountName</span></span>
<span data-ttu-id="4c2c6-126">Key Vault managed storage account name.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="4c2c6-127">A parancsmag egy felügyelt tárfiók nevének FQDN-ét építi fel a tárolónévből, az aktuálisan kijelölt környezetből és a felügyelt tárfiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c2c6-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="4c2c6-128">-AccountResourceId</span></span>
<span data-ttu-id="4c2c6-129">A tárfiók Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-129">Azure resource id of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c2c6-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="4c2c6-130">-ActiveKeyName</span></span>
<span data-ttu-id="4c2c6-131">Annak a tárfiókkulcsnak a neve, amely a sas tokenek létrehozásához szükséges.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c2c6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c2c6-132">-DefaultProfile</span></span>
<span data-ttu-id="4c2c6-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4c2c6-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c2c6-134">-Disable</span><span class="sxs-lookup"><span data-stu-id="4c2c6-134">-Disable</span></span>
<span data-ttu-id="4c2c6-135">Letiltja a felügyelt tárfiók kulcsának használatát a sas tokenek generálásához.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="4c2c6-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="4c2c6-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="4c2c6-137">A kulcs automatikus újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-137">Auto regenerate key.</span></span> <span data-ttu-id="4c2c6-138">Ha igaz, akkor a felügyelt tárfiók inaktív kulcsát a rendszer automatikusan újragenerálja, és az időszak után válik az új aktív kulcssá.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="4c2c6-139">Ha hamis, akkor a felügyelt tárfiók kulcsait a rendszer nem újra létrehozza automatikusan.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="4c2c6-140">-ÉsPeriod</span><span class="sxs-lookup"><span data-stu-id="4c2c6-140">-RegenerationPeriod</span></span>
<span data-ttu-id="4c2c6-141">Időtartam.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-141">Regeneration period.</span></span> <span data-ttu-id="4c2c6-142">Ha engedélyezve van az automatikus újragenerálás kulcs, ez az érték azt adja meg, hogy a felügyelt tárfiók inaktív kulcsai milyen idő után hoznak létre automatikusan új kulcsot, és ez lesz az új aktív kulcs.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c2c6-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="4c2c6-143">-Tag</span></span>
<span data-ttu-id="4c2c6-144">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4c2c6-145">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="4c2c6-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c2c6-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4c2c6-146">-VaultName</span></span>
<span data-ttu-id="4c2c6-147">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-147">Vault name.</span></span>
<span data-ttu-id="4c2c6-148">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c2c6-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c2c6-149">-Confirm</span></span>
<span data-ttu-id="4c2c6-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c2c6-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c2c6-151">-WhatIf</span></span>
<span data-ttu-id="4c2c6-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c2c6-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c2c6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c2c6-154">CommonParameters</span></span>
<span data-ttu-id="4c2c6-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c2c6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c2c6-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c2c6-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c2c6-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c2c6-157">INPUTS</span></span>

### <span data-ttu-id="4c2c6-158">System.String</span><span class="sxs-lookup"><span data-stu-id="4c2c6-158">System.String</span></span>

### <span data-ttu-id="4c2c6-159">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4c2c6-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4c2c6-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4c2c6-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4c2c6-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c2c6-161">OUTPUTS</span></span>

### <span data-ttu-id="4c2c6-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c2c6-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="4c2c6-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4c2c6-163">NOTES</span></span>

## <span data-ttu-id="4c2c6-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c2c6-164">RELATED LINKS</span></span>

[<span data-ttu-id="4c2c6-165">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4c2c6-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
