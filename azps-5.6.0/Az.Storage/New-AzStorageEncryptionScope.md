---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: ab2750bff8ccc3f53761671455bc50fe3ec154d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002454"
---
# <span data-ttu-id="a1f4f-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="a1f4f-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="a1f4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f4f-103">Titkosítási hatókört hoz létre egy tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="a1f4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1f4f-104">SYNTAX</span></span>

### <span data-ttu-id="a1f4f-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1f4f-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f4f-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="a1f4f-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f4f-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a1f4f-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-RequireInfrastructureEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f4f-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="a1f4f-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1f4f-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1f4f-109">DESCRIPTION</span></span>
<span data-ttu-id="a1f4f-110">A **New-AzStorageEncryptionScope** parancsmag titkosítási hatókört hoz létre a Tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="a1f4f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1f4f-111">EXAMPLES</span></span>

### <span data-ttu-id="a1f4f-112">1. példa: Titkosítási tartomány létrehozása a Tártitkosítással</span><span class="sxs-lookup"><span data-stu-id="a1f4f-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="a1f4f-113">Ez a parancs titkosítási hatókört hoz létre a Tártitkosítással.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="a1f4f-114">2. példa: Titkosítási tartomány létrehozása a Keyvault-titkosítás és a RequireInfrastructureEncryption segítségével</span><span class="sxs-lookup"><span data-stu-id="a1f4f-114">Example 2: Create an encryption scope with Keyvault Encryption, and RequireInfrastructureEncryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" `
    -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57" `
    -RequireInfrastructureEncryption 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name         State   Source           KeyVaultKeyUri                                                                          RequireInfrastructureEncryption                                       
----         -----   ------             --------------                                                                        -------------------------------                                     
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57  True 
```

<span data-ttu-id="a1f4f-115">Ez a parancs a Keyvault titkosítás és a RequireInfrastructureEncryption titkosítással hoz létre titkosítási hatókört.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-115">This command creates an encryption scope with Keyvault Encryption and RequireInfrastructureEncryption.</span></span>
<span data-ttu-id="a1f4f-116">A tárfiók identitásának rendelkeznie kell a kulcskulcs lekért,wrapkey és unwrapkey engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="a1f4f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1f4f-117">PARAMETERS</span></span>

### <span data-ttu-id="a1f4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f4f-118">-DefaultProfile</span></span>
<span data-ttu-id="a1f4f-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1f4f-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="a1f4f-120">-EncryptionScopeName</span></span>
<span data-ttu-id="a1f4f-121">Azure Storage EncryptionScope-név</span><span class="sxs-lookup"><span data-stu-id="a1f4f-121">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="a1f4f-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="a1f4f-122">-KeyUri</span></span>
<span data-ttu-id="a1f4f-123">The key Uri</span><span class="sxs-lookup"><span data-stu-id="a1f4f-123">The key Uri</span></span>

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

### <span data-ttu-id="a1f4f-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="a1f4f-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="a1f4f-125">Titkosítási hatókör létrehozása a keySource segítségével Microsoft.Keyvaultként</span><span class="sxs-lookup"><span data-stu-id="a1f4f-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="a1f4f-126">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="a1f4f-126">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="a1f4f-127">A titkosítási hatókör egy másodlagos titkosítási réteget alkalmaz platform felügyelt kulcsokkal a nyugta adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-127">The encryption scope will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="a1f4f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1f4f-128">-ResourceGroupName</span></span>
<span data-ttu-id="a1f4f-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="a1f4f-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1f4f-130">-StorageAccount</span></span>
<span data-ttu-id="a1f4f-131">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="a1f4f-131">Storage account object</span></span>

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

### <span data-ttu-id="a1f4f-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a1f4f-132">-StorageAccountName</span></span>
<span data-ttu-id="a1f4f-133">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="a1f4f-134">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="a1f4f-134">-StorageEncryption</span></span>
<span data-ttu-id="a1f4f-135">Titkosítási hatókör létrehozása a keySource szolgáltatóval Microsoft.Storage-ként.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-135">Create encryption scope with keySource as Microsoft.Storage.</span></span>

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

### <span data-ttu-id="a1f4f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1f4f-136">-Confirm</span></span>
<span data-ttu-id="a1f4f-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1f4f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1f4f-138">-WhatIf</span></span>
<span data-ttu-id="a1f4f-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1f4f-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1f4f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f4f-141">CommonParameters</span></span>
<span data-ttu-id="a1f4f-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1f4f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f4f-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1f4f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f4f-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1f4f-144">INPUTS</span></span>

### <span data-ttu-id="a1f4f-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1f4f-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="a1f4f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1f4f-146">OUTPUTS</span></span>

### <span data-ttu-id="a1f4f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="a1f4f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="a1f4f-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1f4f-148">NOTES</span></span>

## <span data-ttu-id="a1f4f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1f4f-149">RELATED LINKS</span></span>
