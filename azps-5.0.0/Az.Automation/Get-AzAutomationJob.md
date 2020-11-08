---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194830"
---
# <span data-ttu-id="29368-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="29368-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="29368-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29368-102">SYNOPSIS</span></span>
<span data-ttu-id="29368-103">Automatizálási runbook feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="29368-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="29368-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29368-104">SYNTAX</span></span>

### <span data-ttu-id="29368-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29368-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29368-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="29368-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29368-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="29368-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29368-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="29368-108">DESCRIPTION</span></span>
<span data-ttu-id="29368-109">A **Get-AzAutomationJob** parancsmag runbook feladatokat kap az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="29368-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="29368-110">Példák</span><span class="sxs-lookup"><span data-stu-id="29368-110">EXAMPLES</span></span>

### <span data-ttu-id="29368-111">Példa 1: konkrét runbook-feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="29368-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="29368-112">Ez a parancs a megadott GUID azonosítóval rendelkező feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="29368-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="29368-113">2. példa: a runbook minden feladatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="29368-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="29368-114">Ez a parancs a Runbook02 nevű runbook társított összes feladatot megkapja.</span><span class="sxs-lookup"><span data-stu-id="29368-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="29368-115">3. példa: az összes futó feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="29368-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="29368-116">Ez a parancs a Contoso17 nevű automatizálási fiókból kapja meg az összes futó munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="29368-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="29368-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29368-117">PARAMETERS</span></span>

### <span data-ttu-id="29368-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="29368-118">-AutomationAccountName</span></span>
<span data-ttu-id="29368-119">Itt adhatja meg annak az automatizálási fióknak a nevét, amelyhez a parancsmag feladatait kapja.</span><span class="sxs-lookup"><span data-stu-id="29368-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="29368-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29368-120">-DefaultProfile</span></span>
<span data-ttu-id="29368-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="29368-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29368-122">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="29368-122">-EndTime</span></span>
<span data-ttu-id="29368-123">A feladat befejezési időpontját adja meg **DateTimeOffset** -objektumként.</span><span class="sxs-lookup"><span data-stu-id="29368-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="29368-124">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="29368-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="29368-125">Ez a parancsmag olyan feladatokat kap, amelyeknek a záró időpontja a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="29368-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29368-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="29368-126">-Id</span></span>
<span data-ttu-id="29368-127">Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="29368-127">Specifies the ID of a job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29368-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29368-128">-ResourceGroupName</span></span>
<span data-ttu-id="29368-129">Annak az erőforráscsoport a nevét adja meg, amelyben a parancsmag munkahelyeket kap.</span><span class="sxs-lookup"><span data-stu-id="29368-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="29368-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="29368-130">-RunbookName</span></span>
<span data-ttu-id="29368-131">Itt adhatja meg annak a runbook a nevét, amelynek a parancsmagja a feladatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="29368-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29368-132">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="29368-132">-StartTime</span></span>
<span data-ttu-id="29368-133">A feladat kezdési időpontját adja meg **DateTimeOffset** -objektumként.</span><span class="sxs-lookup"><span data-stu-id="29368-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="29368-134">Ez a parancsmag olyan feladatokat kap, amelyeken a paraméter által megadott érték látható vagy azt követően.</span><span class="sxs-lookup"><span data-stu-id="29368-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29368-135">-Állapot</span><span class="sxs-lookup"><span data-stu-id="29368-135">-Status</span></span>
<span data-ttu-id="29368-136">Egy feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="29368-136">Specifies the status of a job.</span></span>
<span data-ttu-id="29368-137">Ez a parancsmag olyan munkafolyamatokat kap, amelyekhez az adott paraméter illik.</span><span class="sxs-lookup"><span data-stu-id="29368-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="29368-138">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="29368-138">Valid values are:</span></span> 
- <span data-ttu-id="29368-139">Aktiválása</span><span class="sxs-lookup"><span data-stu-id="29368-139">Activating</span></span>
- <span data-ttu-id="29368-140">Kész</span><span class="sxs-lookup"><span data-stu-id="29368-140">Completed</span></span>
- <span data-ttu-id="29368-141">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="29368-141">Failed</span></span>
- <span data-ttu-id="29368-142">Várólistán töltött</span><span class="sxs-lookup"><span data-stu-id="29368-142">Queued</span></span>
- <span data-ttu-id="29368-143">Újrakezd</span><span class="sxs-lookup"><span data-stu-id="29368-143">Resuming</span></span>
- <span data-ttu-id="29368-144">Fut</span><span class="sxs-lookup"><span data-stu-id="29368-144">Running</span></span>
- <span data-ttu-id="29368-145">Kezdve</span><span class="sxs-lookup"><span data-stu-id="29368-145">Starting</span></span>
- <span data-ttu-id="29368-146">Megállt</span><span class="sxs-lookup"><span data-stu-id="29368-146">Stopped</span></span>
- <span data-ttu-id="29368-147">Megállás</span><span class="sxs-lookup"><span data-stu-id="29368-147">Stopping</span></span>
- <span data-ttu-id="29368-148">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="29368-148">Suspended</span></span>
- <span data-ttu-id="29368-149">Indokolva kéri</span><span class="sxs-lookup"><span data-stu-id="29368-149">Suspending</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29368-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29368-150">CommonParameters</span></span>
<span data-ttu-id="29368-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29368-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29368-152">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29368-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29368-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29368-153">INPUTS</span></span>

### <span data-ttu-id="29368-154">System. GUID</span><span class="sxs-lookup"><span data-stu-id="29368-154">System.Guid</span></span>

### <span data-ttu-id="29368-155">System. String</span><span class="sxs-lookup"><span data-stu-id="29368-155">System.String</span></span>

## <span data-ttu-id="29368-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29368-156">OUTPUTS</span></span>

### <span data-ttu-id="29368-157">Microsoft. Azure. Command. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="29368-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="29368-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29368-158">NOTES</span></span>

## <span data-ttu-id="29368-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29368-159">RELATED LINKS</span></span>

[<span data-ttu-id="29368-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="29368-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="29368-161">Önéletrajz – AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="29368-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="29368-162">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="29368-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="29368-163">Felfüggesztés – AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="29368-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


