---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478706"
---
# <span data-ttu-id="49eb0-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="49eb0-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="49eb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="49eb0-103">Automatizálási runbook-feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="49eb0-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="49eb0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49eb0-104">SYNTAX</span></span>

### <span data-ttu-id="49eb0-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49eb0-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49eb0-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="49eb0-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49eb0-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="49eb0-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49eb0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49eb0-108">DESCRIPTION</span></span>
<span data-ttu-id="49eb0-109">A **Get-AzAutomation Automation parancsmag** runbook-feladatokat kap az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="49eb0-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="49eb0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49eb0-110">EXAMPLES</span></span>

### <span data-ttu-id="49eb0-111">1. példa: Adott runbook-feladat lekérte</span><span class="sxs-lookup"><span data-stu-id="49eb0-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="49eb0-112">Ez a parancs a megadott GUID azonosítójú feladatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="49eb0-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="49eb0-113">2. példa: Az összes feladat lekérte egy runbookhoz</span><span class="sxs-lookup"><span data-stu-id="49eb0-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="49eb0-114">Ez a parancs a Runbook02 nevű runbookhoz társított összes parancsot beveszi.</span><span class="sxs-lookup"><span data-stu-id="49eb0-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="49eb0-115">3. példa: Az összes futó feladat lekérte</span><span class="sxs-lookup"><span data-stu-id="49eb0-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="49eb0-116">Ez a parancs a Contoso17 nevű automatizálási fiók összes futó állását beveszi.</span><span class="sxs-lookup"><span data-stu-id="49eb0-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="49eb0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49eb0-117">PARAMETERS</span></span>

### <span data-ttu-id="49eb0-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="49eb0-118">-AutomationAccountName</span></span>
<span data-ttu-id="49eb0-119">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="49eb0-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="49eb0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49eb0-120">-DefaultProfile</span></span>
<span data-ttu-id="49eb0-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="49eb0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49eb0-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="49eb0-122">-EndTime</span></span>
<span data-ttu-id="49eb0-123">Egy feladat záró időpontját adja meg **DateTimeOffset-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="49eb0-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="49eb0-124">Megadhat egy olyan karakterláncot, amely érvényes **DateTimeOffset** formátumra konvertálható.</span><span class="sxs-lookup"><span data-stu-id="49eb0-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="49eb0-125">Ez a parancsmag olyan feladatokat kap, amelyek végén a paraméter által megadott érték van megadva vagy előtte.</span><span class="sxs-lookup"><span data-stu-id="49eb0-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="49eb0-126">-Id</span><span class="sxs-lookup"><span data-stu-id="49eb0-126">-Id</span></span>
<span data-ttu-id="49eb0-127">A parancsmag által lekért feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="49eb0-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="49eb0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49eb0-128">-ResourceGroupName</span></span>
<span data-ttu-id="49eb0-129">Annak az erőforráscsoportnak a nevét adja meg, amelyben a parancsmag feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="49eb0-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="49eb0-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="49eb0-130">-RunbookName</span></span>
<span data-ttu-id="49eb0-131">Annak a runbooknak a nevét adja meg, amelynek a parancsmagja feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="49eb0-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="49eb0-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="49eb0-132">-StartTime</span></span>
<span data-ttu-id="49eb0-133">Egy feladat kezdési idejét adja meg **DateTimeOffset-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="49eb0-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="49eb0-134">Ez a parancsmag olyan feladatokat kap, amelyek kezdési ideje a paraméter által megadott értéknél vagy után van.</span><span class="sxs-lookup"><span data-stu-id="49eb0-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="49eb0-135">-Állapot</span><span class="sxs-lookup"><span data-stu-id="49eb0-135">-Status</span></span>
<span data-ttu-id="49eb0-136">Egy feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="49eb0-136">Specifies the status of a job.</span></span>
<span data-ttu-id="49eb0-137">Ez a parancsmag olyan feladatokat kap, amelyek állapota megfelel ennek a paraméternek.</span><span class="sxs-lookup"><span data-stu-id="49eb0-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="49eb0-138">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="49eb0-138">Valid values are:</span></span> 
- <span data-ttu-id="49eb0-139">Aktiválás</span><span class="sxs-lookup"><span data-stu-id="49eb0-139">Activating</span></span>
- <span data-ttu-id="49eb0-140">Befejezve</span><span class="sxs-lookup"><span data-stu-id="49eb0-140">Completed</span></span>
- <span data-ttu-id="49eb0-141">Nem sikerült</span><span class="sxs-lookup"><span data-stu-id="49eb0-141">Failed</span></span>
- <span data-ttu-id="49eb0-142">Várólistán</span><span class="sxs-lookup"><span data-stu-id="49eb0-142">Queued</span></span>
- <span data-ttu-id="49eb0-143">Visszaúszás</span><span class="sxs-lookup"><span data-stu-id="49eb0-143">Resuming</span></span>
- <span data-ttu-id="49eb0-144">Fut</span><span class="sxs-lookup"><span data-stu-id="49eb0-144">Running</span></span>
- <span data-ttu-id="49eb0-145">Indítás</span><span class="sxs-lookup"><span data-stu-id="49eb0-145">Starting</span></span>
- <span data-ttu-id="49eb0-146">Leállítva</span><span class="sxs-lookup"><span data-stu-id="49eb0-146">Stopped</span></span>
- <span data-ttu-id="49eb0-147">Leállítás</span><span class="sxs-lookup"><span data-stu-id="49eb0-147">Stopping</span></span>
- <span data-ttu-id="49eb0-148">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="49eb0-148">Suspended</span></span>
- <span data-ttu-id="49eb0-149">Felfüggesztés</span><span class="sxs-lookup"><span data-stu-id="49eb0-149">Suspending</span></span>

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

### <span data-ttu-id="49eb0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49eb0-150">CommonParameters</span></span>
<span data-ttu-id="49eb0-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49eb0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49eb0-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49eb0-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49eb0-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49eb0-153">INPUTS</span></span>

### <span data-ttu-id="49eb0-154">System.Guid</span><span class="sxs-lookup"><span data-stu-id="49eb0-154">System.Guid</span></span>

### <span data-ttu-id="49eb0-155">System.String</span><span class="sxs-lookup"><span data-stu-id="49eb0-155">System.String</span></span>

## <span data-ttu-id="49eb0-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49eb0-156">OUTPUTS</span></span>

### <span data-ttu-id="49eb0-157">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="49eb0-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="49eb0-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49eb0-158">NOTES</span></span>

## <span data-ttu-id="49eb0-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49eb0-159">RELATED LINKS</span></span>

[<span data-ttu-id="49eb0-160">Get-AzAutomationOutput</span><span class="sxs-lookup"><span data-stu-id="49eb0-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="49eb0-161">Resume-AzAutomation Azerbajdzsán</span><span class="sxs-lookup"><span data-stu-id="49eb0-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="49eb0-162">Stop-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="49eb0-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="49eb0-163">Suspend-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="49eb0-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


