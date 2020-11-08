---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 8080361b0dabd7d4114580777e6508fa4503fbbc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012667"
---
# <span data-ttu-id="d7489-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d7489-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="d7489-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7489-102">SYNOPSIS</span></span>
<span data-ttu-id="d7489-103">Automatizálási runbooks és kapcsolódó ütemezéseket kap.</span><span class="sxs-lookup"><span data-stu-id="d7489-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="d7489-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7489-104">SYNTAX</span></span>

### <span data-ttu-id="d7489-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7489-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7489-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="d7489-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7489-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="d7489-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7489-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="d7489-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7489-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="d7489-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7489-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7489-110">DESCRIPTION</span></span>
<span data-ttu-id="d7489-111">A **Get-AzAutomationScheduledRunbook** parancsmag egy vagy több Azure automatizálási runbooks és kapcsolódó ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="d7489-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="d7489-112">Ez a parancsmag alapértelmezés szerint az ütemezett runbooks kapja.</span><span class="sxs-lookup"><span data-stu-id="d7489-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="d7489-113">Adjon meg egy runbook vagy egy ütemtervet, vagy mindkettőt, ha konkrét runbook-ütemterveket szeretne látni.</span><span class="sxs-lookup"><span data-stu-id="d7489-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="d7489-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d7489-114">EXAMPLES</span></span>

### <span data-ttu-id="d7489-115">Példa 1: az ütemezett runbooks beszerzése</span><span class="sxs-lookup"><span data-stu-id="d7489-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d7489-116">Ez a parancs a Contoso17 nevű Azure automatizálási fiók minden ütemezett runbooks megkapja.</span><span class="sxs-lookup"><span data-stu-id="d7489-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="d7489-117">2. példa: a runbook társított összes ütemezés beolvasása</span><span class="sxs-lookup"><span data-stu-id="d7489-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="d7489-118">Ez a parancs a Contoso17 nevű Azure automatizálási fiók runbook Runbk01 minden ütemezett runbooks megkapja.</span><span class="sxs-lookup"><span data-stu-id="d7489-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="d7489-119">3. példa: az ütemtervhez társított összes runbooks beszerzése</span><span class="sxs-lookup"><span data-stu-id="d7489-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="d7489-120">Ez a parancs a Contoso17 nevű Azure automatizálási fiókban minden ütemezett runbooks bekerül a Schedule01.</span><span class="sxs-lookup"><span data-stu-id="d7489-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d7489-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7489-121">PARAMETERS</span></span>

### <span data-ttu-id="d7489-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d7489-122">-AutomationAccountName</span></span>
<span data-ttu-id="d7489-123">A parancsmag működését biztosító runbook automatizálási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7489-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d7489-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7489-124">-DefaultProfile</span></span>
<span data-ttu-id="d7489-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d7489-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7489-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="d7489-126">-JobScheduleId</span></span>
<span data-ttu-id="d7489-127">Annak az ütemezett feladatnak az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d7489-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d7489-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7489-128">-ResourceGroupName</span></span>
<span data-ttu-id="d7489-129">Annak az ütemezett runbooks a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="d7489-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d7489-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="d7489-130">-RunbookName</span></span>
<span data-ttu-id="d7489-131">Annak a runbook a nevét adja meg, amelyhez a parancsmag ütemezett runbooks kap.</span><span class="sxs-lookup"><span data-stu-id="d7489-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="d7489-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="d7489-132">-ScheduleName</span></span>
<span data-ttu-id="d7489-133">Annak az ütemezésnek a nevét adja meg, amelyre a parancsmag ütemezett runbooks kap.</span><span class="sxs-lookup"><span data-stu-id="d7489-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="d7489-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7489-134">CommonParameters</span></span>
<span data-ttu-id="d7489-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7489-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7489-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7489-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7489-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7489-137">INPUTS</span></span>

### <span data-ttu-id="d7489-138">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d7489-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d7489-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d7489-139">System.String</span></span>

## <span data-ttu-id="d7489-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7489-140">OUTPUTS</span></span>

### <span data-ttu-id="d7489-141">Microsoft. Azure. Command. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="d7489-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="d7489-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7489-142">NOTES</span></span>

## <span data-ttu-id="d7489-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7489-143">RELATED LINKS</span></span>

[<span data-ttu-id="d7489-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d7489-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="d7489-145">Regisztráció törlése – AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d7489-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


