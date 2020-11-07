---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845170"
---
# <span data-ttu-id="c0000-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="c0000-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="c0000-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0000-102">SYNOPSIS</span></span>
<span data-ttu-id="c0000-103">Visszavonhatja a tárterület-fiók összes felhasználói meghatalmazási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="c0000-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="c0000-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0000-104">SYNTAX</span></span>

### <span data-ttu-id="c0000-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0000-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0000-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c0000-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0000-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c0000-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0000-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0000-108">DESCRIPTION</span></span>
<span data-ttu-id="c0000-109">A **Visszavonás-AzStorageAccountUserDelegationKeys** parancsmag visszavonja a tárterület-fiók összes felhasználói meghatalmazási kulcsát, így a tárolási fiók minden identitás sas-tokenje is visszavonásra kerül.</span><span class="sxs-lookup"><span data-stu-id="c0000-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="c0000-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c0000-110">EXAMPLES</span></span>

### <span data-ttu-id="c0000-111">Példa 1: egy tárterület-fiók minden felhasználó által delegált kulcsának visszavonása</span><span class="sxs-lookup"><span data-stu-id="c0000-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="c0000-112">Ez a példa visszavonja egy tárolási fiók minden felhasználó által delegált kulcsát, így a felhasználói meghatalmazási kulcsokból létrehozott összes identitás SAS-tokent visszavonja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="c0000-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="c0000-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0000-113">PARAMETERS</span></span>

### <span data-ttu-id="c0000-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0000-114">-DefaultProfile</span></span>
<span data-ttu-id="c0000-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0000-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0000-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0000-116">-InputObject</span></span>
<span data-ttu-id="c0000-117">A Storage Account objektum, amelyet Get_AzStorageAccount, a New-AzStorageAccount visszaadott.</span><span class="sxs-lookup"><span data-stu-id="c0000-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0000-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0000-118">-PassThru</span></span>
<span data-ttu-id="c0000-119">Ez a parancsmag általában a sikeres befejezéshez nem ad kimenetet, ez a paraméter arra kényszeríti a parancsmagot, hogy a sikeres befejezéshez értéket ($true) ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c0000-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="c0000-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0000-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0000-121">Az erőforráscsoport neve, amely a tárolási fiók erőforrását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c0000-121">The resource group name containing the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0000-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0000-122">-ResourceId</span></span>
<span data-ttu-id="c0000-123">Tárolási fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c0000-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0000-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c0000-124">-StorageAccountName</span></span>
<span data-ttu-id="c0000-125">A tárolási fiók erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="c0000-125">The name of the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0000-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0000-126">-Confirm</span></span>
<span data-ttu-id="c0000-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0000-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0000-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0000-128">-WhatIf</span></span>
<span data-ttu-id="c0000-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c0000-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0000-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0000-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0000-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0000-131">CommonParameters</span></span>
<span data-ttu-id="c0000-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0000-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0000-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0000-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0000-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0000-134">INPUTS</span></span>

### <span data-ttu-id="c0000-135">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c0000-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c0000-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c0000-136">System.String</span></span>

## <span data-ttu-id="c0000-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0000-137">OUTPUTS</span></span>

### <span data-ttu-id="c0000-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0000-138">System.Boolean</span></span>

## <span data-ttu-id="c0000-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0000-139">NOTES</span></span>

## <span data-ttu-id="c0000-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0000-140">RELATED LINKS</span></span>
