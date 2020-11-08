---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016357"
---
# <span data-ttu-id="1349a-101">Get-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="1349a-101">Get-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="1349a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1349a-102">SYNOPSIS</span></span>

<span data-ttu-id="1349a-103">Az Azure automatizálási runbooks és a hozzájuk kapcsolódó ütemterveket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1349a-103">Gets Azure Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="1349a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1349a-104">SYNTAX</span></span>

### <span data-ttu-id="1349a-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1349a-105">ByAll (Default)</span></span>
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="1349a-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="1349a-106">ByJobScheduleId</span></span>
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1349a-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="1349a-107">ByRunbookName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1349a-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="1349a-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1349a-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="1349a-109">ByScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1349a-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="1349a-110">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1349a-111">A **Get-AzureAutomationScheduledRunbook** egy vagy több Azure automatizálási runbooks és kapcsolódó ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="1349a-111">The **Get-AzureAutomationScheduledRunbook** gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="1349a-112">Alapértelmezés szerint minden ütemezett runbooks visszaadott.</span><span class="sxs-lookup"><span data-stu-id="1349a-112">By default, all scheduled runbooks are returned.</span></span>

<span data-ttu-id="1349a-113">Ha meghatározott ütemezett runbook szeretne kapni, adja meg a runbook nevét és az ütemezés nevét.</span><span class="sxs-lookup"><span data-stu-id="1349a-113">To get a specific scheduled runbook, specify the runbook name and the schedule name.</span></span>
<span data-ttu-id="1349a-114">Ha a runbook társított összes ütemezést meg szeretné kapni, akkor csak a runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1349a-114">To get all schedules associated with a runbook, specify just the runbook name.</span></span>
<span data-ttu-id="1349a-115">Ha az ütemtervhez társított összes runbooks meg szeretné kapni, akkor csak az ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1349a-115">To get all runbooks associated with a schedule, specify just the schedule name.</span></span>

## <span data-ttu-id="1349a-116">Példák</span><span class="sxs-lookup"><span data-stu-id="1349a-116">EXAMPLES</span></span>

### <span data-ttu-id="1349a-117">Példa 1: az ütemezett runbooks beszerzése</span><span class="sxs-lookup"><span data-stu-id="1349a-117">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="1349a-118">Ez a parancs a Contoso17 nevű automatizálási fiók minden ütemezett runbooks megkapja.</span><span class="sxs-lookup"><span data-stu-id="1349a-118">This command gets all scheduled runbooks in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1349a-119">2. példa: a runbook társított összes ütemezés beolvasása</span><span class="sxs-lookup"><span data-stu-id="1349a-119">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

<span data-ttu-id="1349a-120">Ez a parancs a Contoso17 nevű automatizálási fiókban minden ütemezett runbooks bekerül az runbook Runbk01.</span><span class="sxs-lookup"><span data-stu-id="1349a-120">This command gets all scheduled runbooks for the runbook Runbk01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1349a-121">3. példa: az ütemtervhez társított összes runbooks beszerzése</span><span class="sxs-lookup"><span data-stu-id="1349a-121">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

<span data-ttu-id="1349a-122">Ez a parancs a Contoso17 nevű automatizálási fiók ütemezési Schedule01 minden ütemezett runbooks megkapja.</span><span class="sxs-lookup"><span data-stu-id="1349a-122">This command gets all scheduled runbooks for the schedule Schedule01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1349a-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1349a-123">PARAMETERS</span></span>

### <span data-ttu-id="1349a-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1349a-124">-AutomationAccountName</span></span>
<span data-ttu-id="1349a-125">Az Azure automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1349a-125">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1349a-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="1349a-126">-JobScheduleId</span></span>
<span data-ttu-id="1349a-127">Az ütemezett feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1349a-127">Specifies the ID of a scheduled job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1349a-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="1349a-128">-Profile</span></span>
<span data-ttu-id="1349a-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1349a-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1349a-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1349a-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1349a-131">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="1349a-131">-RunbookName</span></span>
<span data-ttu-id="1349a-132">Egy runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1349a-132">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1349a-133">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="1349a-133">-ScheduleName</span></span>
<span data-ttu-id="1349a-134">Az ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1349a-134">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1349a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1349a-135">CommonParameters</span></span>
<span data-ttu-id="1349a-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1349a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1349a-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1349a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1349a-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1349a-138">INPUTS</span></span>

## <span data-ttu-id="1349a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1349a-139">OUTPUTS</span></span>

### <span data-ttu-id="1349a-140">Microsoft. Azure. Command. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="1349a-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="1349a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1349a-141">NOTES</span></span>

## <span data-ttu-id="1349a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1349a-142">RELATED LINKS</span></span>

[<span data-ttu-id="1349a-143">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="1349a-143">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)

[<span data-ttu-id="1349a-144">Regisztráció törlése – AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="1349a-144">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


