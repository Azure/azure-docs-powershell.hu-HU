---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 289adecd07837134fed9279758cf1142d30183a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010469"
---
# <span data-ttu-id="c4a14-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="c4a14-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="c4a14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4a14-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a14-103">Helyreállít egy korábban törölt KeyVault-felügyelt tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="c4a14-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="c4a14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4a14-104">SYNTAX</span></span>

### <span data-ttu-id="c4a14-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4a14-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4a14-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c4a14-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4a14-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4a14-107">DESCRIPTION</span></span>
<span data-ttu-id="c4a14-108">Az **Undo-AzKeyVaultManagedStorageAccountRemoval** parancs helyreállít egy korábban törölt felügyelt tárfiókot, feltéve, hogy a helyreállítható törlés engedélyezve van ehhez a tárolóhoz, és hogy a helyreállítás a helyreállítási időszak során történik.</span><span class="sxs-lookup"><span data-stu-id="c4a14-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="c4a14-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4a14-109">EXAMPLES</span></span>

### <span data-ttu-id="c4a14-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c4a14-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

Id                  : https://myvault.vault.azure.net:443/storage/myaccount
Vault Name          : myVault
AccountName         : myAccount
Account Resource Id : /subscriptions/8bc48661-1801-4b7a-8ca1-6a3cadfb4870/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/myaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="c4a14-111">Ez a parancssorozat határozza meg, hogy a megadott tárfiók létezik-e a tárolóban törölt állapotban; A következő parancs helyreállítja a törölt tárfiókot, és visszaállítja azt egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="c4a14-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="c4a14-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4a14-112">PARAMETERS</span></span>

### <span data-ttu-id="c4a14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a14-113">-DefaultProfile</span></span>
<span data-ttu-id="c4a14-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4a14-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a14-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4a14-115">-InputObject</span></span>
<span data-ttu-id="c4a14-116">Törölt Felügyelt tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="c4a14-116">Deleted Managed Storage Account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a14-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c4a14-117">-Name</span></span>
<span data-ttu-id="c4a14-118">A KeyVault felügyelt tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="c4a14-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="c4a14-119">A parancsmag a cél teljes tartománynevét a tároló nevéből, az aktuálisan kijelölt környezetből és a felügyelt tárfiók nevéből építi fel.</span><span class="sxs-lookup"><span data-stu-id="c4a14-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a14-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c4a14-120">-VaultName</span></span>
<span data-ttu-id="c4a14-121">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="c4a14-121">Vault name.</span></span>
<span data-ttu-id="c4a14-122">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="c4a14-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c4a14-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4a14-123">-Confirm</span></span>
<span data-ttu-id="c4a14-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c4a14-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a14-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a14-125">-WhatIf</span></span>
<span data-ttu-id="c4a14-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c4a14-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a14-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4a14-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a14-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a14-128">CommonParameters</span></span>
<span data-ttu-id="c4a14-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a14-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a14-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4a14-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a14-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4a14-131">INPUTS</span></span>

### <span data-ttu-id="c4a14-132">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c4a14-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="c4a14-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4a14-133">OUTPUTS</span></span>

### <span data-ttu-id="c4a14-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c4a14-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c4a14-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4a14-135">NOTES</span></span>

## <span data-ttu-id="c4a14-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4a14-136">RELATED LINKS</span></span>
