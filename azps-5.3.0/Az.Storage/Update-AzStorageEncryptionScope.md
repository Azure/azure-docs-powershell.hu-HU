---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 6c8f07cbdb70b84d235afa7ce953da0bac477f55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375953"
---
# <span data-ttu-id="ce0a5-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="ce0a5-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="ce0a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0a5-103">Tárfiók titkosítási hatókörének módosítása</span><span class="sxs-lookup"><span data-stu-id="ce0a5-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="ce0a5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ce0a5-104">SYNTAX</span></span>

### <span data-ttu-id="ce0a5-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce0a5-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce0a5-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="ce0a5-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce0a5-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ce0a5-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce0a5-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="ce0a5-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce0a5-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="ce0a5-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce0a5-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="ce0a5-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce0a5-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ce0a5-111">DESCRIPTION</span></span>
<span data-ttu-id="ce0a5-112">Az **Update-AzStorageEncryptionScope** parancsmag módosítja a tárfiók titkosítási hatókörét.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="ce0a5-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ce0a5-113">EXAMPLES</span></span>

### <span data-ttu-id="ce0a5-114">1. példa: Titkosítási hatókör letiltása</span><span class="sxs-lookup"><span data-stu-id="ce0a5-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="ce0a5-115">Ez a parancs letiltja a titkosítási hatókört.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="ce0a5-116">2. példa: Titkosítási hatókör engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ce0a5-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="ce0a5-117">Ez a parancs titkosítási hatókört tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="ce0a5-118">3. példa: Titkosítási tartomány frissítése a Tártitkosítás használatára</span><span class="sxs-lookup"><span data-stu-id="ce0a5-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="ce0a5-119">Ez a parancs frissíti a titkosítási hatókört a Tártitkosítás használatára.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="ce0a5-120">4. példa: Titkosítási tartomány frissítése a Keyvault-titkosítás használatára</span><span class="sxs-lookup"><span data-stu-id="ce0a5-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="ce0a5-121">Ez a parancs a Keyvault-titkosítás használatára egy titkosítási hatókört hoz fel.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="ce0a5-122">A tárfiók identitásának rendelkeznie kell a kulcskulcs lekért,wrapkey és unwrapkey engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="ce0a5-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce0a5-123">PARAMETERS</span></span>

### <span data-ttu-id="ce0a5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0a5-124">-DefaultProfile</span></span>
<span data-ttu-id="ce0a5-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce0a5-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="ce0a5-126">-EncryptionScopeName</span></span>
<span data-ttu-id="ce0a5-127">Azure Storage EncryptionScope-név</span><span class="sxs-lookup"><span data-stu-id="ce0a5-127">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault, AccountObject, AccountObjectKeyVault
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0a5-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce0a5-128">-InputObject</span></span>
<span data-ttu-id="ce0a5-129">EncryptionScope objektum</span><span class="sxs-lookup"><span data-stu-id="ce0a5-129">EncryptionScope object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope
Parameter Sets: EncryptionScopeObject, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce0a5-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="ce0a5-130">-KeyUri</span></span>
<span data-ttu-id="ce0a5-131">The key Uri</span><span class="sxs-lookup"><span data-stu-id="ce0a5-131">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0a5-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="ce0a5-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="ce0a5-133">Titkosítási hatókör létrehozása a keySource segítségével Microsoft.Keyvaultként</span><span class="sxs-lookup"><span data-stu-id="ce0a5-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0a5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce0a5-134">-ResourceGroupName</span></span>
<span data-ttu-id="ce0a5-135">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-135">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0a5-136">-State</span><span class="sxs-lookup"><span data-stu-id="ce0a5-136">-State</span></span>
<span data-ttu-id="ce0a5-137">Frissítési titkosítási hatókör állapota, Lehetséges értékek: "Engedélyezve", "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="ce0a5-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0a5-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce0a5-138">-StorageAccount</span></span>
<span data-ttu-id="ce0a5-139">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="ce0a5-139">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce0a5-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ce0a5-140">-StorageAccountName</span></span>
<span data-ttu-id="ce0a5-141">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-141">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0a5-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="ce0a5-142">-StorageEncryption</span></span>
<span data-ttu-id="ce0a5-143">Titkosítási hatókör létrehozása a keySource szolgáltatóval Microsoft.Storage-ként.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject, EncryptionScopeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0a5-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce0a5-144">-Confirm</span></span>
<span data-ttu-id="ce0a5-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce0a5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce0a5-146">-WhatIf</span></span>
<span data-ttu-id="ce0a5-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce0a5-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce0a5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0a5-149">CommonParameters</span></span>
<span data-ttu-id="ce0a5-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0a5-151">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce0a5-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0a5-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce0a5-152">INPUTS</span></span>

### <span data-ttu-id="ce0a5-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce0a5-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ce0a5-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce0a5-154">OUTPUTS</span></span>

### <span data-ttu-id="ce0a5-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="ce0a5-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="ce0a5-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ce0a5-156">NOTES</span></span>

## <span data-ttu-id="ce0a5-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce0a5-157">RELATED LINKS</span></span>
