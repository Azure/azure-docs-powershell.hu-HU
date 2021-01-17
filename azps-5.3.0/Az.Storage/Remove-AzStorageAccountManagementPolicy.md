---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6f4907f9ee94c05161fa602fc5cefd0ead4f6224
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466922"
---
# <span data-ttu-id="01676-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="01676-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="01676-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01676-102">SYNOPSIS</span></span>
<span data-ttu-id="01676-103">Eltávolítja egy Azure Storage-fiók felügyeleti házirendját.</span><span class="sxs-lookup"><span data-stu-id="01676-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="01676-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01676-104">SYNTAX</span></span>

### <span data-ttu-id="01676-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01676-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01676-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="01676-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01676-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="01676-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01676-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="01676-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01676-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01676-109">DESCRIPTION</span></span>
<span data-ttu-id="01676-110">A **Remove-AzStorageAccountManagementPolicy** parancsmag eltávolítja egy Azure Storage-fiók felügyeleti házirendet.</span><span class="sxs-lookup"><span data-stu-id="01676-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="01676-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01676-111">EXAMPLES</span></span>

### <span data-ttu-id="01676-112">1. példa: Tárfiók felügyeleti házirendének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="01676-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="01676-113">Ez a parancs eltávolítja a Tárfiók felügyeleti házirendet.</span><span class="sxs-lookup"><span data-stu-id="01676-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="01676-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01676-114">PARAMETERS</span></span>

### <span data-ttu-id="01676-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01676-115">-DefaultProfile</span></span>
<span data-ttu-id="01676-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01676-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01676-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01676-117">-InputObject</span></span>
<span data-ttu-id="01676-118">Eltávolítható felügyeleti objektum</span><span class="sxs-lookup"><span data-stu-id="01676-118">Management Object to Remove</span></span>

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

### <span data-ttu-id="01676-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01676-119">-PassThru</span></span>
<span data-ttu-id="01676-120">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="01676-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="01676-121">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="01676-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="01676-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01676-122">-ResourceGroupName</span></span>
<span data-ttu-id="01676-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="01676-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="01676-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="01676-124">-StorageAccount</span></span>
<span data-ttu-id="01676-125">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="01676-125">Storage account object</span></span>

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

### <span data-ttu-id="01676-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="01676-126">-StorageAccountName</span></span>
<span data-ttu-id="01676-127">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="01676-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="01676-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="01676-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="01676-129">Tárfiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="01676-129">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="01676-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01676-130">-Confirm</span></span>
<span data-ttu-id="01676-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="01676-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01676-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01676-132">-WhatIf</span></span>
<span data-ttu-id="01676-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="01676-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01676-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01676-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01676-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01676-135">CommonParameters</span></span>
<span data-ttu-id="01676-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01676-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01676-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01676-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01676-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01676-138">INPUTS</span></span>

### <span data-ttu-id="01676-139">System.String</span><span class="sxs-lookup"><span data-stu-id="01676-139">System.String</span></span>

## <span data-ttu-id="01676-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01676-140">OUTPUTS</span></span>

### <span data-ttu-id="01676-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01676-141">System.Boolean</span></span>

## <span data-ttu-id="01676-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01676-142">NOTES</span></span>

## <span data-ttu-id="01676-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01676-143">RELATED LINKS</span></span>
