---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194939"
---
# <span data-ttu-id="247d6-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="247d6-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="247d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="247d6-102">SYNOPSIS</span></span>
<span data-ttu-id="247d6-103">Egy runbook és egy ütemterv közötti társítás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="247d6-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="247d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="247d6-104">SYNTAX</span></span>

### <span data-ttu-id="247d6-105">ByJobScheduleId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="247d6-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="247d6-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="247d6-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="247d6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="247d6-107">DESCRIPTION</span></span>
<span data-ttu-id="247d6-108">A **unregister-AzAutomationScheduledRunbook** parancsmag eltávolítja az Azure automatizálási runbook és az ütemterv közötti társítást.</span><span class="sxs-lookup"><span data-stu-id="247d6-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="247d6-109">Az ütemezés már nem indítja el a runbook.</span><span class="sxs-lookup"><span data-stu-id="247d6-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="247d6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="247d6-110">EXAMPLES</span></span>

### <span data-ttu-id="247d6-111">1. példa: a runbook és az ütemterv közötti társítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="247d6-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="247d6-112">Ez a parancs eltávolítja a Runbk01 nevű runbook társítását és a Runbk01Sched nevű ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="247d6-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="247d6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="247d6-113">PARAMETERS</span></span>

### <span data-ttu-id="247d6-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="247d6-114">-AutomationAccountName</span></span>
<span data-ttu-id="247d6-115">A parancsmag működését biztosító runbook automatizálási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="247d6-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="247d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="247d6-116">-DefaultProfile</span></span>
<span data-ttu-id="247d6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="247d6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="247d6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="247d6-118">-Force</span></span>
<span data-ttu-id="247d6-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="247d6-119">ps_force</span></span>

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

### <span data-ttu-id="247d6-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="247d6-120">-JobScheduleId</span></span>
<span data-ttu-id="247d6-121">Az ütemezett runbook AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="247d6-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="247d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="247d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="247d6-123">Az ütemezett runbook tartozó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="247d6-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="247d6-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="247d6-124">-RunbookName</span></span>
<span data-ttu-id="247d6-125">Annak a runbook a nevét adja meg, amelynek a parancsmagja nem egy ütemtervből áll.</span><span class="sxs-lookup"><span data-stu-id="247d6-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="247d6-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="247d6-126">-ScheduleName</span></span>
<span data-ttu-id="247d6-127">Annak az ütemezésnek a neve, amelyből a parancsmag egy runbook.</span><span class="sxs-lookup"><span data-stu-id="247d6-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="247d6-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="247d6-128">-Confirm</span></span>
<span data-ttu-id="247d6-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="247d6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="247d6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="247d6-130">-WhatIf</span></span>
<span data-ttu-id="247d6-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="247d6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="247d6-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="247d6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="247d6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="247d6-133">CommonParameters</span></span>
<span data-ttu-id="247d6-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="247d6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="247d6-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="247d6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="247d6-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="247d6-136">INPUTS</span></span>

### <span data-ttu-id="247d6-137">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="247d6-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="247d6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="247d6-138">System.String</span></span>

## <span data-ttu-id="247d6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="247d6-139">OUTPUTS</span></span>

### <span data-ttu-id="247d6-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="247d6-140">System.Void</span></span>

## <span data-ttu-id="247d6-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="247d6-141">NOTES</span></span>

## <span data-ttu-id="247d6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="247d6-142">RELATED LINKS</span></span>

[<span data-ttu-id="247d6-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="247d6-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="247d6-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="247d6-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


