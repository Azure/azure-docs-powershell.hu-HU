---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6527FF45-9C16-47E8-8E70-619A0581D2F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: c595779fa8c6b4c246f102a346290e931dc89379
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016369"
---
# <span data-ttu-id="9b519-101">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9b519-101">Get-AzureAutomationJob</span></span>

## <span data-ttu-id="9b519-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b519-102">SYNOPSIS</span></span>

<span data-ttu-id="9b519-103">Egy vagy több Azure automatizálási runbook-feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="9b519-103">Gets one or more Azure Automation runbook jobs.</span></span>

## <span data-ttu-id="9b519-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b519-104">SYNTAX</span></span>

### <span data-ttu-id="9b519-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b519-105">ByAll (Default)</span></span>
```
Get-AzureAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9b519-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="9b519-106">ByJobId</span></span>
```
Get-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b519-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="9b519-107">ByRunbookName</span></span>
```
Get-AzureAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9b519-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b519-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9b519-109">A **Get-AzureAutomationJob** parancsmag egy vagy több runbook-feladatot kap a Microsoft Azure automatizálási szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="9b519-109">The **Get-AzureAutomationJob** cmdlet gets one or more runbook jobs in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="9b519-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9b519-110">EXAMPLES</span></span>

### <span data-ttu-id="9b519-111">Példa 1: konkrét runbook-feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="9b519-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="9b519-112">Ez a parancs a megadott GUID azonosítóval rendelkező feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="9b519-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="9b519-113">2. példa: a runbook minden feladatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="9b519-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -RunbookName "MyRunbook"
```

<span data-ttu-id="9b519-114">Ez a parancs a MyRunbook nevű runbook társított összes feladatot megkapja.</span><span class="sxs-lookup"><span data-stu-id="9b519-114">This command gets all jobs associated with a runbook named MyRunbook.</span></span>

### <span data-ttu-id="9b519-115">2. példa: az összes futó feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="9b519-115">Example 2: Get all running jobs</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Status "Running"
```

<span data-ttu-id="9b519-116">Ez a parancs a Contoso17 nevű automatizálási fiókban minden futó feladatot megkapja.</span><span class="sxs-lookup"><span data-stu-id="9b519-116">This command gets all running jobs in the automation account with the name Contoso17.</span></span>

## <span data-ttu-id="9b519-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b519-117">PARAMETERS</span></span>

### <span data-ttu-id="9b519-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9b519-118">-AutomationAccountName</span></span>
<span data-ttu-id="9b519-119">Az Azure automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b519-119">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="9b519-120">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="9b519-120">-EndTime</span></span>
<span data-ttu-id="9b519-121">A feladat befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b519-121">Specifies the end time for a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b519-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9b519-122">-Id</span></span>
<span data-ttu-id="9b519-123">Egy feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b519-123">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b519-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="9b519-124">-Profile</span></span>
<span data-ttu-id="9b519-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9b519-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b519-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9b519-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9b519-127">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="9b519-127">-RunbookName</span></span>
<span data-ttu-id="9b519-128">Egy runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b519-128">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b519-129">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="9b519-129">-StartTime</span></span>
<span data-ttu-id="9b519-130">A feladat kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b519-130">Specifies the start time of a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b519-131">-Állapot</span><span class="sxs-lookup"><span data-stu-id="9b519-131">-Status</span></span>
<span data-ttu-id="9b519-132">Egy feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b519-132">Specifies the status of a job.</span></span>
<span data-ttu-id="9b519-133">Ez a parancsmag olyan munkafolyamatokat kap, amelyekhez az adott paraméter illik.</span><span class="sxs-lookup"><span data-stu-id="9b519-133">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="9b519-134">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="9b519-134">Valid values are:</span></span> 

- <span data-ttu-id="9b519-135">Kész</span><span class="sxs-lookup"><span data-stu-id="9b519-135">Completed</span></span>
- <span data-ttu-id="9b519-136">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="9b519-136">Failed</span></span>
- <span data-ttu-id="9b519-137">Várólistán töltött</span><span class="sxs-lookup"><span data-stu-id="9b519-137">Queued</span></span>
- <span data-ttu-id="9b519-138">Kezdve</span><span class="sxs-lookup"><span data-stu-id="9b519-138">Starting</span></span>
- <span data-ttu-id="9b519-139">Újrakezd</span><span class="sxs-lookup"><span data-stu-id="9b519-139">Resuming</span></span>
- <span data-ttu-id="9b519-140">Fut</span><span class="sxs-lookup"><span data-stu-id="9b519-140">Running</span></span>
- <span data-ttu-id="9b519-141">Megállt</span><span class="sxs-lookup"><span data-stu-id="9b519-141">Stopped</span></span>
- <span data-ttu-id="9b519-142">Megállás</span><span class="sxs-lookup"><span data-stu-id="9b519-142">Stopping</span></span>
- <span data-ttu-id="9b519-143">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="9b519-143">Suspended</span></span>
- <span data-ttu-id="9b519-144">Indokolva kéri</span><span class="sxs-lookup"><span data-stu-id="9b519-144">Suspending</span></span>
- <span data-ttu-id="9b519-145">Aktiválása</span><span class="sxs-lookup"><span data-stu-id="9b519-145">Activating</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b519-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b519-146">CommonParameters</span></span>
<span data-ttu-id="9b519-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b519-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b519-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b519-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b519-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b519-149">INPUTS</span></span>

## <span data-ttu-id="9b519-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b519-150">OUTPUTS</span></span>

### <span data-ttu-id="9b519-151">Microsoft. Azure. Command. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="9b519-151">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="9b519-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b519-152">NOTES</span></span>

## <span data-ttu-id="9b519-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b519-153">RELATED LINKS</span></span>

[<span data-ttu-id="9b519-154">Önéletrajz – AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9b519-154">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="9b519-155">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9b519-155">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="9b519-156">Felfüggesztés – AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9b519-156">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


