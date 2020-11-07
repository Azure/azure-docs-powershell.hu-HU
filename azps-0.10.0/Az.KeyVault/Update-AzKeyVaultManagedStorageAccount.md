---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/update-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ea3d16ec55186017852df30f6ff745f79703f224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843837"
---
# <span data-ttu-id="86534-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86534-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="86534-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86534-102">SYNOPSIS</span></span>
<span data-ttu-id="86534-103">Frissítheti egy kulcs típusú, felügyelt Azure-tárterület szerkeszthető attribútumait.</span><span class="sxs-lookup"><span data-stu-id="86534-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="86534-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86534-104">SYNTAX</span></span>

```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86534-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86534-105">DESCRIPTION</span></span>
<span data-ttu-id="86534-106">Frissítheti egy kulcs típusú, felügyelt Azure-tárterület szerkeszthető attribútumát.</span><span class="sxs-lookup"><span data-stu-id="86534-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="86534-107">Példák</span><span class="sxs-lookup"><span data-stu-id="86534-107">EXAMPLES</span></span>

### <span data-ttu-id="86534-108">Példa 1: az aktív kulcs frissítése az "azonosító2"-ra egy Key Vault Managed Azure Storage-fiókban.</span><span class="sxs-lookup"><span data-stu-id="86534-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="86534-109">Frissíti a Key Vault Managed Azure tárhely-fiók aktív kulcsát a "azonosító2" értékre.</span><span class="sxs-lookup"><span data-stu-id="86534-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="86534-110">az "azonosító2" a frissítés után a SAS-tokenek generálásához használható.</span><span class="sxs-lookup"><span data-stu-id="86534-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="86534-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86534-111">PARAMETERS</span></span>

### <span data-ttu-id="86534-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="86534-112">-AccountName</span></span>
<span data-ttu-id="86534-113">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="86534-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="86534-114">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="86534-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="86534-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="86534-115">-ActiveKeyName</span></span>
<span data-ttu-id="86534-116">Az aktív kulcs neve</span><span class="sxs-lookup"><span data-stu-id="86534-116">Active key name.</span></span>
<span data-ttu-id="86534-117">Ha nem adja meg, akkor a felügyelt tárterület-fiók aktív kulcsnévének meglévő értéke változatlan marad</span><span class="sxs-lookup"><span data-stu-id="86534-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86534-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="86534-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="86534-119">Automatikus újragenerálási kulcs.</span><span class="sxs-lookup"><span data-stu-id="86534-119">Auto regenerate key.</span></span>
<span data-ttu-id="86534-120">Ha nem adja meg, akkor a felügyelt tárterület-fiók automatikus újragenerálási kulcsának meglévő értéke változatlan marad</span><span class="sxs-lookup"><span data-stu-id="86534-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86534-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86534-121">-DefaultProfile</span></span>
<span data-ttu-id="86534-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="86534-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86534-123">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="86534-123">-Enable</span></span>
<span data-ttu-id="86534-124">Ha van, akkor lehetővé teszi a felügyelt tárterület-fiók kulcs használatát a sas-tokenek generálásához, ha az érték igaz.</span><span class="sxs-lookup"><span data-stu-id="86534-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="86534-125">Letiltja a felügyelt tárterület-fiók kulcs használatát a sas-token generálásához, ha az érték hamis.</span><span class="sxs-lookup"><span data-stu-id="86534-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="86534-126">Ha nem adja meg, akkor a tárterület-fiók engedélyezve/letiltva állapotának meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="86534-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86534-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86534-127">-PassThru</span></span>
<span data-ttu-id="86534-128">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="86534-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="86534-129">Ha ez a kapcsoló van megadva, a felügyelt tárterület-ügyfél visszaadása objektum.</span><span class="sxs-lookup"><span data-stu-id="86534-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="86534-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="86534-130">-RegenerationPeriod</span></span>
<span data-ttu-id="86534-131">A regeneráció időszaka</span><span class="sxs-lookup"><span data-stu-id="86534-131">Regeneration period.</span></span> <span data-ttu-id="86534-132">Ha az automatikus újragenerálási kulcs engedélyezve van, ez az érték határozza meg azt a időszak, amely után a felügyelt tárolási fiók inaktív kulcsát újra létrehozta a rendszer, és az aktív kulcs lesz.</span><span class="sxs-lookup"><span data-stu-id="86534-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="86534-133">Ha nem adja meg, a felügyelt tárterületet tároló kulcsok átgenerálási időszakának meglévő értéke változatlan marad</span><span class="sxs-lookup"><span data-stu-id="86534-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="86534-134">-Címke</span><span class="sxs-lookup"><span data-stu-id="86534-134">-Tag</span></span>
<span data-ttu-id="86534-135">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="86534-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="86534-136">Példa:</span><span class="sxs-lookup"><span data-stu-id="86534-136">For example:</span></span>

<span data-ttu-id="86534-137">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="86534-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="86534-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="86534-138">-VaultName</span></span>
<span data-ttu-id="86534-139">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="86534-139">Vault name.</span></span>
<span data-ttu-id="86534-140">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="86534-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="86534-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86534-141">-Confirm</span></span>
<span data-ttu-id="86534-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86534-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86534-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86534-143">-WhatIf</span></span>
<span data-ttu-id="86534-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86534-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86534-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86534-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86534-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86534-146">CommonParameters</span></span>
<span data-ttu-id="86534-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86534-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86534-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86534-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86534-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86534-149">INPUTS</span></span>

### <span data-ttu-id="86534-150">Nincs</span><span class="sxs-lookup"><span data-stu-id="86534-150">None</span></span>
<span data-ttu-id="86534-151">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="86534-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86534-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86534-152">OUTPUTS</span></span>

### <span data-ttu-id="86534-153">Microsoft. Azure. Command. ManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="86534-153">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="86534-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86534-154">NOTES</span></span>

## <span data-ttu-id="86534-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86534-155">RELATED LINKS</span></span>

[<span data-ttu-id="86534-156">Az.-boltozat</span><span class="sxs-lookup"><span data-stu-id="86534-156">Az.KeyVault</span></span>](/powershell/module/Az.keyvault)
