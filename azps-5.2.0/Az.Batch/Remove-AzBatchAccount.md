---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361268"
---
# <span data-ttu-id="11229-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="11229-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="11229-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11229-102">SYNOPSIS</span></span>
<span data-ttu-id="11229-103">Eltávolít egy Batch-fiókot.</span><span class="sxs-lookup"><span data-stu-id="11229-103">Removes a Batch account.</span></span>

## <span data-ttu-id="11229-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11229-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11229-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11229-105">DESCRIPTION</span></span>
<span data-ttu-id="11229-106">A **Remove-AzBatchAccount** parancsmag eltávolít egy Azure Batch-fiókot.</span><span class="sxs-lookup"><span data-stu-id="11229-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="11229-107">Ez a parancsmag a fiók eltávolítása előtt megkérdezi, hacsak meg nem adja a *Force paramétert.*</span><span class="sxs-lookup"><span data-stu-id="11229-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="11229-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11229-108">EXAMPLES</span></span>

### <span data-ttu-id="11229-109">1. példa: Batch-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="11229-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="11229-110">Ez a parancs eltávolítja a pfuller nevű Batch-fiókot.</span><span class="sxs-lookup"><span data-stu-id="11229-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="11229-111">Ez a parancs megerősítést kér a fiók törlése előtt.</span><span class="sxs-lookup"><span data-stu-id="11229-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="11229-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11229-112">PARAMETERS</span></span>

### <span data-ttu-id="11229-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="11229-113">-AccountName</span></span>
<span data-ttu-id="11229-114">Annak a Batch-fióknak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="11229-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11229-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11229-115">-DefaultProfile</span></span>
<span data-ttu-id="11229-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11229-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11229-117">-Force</span><span class="sxs-lookup"><span data-stu-id="11229-117">-Force</span></span>
<span data-ttu-id="11229-118">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="11229-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="11229-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11229-119">-ResourceGroupName</span></span>
<span data-ttu-id="11229-120">Annak a fióknak az erőforráscsoportját adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="11229-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11229-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11229-121">-Confirm</span></span>
<span data-ttu-id="11229-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="11229-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11229-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11229-123">-WhatIf</span></span>
<span data-ttu-id="11229-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="11229-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11229-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11229-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11229-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11229-126">CommonParameters</span></span>
<span data-ttu-id="11229-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11229-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11229-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11229-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11229-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11229-129">INPUTS</span></span>

### <span data-ttu-id="11229-130">System.String</span><span class="sxs-lookup"><span data-stu-id="11229-130">System.String</span></span>

## <span data-ttu-id="11229-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11229-131">OUTPUTS</span></span>

### <span data-ttu-id="11229-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="11229-132">System.Void</span></span>

## <span data-ttu-id="11229-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11229-133">NOTES</span></span>

## <span data-ttu-id="11229-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11229-134">RELATED LINKS</span></span>

[<span data-ttu-id="11229-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="11229-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="11229-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="11229-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="11229-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="11229-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="11229-138">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="11229-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
