---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 85a0bc0f552688d036dc76ebbc6d15c608ade433
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843901"
---
# <span data-ttu-id="04941-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04941-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="04941-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04941-102">SYNOPSIS</span></span>
<span data-ttu-id="04941-103">Hozzáad egy meglévő Azure-tárterületet a megadott kulcs boltozatához a Key Vault szolgáltatás által felügyelt kulcsok számára.</span><span class="sxs-lookup"><span data-stu-id="04941-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="04941-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04941-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04941-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04941-105">DESCRIPTION</span></span>
<span data-ttu-id="04941-106">Egy meglévő Azure-tárterületet állít be a fő boltozattal a tároló fiók kulcsaival.</span><span class="sxs-lookup"><span data-stu-id="04941-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="04941-107">A tárterület-fióknak már léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="04941-107">The Storage Account must already exist.</span></span> <span data-ttu-id="04941-108">A tárolási kulcsokat a hívó nem érheti el.</span><span class="sxs-lookup"><span data-stu-id="04941-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="04941-109">A Key Vault automatikusan újragenerálja és átváltja az aktív kulcsot a megújulási időszak alapján.</span><span class="sxs-lookup"><span data-stu-id="04941-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="04941-110">Példák</span><span class="sxs-lookup"><span data-stu-id="04941-110">EXAMPLES</span></span>

### <span data-ttu-id="04941-111">1. példa: az Azure Storage-fiók beállítása a Key Vault segítségével a kulcsok kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="04941-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="04941-112">A Key Vault által felügyelt kulcsokat tároló fiókot állít be.</span><span class="sxs-lookup"><span data-stu-id="04941-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="04941-113">Az aktív kulcs a "key1".</span><span class="sxs-lookup"><span data-stu-id="04941-113">The active key set is 'key1'.</span></span> <span data-ttu-id="04941-114">Ez a kulcs a sas-tokenek generálásához használható.</span><span class="sxs-lookup"><span data-stu-id="04941-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="04941-115">A kulcsfájl a parancs időpontjában a parancs időpontjában a regeneráció után újragenerálja a "azonosító2" billentyűt, majd aktív kulcsként adja meg.</span><span class="sxs-lookup"><span data-stu-id="04941-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="04941-116">Az automatikus regenerálási folyamat továbbra is az "key1" és a "azonosító2" között fog folytatódni a 90 napok közötti eltéréssel.</span><span class="sxs-lookup"><span data-stu-id="04941-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="04941-117">2. példa: a klasszikus Azure Storage-fiók beállítása a Key Vault segítségével a kulcsok kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="04941-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="04941-118">Klasszikus tárolási fiókot állít be a fő boltozattal a kulcsok kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="04941-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="04941-119">Az aktív kulcs az "elsődleges" érték.</span><span class="sxs-lookup"><span data-stu-id="04941-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="04941-120">Ez a kulcs a sas-tokenek generálásához használható.</span><span class="sxs-lookup"><span data-stu-id="04941-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="04941-121">A kulcs-boltozat a parancs időpontjában a második kulcs után újragenerálja a "másodlagos" billentyűt, majd aktív kulcsként adja meg.</span><span class="sxs-lookup"><span data-stu-id="04941-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="04941-122">Ez az automatikus regenerálási folyamat az "elsődleges" és a "másodlagos" között az 90 napok közötti eltérést követően folytatódik.</span><span class="sxs-lookup"><span data-stu-id="04941-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="04941-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04941-123">PARAMETERS</span></span>

### <span data-ttu-id="04941-124">-AccountName</span><span class="sxs-lookup"><span data-stu-id="04941-124">-AccountName</span></span>
<span data-ttu-id="04941-125">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="04941-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="04941-126">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="04941-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04941-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="04941-127">-AccountResourceId</span></span>
<span data-ttu-id="04941-128">A tárolási fiók Azure erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="04941-128">Azure resource id of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04941-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="04941-129">-ActiveKeyName</span></span>
<span data-ttu-id="04941-130">Annak a tárterület-fióknak a neve, amelyet a sas-tokenek generálásához kell használni.</span><span class="sxs-lookup"><span data-stu-id="04941-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04941-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04941-131">-DefaultProfile</span></span>
<span data-ttu-id="04941-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="04941-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04941-133">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="04941-133">-Disable</span></span>
<span data-ttu-id="04941-134">Letiltja a felügyelt tárterület-fiók kulcsát a sas-tokenek generálásához.</span><span class="sxs-lookup"><span data-stu-id="04941-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="04941-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="04941-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="04941-136">Automatikus újragenerálási kulcs.</span><span class="sxs-lookup"><span data-stu-id="04941-136">Auto regenerate key.</span></span> <span data-ttu-id="04941-137">Ha igaz, akkor a felügyelt tárterület-fiók inaktív kulcsa automatikusan újra létrejön, és a regeneráció után válik az új aktív kulcs.</span><span class="sxs-lookup"><span data-stu-id="04941-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="04941-138">Ha hamis, akkor a felügyelt tárterület fiók kulcsait nem kell automatikusan újragenerálni.</span><span class="sxs-lookup"><span data-stu-id="04941-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="04941-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="04941-139">-RegenerationPeriod</span></span>
<span data-ttu-id="04941-140">A regeneráció időszaka</span><span class="sxs-lookup"><span data-stu-id="04941-140">Regeneration period.</span></span> <span data-ttu-id="04941-141">Ha az automatikus újragenerálási kulcs engedélyezve van, ez az érték határozza meg azt a időszak, amely után a felügyelt tárolási fiók inaktív kulcsát újra létrehozta a rendszer, és az új aktív kulcs lesz.</span><span class="sxs-lookup"><span data-stu-id="04941-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04941-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="04941-142">-Tag</span></span>
<span data-ttu-id="04941-143">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="04941-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="04941-144">Példa:</span><span class="sxs-lookup"><span data-stu-id="04941-144">For example:</span></span>

<span data-ttu-id="04941-145">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="04941-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04941-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="04941-146">-VaultName</span></span>
<span data-ttu-id="04941-147">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="04941-147">Vault name.</span></span>
<span data-ttu-id="04941-148">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="04941-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="04941-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="04941-149">-Confirm</span></span>
<span data-ttu-id="04941-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="04941-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04941-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04941-151">-WhatIf</span></span>
<span data-ttu-id="04941-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="04941-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04941-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04941-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04941-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04941-154">CommonParameters</span></span>
<span data-ttu-id="04941-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04941-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04941-156">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04941-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04941-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04941-157">INPUTS</span></span>

### <span data-ttu-id="04941-158">Nincs</span><span class="sxs-lookup"><span data-stu-id="04941-158">None</span></span>
<span data-ttu-id="04941-159">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="04941-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04941-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04941-160">OUTPUTS</span></span>

### <span data-ttu-id="04941-161">Microsoft. Azure. Command. ManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="04941-161">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="04941-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04941-162">NOTES</span></span>

## <span data-ttu-id="04941-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04941-163">RELATED LINKS</span></span>

[<span data-ttu-id="04941-164">Az.-boltozat</span><span class="sxs-lookup"><span data-stu-id="04941-164">Az.KeyVault</span></span>](/powershell/module/Az.keyvault)
