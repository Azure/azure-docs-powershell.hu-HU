---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 6dfe33146ba2e35c728211f7f4b17fcfccf40ad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014198"
---
# <span data-ttu-id="480f5-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="480f5-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="480f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="480f5-102">SYNOPSIS</span></span>
<span data-ttu-id="480f5-103">Az automatizálási runbookok és a hozzájuk tartozó ütemezések lekérte.</span><span class="sxs-lookup"><span data-stu-id="480f5-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="480f5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="480f5-104">SYNTAX</span></span>

### <span data-ttu-id="480f5-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="480f5-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="480f5-106">ByScheduleId</span><span class="sxs-lookup"><span data-stu-id="480f5-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="480f5-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="480f5-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="480f5-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="480f5-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="480f5-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="480f5-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="480f5-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="480f5-110">DESCRIPTION</span></span>
<span data-ttu-id="480f5-111">A **Get-AzAutomationScheduledRunbook parancsmag** egy vagy több Azure Automation-runbookot és kapcsolódó ütemezést kap.</span><span class="sxs-lookup"><span data-stu-id="480f5-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="480f5-112">Alapértelmezés szerint ez a parancsmag az összes ütemezett runbookot megkapja.</span><span class="sxs-lookup"><span data-stu-id="480f5-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="480f5-113">Adja meg a runbook nevét vagy egy ütemezést, vagy mindkettőt a konkrét runbook-ütemezések nevére.</span><span class="sxs-lookup"><span data-stu-id="480f5-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="480f5-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="480f5-114">EXAMPLES</span></span>

### <span data-ttu-id="480f5-115">1. példa: Az összes ütemezett runbook lekérte</span><span class="sxs-lookup"><span data-stu-id="480f5-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="480f5-116">Ez a parancs a Contoso17 nevű Azure Automation-fiók összes ütemezett runbookját megkapja.</span><span class="sxs-lookup"><span data-stu-id="480f5-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="480f5-117">2. példa: A runbookhoz társított összes ütemezés lekérte</span><span class="sxs-lookup"><span data-stu-id="480f5-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="480f5-118">Ez a parancs a Contoso17 nevű Azure Automation-fiók runbook Runbk01 nevű runbookjára vonatkozó összes ütemezett runbookot megkapja.</span><span class="sxs-lookup"><span data-stu-id="480f5-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="480f5-119">3. példa: Az ütemezéshez társított összes runbook lekérte</span><span class="sxs-lookup"><span data-stu-id="480f5-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="480f5-120">Ez a parancs a Contoso17 nevű Azure Automation-fiók Schedule01 ütemezésének összes ütemezett runbookját megkapja.</span><span class="sxs-lookup"><span data-stu-id="480f5-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="480f5-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="480f5-121">PARAMETERS</span></span>

### <span data-ttu-id="480f5-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="480f5-122">-AutomationAccountName</span></span>
<span data-ttu-id="480f5-123">Annak a runbooknak az automatizálási fiókja, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="480f5-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="480f5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480f5-124">-DefaultProfile</span></span>
<span data-ttu-id="480f5-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="480f5-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="480f5-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="480f5-126">-JobScheduleId</span></span>
<span data-ttu-id="480f5-127">A parancsmag által lekért ütemezett feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="480f5-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="480f5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="480f5-128">-ResourceGroupName</span></span>
<span data-ttu-id="480f5-129">A parancsmag által lekért ütemezett runbookok erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="480f5-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="480f5-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="480f5-130">-RunbookName</span></span>
<span data-ttu-id="480f5-131">Annak a runbooknak a nevét adja meg, amelyhez ez a parancsmag ütemezett runbookokat kap.</span><span class="sxs-lookup"><span data-stu-id="480f5-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="480f5-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="480f5-132">-ScheduleName</span></span>
<span data-ttu-id="480f5-133">Annak az ütemezésnek a nevét adja meg, amelyhez ez a parancsmag ütemezett runbookokat kap.</span><span class="sxs-lookup"><span data-stu-id="480f5-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="480f5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480f5-134">CommonParameters</span></span>
<span data-ttu-id="480f5-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="480f5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480f5-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="480f5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480f5-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="480f5-137">INPUTS</span></span>

### <span data-ttu-id="480f5-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="480f5-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="480f5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="480f5-139">System.String</span></span>

## <span data-ttu-id="480f5-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="480f5-140">OUTPUTS</span></span>

### <span data-ttu-id="480f5-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span><span class="sxs-lookup"><span data-stu-id="480f5-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="480f5-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="480f5-142">NOTES</span></span>

## <span data-ttu-id="480f5-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="480f5-143">RELATED LINKS</span></span>

[<span data-ttu-id="480f5-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="480f5-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="480f5-145">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="480f5-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


