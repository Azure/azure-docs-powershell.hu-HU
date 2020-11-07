---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 4bd6db0cf8dce4270e14337ee1168002618e3dc3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848253"
---
# <span data-ttu-id="f3f49-101">Add-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f3f49-101">Add-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="f3f49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3f49-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f49-103">Hozzáad egy meglévő Azure-tárterületet a megadott kulcs boltozatához a Key Vault szolgáltatás által felügyelt kulcsok számára.</span><span class="sxs-lookup"><span data-stu-id="f3f49-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3f49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3f49-104">SYNTAX</span></span>

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3f49-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3f49-105">DESCRIPTION</span></span>
<span data-ttu-id="f3f49-106">Egy meglévő Azure-tárterületet állít be a fő boltozattal a tároló fiók kulcsaival.</span><span class="sxs-lookup"><span data-stu-id="f3f49-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="f3f49-107">A tárterület-fióknak már léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="f3f49-107">The Storage Account must already exist.</span></span> <span data-ttu-id="f3f49-108">A tárolási kulcsokat a hívó nem érheti el.</span><span class="sxs-lookup"><span data-stu-id="f3f49-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="f3f49-109">A Key Vault automatikusan újragenerálja és átváltja az aktív kulcsot a megújulási időszak alapján.</span><span class="sxs-lookup"><span data-stu-id="f3f49-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="f3f49-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f3f49-110">EXAMPLES</span></span>

### <span data-ttu-id="f3f49-111">1. példa: az Azure Storage-fiók beállítása a Key Vault segítségével a kulcsok kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="f3f49-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="f3f49-112">A Key Vault által felügyelt kulcsokat tároló fiókot állít be.</span><span class="sxs-lookup"><span data-stu-id="f3f49-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="f3f49-113">Az aktív kulcs a "key1".</span><span class="sxs-lookup"><span data-stu-id="f3f49-113">The active key set is 'key1'.</span></span> <span data-ttu-id="f3f49-114">Ez a kulcs a sas-tokenek generálásához használható.</span><span class="sxs-lookup"><span data-stu-id="f3f49-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="f3f49-115">A kulcsfájl a parancs időpontjában a parancs időpontjában a regeneráció után újragenerálja a "azonosító2" billentyűt, majd aktív kulcsként adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f49-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="f3f49-116">Az automatikus regenerálási folyamat továbbra is az "key1" és a "azonosító2" között fog folytatódni a 90 napok közötti eltéréssel.</span><span class="sxs-lookup"><span data-stu-id="f3f49-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="f3f49-117">2. példa: a klasszikus Azure Storage-fiók beállítása a Key Vault segítségével a kulcsok kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="f3f49-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="f3f49-118">Klasszikus tárolási fiókot állít be a fő boltozattal a kulcsok kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f3f49-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="f3f49-119">Az aktív kulcs az "elsődleges" érték.</span><span class="sxs-lookup"><span data-stu-id="f3f49-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="f3f49-120">Ez a kulcs a sas-tokenek generálásához használható.</span><span class="sxs-lookup"><span data-stu-id="f3f49-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="f3f49-121">A kulcs-boltozat a parancs időpontjában a második kulcs után újragenerálja a "másodlagos" billentyűt, majd aktív kulcsként adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f49-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="f3f49-122">Ez az automatikus regenerálási folyamat az "elsődleges" és a "másodlagos" között az 90 napok közötti eltérést követően folytatódik.</span><span class="sxs-lookup"><span data-stu-id="f3f49-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="f3f49-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3f49-123">PARAMETERS</span></span>

### <span data-ttu-id="f3f49-124">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f3f49-124">-AccountName</span></span>
<span data-ttu-id="f3f49-125">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f3f49-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="f3f49-126">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="f3f49-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="f3f49-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f3f49-127">-AccountResourceId</span></span>
<span data-ttu-id="f3f49-128">A tárolási fiók Azure erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f3f49-128">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="f3f49-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="f3f49-129">-ActiveKeyName</span></span>
<span data-ttu-id="f3f49-130">Annak a tárterület-fióknak a neve, amelyet a sas-tokenek generálásához kell használni.</span><span class="sxs-lookup"><span data-stu-id="f3f49-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="f3f49-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f49-131">-DefaultProfile</span></span>
<span data-ttu-id="f3f49-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f3f49-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3f49-133">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="f3f49-133">-Disable</span></span>
<span data-ttu-id="f3f49-134">Letiltja a felügyelt tárterület-fiók kulcsát a sas-tokenek generálásához.</span><span class="sxs-lookup"><span data-stu-id="f3f49-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="f3f49-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="f3f49-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="f3f49-136">Automatikus újragenerálási kulcs.</span><span class="sxs-lookup"><span data-stu-id="f3f49-136">Auto regenerate key.</span></span> <span data-ttu-id="f3f49-137">Ha igaz, akkor a felügyelt tárterület-fiók inaktív kulcsa automatikusan újra létrejön, és a regeneráció után válik az új aktív kulcs.</span><span class="sxs-lookup"><span data-stu-id="f3f49-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="f3f49-138">Ha hamis, akkor a felügyelt tárterület fiók kulcsait nem kell automatikusan újragenerálni.</span><span class="sxs-lookup"><span data-stu-id="f3f49-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="f3f49-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="f3f49-139">-RegenerationPeriod</span></span>
<span data-ttu-id="f3f49-140">A regeneráció időszaka</span><span class="sxs-lookup"><span data-stu-id="f3f49-140">Regeneration period.</span></span> <span data-ttu-id="f3f49-141">Ha az automatikus újragenerálási kulcs engedélyezve van, ez az érték határozza meg azt a időszak, amely után a felügyelt tárolási fiók inaktív kulcsát újra létrehozta a rendszer, és az új aktív kulcs lesz.</span><span class="sxs-lookup"><span data-stu-id="f3f49-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="f3f49-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="f3f49-142">-Tag</span></span>
<span data-ttu-id="f3f49-143">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="f3f49-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f3f49-144">Példa:</span><span class="sxs-lookup"><span data-stu-id="f3f49-144">For example:</span></span>

<span data-ttu-id="f3f49-145">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="f3f49-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f3f49-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f3f49-146">-VaultName</span></span>
<span data-ttu-id="f3f49-147">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="f3f49-147">Vault name.</span></span>
<span data-ttu-id="f3f49-148">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="f3f49-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f3f49-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3f49-149">-Confirm</span></span>
<span data-ttu-id="f3f49-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3f49-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3f49-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3f49-151">-WhatIf</span></span>
<span data-ttu-id="f3f49-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3f49-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3f49-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3f49-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3f49-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f49-154">CommonParameters</span></span>
<span data-ttu-id="f3f49-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3f49-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f49-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f49-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f49-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3f49-157">INPUTS</span></span>

## <span data-ttu-id="f3f49-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3f49-158">OUTPUTS</span></span>

### <span data-ttu-id="f3f49-159">Microsoft. Azure. Command. ManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="f3f49-159">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="f3f49-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3f49-160">NOTES</span></span>

## <span data-ttu-id="f3f49-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3f49-161">RELATED LINKS</span></span>

[<span data-ttu-id="f3f49-162">AzureRM. Vault</span><span class="sxs-lookup"><span data-stu-id="f3f49-162">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
