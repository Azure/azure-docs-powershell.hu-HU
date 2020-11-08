---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024748"
---
# <span data-ttu-id="cbe4d-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="cbe4d-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="cbe4d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbe4d-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe4d-103">Eltávolítja az Azure Managed Azure Storage SAS definícióit.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="cbe4d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbe4d-104">SYNTAX</span></span>

### <span data-ttu-id="cbe4d-105">ByDefinitionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbe4d-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbe4d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cbe4d-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbe4d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbe4d-107">DESCRIPTION</span></span>
<span data-ttu-id="cbe4d-108">Eltávolítja az Azure Managed Azure Storage SAS definícióit.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="cbe4d-109">Ez a beállítás eltávolítja azt a titkot is, amellyel a SAS-tokent a SAS-definícióval szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="cbe4d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cbe4d-110">EXAMPLES</span></span>

### <span data-ttu-id="cbe4d-111">Példa 1: az Azure Managed Azure Storage SAS definíciójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
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

<span data-ttu-id="cbe4d-112">Eltávolítja a "mystorageaccount" fiók "myvault" mysasdef társított "" fiókkal társított kulcs-Vault Managed Storage SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="cbe4d-113">2. példa: távolítsa el a Key Vault Managed Azure Storage SAS definícióját felhasználó megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
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

<span data-ttu-id="cbe4d-114">Eltávolítja a "mystorageaccount" fiók "myvault" mysasdef társított "" fiókkal társított kulcs-Vault Managed Storage SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="cbe4d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbe4d-115">PARAMETERS</span></span>

### <span data-ttu-id="cbe4d-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cbe4d-116">-AccountName</span></span>
<span data-ttu-id="cbe4d-117">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-117">Storage account name.</span></span>
<span data-ttu-id="cbe4d-118">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a boltozat neve, a jelenleg kijelölt környezet és a tárolási fiók neve között.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="cbe4d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe4d-119">-DefaultProfile</span></span>
<span data-ttu-id="cbe4d-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cbe4d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbe4d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cbe4d-121">-Force</span></span>
<span data-ttu-id="cbe4d-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cbe4d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbe4d-123">-InputObject</span></span>
<span data-ttu-id="cbe4d-124">ManagedStorageSasDefinition objektum</span><span class="sxs-lookup"><span data-stu-id="cbe4d-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="cbe4d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cbe4d-125">-Name</span></span>
<span data-ttu-id="cbe4d-126">Storage sas-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-126">Storage sas definition name.</span></span>
<span data-ttu-id="cbe4d-127">Parancsmag: a tároló biztonsági társításának FQDN-definícióját a boltozat neve, a jelenleg kijelölt környezet, a tárolási fiók neve és a sas-definíció neve alapján építi ki.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="cbe4d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbe4d-128">-PassThru</span></span>
<span data-ttu-id="cbe4d-129">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cbe4d-130">Ha meg van adva ez a kapcsoló, akkor a parancsmag a törölt tárterület-fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="cbe4d-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cbe4d-131">-VaultName</span></span>
<span data-ttu-id="cbe4d-132">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-132">Vault name.</span></span>
<span data-ttu-id="cbe4d-133">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="cbe4d-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cbe4d-134">-Confirm</span></span>
<span data-ttu-id="cbe4d-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbe4d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbe4d-136">-WhatIf</span></span>
<span data-ttu-id="cbe4d-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbe4d-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbe4d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe4d-139">CommonParameters</span></span>
<span data-ttu-id="cbe4d-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbe4d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe4d-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe4d-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbe4d-142">INPUTS</span></span>

### <span data-ttu-id="cbe4d-143">Microsoft. Azure. Command. PSKeyVaultManagedStorageSasDefinitionIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="cbe4d-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="cbe4d-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbe4d-144">OUTPUTS</span></span>

### <span data-ttu-id="cbe4d-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="cbe4d-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="cbe4d-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbe4d-146">NOTES</span></span>

## <span data-ttu-id="cbe4d-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbe4d-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

