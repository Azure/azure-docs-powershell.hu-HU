---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478466"
---
# <span data-ttu-id="d8cfb-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d8cfb-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="d8cfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cfb-103">Eltávolít egy társítást egy runbook és egy ütemterv között.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="d8cfb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8cfb-104">SYNTAX</span></span>

### <span data-ttu-id="d8cfb-105">ByScheduleId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8cfb-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8cfb-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="d8cfb-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8cfb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8cfb-107">DESCRIPTION</span></span>
<span data-ttu-id="d8cfb-108">A **Unregister-AzAutomationScheduledRunbook parancsmag** eltávolítja az Azure Automation-runbook és az ütemezés közötti kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="d8cfb-109">Az ütemezés a továbbiakban nem kezdi el a runbookot.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="d8cfb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8cfb-110">EXAMPLES</span></span>

### <span data-ttu-id="d8cfb-111">1. példa: A runbook és az ütemezés társításának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d8cfb-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="d8cfb-112">Ez a parancs eltávolítja a Társítás a Runbk01 nevű runbook és a Runbk01Sched nevű ütemezés között.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="d8cfb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8cfb-113">PARAMETERS</span></span>

### <span data-ttu-id="d8cfb-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8cfb-114">-AutomationAccountName</span></span>
<span data-ttu-id="d8cfb-115">Annak a runbooknak az automatizálási fiókja, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d8cfb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cfb-116">-DefaultProfile</span></span>
<span data-ttu-id="d8cfb-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d8cfb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8cfb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d8cfb-118">-Force</span></span>
<span data-ttu-id="d8cfb-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="d8cfb-119">ps_force</span></span>

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

### <span data-ttu-id="d8cfb-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="d8cfb-120">-JobScheduleId</span></span>
<span data-ttu-id="d8cfb-121">Egy ütemezett runbook azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8cfb-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8cfb-123">Az ütemezett runbook erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="d8cfb-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="d8cfb-124">-RunbookName</span></span>
<span data-ttu-id="d8cfb-125">Annak a runbooknak a nevét adja meg, amelyből a parancsmag társítja az ütemezést.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfb-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="d8cfb-126">-ScheduleName</span></span>
<span data-ttu-id="d8cfb-127">Annak az ütemezésnek a nevét adja meg, amelyből a parancsmag társítja a runbookot.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8cfb-128">-Confirm</span></span>
<span data-ttu-id="d8cfb-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8cfb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8cfb-130">-WhatIf</span></span>
<span data-ttu-id="d8cfb-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8cfb-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8cfb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cfb-133">CommonParameters</span></span>
<span data-ttu-id="d8cfb-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8cfb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cfb-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8cfb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cfb-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8cfb-136">INPUTS</span></span>

### <span data-ttu-id="d8cfb-137">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d8cfb-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d8cfb-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d8cfb-138">System.String</span></span>

## <span data-ttu-id="d8cfb-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8cfb-139">OUTPUTS</span></span>

### <span data-ttu-id="d8cfb-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="d8cfb-140">System.Void</span></span>

## <span data-ttu-id="d8cfb-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8cfb-141">NOTES</span></span>

## <span data-ttu-id="d8cfb-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8cfb-142">RELATED LINKS</span></span>

[<span data-ttu-id="d8cfb-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d8cfb-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="d8cfb-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d8cfb-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


