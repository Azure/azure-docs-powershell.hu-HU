---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373182"
---
# <span data-ttu-id="df076-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="df076-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="df076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df076-102">SYNOPSIS</span></span>
<span data-ttu-id="df076-103">Eltávolít egy Automatizálási változót.</span><span class="sxs-lookup"><span data-stu-id="df076-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="df076-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df076-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df076-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df076-105">DESCRIPTION</span></span>
<span data-ttu-id="df076-106">Az **Remove-AzAutomationVariable** parancsmag eltávolít egy változót az Azure Automationből.</span><span class="sxs-lookup"><span data-stu-id="df076-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="df076-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df076-107">EXAMPLES</span></span>

### <span data-ttu-id="df076-108">1. példa: Változó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="df076-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="df076-109">Ez a parancs eltávolít egy StringVariable22 nevű változót a Contoso17 nevű automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="df076-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="df076-110">Ez a parancs a *Force paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="df076-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="df076-111">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df076-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="df076-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df076-112">PARAMETERS</span></span>

### <span data-ttu-id="df076-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df076-113">-AutomationAccountName</span></span>
<span data-ttu-id="df076-114">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által törölt változót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="df076-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="df076-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df076-115">-DefaultProfile</span></span>
<span data-ttu-id="df076-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="df076-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df076-117">-Name</span><span class="sxs-lookup"><span data-stu-id="df076-117">-Name</span></span>
<span data-ttu-id="df076-118">Annak a változónak a nevét adja meg, amelyből a parancsmag töröl.</span><span class="sxs-lookup"><span data-stu-id="df076-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="df076-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df076-119">-ResourceGroupName</span></span>
<span data-ttu-id="df076-120">Azt az erőforráscsoportot adja meg, amelyből a parancsmag töröl egy változót.</span><span class="sxs-lookup"><span data-stu-id="df076-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="df076-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df076-121">-Confirm</span></span>
<span data-ttu-id="df076-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="df076-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df076-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df076-123">-WhatIf</span></span>
<span data-ttu-id="df076-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="df076-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df076-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df076-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df076-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df076-126">CommonParameters</span></span>
<span data-ttu-id="df076-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df076-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df076-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df076-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df076-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df076-129">INPUTS</span></span>

### <span data-ttu-id="df076-130">System.String</span><span class="sxs-lookup"><span data-stu-id="df076-130">System.String</span></span>

## <span data-ttu-id="df076-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df076-131">OUTPUTS</span></span>

### <span data-ttu-id="df076-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="df076-132">System.Void</span></span>

## <span data-ttu-id="df076-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df076-133">NOTES</span></span>

## <span data-ttu-id="df076-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df076-134">RELATED LINKS</span></span>

[<span data-ttu-id="df076-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="df076-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="df076-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="df076-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="df076-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="df076-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


