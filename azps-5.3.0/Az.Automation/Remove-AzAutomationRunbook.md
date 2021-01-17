---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478541"
---
# <span data-ttu-id="e8ae9-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e8ae9-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="e8ae9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ae9-103">Eltávolít egy runbookot.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-103">Removes a runbook.</span></span>

## <span data-ttu-id="e8ae9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e8ae9-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8ae9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e8ae9-105">DESCRIPTION</span></span>
<span data-ttu-id="e8ae9-106">A **Remove-AzAutomationRunbook** parancsmag eltávolítja a runbookot az Azure Automationből.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="e8ae9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e8ae9-107">EXAMPLES</span></span>

### <span data-ttu-id="e8ae9-108">1. példa: Runbook eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e8ae9-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e8ae9-109">Ez a parancs eltávolítja a Runbook03 nevű runbookot a Contoso17 nevű Azure Automation-fiókból.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e8ae9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8ae9-110">PARAMETERS</span></span>

### <span data-ttu-id="e8ae9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e8ae9-111">-AutomationAccountName</span></span>
<span data-ttu-id="e8ae9-112">Annak az automatizálási fióknak a nevét adja meg, amelyből ez a parancsmag eltávolít egy runbookot.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="e8ae9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ae9-113">-DefaultProfile</span></span>
<span data-ttu-id="e8ae9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e8ae9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8ae9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e8ae9-115">-Force</span></span>
<span data-ttu-id="e8ae9-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="e8ae9-116">ps_force</span></span>

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

### <span data-ttu-id="e8ae9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e8ae9-117">-Name</span></span>
<span data-ttu-id="e8ae9-118">Annak a runbooknak a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ae9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ae9-119">-ResourceGroupName</span></span>
<span data-ttu-id="e8ae9-120">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja közzétesz egy runbookot.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ae9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8ae9-121">-Confirm</span></span>
<span data-ttu-id="e8ae9-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ae9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ae9-123">-WhatIf</span></span>
<span data-ttu-id="e8ae9-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8ae9-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ae9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ae9-126">CommonParameters</span></span>
<span data-ttu-id="e8ae9-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ae9-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ae9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ae9-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8ae9-129">INPUTS</span></span>

### <span data-ttu-id="e8ae9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e8ae9-130">System.String</span></span>

## <span data-ttu-id="e8ae9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8ae9-131">OUTPUTS</span></span>

### <span data-ttu-id="e8ae9-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="e8ae9-132">System.Void</span></span>

## <span data-ttu-id="e8ae9-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e8ae9-133">NOTES</span></span>

## <span data-ttu-id="e8ae9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8ae9-134">RELATED LINKS</span></span>

[<span data-ttu-id="e8ae9-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e8ae9-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="e8ae9-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e8ae9-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="e8ae9-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e8ae9-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="e8ae9-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e8ae9-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e8ae9-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e8ae9-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e8ae9-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e8ae9-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="e8ae9-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e8ae9-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="e8ae9-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e8ae9-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


