---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 3d854d6b820f6c2e23d99e3397173ec45d5b7697
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846045"
---
# <span data-ttu-id="ae9bd-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="ae9bd-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="ae9bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ae9bd-103">Visszanyeri a korábban törölt, legutóbb törölt, beépített tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="ae9bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae9bd-104">SYNTAX</span></span>

### <span data-ttu-id="ae9bd-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae9bd-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae9bd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae9bd-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae9bd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae9bd-107">DESCRIPTION</span></span>
<span data-ttu-id="ae9bd-108">A **Visszavonás-AzKeyVaultManagedStorageAccountRemoval** parancs visszanyeri a korábban törölt távtárolású tárterületet, feltéve, hogy az ehhez a tárolóhoz engedélyezve van a Soft DELETE, és a helyreállítási időszak során a helyreállítási kísérlet bekövetkezik.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="ae9bd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ae9bd-109">EXAMPLES</span></span>

### <span data-ttu-id="ae9bd-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ae9bd-110">Example 1</span></span>
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

<span data-ttu-id="ae9bd-111">A parancsok ezen sorozata határozza meg, hogy a megadott tárterület egy törölt állapotban van-e a boltozatban; a későbbi parancs visszanyeri a törölt tárterületet, így aktív állapotba kerül.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="ae9bd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae9bd-112">PARAMETERS</span></span>

### <span data-ttu-id="ae9bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae9bd-113">-DefaultProfile</span></span>
<span data-ttu-id="ae9bd-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae9bd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae9bd-115">-InputObject</span></span>
<span data-ttu-id="ae9bd-116">Távtárolású tárterület-objektum törölve</span><span class="sxs-lookup"><span data-stu-id="ae9bd-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="ae9bd-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae9bd-117">-Name</span></span>
<span data-ttu-id="ae9bd-118">A boltozattal felügyelt tárterület-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="ae9bd-119">Parancsmag: a cél teljes tartománynevét építi ki a boltozat nevéből, a jelenleg kijelölt környezetből és a felügyelt tárterület fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="ae9bd-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ae9bd-120">-VaultName</span></span>
<span data-ttu-id="ae9bd-121">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-121">Vault name.</span></span>
<span data-ttu-id="ae9bd-122">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ae9bd-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae9bd-123">-Confirm</span></span>
<span data-ttu-id="ae9bd-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae9bd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae9bd-125">-WhatIf</span></span>
<span data-ttu-id="ae9bd-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae9bd-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae9bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae9bd-128">CommonParameters</span></span>
<span data-ttu-id="ae9bd-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae9bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae9bd-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae9bd-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae9bd-131">INPUTS</span></span>

### <span data-ttu-id="ae9bd-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ae9bd-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="ae9bd-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae9bd-133">OUTPUTS</span></span>

### <span data-ttu-id="ae9bd-134">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="ae9bd-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ae9bd-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae9bd-135">NOTES</span></span>

## <span data-ttu-id="ae9bd-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae9bd-136">RELATED LINKS</span></span>
