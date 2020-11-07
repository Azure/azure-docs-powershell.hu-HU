---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 2d2e1ff127ce5d355831131c6e366712efee1c29
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849282"
---
# <span data-ttu-id="4ba56-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ba56-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="4ba56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ba56-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba56-103">Frissítheti egy kulcs típusú, felügyelt Azure-tárterület szerkeszthető attribútumait.</span><span class="sxs-lookup"><span data-stu-id="4ba56-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ba56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ba56-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ba56-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ba56-105">DESCRIPTION</span></span>
<span data-ttu-id="4ba56-106">Frissítheti egy kulcs típusú, felügyelt Azure-tárterület szerkeszthető attribútumát.</span><span class="sxs-lookup"><span data-stu-id="4ba56-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="4ba56-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4ba56-107">EXAMPLES</span></span>

### <span data-ttu-id="4ba56-108">Példa 1: az aktív kulcs frissítése az "azonosító2"-ra egy Key Vault Managed Azure Storage-fiókban.</span><span class="sxs-lookup"><span data-stu-id="4ba56-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="4ba56-109">Frissíti a Key Vault Managed Azure tárhely-fiók aktív kulcsát a "azonosító2" értékre.</span><span class="sxs-lookup"><span data-stu-id="4ba56-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="4ba56-110">az "azonosító2" a frissítés után a SAS-tokenek generálásához használható.</span><span class="sxs-lookup"><span data-stu-id="4ba56-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="4ba56-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ba56-111">PARAMETERS</span></span>

### <span data-ttu-id="4ba56-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4ba56-112">-AccountName</span></span>
<span data-ttu-id="4ba56-113">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="4ba56-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="4ba56-114">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="4ba56-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="4ba56-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="4ba56-115">-ActiveKeyName</span></span>
<span data-ttu-id="4ba56-116">Az aktív kulcs neve</span><span class="sxs-lookup"><span data-stu-id="4ba56-116">Active key name.</span></span>
<span data-ttu-id="4ba56-117">Ha nem adja meg, akkor a felügyelt tárterület-fiók aktív kulcsnévének meglévő értéke változatlan marad</span><span class="sxs-lookup"><span data-stu-id="4ba56-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="4ba56-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="4ba56-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="4ba56-119">Automatikus újragenerálási kulcs.</span><span class="sxs-lookup"><span data-stu-id="4ba56-119">Auto regenerate key.</span></span>
<span data-ttu-id="4ba56-120">Ha nem adja meg, akkor a felügyelt tárterület-fiók automatikus újragenerálási kulcsának meglévő értéke változatlan marad</span><span class="sxs-lookup"><span data-stu-id="4ba56-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="4ba56-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba56-121">-DefaultProfile</span></span>
<span data-ttu-id="4ba56-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4ba56-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ba56-123">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="4ba56-123">-Enable</span></span>
<span data-ttu-id="4ba56-124">Ha van, akkor lehetővé teszi a felügyelt tárterület-fiók kulcs használatát a sas-tokenek generálásához, ha az érték igaz.</span><span class="sxs-lookup"><span data-stu-id="4ba56-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="4ba56-125">Letiltja a felügyelt tárterület-fiók kulcs használatát a sas-token generálásához, ha az érték hamis.</span><span class="sxs-lookup"><span data-stu-id="4ba56-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="4ba56-126">Ha nem adja meg, akkor a tárterület-fiók engedélyezve/letiltva állapotának meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="4ba56-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="4ba56-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ba56-127">-PassThru</span></span>
<span data-ttu-id="4ba56-128">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="4ba56-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="4ba56-129">Ha ez a kapcsoló van megadva, a felügyelt tárterület-ügyfél visszaadása objektum.</span><span class="sxs-lookup"><span data-stu-id="4ba56-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="4ba56-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="4ba56-130">-RegenerationPeriod</span></span>
<span data-ttu-id="4ba56-131">A regeneráció időszaka</span><span class="sxs-lookup"><span data-stu-id="4ba56-131">Regeneration period.</span></span> <span data-ttu-id="4ba56-132">Ha az automatikus újragenerálási kulcs engedélyezve van, ez az érték határozza meg azt a időszak, amely után a felügyelt tárolási fiók inaktív kulcsát újra létrehozta a rendszer, és az aktív kulcs lesz.</span><span class="sxs-lookup"><span data-stu-id="4ba56-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="4ba56-133">Ha nem adja meg, a felügyelt tárterületet tároló kulcsok átgenerálási időszakának meglévő értéke változatlan marad</span><span class="sxs-lookup"><span data-stu-id="4ba56-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="4ba56-134">-Címke</span><span class="sxs-lookup"><span data-stu-id="4ba56-134">-Tag</span></span>
<span data-ttu-id="4ba56-135">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="4ba56-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4ba56-136">Példa:</span><span class="sxs-lookup"><span data-stu-id="4ba56-136">For example:</span></span>

<span data-ttu-id="4ba56-137">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="4ba56-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4ba56-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4ba56-138">-VaultName</span></span>
<span data-ttu-id="4ba56-139">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="4ba56-139">Vault name.</span></span>
<span data-ttu-id="4ba56-140">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="4ba56-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4ba56-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ba56-141">-Confirm</span></span>
<span data-ttu-id="4ba56-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ba56-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba56-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba56-143">-WhatIf</span></span>
<span data-ttu-id="4ba56-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ba56-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ba56-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ba56-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba56-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba56-146">CommonParameters</span></span>
<span data-ttu-id="4ba56-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ba56-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba56-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ba56-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba56-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ba56-149">INPUTS</span></span>

## <span data-ttu-id="4ba56-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ba56-150">OUTPUTS</span></span>

### <span data-ttu-id="4ba56-151">Microsoft. Azure. Command. ManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="4ba56-151">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="4ba56-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ba56-152">NOTES</span></span>

## <span data-ttu-id="4ba56-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ba56-153">RELATED LINKS</span></span>

[<span data-ttu-id="4ba56-154">AzureRM. Vault</span><span class="sxs-lookup"><span data-stu-id="4ba56-154">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
