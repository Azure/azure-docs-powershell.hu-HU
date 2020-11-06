---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 1a21db1918d9baef48d3efd15dc72c2cb542a925
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496024"
---
# <span data-ttu-id="fab2c-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fab2c-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fab2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fab2c-102">SYNOPSIS</span></span>
<span data-ttu-id="fab2c-103">Frissítheti egy kulcs típusú, felügyelt Azure-tárterület szerkeszthető attribútumait.</span><span class="sxs-lookup"><span data-stu-id="fab2c-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fab2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fab2c-104">SYNTAX</span></span>

### <span data-ttu-id="fab2c-105">ByDefinitionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fab2c-105">ByDefinitionName (Default)</span></span>
```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fab2c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fab2c-106">ByInputObject</span></span>
```
Update-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fab2c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fab2c-107">DESCRIPTION</span></span>
<span data-ttu-id="fab2c-108">Frissítheti egy kulcs típusú, felügyelt Azure-tárterület szerkeszthető attribútumát.</span><span class="sxs-lookup"><span data-stu-id="fab2c-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="fab2c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fab2c-109">EXAMPLES</span></span>

### <span data-ttu-id="fab2c-110">Példa 1: az aktív kulcs frissítése az "azonosító2"-ra egy Key Vault Managed Azure Storage-fiókban.</span><span class="sxs-lookup"><span data-stu-id="fab2c-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="fab2c-111">Frissíti a Key Vault Managed Azure tárhely-fiók aktív kulcsát a "azonosító2" értékre.</span><span class="sxs-lookup"><span data-stu-id="fab2c-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="fab2c-112">az "azonosító2" a frissítés után a SAS-tokenek generálásához használható.</span><span class="sxs-lookup"><span data-stu-id="fab2c-112">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="fab2c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fab2c-113">PARAMETERS</span></span>

### <span data-ttu-id="fab2c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fab2c-114">-AccountName</span></span>
<span data-ttu-id="fab2c-115">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="fab2c-115">Key Vault managed storage account name.</span></span> <span data-ttu-id="fab2c-116">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="fab2c-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="fab2c-117">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="fab2c-117">-ActiveKeyName</span></span>
<span data-ttu-id="fab2c-118">Az aktív kulcs neve</span><span class="sxs-lookup"><span data-stu-id="fab2c-118">Active key name.</span></span>
<span data-ttu-id="fab2c-119">Ha nem adja meg, akkor a felügyelt tárterület-fiók aktív kulcsnévének meglévő értéke változatlan marad</span><span class="sxs-lookup"><span data-stu-id="fab2c-119">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2c-120">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="fab2c-120">-AutoRegenerateKey</span></span>
<span data-ttu-id="fab2c-121">Automatikus újragenerálási kulcs.</span><span class="sxs-lookup"><span data-stu-id="fab2c-121">Auto regenerate key.</span></span>
<span data-ttu-id="fab2c-122">Ha nem adja meg, akkor a felügyelt tárterület-fiók automatikus újragenerálási kulcsának meglévő értéke változatlan marad</span><span class="sxs-lookup"><span data-stu-id="fab2c-122">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab2c-123">-DefaultProfile</span></span>
<span data-ttu-id="fab2c-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fab2c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2c-125">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="fab2c-125">-Enable</span></span>
<span data-ttu-id="fab2c-126">Ha van, akkor lehetővé teszi a felügyelt tárterület-fiók kulcs használatát a sas-tokenek generálásához, ha az érték igaz.</span><span class="sxs-lookup"><span data-stu-id="fab2c-126">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="fab2c-127">Letiltja a felügyelt tárterület-fiók kulcs használatát a sas-token generálásához, ha az érték hamis.</span><span class="sxs-lookup"><span data-stu-id="fab2c-127">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="fab2c-128">Ha nem adja meg, akkor a tárterület-fiók engedélyezve/letiltva állapotának meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="fab2c-128">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fab2c-129">-InputObject</span></span>
<span data-ttu-id="fab2c-130">ManagedStorageAccount objektum</span><span class="sxs-lookup"><span data-stu-id="fab2c-130">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="fab2c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fab2c-131">-PassThru</span></span>
<span data-ttu-id="fab2c-132">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="fab2c-132">Cmdlet does not return object by default.</span></span> <span data-ttu-id="fab2c-133">Ha ez a kapcsoló van megadva, a felügyelt tárterület-ügyfél visszaadása objektum.</span><span class="sxs-lookup"><span data-stu-id="fab2c-133">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="fab2c-134">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="fab2c-134">-RegenerationPeriod</span></span>
<span data-ttu-id="fab2c-135">A regeneráció időszaka</span><span class="sxs-lookup"><span data-stu-id="fab2c-135">Regeneration period.</span></span> <span data-ttu-id="fab2c-136">Ha az automatikus újragenerálási kulcs engedélyezve van, ez az érték határozza meg azt a időszak, amely után a felügyelt tárolási fiók inaktív kulcsát újra létrehozta a rendszer, és az aktív kulcs lesz.</span><span class="sxs-lookup"><span data-stu-id="fab2c-136">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="fab2c-137">Ha nem adja meg, a felügyelt tárterületet tároló kulcsok átgenerálási időszakának meglévő értéke változatlan marad</span><span class="sxs-lookup"><span data-stu-id="fab2c-137">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2c-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="fab2c-138">-Tag</span></span>
<span data-ttu-id="fab2c-139">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="fab2c-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fab2c-140">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="fab2c-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2c-141">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fab2c-141">-VaultName</span></span>
<span data-ttu-id="fab2c-142">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="fab2c-142">Vault name.</span></span>
<span data-ttu-id="fab2c-143">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="fab2c-143">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fab2c-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fab2c-144">-Confirm</span></span>
<span data-ttu-id="fab2c-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fab2c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fab2c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab2c-146">-WhatIf</span></span>
<span data-ttu-id="fab2c-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fab2c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab2c-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fab2c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fab2c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab2c-149">CommonParameters</span></span>
<span data-ttu-id="fab2c-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fab2c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab2c-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab2c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab2c-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fab2c-152">INPUTS</span></span>

### <span data-ttu-id="fab2c-153">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccountIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="fab2c-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="fab2c-154">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fab2c-154">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fab2c-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fab2c-155">OUTPUTS</span></span>

### <span data-ttu-id="fab2c-156">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="fab2c-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fab2c-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fab2c-157">NOTES</span></span>

## <span data-ttu-id="fab2c-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fab2c-158">RELATED LINKS</span></span>

[<span data-ttu-id="fab2c-159">AzureRM. Vault</span><span class="sxs-lookup"><span data-stu-id="fab2c-159">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
