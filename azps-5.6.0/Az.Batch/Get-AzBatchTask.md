---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: 214ee3b030757da9acf632b2768a94b1ab026cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012725"
---
# <span data-ttu-id="5c836-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5c836-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="5c836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c836-102">SYNOPSIS</span></span>
<span data-ttu-id="5c836-103">Egy feladat kötegfeladatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5c836-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="5c836-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5c836-104">SYNTAX</span></span>

### <span data-ttu-id="5c836-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5c836-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c836-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="5c836-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c836-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="5c836-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c836-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5c836-108">DESCRIPTION</span></span>
<span data-ttu-id="5c836-109">A **Get-AzBatchTask** parancsmag Azure Batch-feladatokat kap egy kötegfeladathoz.</span><span class="sxs-lookup"><span data-stu-id="5c836-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="5c836-110">Adjon meg egy feladatot a *JobId vagy* a *Job paraméter* alapján.</span><span class="sxs-lookup"><span data-stu-id="5c836-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="5c836-111">Egyetlen feladat végrehajtásához adja meg az *Azonosító paramétert.*</span><span class="sxs-lookup"><span data-stu-id="5c836-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="5c836-112">A Szűrő  paraméter megadásával lekértheti az OData-szűrőnek megfelelő feladatokat.</span><span class="sxs-lookup"><span data-stu-id="5c836-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="5c836-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5c836-113">EXAMPLES</span></span>

### <span data-ttu-id="5c836-114">1. példa: Feladat lekérte azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="5c836-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         :
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 :
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               :
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="5c836-115">Ez a parancs a Feladat01 feladat alatt a Feladat03 azonosítóval kapja meg a feladatot.</span><span class="sxs-lookup"><span data-stu-id="5c836-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="5c836-116">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="5c836-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5c836-117">2. példa: Az összes befejezett tevékenység lekérte egy adott feladatból</span><span class="sxs-lookup"><span data-stu-id="5c836-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         :
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               :
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         :
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               :
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="5c836-118">Ez a parancs az id Job02 azonosítójú feladatból kapja meg az elkészült feladatokat.</span><span class="sxs-lookup"><span data-stu-id="5c836-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="5c836-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c836-119">PARAMETERS</span></span>

### <span data-ttu-id="5c836-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5c836-120">-BatchContext</span></span>
<span data-ttu-id="5c836-121">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="5c836-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5c836-122">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="5c836-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5c836-123">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="5c836-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5c836-124">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="5c836-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5c836-125">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="5c836-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c836-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c836-126">-DefaultProfile</span></span>
<span data-ttu-id="5c836-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c836-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c836-128">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="5c836-128">-Expand</span></span>
<span data-ttu-id="5c836-129">OData kibontó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5c836-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="5c836-130">A paraméter értékét megadva lekérte a fő entitás társított entitását.</span><span class="sxs-lookup"><span data-stu-id="5c836-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c836-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="5c836-131">-Filter</span></span>
<span data-ttu-id="5c836-132">OData-szűrő záradékot ad meg a feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="5c836-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="5c836-133">Ha nem ad meg szűrőt, ez a parancsmag a Batch-fiók vagy -feladat összes feladatát visszaadja.</span><span class="sxs-lookup"><span data-stu-id="5c836-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c836-134">-Id</span><span class="sxs-lookup"><span data-stu-id="5c836-134">-Id</span></span>
<span data-ttu-id="5c836-135">A parancsmag által lekért feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5c836-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="5c836-136">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="5c836-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c836-137">-Job</span><span class="sxs-lookup"><span data-stu-id="5c836-137">-Job</span></span>
<span data-ttu-id="5c836-138">Azt a feladatot adja meg, amely a parancsmag által lekért feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5c836-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="5c836-139">**PSCloudFeladat-objektum** beszerzéséhez használja a Get-AzBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5c836-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c836-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="5c836-140">-JobId</span></span>
<span data-ttu-id="5c836-141">Annak a feladatnak az azonosítóját adja meg, amely a parancsmag által lekért feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5c836-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c836-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5c836-142">-MaxCount</span></span>
<span data-ttu-id="5c836-143">Azt adja meg, hogy legfeljebb hány tevékenység adható vissza.</span><span class="sxs-lookup"><span data-stu-id="5c836-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="5c836-144">Ha nullát (0) vagy kisebb értéket ad meg, a parancsmag nem használ felső korlátot.</span><span class="sxs-lookup"><span data-stu-id="5c836-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="5c836-145">Az alapértelmezett érték 1000.</span><span class="sxs-lookup"><span data-stu-id="5c836-145">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c836-146">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="5c836-146">-Select</span></span>
<span data-ttu-id="5c836-147">OData-választó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5c836-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="5c836-148">A paraméter értékét megadva az összes objektumtulajdonság helyett konkrét tulajdonságokat kap.</span><span class="sxs-lookup"><span data-stu-id="5c836-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c836-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c836-149">CommonParameters</span></span>
<span data-ttu-id="5c836-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c836-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c836-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c836-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c836-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c836-152">INPUTS</span></span>

### <span data-ttu-id="5c836-153">System.String</span><span class="sxs-lookup"><span data-stu-id="5c836-153">System.String</span></span>

### <span data-ttu-id="5c836-154">Microsoft.Azure.Commands.Bat. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="5c836-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="5c836-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5c836-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5c836-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c836-156">OUTPUTS</span></span>

### <span data-ttu-id="5c836-157">Microsoft.Azure.Commands.Bat. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="5c836-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="5c836-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5c836-158">NOTES</span></span>

## <span data-ttu-id="5c836-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c836-159">RELATED LINKS</span></span>

[<span data-ttu-id="5c836-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5c836-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5c836-161">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="5c836-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="5c836-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5c836-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="5c836-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5c836-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="5c836-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5c836-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="5c836-165">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5c836-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
