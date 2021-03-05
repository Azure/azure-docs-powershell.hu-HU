---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: 46dee36dccc4a6e73620732df18059f64ccb6587
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004742"
---
# <span data-ttu-id="4e0f4-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4e0f4-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="4e0f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e0f4-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0f4-103">Eltávolít egy Automatizálási változót.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="4e0f4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4e0f4-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e0f4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4e0f4-105">DESCRIPTION</span></span>
<span data-ttu-id="4e0f4-106">Az **Remove-AzAutomationVariable** parancsmag eltávolít egy változót az Azure Automationből.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="4e0f4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4e0f4-107">EXAMPLES</span></span>

### <span data-ttu-id="4e0f4-108">1. példa: Változó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4e0f4-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4e0f4-109">Ez a parancs eltávolít egy StringVariable22 nevű változót a Contoso17 nevű automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="4e0f4-110">Ez a parancs a *Force paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4e0f4-111">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4e0f4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e0f4-112">PARAMETERS</span></span>

### <span data-ttu-id="4e0f4-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4e0f4-113">-AutomationAccountName</span></span>
<span data-ttu-id="4e0f4-114">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által törölt változót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="4e0f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0f4-115">-DefaultProfile</span></span>
<span data-ttu-id="4e0f4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4e0f4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e0f4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4e0f4-117">-Name</span></span>
<span data-ttu-id="4e0f4-118">Annak a változónak a nevét adja meg, amelyből a parancsmag töröl.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0f4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e0f4-119">-ResourceGroupName</span></span>
<span data-ttu-id="4e0f4-120">Azt az erőforráscsoportot adja meg, amelyből a parancsmag töröl egy változót.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="4e0f4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e0f4-121">-Confirm</span></span>
<span data-ttu-id="4e0f4-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e0f4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e0f4-123">-WhatIf</span></span>
<span data-ttu-id="4e0f4-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e0f4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e0f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0f4-126">CommonParameters</span></span>
<span data-ttu-id="4e0f4-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e0f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0f4-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e0f4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0f4-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e0f4-129">INPUTS</span></span>

### <span data-ttu-id="4e0f4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4e0f4-130">System.String</span></span>

## <span data-ttu-id="4e0f4-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e0f4-131">OUTPUTS</span></span>

### <span data-ttu-id="4e0f4-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="4e0f4-132">System.Void</span></span>

## <span data-ttu-id="4e0f4-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4e0f4-133">NOTES</span></span>

## <span data-ttu-id="4e0f4-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e0f4-134">RELATED LINKS</span></span>

[<span data-ttu-id="4e0f4-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4e0f4-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="4e0f4-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4e0f4-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="4e0f4-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4e0f4-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


