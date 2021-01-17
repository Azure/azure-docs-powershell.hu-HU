---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 9daa0e1a1b1bc6ec980f3c3f65d79840648fdaf8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478354"
---
# <span data-ttu-id="07cab-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="07cab-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="07cab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07cab-102">SYNOPSIS</span></span>
<span data-ttu-id="07cab-103">Kötegelt feladatütemterveket kap.</span><span class="sxs-lookup"><span data-stu-id="07cab-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="07cab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07cab-104">SYNTAX</span></span>

### <span data-ttu-id="07cab-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07cab-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07cab-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="07cab-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07cab-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07cab-107">DESCRIPTION</span></span>
<span data-ttu-id="07cab-108">A **Get-AzBatch JobSchedule** parancsmag az Azure Batch-feladatütemezőket kapja a BatchContext paraméterrel megadott *Batch-fiókhoz.*</span><span class="sxs-lookup"><span data-stu-id="07cab-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="07cab-109">Adjon meg egy azonosítót egyetlen munkabeosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="07cab-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="07cab-110">Adja meg *a Szűrő* paramétert az OData-szűrőnek megfelelő feladatütemtervek be szereznie.</span><span class="sxs-lookup"><span data-stu-id="07cab-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="07cab-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07cab-111">EXAMPLES</span></span>

### <span data-ttu-id="07cab-112">1. példa: Munkabeosztás lekérte azonosító megadásával</span><span class="sxs-lookup"><span data-stu-id="07cab-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 :
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

<span data-ttu-id="07cab-113">Ez a parancs a Feladatütemterv23 azonosítójú munkabeosztást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="07cab-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="07cab-114">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="07cab-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="07cab-115">2. példa: Munkabeosztások lekérte szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="07cab-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 :
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 :
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

<span data-ttu-id="07cab-116">Ez a parancs a Szűrés paraméter megadásával az összes olyan  feladatütemtervet beveszi, amely a Feladat mezővel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="07cab-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="07cab-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07cab-117">PARAMETERS</span></span>

### <span data-ttu-id="07cab-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="07cab-118">-BatchContext</span></span>
<span data-ttu-id="07cab-119">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="07cab-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="07cab-120">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="07cab-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="07cab-121">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="07cab-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="07cab-122">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="07cab-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="07cab-123">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="07cab-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="07cab-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07cab-124">-DefaultProfile</span></span>
<span data-ttu-id="07cab-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07cab-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07cab-126">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="07cab-126">-Expand</span></span>
<span data-ttu-id="07cab-127">OData-kibontó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="07cab-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="07cab-128">Adjon meg egy értéket a paraméterhez a bejő fő entitás társított entitásának lekérthez.</span><span class="sxs-lookup"><span data-stu-id="07cab-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="07cab-129">-Filter</span><span class="sxs-lookup"><span data-stu-id="07cab-129">-Filter</span></span>
<span data-ttu-id="07cab-130">OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="07cab-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="07cab-131">Ez a parancsmag olyan feladatütemterveket ad vissza, amelyek megfelelnek a paraméter által megadott szűrőnek.</span><span class="sxs-lookup"><span data-stu-id="07cab-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="07cab-132">Ha nem ad meg szűrőt, ez a parancsmag a Köteg környezet összes feladatütemtervét visszaadja.</span><span class="sxs-lookup"><span data-stu-id="07cab-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cab-133">-Id</span><span class="sxs-lookup"><span data-stu-id="07cab-133">-Id</span></span>
<span data-ttu-id="07cab-134">A parancsmag által lekért feladatütemterv azonosítója.</span><span class="sxs-lookup"><span data-stu-id="07cab-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="07cab-135">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="07cab-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07cab-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="07cab-136">-MaxCount</span></span>
<span data-ttu-id="07cab-137">Azt adja meg, hogy legfeljebb hány munkabeosztást kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="07cab-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="07cab-138">Ha nullát (0) vagy kisebb értéket ad meg, a parancsmag nem használ felső korlátot.</span><span class="sxs-lookup"><span data-stu-id="07cab-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="07cab-139">Az alapértelmezett érték 1000.</span><span class="sxs-lookup"><span data-stu-id="07cab-139">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cab-140">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="07cab-140">-Select</span></span>
<span data-ttu-id="07cab-141">OData-választó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="07cab-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="07cab-142">A paraméter értékét megadva az összes objektumtulajdonság helyett konkrét tulajdonságokat kap.</span><span class="sxs-lookup"><span data-stu-id="07cab-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="07cab-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07cab-143">CommonParameters</span></span>
<span data-ttu-id="07cab-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07cab-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07cab-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07cab-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07cab-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07cab-146">INPUTS</span></span>

### <span data-ttu-id="07cab-147">System.String</span><span class="sxs-lookup"><span data-stu-id="07cab-147">System.String</span></span>

### <span data-ttu-id="07cab-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="07cab-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="07cab-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07cab-149">OUTPUTS</span></span>

### <span data-ttu-id="07cab-150">Microsoft.Azure.Commands.Bat. Models.PSCloudSchedule</span><span class="sxs-lookup"><span data-stu-id="07cab-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="07cab-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07cab-151">NOTES</span></span>

## <span data-ttu-id="07cab-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07cab-152">RELATED LINKS</span></span>

[<span data-ttu-id="07cab-153">Disable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="07cab-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="07cab-154">Enable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="07cab-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="07cab-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="07cab-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="07cab-156">New-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="07cab-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="07cab-157">Remove-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="07cab-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="07cab-158">Stop-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="07cab-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="07cab-159">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="07cab-159">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
