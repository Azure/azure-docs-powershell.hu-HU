---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: a8e8bb9a4a006c30275f1de959181ad640a04f88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680359"
---
# <span data-ttu-id="482ef-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="482ef-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="482ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="482ef-102">SYNOPSIS</span></span>
<span data-ttu-id="482ef-103">Visszanyeri a korábban törölt, legutóbb törölt, beépített tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="482ef-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="482ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="482ef-104">SYNTAX</span></span>

### <span data-ttu-id="482ef-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="482ef-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="482ef-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="482ef-106">InputObject</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval
 [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="482ef-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="482ef-107">DESCRIPTION</span></span>
<span data-ttu-id="482ef-108">A **Visszavonás-AzureKeyVaultManagedStorageAccountRemoval** parancs visszanyeri a korábban törölt távtárolású tárterületet, feltéve, hogy az ehhez a tárolóhoz engedélyezve van a Soft DELETE, és a helyreállítási időszak során a helyreállítási kísérlet bekövetkezik.</span><span class="sxs-lookup"><span data-stu-id="482ef-108">The **Undo-AzureKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="482ef-109">Példák</span><span class="sxs-lookup"><span data-stu-id="482ef-109">EXAMPLES</span></span>

### <span data-ttu-id="482ef-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="482ef-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzureKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

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

<span data-ttu-id="482ef-111">A parancsok ezen sorozata határozza meg, hogy a megadott tárterület egy törölt állapotban van-e a boltozatban; a későbbi parancs visszanyeri a törölt tárterületet, így aktív állapotba kerül.</span><span class="sxs-lookup"><span data-stu-id="482ef-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="482ef-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="482ef-112">PARAMETERS</span></span>

### <span data-ttu-id="482ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482ef-113">-DefaultProfile</span></span>
<span data-ttu-id="482ef-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="482ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="482ef-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="482ef-115">-InputObject</span></span>
<span data-ttu-id="482ef-116">Távtárolású tárterület-objektum törölve</span><span class="sxs-lookup"><span data-stu-id="482ef-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="482ef-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="482ef-117">-Name</span></span>
<span data-ttu-id="482ef-118">A boltozattal felügyelt tárterület-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="482ef-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="482ef-119">Parancsmag: a cél teljes tartománynevét építi ki a boltozat nevéből, a jelenleg kijelölt környezetből és a felügyelt tárterület fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="482ef-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="482ef-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="482ef-120">-VaultName</span></span>
<span data-ttu-id="482ef-121">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="482ef-121">Vault name.</span></span>
<span data-ttu-id="482ef-122">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="482ef-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="482ef-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="482ef-123">-Confirm</span></span>
<span data-ttu-id="482ef-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="482ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="482ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="482ef-125">-WhatIf</span></span>
<span data-ttu-id="482ef-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="482ef-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="482ef-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="482ef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="482ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482ef-128">CommonParameters</span></span>
<span data-ttu-id="482ef-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="482ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482ef-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="482ef-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482ef-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="482ef-131">INPUTS</span></span>

### <span data-ttu-id="482ef-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="482ef-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="482ef-133">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="482ef-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="482ef-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="482ef-134">OUTPUTS</span></span>

### <span data-ttu-id="482ef-135">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="482ef-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="482ef-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="482ef-136">NOTES</span></span>

## <span data-ttu-id="482ef-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="482ef-137">RELATED LINKS</span></span>
