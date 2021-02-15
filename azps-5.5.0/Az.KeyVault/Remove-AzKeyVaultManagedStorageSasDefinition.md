---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159579"
---
# <span data-ttu-id="7ab4f-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="7ab4f-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="7ab4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ab4f-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab4f-103">Eltávolít egy kulcstár által felügyelt Azure Storage SAS-definíciókat.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="7ab4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ab4f-104">SYNTAX</span></span>

### <span data-ttu-id="7ab4f-105">ByDefinitionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ab4f-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ab4f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7ab4f-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ab4f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ab4f-107">DESCRIPTION</span></span>
<span data-ttu-id="7ab4f-108">Eltávolít egy kulcstár által felügyelt Azure Storage SAS-definíciókat.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="7ab4f-109">Ezzel az SAS-definíció alapján eltávolítja az SAS-jogkivonat lekért titkosságát is.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="7ab4f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ab4f-110">EXAMPLES</span></span>

### <span data-ttu-id="7ab4f-111">1. példa: Távolítsa el a kulcstár által felügyelt Azure Storage SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="7ab4f-112">Eltávolítja a mystorageaccount nevű fiókkal társított kulcstár által felügyelt TÁROLÓ SAS-definíció "mysasdef" nevű definícióját a myvault tárolóban.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="7ab4f-113">2. példa: Felhasználó jóváhagyása nélkül távolítsa el a kulcstár által felügyelt Azure Storage SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="7ab4f-114">Eltávolítja a "myvault" tárolóban a "mystorageaccount" fiókkal társított kulcstár által felügyelt TÁROLÓ SAS-definíció "mysasdef" definícióját.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="7ab4f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ab4f-115">PARAMETERS</span></span>

### <span data-ttu-id="7ab4f-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7ab4f-116">-AccountName</span></span>
<span data-ttu-id="7ab4f-117">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-117">Storage account name.</span></span>
<span data-ttu-id="7ab4f-118">A parancsmag egy felügyelt tárfiók nevének FQDN-ét építi fel a tároló nevéből, amely jelenleg ki van jelölve a környezet és a tárfiók neve között.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab4f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab4f-119">-DefaultProfile</span></span>
<span data-ttu-id="7ab4f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7ab4f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ab4f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7ab4f-121">-Force</span></span>
<span data-ttu-id="7ab4f-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7ab4f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ab4f-123">-InputObject</span></span>
<span data-ttu-id="7ab4f-124">ManagedStorageSasDefinition objektum.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-124">ManagedStorageSasDefinition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab4f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7ab4f-125">-Name</span></span>
<span data-ttu-id="7ab4f-126">Tárterület sas-definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-126">Storage sas definition name.</span></span>
<span data-ttu-id="7ab4f-127">A parancsmag egy tárolónévből ( jelenleg kijelölt környezetből, tárfiók neve és sas-definíció neve) származó tár sas-definíciójának teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab4f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ab4f-128">-PassThru</span></span>
<span data-ttu-id="7ab4f-129">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7ab4f-130">Ha ez a kapcsoló meg van adva, a parancsmag a törölt felügyelt tárfiókot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="7ab4f-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7ab4f-131">-VaultName</span></span>
<span data-ttu-id="7ab4f-132">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-132">Vault name.</span></span>
<span data-ttu-id="7ab4f-133">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7ab4f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ab4f-134">-Confirm</span></span>
<span data-ttu-id="7ab4f-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ab4f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ab4f-136">-WhatIf</span></span>
<span data-ttu-id="7ab4f-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ab4f-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ab4f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab4f-139">CommonParameters</span></span>
<span data-ttu-id="7ab4f-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab4f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab4f-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ab4f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab4f-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ab4f-142">INPUTS</span></span>

### <span data-ttu-id="7ab4f-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7ab4f-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="7ab4f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ab4f-144">OUTPUTS</span></span>

### <span data-ttu-id="7ab4f-145">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="7ab4f-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="7ab4f-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ab4f-146">NOTES</span></span>

## <span data-ttu-id="7ab4f-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ab4f-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

