---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: c09218b960fb6c11b685106a3cb90bfdfd2f546a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323942"
---
# <span data-ttu-id="af5cc-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="af5cc-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="af5cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="af5cc-103">Lekérte a kulcstár által felügyelt TÁROLÓ SAS-definíciókat.</span><span class="sxs-lookup"><span data-stu-id="af5cc-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="af5cc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="af5cc-104">SYNTAX</span></span>

### <span data-ttu-id="af5cc-105">ByDefinitionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af5cc-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af5cc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="af5cc-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af5cc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="af5cc-107">DESCRIPTION</span></span>
<span data-ttu-id="af5cc-108">Egy kulcstár által felügyelt TÁROLÓ SAS-definíciót kap, ha a definíció neve meg van adva.</span><span class="sxs-lookup"><span data-stu-id="af5cc-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="af5cc-109">Ha a definíció neve nincs megadva, akkor a rendszer felsorolja a tárolóban a megadott kulcstár által felügyelt tárfiókhoz társított ÖSSZES SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="af5cc-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="af5cc-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="af5cc-110">EXAMPLES</span></span>

### <span data-ttu-id="af5cc-111">1. példa: Az összes felügyelt tároló tároló SAS-definíciójának felsorolása</span><span class="sxs-lookup"><span data-stu-id="af5cc-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="af5cc-112">A "myvault" tároló által kezelt, kulcstár által felügyelt tárfiókkal (mystorageaccount) társított ÖSSZES SAS-definíciót sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="af5cc-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="af5cc-113">2. példa: A kulcstár felügyelt tárfiókja</span><span class="sxs-lookup"><span data-stu-id="af5cc-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="af5cc-114">A "myvault" nevű tároló által kezelt kulcstár által kezelt tárfiókkal (mystorageaccount) társított SAS-definíciós "accountsas" adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="af5cc-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="af5cc-115">3. példa: Az összes kulcstár által felügyelt tár SAS-definíciójának felsorolása szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="af5cc-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name "account*"

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas1
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas1
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas2
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas2
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="af5cc-116">A "fiók" kezdetű "mystorageaccount" nevű tároló által kezelt kulcstárhoz tartozó ÖSSZES SAS-definíciót sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="af5cc-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="af5cc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af5cc-117">PARAMETERS</span></span>

### <span data-ttu-id="af5cc-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="af5cc-118">-AccountName</span></span>
<span data-ttu-id="af5cc-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="af5cc-119">Vault name.</span></span>
<span data-ttu-id="af5cc-120">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="af5cc-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="af5cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af5cc-121">-DefaultProfile</span></span>
<span data-ttu-id="af5cc-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="af5cc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af5cc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af5cc-123">-InputObject</span></span>
<span data-ttu-id="af5cc-124">ManagedStorageAccount objektum.</span><span class="sxs-lookup"><span data-stu-id="af5cc-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="af5cc-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="af5cc-125">-InRemovedState</span></span>
<span data-ttu-id="af5cc-126">Megadja, hogy meg kell-e mutatni a korábban törölt tárolási sas-definíciókat a kimenetben.</span><span class="sxs-lookup"><span data-stu-id="af5cc-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="af5cc-127">-Name</span><span class="sxs-lookup"><span data-stu-id="af5cc-127">-Name</span></span>
<span data-ttu-id="af5cc-128">Tárterület sas-definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="af5cc-128">Storage sas definition name.</span></span>
<span data-ttu-id="af5cc-129">A parancsmag egy tárolónévből ( jelenleg kijelölt környezetből, tárfiók neve és sas-definíció neve) származó tár sas-definíciójának teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="af5cc-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5cc-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="af5cc-130">-VaultName</span></span>
<span data-ttu-id="af5cc-131">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="af5cc-131">Vault name.</span></span>
<span data-ttu-id="af5cc-132">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="af5cc-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="af5cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af5cc-133">CommonParameters</span></span>
<span data-ttu-id="af5cc-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af5cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af5cc-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af5cc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af5cc-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af5cc-136">INPUTS</span></span>

### <span data-ttu-id="af5cc-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="af5cc-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="af5cc-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af5cc-138">OUTPUTS</span></span>

### <span data-ttu-id="af5cc-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="af5cc-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="af5cc-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="af5cc-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="af5cc-141">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="af5cc-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="af5cc-142">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="af5cc-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="af5cc-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="af5cc-143">NOTES</span></span>

## <span data-ttu-id="af5cc-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af5cc-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

