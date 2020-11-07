---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 6e825e6d582117a919691aea4780868191e8e4a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679628"
---
# <span data-ttu-id="daa0e-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="daa0e-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="daa0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="daa0e-102">SYNOPSIS</span></span>
<span data-ttu-id="daa0e-103">Automatizálási runbook feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="daa0e-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="daa0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="daa0e-104">SYNTAX</span></span>

### <span data-ttu-id="daa0e-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="daa0e-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="daa0e-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="daa0e-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="daa0e-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="daa0e-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daa0e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="daa0e-108">DESCRIPTION</span></span>
<span data-ttu-id="daa0e-109">A **Get-AzureRmAutomationJob** parancsmag runbook feladatokat kap az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="daa0e-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="daa0e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="daa0e-110">EXAMPLES</span></span>

### <span data-ttu-id="daa0e-111">Példa 1: konkrét runbook-feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="daa0e-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="daa0e-112">Ez a parancs a megadott GUID azonosítóval rendelkező feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="daa0e-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="daa0e-113">2. példa: a runbook minden feladatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="daa0e-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="daa0e-114">Ez a parancs a Runbook02 nevű runbook társított összes feladatot megkapja.</span><span class="sxs-lookup"><span data-stu-id="daa0e-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="daa0e-115">3. példa: az összes futó feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="daa0e-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="daa0e-116">Ez a parancs a Contoso17 nevű automatizálási fiókból kapja meg az összes futó munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="daa0e-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="daa0e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="daa0e-117">PARAMETERS</span></span>

### <span data-ttu-id="daa0e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="daa0e-118">-AutomationAccountName</span></span>
<span data-ttu-id="daa0e-119">Itt adhatja meg annak az automatizálási fióknak a nevét, amelyhez a parancsmag feladatait kapja.</span><span class="sxs-lookup"><span data-stu-id="daa0e-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="daa0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa0e-120">-DefaultProfile</span></span>
<span data-ttu-id="daa0e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="daa0e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="daa0e-122">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="daa0e-122">-EndTime</span></span>
<span data-ttu-id="daa0e-123">A feladat befejezési időpontját adja meg **DateTimeOffset** -objektumként.</span><span class="sxs-lookup"><span data-stu-id="daa0e-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="daa0e-124">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="daa0e-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="daa0e-125">Ez a parancsmag olyan feladatokat kap, amelyeknek a záró időpontja a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="daa0e-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="daa0e-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="daa0e-126">-Id</span></span>
<span data-ttu-id="daa0e-127">Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="daa0e-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="daa0e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa0e-128">-ResourceGroupName</span></span>
<span data-ttu-id="daa0e-129">Annak az erőforráscsoport a nevét adja meg, amelyben a parancsmag munkahelyeket kap.</span><span class="sxs-lookup"><span data-stu-id="daa0e-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="daa0e-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="daa0e-130">-RunbookName</span></span>
<span data-ttu-id="daa0e-131">Itt adhatja meg annak a runbook a nevét, amelynek a parancsmagja a feladatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="daa0e-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="daa0e-132">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="daa0e-132">-StartTime</span></span>
<span data-ttu-id="daa0e-133">A feladat kezdési időpontját adja meg **DateTimeOffset** -objektumként.</span><span class="sxs-lookup"><span data-stu-id="daa0e-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="daa0e-134">Ez a parancsmag olyan feladatokat kap, amelyeken a paraméter által megadott érték látható vagy azt követően.</span><span class="sxs-lookup"><span data-stu-id="daa0e-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="daa0e-135">-Állapot</span><span class="sxs-lookup"><span data-stu-id="daa0e-135">-Status</span></span>
<span data-ttu-id="daa0e-136">Egy feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="daa0e-136">Specifies the status of a job.</span></span>
<span data-ttu-id="daa0e-137">Ez a parancsmag olyan munkafolyamatokat kap, amelyekhez az adott paraméter illik.</span><span class="sxs-lookup"><span data-stu-id="daa0e-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="daa0e-138">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="daa0e-138">Valid values are:</span></span> 
- <span data-ttu-id="daa0e-139">Aktiválása</span><span class="sxs-lookup"><span data-stu-id="daa0e-139">Activating</span></span>
- <span data-ttu-id="daa0e-140">Kész</span><span class="sxs-lookup"><span data-stu-id="daa0e-140">Completed</span></span>
- <span data-ttu-id="daa0e-141">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="daa0e-141">Failed</span></span>
- <span data-ttu-id="daa0e-142">Várólistán töltött</span><span class="sxs-lookup"><span data-stu-id="daa0e-142">Queued</span></span>
- <span data-ttu-id="daa0e-143">Újrakezd</span><span class="sxs-lookup"><span data-stu-id="daa0e-143">Resuming</span></span>
- <span data-ttu-id="daa0e-144">Fut</span><span class="sxs-lookup"><span data-stu-id="daa0e-144">Running</span></span>
- <span data-ttu-id="daa0e-145">Kezdve</span><span class="sxs-lookup"><span data-stu-id="daa0e-145">Starting</span></span>
- <span data-ttu-id="daa0e-146">Megállt</span><span class="sxs-lookup"><span data-stu-id="daa0e-146">Stopped</span></span>
- <span data-ttu-id="daa0e-147">Megállás</span><span class="sxs-lookup"><span data-stu-id="daa0e-147">Stopping</span></span>
- <span data-ttu-id="daa0e-148">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="daa0e-148">Suspended</span></span>
- <span data-ttu-id="daa0e-149">Indokolva kéri</span><span class="sxs-lookup"><span data-stu-id="daa0e-149">Suspending</span></span>

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

### <span data-ttu-id="daa0e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa0e-150">CommonParameters</span></span>
<span data-ttu-id="daa0e-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="daa0e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa0e-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daa0e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa0e-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="daa0e-153">INPUTS</span></span>

### <span data-ttu-id="daa0e-154">System. GUID</span><span class="sxs-lookup"><span data-stu-id="daa0e-154">System.Guid</span></span>

### <span data-ttu-id="daa0e-155">System. String</span><span class="sxs-lookup"><span data-stu-id="daa0e-155">System.String</span></span>

## <span data-ttu-id="daa0e-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="daa0e-156">OUTPUTS</span></span>

### <span data-ttu-id="daa0e-157">Microsoft. Azure. Command. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="daa0e-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="daa0e-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="daa0e-158">NOTES</span></span>

## <span data-ttu-id="daa0e-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="daa0e-159">RELATED LINKS</span></span>

[<span data-ttu-id="daa0e-160">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="daa0e-160">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="daa0e-161">Önéletrajz – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="daa0e-161">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="daa0e-162">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="daa0e-162">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="daa0e-163">Felfüggesztés – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="daa0e-163">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


