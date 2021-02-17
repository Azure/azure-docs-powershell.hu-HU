---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: b0709c7b839ca992d415cd5ba9fff58e769120fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205327"
---
# <span data-ttu-id="673ad-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="673ad-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="673ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="673ad-102">SYNOPSIS</span></span>
<span data-ttu-id="673ad-103">Batch-fiókhoz vagy feladatütemtervhez kap kötegelt feladatokat.</span><span class="sxs-lookup"><span data-stu-id="673ad-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="673ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="673ad-104">SYNTAX</span></span>

### <span data-ttu-id="673ad-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="673ad-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="673ad-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="673ad-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="673ad-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="673ad-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="673ad-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="673ad-108">DESCRIPTION</span></span>
<span data-ttu-id="673ad-109">A **Get-AzBatch Jobs** parancsmag a *BatchAccountContext* paraméterrel megadott Batch-fiók Azure Batch-feladatokkal való feldolgozását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="673ad-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="673ad-110">Az Azonosító *paramétert* használva egyetlen feladatot kaphat.</span><span class="sxs-lookup"><span data-stu-id="673ad-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="673ad-111">A Szűrő  paraméter használatával lekértheti az OData-szűrőnek megfelelő feladatokat.</span><span class="sxs-lookup"><span data-stu-id="673ad-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="673ad-112">Ha feladatütemterv-azonosítót vagy **PSCloudSchedule-példányt** ad meg, ez a parancsmag csak az adott munkabeosztáshoz szükséges feladatokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="673ad-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="673ad-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="673ad-113">EXAMPLES</span></span>

### <span data-ttu-id="673ad-114">1. példa: Kötegelt feladat lekért azonosítója</span><span class="sxs-lookup"><span data-stu-id="673ad-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 :
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="673ad-115">Ez a parancs a Job01 azonosítójú feladatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="673ad-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="673ad-116">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="673ad-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="673ad-117">2. példa: Az összes aktív feladat lekérte egy munkabeosztáshoz</span><span class="sxs-lookup"><span data-stu-id="673ad-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 :
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="673ad-118">Ez a parancs a Feladatütemező27 azonosítójú munkabeosztás aktív munkáihoz jut.</span><span class="sxs-lookup"><span data-stu-id="673ad-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="673ad-119">3. példa: Az összes feladatot egy beosztásba beveszi a folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="673ad-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 :
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="673ad-120">Ez a parancs a feladatütemtervet kapja meg, amely a Feladat ütemezése27 azonosítót Get-AzBatchJobSchedule parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="673ad-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="673ad-121">A parancs a folyamat műveleti operátorával átadja ezt a feladatütemtervet az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="673ad-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="673ad-122">A parancs a munkabeosztás összes állását beveszi.</span><span class="sxs-lookup"><span data-stu-id="673ad-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="673ad-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="673ad-123">PARAMETERS</span></span>

### <span data-ttu-id="673ad-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="673ad-124">-BatchContext</span></span>
<span data-ttu-id="673ad-125">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="673ad-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="673ad-126">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="673ad-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="673ad-127">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot, és töltse ki a hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="673ad-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="673ad-128">Megosztott kulcsú hitelesítés használata esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="673ad-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="673ad-129">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="673ad-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="673ad-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="673ad-130">-DefaultProfile</span></span>
<span data-ttu-id="673ad-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="673ad-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="673ad-132">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="673ad-132">-Expand</span></span>
<span data-ttu-id="673ad-133">OData-kibontó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="673ad-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="673ad-134">Adjon meg egy értéket a paraméterhez a bejő fő entitás társított entitásának lekérthez.</span><span class="sxs-lookup"><span data-stu-id="673ad-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="673ad-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="673ad-135">-Filter</span></span>
<span data-ttu-id="673ad-136">OData-szűrő záradékot ad meg a feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="673ad-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="673ad-137">Ha nem ad meg szűrőt, ez a parancsmag a Batch-fiókhoz vagy feladatütemtervhez megadott összes feladatot visszaadja.</span><span class="sxs-lookup"><span data-stu-id="673ad-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="673ad-138">-Id</span><span class="sxs-lookup"><span data-stu-id="673ad-138">-Id</span></span>
<span data-ttu-id="673ad-139">A parancsmag által lekért feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="673ad-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="673ad-140">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="673ad-140">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="673ad-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="673ad-141">-JobSchedule</span></span>
<span data-ttu-id="673ad-142">Egy **PSCloudSchedule** objektumot ad meg, amely a feladatokat tartalmazó munkabeosztást képviseli.</span><span class="sxs-lookup"><span data-stu-id="673ad-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="673ad-143">**PSCloudSchedule-objektum** beszerzéséhez használja a Get-AzBatchJobSchedule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="673ad-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="673ad-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="673ad-144">-JobScheduleId</span></span>
<span data-ttu-id="673ad-145">Megadja annak a beosztásnak az azonosítóját, amely a feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="673ad-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="673ad-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="673ad-146">-MaxCount</span></span>
<span data-ttu-id="673ad-147">A vissza nem térő feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="673ad-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="673ad-148">Ha nullát (0) vagy kisebb értéket ad meg, a parancsmag nem használ felső korlátot.</span><span class="sxs-lookup"><span data-stu-id="673ad-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="673ad-149">Az alapértelmezett érték 1000.</span><span class="sxs-lookup"><span data-stu-id="673ad-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="673ad-150">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="673ad-150">-Select</span></span>
<span data-ttu-id="673ad-151">OData-választó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="673ad-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="673ad-152">A paraméter értékét megadva az összes objektumtulajdonság helyett konkrét tulajdonságokat kap.</span><span class="sxs-lookup"><span data-stu-id="673ad-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="673ad-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="673ad-153">CommonParameters</span></span>
<span data-ttu-id="673ad-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="673ad-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="673ad-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="673ad-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="673ad-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="673ad-156">INPUTS</span></span>

### <span data-ttu-id="673ad-157">System.String</span><span class="sxs-lookup"><span data-stu-id="673ad-157">System.String</span></span>

### <span data-ttu-id="673ad-158">Microsoft.Azure.Commands.Bat. Models.PSCloudSchedule</span><span class="sxs-lookup"><span data-stu-id="673ad-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="673ad-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="673ad-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="673ad-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="673ad-160">OUTPUTS</span></span>

### <span data-ttu-id="673ad-161">Microsoft.Azure.Commands.Bat. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="673ad-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="673ad-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="673ad-162">NOTES</span></span>

## <span data-ttu-id="673ad-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="673ad-163">RELATED LINKS</span></span>

[<span data-ttu-id="673ad-164">Disable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="673ad-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="673ad-165">Enable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="673ad-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="673ad-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="673ad-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="673ad-167">Get-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="673ad-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="673ad-168">New-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="673ad-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="673ad-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="673ad-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="673ad-170">Stop-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="673ad-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="673ad-171">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="673ad-171">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
