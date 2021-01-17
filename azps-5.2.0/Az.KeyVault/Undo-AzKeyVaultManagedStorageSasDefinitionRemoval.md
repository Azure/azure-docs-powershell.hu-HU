---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: bb44bc8f5e4537691d1e5d5493a29111ceaf42a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335034"
---
# <span data-ttu-id="64496-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="64496-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="64496-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64496-102">SYNOPSIS</span></span>
<span data-ttu-id="64496-103">Helyreállít egy korábban törölt KeyVault-felügyelt tárTERÜLET SAS-definícióját.</span><span class="sxs-lookup"><span data-stu-id="64496-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="64496-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64496-104">SYNTAX</span></span>

### <span data-ttu-id="64496-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64496-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64496-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="64496-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64496-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64496-107">DESCRIPTION</span></span>
<span data-ttu-id="64496-108">Az **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** parancs helyreállít egy korábban törölt felügyelt tár SAS-definíciót, feltéve hogy a helyreállítható törlés engedélyezve van ehhez a tárolóhoz, és hogy a helyreállítás a helyreállítási időszak során történik.</span><span class="sxs-lookup"><span data-stu-id="64496-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="64496-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64496-109">EXAMPLES</span></span>

### <span data-ttu-id="64496-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="64496-110">Example 1</span></span>
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

<span data-ttu-id="64496-111">Ez a parancssorozat határozza meg, hogy a megadott tárTERÜLET SAS-definíciója létezik-e a tárolóban törölt állapotban; az ezt követő parancs helyreállítja a törölt sas-definíciót, és visszaállítja azt egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="64496-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="64496-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64496-112">PARAMETERS</span></span>

### <span data-ttu-id="64496-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="64496-113">-AccountName</span></span>
<span data-ttu-id="64496-114">KeyVault-felügyelt tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="64496-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="64496-115">A parancsmag egy felügyelt tár SAS-definíciójának teljes tartománynevét építi fel a tárolónévből, a jelenleg kijelölt környezetből és a felügyelt tárfiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="64496-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

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

### <span data-ttu-id="64496-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64496-116">-DefaultProfile</span></span>
<span data-ttu-id="64496-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64496-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64496-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64496-118">-InputObject</span></span>
<span data-ttu-id="64496-119">Törölt felügyelt tárTERÜLET SAS-definíciós objektuma</span><span class="sxs-lookup"><span data-stu-id="64496-119">Deleted managed storage SAS definition object</span></span>

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

### <span data-ttu-id="64496-120">-Name</span><span class="sxs-lookup"><span data-stu-id="64496-120">-Name</span></span>
<span data-ttu-id="64496-121">A KeyVault által felügyelt tárTERÜLET SAS-definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="64496-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="64496-122">A parancsmag a cél teljes tartománynevét a tároló neve, az aktuálisan kijelölt környezet, a felügyelt tárfiók neve és az SAS-definíció neve alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="64496-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

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

### <span data-ttu-id="64496-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="64496-123">-VaultName</span></span>
<span data-ttu-id="64496-124">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="64496-124">Vault name.</span></span>
<span data-ttu-id="64496-125">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="64496-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="64496-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64496-126">-Confirm</span></span>
<span data-ttu-id="64496-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="64496-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64496-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64496-128">-WhatIf</span></span>
<span data-ttu-id="64496-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="64496-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64496-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64496-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64496-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64496-131">CommonParameters</span></span>
<span data-ttu-id="64496-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64496-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64496-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64496-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64496-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64496-134">INPUTS</span></span>

### <span data-ttu-id="64496-135">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="64496-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="64496-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64496-136">OUTPUTS</span></span>

### <span data-ttu-id="64496-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="64496-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="64496-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64496-138">NOTES</span></span>

## <span data-ttu-id="64496-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64496-139">RELATED LINKS</span></span>
