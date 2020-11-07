---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 56883ecc1ca562ed4a259be9d1940683e652a280
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835789"
---
# <span data-ttu-id="66c20-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="66c20-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="66c20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66c20-102">SYNOPSIS</span></span>
<span data-ttu-id="66c20-103">Hozzáad egy meglévő Azure-tárterületet a megadott kulcs boltozatához a Key Vault szolgáltatás által felügyelt kulcsok számára.</span><span class="sxs-lookup"><span data-stu-id="66c20-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="66c20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66c20-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66c20-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66c20-105">DESCRIPTION</span></span>
<span data-ttu-id="66c20-106">Egy meglévő Azure-tárterületet állít be a fő boltozattal a tároló fiók kulcsaival.</span><span class="sxs-lookup"><span data-stu-id="66c20-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="66c20-107">A tárterület-fióknak már léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="66c20-107">The Storage Account must already exist.</span></span> <span data-ttu-id="66c20-108">A tárolási kulcsokat a hívó nem érheti el.</span><span class="sxs-lookup"><span data-stu-id="66c20-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="66c20-109">A Key Vault automatikusan újragenerálja és átváltja az aktív kulcsot a megújulási időszak alapján.</span><span class="sxs-lookup"><span data-stu-id="66c20-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="66c20-110">Lásd: [Azure Key Vault Managed Storage Account-PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) a funkció áttekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="66c20-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="66c20-111">Példák</span><span class="sxs-lookup"><span data-stu-id="66c20-111">EXAMPLES</span></span>

### <span data-ttu-id="66c20-112">1. példa: az Azure Storage-fiók beállítása a Key Vault segítségével a kulcsok kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="66c20-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="66c20-113">A Key Vault által felügyelt kulcsokat tároló fiókot állít be.</span><span class="sxs-lookup"><span data-stu-id="66c20-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="66c20-114">Az aktív kulcs a "key1".</span><span class="sxs-lookup"><span data-stu-id="66c20-114">The active key set is 'key1'.</span></span> <span data-ttu-id="66c20-115">Ez a kulcs a sas-tokenek generálásához használható.</span><span class="sxs-lookup"><span data-stu-id="66c20-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="66c20-116">A kulcsfájl a parancs időpontjában a parancs időpontjában a regeneráció után újragenerálja a "azonosító2" billentyűt, majd aktív kulcsként adja meg.</span><span class="sxs-lookup"><span data-stu-id="66c20-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="66c20-117">Az automatikus regenerálási folyamat továbbra is az "key1" és a "azonosító2" között fog folytatódni a 90 napok közötti eltéréssel.</span><span class="sxs-lookup"><span data-stu-id="66c20-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="66c20-118">2. példa: a klasszikus Azure Storage-fiók beállítása a Key Vault segítségével a kulcsok kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="66c20-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="66c20-119">Klasszikus tárolási fiókot állít be a fő boltozattal a kulcsok kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="66c20-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="66c20-120">Az aktív kulcs az "elsődleges" érték.</span><span class="sxs-lookup"><span data-stu-id="66c20-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="66c20-121">Ez a kulcs a sas-tokenek generálásához használható.</span><span class="sxs-lookup"><span data-stu-id="66c20-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="66c20-122">A kulcs-boltozat a parancs időpontjában a második kulcs után újragenerálja a "másodlagos" billentyűt, majd aktív kulcsként adja meg.</span><span class="sxs-lookup"><span data-stu-id="66c20-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="66c20-123">Ez az automatikus regenerálási folyamat az "elsődleges" és a "másodlagos" között az 90 napok közötti eltérést követően folytatódik.</span><span class="sxs-lookup"><span data-stu-id="66c20-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="66c20-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66c20-124">PARAMETERS</span></span>

### <span data-ttu-id="66c20-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66c20-125">-AccountName</span></span>
<span data-ttu-id="66c20-126">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="66c20-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="66c20-127">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="66c20-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="66c20-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="66c20-128">-AccountResourceId</span></span>
<span data-ttu-id="66c20-129">A tárolási fiók Azure erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="66c20-129">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="66c20-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="66c20-130">-ActiveKeyName</span></span>
<span data-ttu-id="66c20-131">Annak a tárterület-fióknak a neve, amelyet a sas-tokenek generálásához kell használni.</span><span class="sxs-lookup"><span data-stu-id="66c20-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="66c20-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c20-132">-DefaultProfile</span></span>
<span data-ttu-id="66c20-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="66c20-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66c20-134">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="66c20-134">-Disable</span></span>
<span data-ttu-id="66c20-135">Letiltja a felügyelt tárterület-fiók kulcsát a sas-tokenek generálásához.</span><span class="sxs-lookup"><span data-stu-id="66c20-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="66c20-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="66c20-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="66c20-137">Automatikus újragenerálási kulcs.</span><span class="sxs-lookup"><span data-stu-id="66c20-137">Auto regenerate key.</span></span> <span data-ttu-id="66c20-138">Ha igaz, akkor a felügyelt tárterület-fiók inaktív kulcsa automatikusan újra létrejön, és a regeneráció után válik az új aktív kulcs.</span><span class="sxs-lookup"><span data-stu-id="66c20-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="66c20-139">Ha hamis, akkor a felügyelt tárterület fiók kulcsait nem kell automatikusan újragenerálni.</span><span class="sxs-lookup"><span data-stu-id="66c20-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="66c20-140">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="66c20-140">-RegenerationPeriod</span></span>
<span data-ttu-id="66c20-141">A regeneráció időszaka</span><span class="sxs-lookup"><span data-stu-id="66c20-141">Regeneration period.</span></span> <span data-ttu-id="66c20-142">Ha az automatikus újragenerálási kulcs engedélyezve van, ez az érték határozza meg azt a időszak, amely után a felügyelt tárolási fiók inaktív kulcsát újra létrehozta a rendszer, és az új aktív kulcs lesz.</span><span class="sxs-lookup"><span data-stu-id="66c20-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="66c20-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="66c20-143">-Tag</span></span>
<span data-ttu-id="66c20-144">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="66c20-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="66c20-145">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="66c20-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="66c20-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="66c20-146">-VaultName</span></span>
<span data-ttu-id="66c20-147">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="66c20-147">Vault name.</span></span>
<span data-ttu-id="66c20-148">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="66c20-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="66c20-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="66c20-149">-Confirm</span></span>
<span data-ttu-id="66c20-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="66c20-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66c20-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66c20-151">-WhatIf</span></span>
<span data-ttu-id="66c20-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="66c20-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66c20-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66c20-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66c20-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c20-154">CommonParameters</span></span>
<span data-ttu-id="66c20-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66c20-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c20-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66c20-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c20-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66c20-157">INPUTS</span></span>

### <span data-ttu-id="66c20-158">System. String</span><span class="sxs-lookup"><span data-stu-id="66c20-158">System.String</span></span>

### <span data-ttu-id="66c20-159">System. null ' 1 [[System. időszak, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="66c20-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="66c20-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="66c20-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="66c20-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66c20-161">OUTPUTS</span></span>

### <span data-ttu-id="66c20-162">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="66c20-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="66c20-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66c20-163">NOTES</span></span>

## <span data-ttu-id="66c20-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66c20-164">RELATED LINKS</span></span>

[<span data-ttu-id="66c20-165">Az.-boltozat</span><span class="sxs-lookup"><span data-stu-id="66c20-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
