---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: da687cc3831f4a3cb278dbf032905b39750b8c8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004758"
---
# <span data-ttu-id="b5855-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b5855-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="b5855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5855-102">SYNOPSIS</span></span>
<span data-ttu-id="b5855-103">Törli az automatizálási ütemezést.</span><span class="sxs-lookup"><span data-stu-id="b5855-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="b5855-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5855-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5855-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5855-105">DESCRIPTION</span></span>
<span data-ttu-id="b5855-106">A **Remove-AzAutomationSchedule** parancsmag törli az ütemezést az Azure Automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="b5855-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="b5855-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5855-107">EXAMPLES</span></span>

### <span data-ttu-id="b5855-108">1. példa: Ütemezés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b5855-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b5855-109">Ez a parancs törli az Erőforráscsoport01 erőforráscsoport Contoso17 automatizálási fiókjában az Schedule01 nevű ütemezést.</span><span class="sxs-lookup"><span data-stu-id="b5855-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="b5855-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5855-110">PARAMETERS</span></span>

### <span data-ttu-id="b5855-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b5855-111">-AutomationAccountName</span></span>
<span data-ttu-id="b5855-112">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja eltávolít egy ütemezést.</span><span class="sxs-lookup"><span data-stu-id="b5855-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="b5855-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5855-113">-DefaultProfile</span></span>
<span data-ttu-id="b5855-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b5855-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5855-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b5855-115">-Force</span></span>
<span data-ttu-id="b5855-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="b5855-116">ps_force</span></span>

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

### <span data-ttu-id="b5855-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b5855-117">-Name</span></span>
<span data-ttu-id="b5855-118">Annak az ütemezésnek a nevét adja meg, amelyből a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b5855-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b5855-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5855-119">-ResourceGroupName</span></span>
<span data-ttu-id="b5855-120">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja eltávolítja az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="b5855-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="b5855-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5855-121">-Confirm</span></span>
<span data-ttu-id="b5855-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b5855-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5855-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5855-123">-WhatIf</span></span>
<span data-ttu-id="b5855-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b5855-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5855-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5855-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5855-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5855-126">CommonParameters</span></span>
<span data-ttu-id="b5855-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5855-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5855-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5855-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5855-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5855-129">INPUTS</span></span>

### <span data-ttu-id="b5855-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b5855-130">System.String</span></span>

## <span data-ttu-id="b5855-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5855-131">OUTPUTS</span></span>

### <span data-ttu-id="b5855-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="b5855-132">System.Void</span></span>

## <span data-ttu-id="b5855-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5855-133">NOTES</span></span>

## <span data-ttu-id="b5855-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5855-134">RELATED LINKS</span></span>

[<span data-ttu-id="b5855-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b5855-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="b5855-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b5855-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="b5855-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b5855-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


