---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6f4907f9ee94c05161fa602fc5cefd0ead4f6224
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195037"
---
# <span data-ttu-id="749cb-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="749cb-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="749cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="749cb-102">SYNOPSIS</span></span>
<span data-ttu-id="749cb-103">Egy Azure-tárterületet tároló fiók kezelési házirendjét távolítja el.</span><span class="sxs-lookup"><span data-stu-id="749cb-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="749cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="749cb-104">SYNTAX</span></span>

### <span data-ttu-id="749cb-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="749cb-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="749cb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="749cb-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="749cb-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="749cb-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="749cb-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="749cb-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="749cb-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="749cb-109">DESCRIPTION</span></span>
<span data-ttu-id="749cb-110">A **Remove-AzStorageAccountManagementPolicy** parancsmag eltávolítja az Azure Storage-fiók kezelési házirendjét.</span><span class="sxs-lookup"><span data-stu-id="749cb-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="749cb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="749cb-111">EXAMPLES</span></span>

### <span data-ttu-id="749cb-112">1. példa: a tárolási fiók kezelési házirendjének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="749cb-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="749cb-113">Ez a parancs eltávolítja a tárolási fiók kezelési házirendjét.</span><span class="sxs-lookup"><span data-stu-id="749cb-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="749cb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="749cb-114">PARAMETERS</span></span>

### <span data-ttu-id="749cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="749cb-115">-DefaultProfile</span></span>
<span data-ttu-id="749cb-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="749cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="749cb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="749cb-117">-InputObject</span></span>
<span data-ttu-id="749cb-118">Eltávolítandó felügyeleti objektum</span><span class="sxs-lookup"><span data-stu-id="749cb-118">Management Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: PolicyObject
Aliases: ManagementPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="749cb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="749cb-119">-PassThru</span></span>
<span data-ttu-id="749cb-120">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="749cb-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="749cb-121">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="749cb-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="749cb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="749cb-122">-ResourceGroupName</span></span>
<span data-ttu-id="749cb-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="749cb-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="749cb-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="749cb-124">-StorageAccount</span></span>
<span data-ttu-id="749cb-125">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="749cb-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="749cb-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="749cb-126">-StorageAccountName</span></span>
<span data-ttu-id="749cb-127">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="749cb-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="749cb-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="749cb-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="749cb-129">Tárolási fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="749cb-129">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749cb-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="749cb-130">-Confirm</span></span>
<span data-ttu-id="749cb-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="749cb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="749cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="749cb-132">-WhatIf</span></span>
<span data-ttu-id="749cb-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="749cb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="749cb-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="749cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="749cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="749cb-135">CommonParameters</span></span>
<span data-ttu-id="749cb-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="749cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="749cb-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="749cb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="749cb-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="749cb-138">INPUTS</span></span>

### <span data-ttu-id="749cb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="749cb-139">System.String</span></span>

## <span data-ttu-id="749cb-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="749cb-140">OUTPUTS</span></span>

### <span data-ttu-id="749cb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="749cb-141">System.Boolean</span></span>

## <span data-ttu-id="749cb-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="749cb-142">NOTES</span></span>

## <span data-ttu-id="749cb-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="749cb-143">RELATED LINKS</span></span>