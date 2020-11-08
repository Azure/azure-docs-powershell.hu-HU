---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185788"
---
# <span data-ttu-id="6ccc3-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="6ccc3-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="6ccc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ccc3-102">SYNOPSIS</span></span>
<span data-ttu-id="6ccc3-103">Visszavonhatja a tárterület-fiók összes felhasználói meghatalmazási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="6ccc3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ccc3-104">SYNTAX</span></span>

### <span data-ttu-id="6ccc3-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ccc3-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ccc3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6ccc3-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ccc3-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6ccc3-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ccc3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ccc3-108">DESCRIPTION</span></span>
<span data-ttu-id="6ccc3-109">A **Visszavonás-AzStorageAccountUserDelegationKeys** parancsmag visszavonja a tárterület-fiók összes felhasználói meghatalmazási kulcsát, így a tárolási fiók minden identitás sas-tokenje is visszavonásra kerül.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="6ccc3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6ccc3-110">EXAMPLES</span></span>

### <span data-ttu-id="6ccc3-111">Példa 1: egy tárterület-fiók minden felhasználó által delegált kulcsának visszavonása</span><span class="sxs-lookup"><span data-stu-id="6ccc3-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="6ccc3-112">Ez a példa visszavonja egy tárolási fiók minden felhasználó által delegált kulcsát, így a felhasználói meghatalmazási kulcsokból létrehozott összes identitás SAS-tokent visszavonja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="6ccc3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ccc3-113">PARAMETERS</span></span>

### <span data-ttu-id="6ccc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ccc3-114">-DefaultProfile</span></span>
<span data-ttu-id="6ccc3-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ccc3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ccc3-116">-InputObject</span></span>
<span data-ttu-id="6ccc3-117">A Storage Account objektum, amelyet Get_AzStorageAccount, a New-AzStorageAccount visszaadott.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

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

### <span data-ttu-id="6ccc3-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ccc3-118">-PassThru</span></span>
<span data-ttu-id="6ccc3-119">Ez a parancsmag általában a sikeres befejezéshez nem ad kimenetet, ez a paraméter arra kényszeríti a parancsmagot, hogy a sikeres befejezéshez értéket ($true) ad vissza.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="6ccc3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ccc3-120">-ResourceGroupName</span></span>
<span data-ttu-id="6ccc3-121">Az erőforráscsoport neve, amely a tárolási fiók erőforrását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="6ccc3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ccc3-122">-ResourceId</span></span>
<span data-ttu-id="6ccc3-123">Tárolási fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6ccc3-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="6ccc3-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6ccc3-124">-StorageAccountName</span></span>
<span data-ttu-id="6ccc3-125">A tárolási fiók erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-125">The name of the storage account resource.</span></span>

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

### <span data-ttu-id="6ccc3-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6ccc3-126">-Confirm</span></span>
<span data-ttu-id="6ccc3-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ccc3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ccc3-128">-WhatIf</span></span>
<span data-ttu-id="6ccc3-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ccc3-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ccc3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ccc3-131">CommonParameters</span></span>
<span data-ttu-id="6ccc3-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ccc3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ccc3-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ccc3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ccc3-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ccc3-134">INPUTS</span></span>

### <span data-ttu-id="6ccc3-135">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ccc3-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6ccc3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6ccc3-136">System.String</span></span>

## <span data-ttu-id="6ccc3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ccc3-137">OUTPUTS</span></span>

### <span data-ttu-id="6ccc3-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ccc3-138">System.Boolean</span></span>

## <span data-ttu-id="6ccc3-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ccc3-139">NOTES</span></span>

## <span data-ttu-id="6ccc3-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ccc3-140">RELATED LINKS</span></span>
