---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: fe8d7b4407aa5afc3454d80e4cf45c102d9006bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505675"
---
# <span data-ttu-id="4159b-101">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4159b-101">Get-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="4159b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4159b-102">SYNOPSIS</span></span>
<span data-ttu-id="4159b-103">Automatizálási runbooks és kapcsolódó ütemezéseket kap.</span><span class="sxs-lookup"><span data-stu-id="4159b-103">Gets Automation runbooks and associated schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4159b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4159b-104">SYNTAX</span></span>

### <span data-ttu-id="4159b-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4159b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4159b-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="4159b-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4159b-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="4159b-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4159b-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="4159b-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4159b-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="4159b-109">ByScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4159b-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="4159b-110">DESCRIPTION</span></span>
<span data-ttu-id="4159b-111">A **Get-AzureRmAutomationScheduledRunbook** parancsmag egy vagy több Azure automatizálási runbooks és kapcsolódó ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="4159b-111">The **Get-AzureRmAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="4159b-112">Ez a parancsmag alapértelmezés szerint az ütemezett runbooks kapja.</span><span class="sxs-lookup"><span data-stu-id="4159b-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="4159b-113">Adjon meg egy runbook vagy egy ütemtervet, vagy mindkettőt, ha konkrét runbook-ütemterveket szeretne látni.</span><span class="sxs-lookup"><span data-stu-id="4159b-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="4159b-114">Példák</span><span class="sxs-lookup"><span data-stu-id="4159b-114">EXAMPLES</span></span>

### <span data-ttu-id="4159b-115">Példa 1: az ütemezett runbooks beszerzése</span><span class="sxs-lookup"><span data-stu-id="4159b-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4159b-116">Ez a parancs a Contoso17 nevű Azure automatizálási fiók minden ütemezett runbooks megkapja.</span><span class="sxs-lookup"><span data-stu-id="4159b-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="4159b-117">2. példa: a runbook társított összes ütemezés beolvasása</span><span class="sxs-lookup"><span data-stu-id="4159b-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="4159b-118">Ez a parancs a Contoso17 nevű Azure automatizálási fiók runbook Runbk01 minden ütemezett runbooks megkapja.</span><span class="sxs-lookup"><span data-stu-id="4159b-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="4159b-119">3. példa: az ütemtervhez társított összes runbooks beszerzése</span><span class="sxs-lookup"><span data-stu-id="4159b-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="4159b-120">Ez a parancs a Contoso17 nevű Azure automatizálási fiókban minden ütemezett runbooks bekerül a Schedule01.</span><span class="sxs-lookup"><span data-stu-id="4159b-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="4159b-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4159b-121">PARAMETERS</span></span>

### <span data-ttu-id="4159b-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4159b-122">-AutomationAccountName</span></span>
<span data-ttu-id="4159b-123">A parancsmag működését biztosító runbook automatizálási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4159b-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4159b-124">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="4159b-124">-JobScheduleId</span></span>
<span data-ttu-id="4159b-125">Annak az ütemezett feladatnak az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="4159b-125">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4159b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4159b-126">-ResourceGroupName</span></span>
<span data-ttu-id="4159b-127">Annak az ütemezett runbooks a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="4159b-127">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4159b-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="4159b-128">-RunbookName</span></span>
<span data-ttu-id="4159b-129">Annak a runbook a nevét adja meg, amelyhez a parancsmag ütemezett runbooks kap.</span><span class="sxs-lookup"><span data-stu-id="4159b-129">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="4159b-130">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="4159b-130">-ScheduleName</span></span>
<span data-ttu-id="4159b-131">Annak az ütemezésnek a nevét adja meg, amelyre a parancsmag ütemezett runbooks kap.</span><span class="sxs-lookup"><span data-stu-id="4159b-131">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="4159b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4159b-132">-DefaultProfile</span></span>
<span data-ttu-id="4159b-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4159b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4159b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4159b-134">CommonParameters</span></span>
<span data-ttu-id="4159b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4159b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4159b-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4159b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4159b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4159b-137">INPUTS</span></span>

## <span data-ttu-id="4159b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4159b-138">OUTPUTS</span></span>

### <span data-ttu-id="4159b-139">Microsoft. Azure. Command. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="4159b-139">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="4159b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4159b-140">NOTES</span></span>

## <span data-ttu-id="4159b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4159b-141">RELATED LINKS</span></span>

[<span data-ttu-id="4159b-142">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4159b-142">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="4159b-143">Regisztráció törlése – AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4159b-143">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


