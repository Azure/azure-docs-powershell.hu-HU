---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 9daa0e1a1b1bc6ec980f3c3f65d79840648fdaf8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024206"
---
# <span data-ttu-id="92813-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="92813-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="92813-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92813-102">SYNOPSIS</span></span>
<span data-ttu-id="92813-103">Kötegelt munka ütemezéseit kapja.</span><span class="sxs-lookup"><span data-stu-id="92813-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="92813-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92813-104">SYNTAX</span></span>

### <span data-ttu-id="92813-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92813-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92813-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="92813-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92813-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="92813-107">DESCRIPTION</span></span>
<span data-ttu-id="92813-108">A **Get-AzBatchJobSchedule** parancsmag Azure kötegelt feladatok ütemezéseit kapja meg a *BatchContext* paraméter által megadott köteg számlára.</span><span class="sxs-lookup"><span data-stu-id="92813-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="92813-109">Adjon meg egy azonosítót egyetlen munkaütemezés beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="92813-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="92813-110">Adja meg azt a *szűrési* paramétert, amely egy Open Data Protocol (OData) szűrőnek megfelelő munkabeosztásokat kap.</span><span class="sxs-lookup"><span data-stu-id="92813-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="92813-111">Példák</span><span class="sxs-lookup"><span data-stu-id="92813-111">EXAMPLES</span></span>

### <span data-ttu-id="92813-112">Példa 1: beosztás beszerzése az azonosító megadásával</span><span class="sxs-lookup"><span data-stu-id="92813-112">Example 1: Get a job schedule by specifying an ID</span></span>
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

<span data-ttu-id="92813-113">Ez a parancs a JobSchedule23 AZONOSÍTÓval rendelkező munkabeosztást kapja.</span><span class="sxs-lookup"><span data-stu-id="92813-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="92813-114">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="92813-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="92813-115">2. példa: nyomtatási ütemtervek beszerzése szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="92813-115">Example 2: Get job schedules by using a filter</span></span>
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

<span data-ttu-id="92813-116">Ez a parancs a *szűrési* paraméter megadásával beilleszti az összes olyan munkabeosztást, amelynek a feladattal kezdődő azonosítói vannak.</span><span class="sxs-lookup"><span data-stu-id="92813-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="92813-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92813-117">PARAMETERS</span></span>

### <span data-ttu-id="92813-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="92813-118">-BatchContext</span></span>
<span data-ttu-id="92813-119">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="92813-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="92813-120">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="92813-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="92813-121">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="92813-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="92813-122">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="92813-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="92813-123">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="92813-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="92813-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92813-124">-DefaultProfile</span></span>
<span data-ttu-id="92813-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92813-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92813-126">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="92813-126">-Expand</span></span>
<span data-ttu-id="92813-127">Az Open Data Protocol (OData) kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="92813-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="92813-128">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz tartozó társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="92813-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="92813-129">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="92813-129">-Filter</span></span>
<span data-ttu-id="92813-130">Egy OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="92813-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="92813-131">Ez a parancsmag olyan munkabeosztásokat ad eredményül, amelyek megfelelnek a paraméter által megadott szűrőnek.</span><span class="sxs-lookup"><span data-stu-id="92813-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="92813-132">Ha nem ad meg szűrőt, ez a parancsmag a köteg környezetéhez tartozó összes nyomtatási ütemtervet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="92813-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="92813-133">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="92813-133">-Id</span></span>
<span data-ttu-id="92813-134">A parancsmag által beolvasott ütemterv AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="92813-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="92813-135">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="92813-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="92813-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="92813-136">-MaxCount</span></span>
<span data-ttu-id="92813-137">Az eredményül adott munkabeosztások maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="92813-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="92813-138">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="92813-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="92813-139">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="92813-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="92813-140">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="92813-140">-Select</span></span>
<span data-ttu-id="92813-141">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="92813-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="92813-142">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="92813-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="92813-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92813-143">CommonParameters</span></span>
<span data-ttu-id="92813-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92813-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92813-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="92813-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92813-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92813-146">INPUTS</span></span>

### <span data-ttu-id="92813-147">System. String</span><span class="sxs-lookup"><span data-stu-id="92813-147">System.String</span></span>

### <span data-ttu-id="92813-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="92813-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="92813-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92813-149">OUTPUTS</span></span>

### <span data-ttu-id="92813-150">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="92813-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="92813-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92813-151">NOTES</span></span>

## <span data-ttu-id="92813-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92813-152">RELATED LINKS</span></span>

[<span data-ttu-id="92813-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="92813-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="92813-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="92813-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="92813-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="92813-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="92813-156">Új – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="92813-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="92813-157">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="92813-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="92813-158">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="92813-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="92813-159">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="92813-159">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
