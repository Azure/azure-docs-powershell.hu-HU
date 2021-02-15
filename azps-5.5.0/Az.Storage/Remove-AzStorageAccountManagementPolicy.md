---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6f4907f9ee94c05161fa602fc5cefd0ead4f6224
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157994"
---
# <span data-ttu-id="261af-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="261af-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="261af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="261af-102">SYNOPSIS</span></span>
<span data-ttu-id="261af-103">Eltávolítja egy Azure Storage-fiók felügyeleti házirendját.</span><span class="sxs-lookup"><span data-stu-id="261af-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="261af-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="261af-104">SYNTAX</span></span>

### <span data-ttu-id="261af-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="261af-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261af-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="261af-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261af-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="261af-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261af-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="261af-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="261af-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="261af-109">DESCRIPTION</span></span>
<span data-ttu-id="261af-110">A **Remove-AzStorageAccountManagementPolicy** parancsmag eltávolítja egy Azure Storage-fiók felügyeleti házirendet.</span><span class="sxs-lookup"><span data-stu-id="261af-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="261af-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="261af-111">EXAMPLES</span></span>

### <span data-ttu-id="261af-112">1. példa: Tárfiók felügyeleti házirendének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="261af-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="261af-113">Ez a parancs eltávolítja a Tárfiók felügyeleti házirendet.</span><span class="sxs-lookup"><span data-stu-id="261af-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="261af-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="261af-114">PARAMETERS</span></span>

### <span data-ttu-id="261af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261af-115">-DefaultProfile</span></span>
<span data-ttu-id="261af-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="261af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="261af-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="261af-117">-InputObject</span></span>
<span data-ttu-id="261af-118">Eltávolítható felügyeleti objektum</span><span class="sxs-lookup"><span data-stu-id="261af-118">Management Object to Remove</span></span>

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

### <span data-ttu-id="261af-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="261af-119">-PassThru</span></span>
<span data-ttu-id="261af-120">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="261af-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="261af-121">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="261af-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="261af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="261af-122">-ResourceGroupName</span></span>
<span data-ttu-id="261af-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="261af-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="261af-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="261af-124">-StorageAccount</span></span>
<span data-ttu-id="261af-125">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="261af-125">Storage account object</span></span>

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

### <span data-ttu-id="261af-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="261af-126">-StorageAccountName</span></span>
<span data-ttu-id="261af-127">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="261af-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="261af-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="261af-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="261af-129">Tárfiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="261af-129">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="261af-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="261af-130">-Confirm</span></span>
<span data-ttu-id="261af-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="261af-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="261af-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="261af-132">-WhatIf</span></span>
<span data-ttu-id="261af-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="261af-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="261af-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="261af-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="261af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261af-135">CommonParameters</span></span>
<span data-ttu-id="261af-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="261af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261af-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="261af-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261af-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="261af-138">INPUTS</span></span>

### <span data-ttu-id="261af-139">System.String</span><span class="sxs-lookup"><span data-stu-id="261af-139">System.String</span></span>

## <span data-ttu-id="261af-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="261af-140">OUTPUTS</span></span>

### <span data-ttu-id="261af-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="261af-141">System.Boolean</span></span>

## <span data-ttu-id="261af-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="261af-142">NOTES</span></span>

## <span data-ttu-id="261af-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="261af-143">RELATED LINKS</span></span>
