---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348413"
---
# <span data-ttu-id="5c1bd-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c1bd-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="5c1bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1bd-103">Eltávolít egy tárolt hozzáférési házirendet egy Azure-tárolótáblából.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="5c1bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5c1bd-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c1bd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5c1bd-105">DESCRIPTION</span></span>
<span data-ttu-id="5c1bd-106">A **Remove-AzStorageTableStoredAccessPolicy** parancsmag eltávolít egy tárolt hozzáférési házirendet egy Azure-tárolótáblából.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="5c1bd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5c1bd-107">EXAMPLES</span></span>

### <span data-ttu-id="5c1bd-108">1. példa: Tárolt hozzáférési házirend eltávolítása egy tárolótáblából</span><span class="sxs-lookup"><span data-stu-id="5c1bd-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="5c1bd-109">Ez a parancs eltávolítja a Policy05 nevű házirendet a MyTable nevű tárolótáblából.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="5c1bd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c1bd-110">PARAMETERS</span></span>

### <span data-ttu-id="5c1bd-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5c1bd-111">-Context</span></span>
<span data-ttu-id="5c1bd-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5c1bd-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1bd-114">-DefaultProfile</span></span>
<span data-ttu-id="5c1bd-115">kommunikáció az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-115">communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1bd-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c1bd-116">-PassThru</span></span>
<span data-ttu-id="5c1bd-117">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="5c1bd-118">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5c1bd-119">-Házirend</span><span class="sxs-lookup"><span data-stu-id="5c1bd-119">-Policy</span></span>
<span data-ttu-id="5c1bd-120">A parancsmag által eltávolított tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1bd-121">-Table</span><span class="sxs-lookup"><span data-stu-id="5c1bd-121">-Table</span></span>
<span data-ttu-id="5c1bd-122">Az Azure-tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-122">Specifies the Azure table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1bd-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c1bd-123">-Confirm</span></span>
<span data-ttu-id="5c1bd-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1bd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c1bd-125">-WhatIf</span></span>
<span data-ttu-id="5c1bd-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c1bd-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1bd-128">CommonParameters</span></span>
<span data-ttu-id="5c1bd-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c1bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1bd-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1bd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1bd-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c1bd-131">INPUTS</span></span>

### <span data-ttu-id="5c1bd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5c1bd-132">System.String</span></span>

### <span data-ttu-id="5c1bd-133">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c1bd-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5c1bd-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c1bd-134">OUTPUTS</span></span>

### <span data-ttu-id="5c1bd-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5c1bd-135">System.Boolean</span></span>

## <span data-ttu-id="5c1bd-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5c1bd-136">NOTES</span></span>

## <span data-ttu-id="5c1bd-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c1bd-137">RELATED LINKS</span></span>

[<span data-ttu-id="5c1bd-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c1bd-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5c1bd-139">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="5c1bd-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="5c1bd-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c1bd-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5c1bd-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c1bd-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
