---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: 011bdd96d69ae73ca62145b85f6e636751f8eb9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158090"
---
# <span data-ttu-id="444ef-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="444ef-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="444ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="444ef-102">SYNOPSIS</span></span>
<span data-ttu-id="444ef-103">Titkosítási hatókört hoz létre egy tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="444ef-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="444ef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="444ef-104">SYNTAX</span></span>

### <span data-ttu-id="444ef-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="444ef-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444ef-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="444ef-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444ef-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="444ef-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444ef-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="444ef-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="444ef-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="444ef-109">DESCRIPTION</span></span>
<span data-ttu-id="444ef-110">A **New-AzStorageEncryptionScope** parancsmag titkosítási hatókört hoz létre a Tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="444ef-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="444ef-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="444ef-111">EXAMPLES</span></span>

### <span data-ttu-id="444ef-112">1. példa: Titkosítási tartomány létrehozása a Tártitkosítással</span><span class="sxs-lookup"><span data-stu-id="444ef-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="444ef-113">Ez a parancs titkosítási hatókört hoz létre a Tártitkosítással.</span><span class="sxs-lookup"><span data-stu-id="444ef-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="444ef-114">2. példa: Titkosítási tartomány létrehozása Keyvault-titkosítással</span><span class="sxs-lookup"><span data-stu-id="444ef-114">Example 2: Create an encryption scope with Keyvault Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="444ef-115">Ez a parancs a Keyvault titkosítással titkosítási hatókört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="444ef-115">This command creates an encryption scope with Keyvault Encryption.</span></span>
<span data-ttu-id="444ef-116">A tárfiók identitásának be kell szereznie, wrapkey,unwrapkey engedélyekkel kell rendelkeznie a keyvault kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="444ef-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="444ef-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="444ef-117">PARAMETERS</span></span>

### <span data-ttu-id="444ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="444ef-118">-DefaultProfile</span></span>
<span data-ttu-id="444ef-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="444ef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="444ef-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="444ef-120">-EncryptionScopeName</span></span>
<span data-ttu-id="444ef-121">Azure Storage EncryptionScope-név</span><span class="sxs-lookup"><span data-stu-id="444ef-121">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444ef-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="444ef-122">-KeyUri</span></span>
<span data-ttu-id="444ef-123">The key Uri</span><span class="sxs-lookup"><span data-stu-id="444ef-123">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444ef-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="444ef-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="444ef-125">Titkosítási hatókör létrehozása a keySource segítségével Microsoft.Keyvaultként</span><span class="sxs-lookup"><span data-stu-id="444ef-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444ef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="444ef-126">-ResourceGroupName</span></span>
<span data-ttu-id="444ef-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="444ef-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="444ef-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="444ef-128">-StorageAccount</span></span>
<span data-ttu-id="444ef-129">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="444ef-129">Storage account object</span></span>

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

### <span data-ttu-id="444ef-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="444ef-130">-StorageAccountName</span></span>
<span data-ttu-id="444ef-131">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="444ef-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="444ef-132">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="444ef-132">-StorageEncryption</span></span>
<span data-ttu-id="444ef-133">Titkosítási hatókör létrehozása a keySource szolgáltatóval Microsoft.Storage-ként.</span><span class="sxs-lookup"><span data-stu-id="444ef-133">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444ef-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="444ef-134">-Confirm</span></span>
<span data-ttu-id="444ef-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="444ef-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="444ef-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="444ef-136">-WhatIf</span></span>
<span data-ttu-id="444ef-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="444ef-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="444ef-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="444ef-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="444ef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="444ef-139">CommonParameters</span></span>
<span data-ttu-id="444ef-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="444ef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="444ef-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="444ef-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="444ef-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="444ef-142">INPUTS</span></span>

### <span data-ttu-id="444ef-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="444ef-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="444ef-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="444ef-144">OUTPUTS</span></span>

### <span data-ttu-id="444ef-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="444ef-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="444ef-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="444ef-146">NOTES</span></span>

## <span data-ttu-id="444ef-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="444ef-147">RELATED LINKS</span></span>
