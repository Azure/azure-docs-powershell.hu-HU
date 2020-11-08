---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: c09218b960fb6c11b685106a3cb90bfdfd2f546a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024749"
---
# <span data-ttu-id="6e938-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="6e938-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="6e938-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e938-102">SYNOPSIS</span></span>
<span data-ttu-id="6e938-103">Beolvassa a fontos Vault-tárolók biztonsági társításának definícióit.</span><span class="sxs-lookup"><span data-stu-id="6e938-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="6e938-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e938-104">SYNTAX</span></span>

### <span data-ttu-id="6e938-105">ByDefinitionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e938-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e938-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6e938-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e938-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e938-107">DESCRIPTION</span></span>
<span data-ttu-id="6e938-108">A felügyelt tárterületet tároló biztonsági társítási definíciót kapja, ha a definíció neve meg van adva.</span><span class="sxs-lookup"><span data-stu-id="6e938-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="6e938-109">Ha a definíció neve nincs megadva, akkor a rendszer a tárolóban a megadott kulcsos boltozat-fiókhoz társított összes SAS-definíciót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6e938-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="6e938-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6e938-110">EXAMPLES</span></span>

### <span data-ttu-id="6e938-111">1. példa: az összes fontos Vault Managed Storage SAS definíciójának listázása</span><span class="sxs-lookup"><span data-stu-id="6e938-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
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

<span data-ttu-id="6e938-112">A "myvault" által kezelt "mystorageaccount" kulcs boltozattal kezelt tárterület-fiókkal társított összes biztonsági társítási definíció felsorolása</span><span class="sxs-lookup"><span data-stu-id="6e938-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="6e938-113">2. példa: fontos boltozatos tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="6e938-113">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="6e938-114">A "accountsas" a "mystorageaccount" "myvault" által felügyelt "" című, a "" kulcs boltozat-definíciójának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6e938-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="6e938-115">3. példa: az összes fontos Vault Managed Storage SAS-definíció listázása szűréssel</span><span class="sxs-lookup"><span data-stu-id="6e938-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
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

<span data-ttu-id="6e938-116">A "fiók" kezdetű "myvault" "mystorageaccount" kulcs boltozattal kezelt tárterület-fiókjával társított összes biztonsági társítási definíciót felsorolja.</span><span class="sxs-lookup"><span data-stu-id="6e938-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="6e938-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e938-117">PARAMETERS</span></span>

### <span data-ttu-id="6e938-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6e938-118">-AccountName</span></span>
<span data-ttu-id="6e938-119">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="6e938-119">Vault name.</span></span>
<span data-ttu-id="6e938-120">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="6e938-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="6e938-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e938-121">-DefaultProfile</span></span>
<span data-ttu-id="6e938-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6e938-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e938-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e938-123">-InputObject</span></span>
<span data-ttu-id="6e938-124">ManagedStorageAccount objektum</span><span class="sxs-lookup"><span data-stu-id="6e938-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="6e938-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="6e938-125">-InRemovedState</span></span>
<span data-ttu-id="6e938-126">Itt adhatja meg, hogy megjelenjen-e a korábban törölt tárterület sas-definíciója a kimenetben.</span><span class="sxs-lookup"><span data-stu-id="6e938-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="6e938-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e938-127">-Name</span></span>
<span data-ttu-id="6e938-128">Storage sas-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="6e938-128">Storage sas definition name.</span></span>
<span data-ttu-id="6e938-129">Parancsmag: a tároló biztonsági társításának FQDN-definícióját a boltozat neve, a jelenleg kijelölt környezet, a tárolási fiók neve és a sas-definíció neve alapján építi ki.</span><span class="sxs-lookup"><span data-stu-id="6e938-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="6e938-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6e938-130">-VaultName</span></span>
<span data-ttu-id="6e938-131">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="6e938-131">Vault name.</span></span>
<span data-ttu-id="6e938-132">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="6e938-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="6e938-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e938-133">CommonParameters</span></span>
<span data-ttu-id="6e938-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e938-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e938-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6e938-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e938-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e938-136">INPUTS</span></span>

### <span data-ttu-id="6e938-137">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccountIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="6e938-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="6e938-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e938-138">OUTPUTS</span></span>

### <span data-ttu-id="6e938-139">Microsoft. Azure. Command. PSKeyVaultManagedStorageSasDefinitionIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="6e938-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="6e938-140">Microsoft. Azure. Command. PSKeyVaultManagedStorageSasDefinition. models.</span><span class="sxs-lookup"><span data-stu-id="6e938-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="6e938-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="6e938-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="6e938-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6e938-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="6e938-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e938-143">NOTES</span></span>

## <span data-ttu-id="6e938-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e938-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

