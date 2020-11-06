---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 4509190a8417379c9d5bc9eae9d6d12609def4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505683"
---
# <span data-ttu-id="52004-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="52004-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="52004-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52004-102">SYNOPSIS</span></span>
<span data-ttu-id="52004-103">Automatizálási runbook feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="52004-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52004-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52004-104">SYNTAX</span></span>

### <span data-ttu-id="52004-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52004-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52004-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="52004-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52004-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="52004-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52004-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="52004-108">DESCRIPTION</span></span>
<span data-ttu-id="52004-109">A **Get-AzureRmAutomationJob** parancsmag runbook feladatokat kap az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="52004-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="52004-110">Példák</span><span class="sxs-lookup"><span data-stu-id="52004-110">EXAMPLES</span></span>

### <span data-ttu-id="52004-111">Példa 1: konkrét runbook-feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="52004-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="52004-112">Ez a parancs a megadott GUID azonosítóval rendelkező feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="52004-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="52004-113">2. példa: a runbook minden feladatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="52004-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="52004-114">Ez a parancs a Runbook02 nevű runbook társított összes feladatot megkapja.</span><span class="sxs-lookup"><span data-stu-id="52004-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="52004-115">3. példa: az összes futó feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="52004-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="52004-116">Ez a parancs a Contoso17 nevű automatizálási fiókból kapja meg az összes futó munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="52004-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="52004-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52004-117">PARAMETERS</span></span>

### <span data-ttu-id="52004-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="52004-118">-AutomationAccountName</span></span>
<span data-ttu-id="52004-119">Itt adhatja meg annak az automatizálási fióknak a nevét, amelyhez a parancsmag feladatait kapja.</span><span class="sxs-lookup"><span data-stu-id="52004-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="52004-120">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="52004-120">-EndTime</span></span>
<span data-ttu-id="52004-121">A feladat befejezési időpontját adja meg **DateTimeOffset** -objektumként.</span><span class="sxs-lookup"><span data-stu-id="52004-121">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="52004-122">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="52004-122">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="52004-123">Ez a parancsmag olyan feladatokat kap, amelyeknek a záró időpontja a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="52004-123">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="52004-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="52004-124">-Id</span></span>
<span data-ttu-id="52004-125">Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="52004-125">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="52004-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52004-126">-ResourceGroupName</span></span>
<span data-ttu-id="52004-127">Annak az erőforráscsoport a nevét adja meg, amelyben a parancsmag munkahelyeket kap.</span><span class="sxs-lookup"><span data-stu-id="52004-127">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="52004-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="52004-128">-RunbookName</span></span>
<span data-ttu-id="52004-129">Itt adhatja meg annak a runbook a nevét, amelynek a parancsmagja a feladatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="52004-129">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="52004-130">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="52004-130">-StartTime</span></span>
<span data-ttu-id="52004-131">A feladat kezdési időpontját adja meg **DateTimeOffset** -objektumként.</span><span class="sxs-lookup"><span data-stu-id="52004-131">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="52004-132">Ez a parancsmag olyan feladatokat kap, amelyeken a paraméter által megadott érték látható vagy azt követően.</span><span class="sxs-lookup"><span data-stu-id="52004-132">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="52004-133">-Állapot</span><span class="sxs-lookup"><span data-stu-id="52004-133">-Status</span></span>
<span data-ttu-id="52004-134">Egy feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="52004-134">Specifies the status of a job.</span></span>
<span data-ttu-id="52004-135">Ez a parancsmag olyan munkafolyamatokat kap, amelyekhez az adott paraméter illik.</span><span class="sxs-lookup"><span data-stu-id="52004-135">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="52004-136">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="52004-136">Valid values are:</span></span> 

- <span data-ttu-id="52004-137">Aktiválása</span><span class="sxs-lookup"><span data-stu-id="52004-137">Activating</span></span>
- <span data-ttu-id="52004-138">Kész</span><span class="sxs-lookup"><span data-stu-id="52004-138">Completed</span></span>
- <span data-ttu-id="52004-139">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="52004-139">Failed</span></span>
- <span data-ttu-id="52004-140">Várólistán töltött</span><span class="sxs-lookup"><span data-stu-id="52004-140">Queued</span></span>
- <span data-ttu-id="52004-141">Újrakezd</span><span class="sxs-lookup"><span data-stu-id="52004-141">Resuming</span></span>
- <span data-ttu-id="52004-142">Fut</span><span class="sxs-lookup"><span data-stu-id="52004-142">Running</span></span>
- <span data-ttu-id="52004-143">Kezdve</span><span class="sxs-lookup"><span data-stu-id="52004-143">Starting</span></span>
- <span data-ttu-id="52004-144">Megállt</span><span class="sxs-lookup"><span data-stu-id="52004-144">Stopped</span></span>
- <span data-ttu-id="52004-145">Megállás</span><span class="sxs-lookup"><span data-stu-id="52004-145">Stopping</span></span>
- <span data-ttu-id="52004-146">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="52004-146">Suspended</span></span>
- <span data-ttu-id="52004-147">Indokolva kéri</span><span class="sxs-lookup"><span data-stu-id="52004-147">Suspending</span></span>

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

### <span data-ttu-id="52004-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52004-148">-DefaultProfile</span></span>
<span data-ttu-id="52004-149">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52004-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52004-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52004-150">CommonParameters</span></span>
<span data-ttu-id="52004-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52004-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52004-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52004-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52004-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52004-153">INPUTS</span></span>

## <span data-ttu-id="52004-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52004-154">OUTPUTS</span></span>

### <span data-ttu-id="52004-155">Microsoft. Azure. Command. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="52004-155">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="52004-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52004-156">NOTES</span></span>

## <span data-ttu-id="52004-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52004-157">RELATED LINKS</span></span>

[<span data-ttu-id="52004-158">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="52004-158">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="52004-159">Önéletrajz – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="52004-159">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="52004-160">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="52004-160">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="52004-161">Felfüggesztés – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="52004-161">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


