---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: bb44bc8f5e4537691d1e5d5493a29111ceaf42a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194752"
---
# <span data-ttu-id="77dc6-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="77dc6-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="77dc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="77dc6-103">Visszanyeri a korábban törölt, "a" beépített "tároló" SAS definíciót.</span><span class="sxs-lookup"><span data-stu-id="77dc6-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="77dc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77dc6-104">SYNTAX</span></span>

### <span data-ttu-id="77dc6-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77dc6-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77dc6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="77dc6-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77dc6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="77dc6-107">DESCRIPTION</span></span>
<span data-ttu-id="77dc6-108">A **Visszavonás – AzKeyVaultManagedStorageSasDefinitionRemoval** parancs helyreállítja a korábban törölt, felügyelt tárterületet tartalmazó biztonsági társítások definícióját, feltéve, hogy az ehhez a tárolóhoz engedélyezve van a Soft DELETE, és a helyreállítási időszak során a helyreállítási kísérlet bekövetkezik.</span><span class="sxs-lookup"><span data-stu-id="77dc6-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="77dc6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="77dc6-109">EXAMPLES</span></span>

### <span data-ttu-id="77dc6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="77dc6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName myVault -AccountName myAccount -Name mySasName -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageSasDefinitionRemoval -VaultName myVault -AccountName myAccount -Name mySasName

Id          : https://myvault.vault.azure.net:443/storage/myaccount/sas/mysasname
Secret Id   : https://myvault.vault.azure.net/secrets/myaccount-mysasname
Vault Name  : myVault
AccountName : myAccount
Name        : mySasName
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="77dc6-111">A parancsok ezen sorozata határozza meg, hogy a megadott tárterület SAS-definíciója létezik-e egy törölt állapotban; a későbbi parancs visszanyeri a törölt sas-definíciót, így aktív állapotba kerül.</span><span class="sxs-lookup"><span data-stu-id="77dc6-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="77dc6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77dc6-112">PARAMETERS</span></span>

### <span data-ttu-id="77dc6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="77dc6-113">-AccountName</span></span>
<span data-ttu-id="77dc6-114">A boltozattal felügyelt tárterület-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="77dc6-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="77dc6-115">Parancsmag: a felügyelt tárterület biztonsági társításának FQDN-definícióját a Vault name, a jelenleg kijelölt környezet és a felügyelt tárterület fiók neve alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="77dc6-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77dc6-116">-DefaultProfile</span></span>
<span data-ttu-id="77dc6-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77dc6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77dc6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77dc6-118">-InputObject</span></span>
<span data-ttu-id="77dc6-119">A Managed Storage SAS definition objektum törlése</span><span class="sxs-lookup"><span data-stu-id="77dc6-119">Deleted managed storage SAS definition object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77dc6-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77dc6-120">-Name</span></span>
<span data-ttu-id="77dc6-121">A boltozattal felügyelt tárterület SAS-definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="77dc6-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="77dc6-122">Parancsmag: a cél teljes tartománynevét építi ki a boltozat nevéből, a jelenleg kijelölt környezetből, a felügyelt tárterület fiók nevéből és a SAS-definíció nevéből.</span><span class="sxs-lookup"><span data-stu-id="77dc6-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dc6-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="77dc6-123">-VaultName</span></span>
<span data-ttu-id="77dc6-124">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="77dc6-124">Vault name.</span></span>
<span data-ttu-id="77dc6-125">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="77dc6-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dc6-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77dc6-126">-Confirm</span></span>
<span data-ttu-id="77dc6-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77dc6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77dc6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77dc6-128">-WhatIf</span></span>
<span data-ttu-id="77dc6-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77dc6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77dc6-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77dc6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77dc6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77dc6-131">CommonParameters</span></span>
<span data-ttu-id="77dc6-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77dc6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77dc6-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="77dc6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77dc6-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77dc6-134">INPUTS</span></span>

### <span data-ttu-id="77dc6-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="77dc6-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="77dc6-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77dc6-136">OUTPUTS</span></span>

### <span data-ttu-id="77dc6-137">Microsoft. Azure. Command. PSKeyVaultManagedStorageSasDefinition. models.</span><span class="sxs-lookup"><span data-stu-id="77dc6-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="77dc6-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77dc6-138">NOTES</span></span>

## <span data-ttu-id="77dc6-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77dc6-139">RELATED LINKS</span></span>