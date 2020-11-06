---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: c8b51f3822ce52fd21aa1d2b8df45d11108d713a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495167"
---
# <span data-ttu-id="c15b9-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c15b9-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="c15b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c15b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c15b9-103">Kötegelt munka ütemezéseit kapja.</span><span class="sxs-lookup"><span data-stu-id="c15b9-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c15b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c15b9-104">SYNTAX</span></span>

### <span data-ttu-id="c15b9-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c15b9-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c15b9-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="c15b9-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c15b9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c15b9-107">DESCRIPTION</span></span>
<span data-ttu-id="c15b9-108">A **Get-AzureBatchJobSchedule** parancsmag Azure kötegelt feladatok ütemezéseit kapja meg a *BatchContext* paraméter által megadott köteg számlára.</span><span class="sxs-lookup"><span data-stu-id="c15b9-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="c15b9-109">Adjon meg egy azonosítót egyetlen munkaütemezés beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="c15b9-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="c15b9-110">Adja meg azt a *szűrési* paramétert, amely egy Open Data Protocol (OData) szűrőnek megfelelő munkabeosztásokat kap.</span><span class="sxs-lookup"><span data-stu-id="c15b9-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="c15b9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c15b9-111">EXAMPLES</span></span>

### <span data-ttu-id="c15b9-112">Példa 1: beosztás beszerzése az azonosító megadásával</span><span class="sxs-lookup"><span data-stu-id="c15b9-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
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

<span data-ttu-id="c15b9-113">Ez a parancs a JobSchedule23 AZONOSÍTÓval rendelkező munkabeosztást kapja.</span><span class="sxs-lookup"><span data-stu-id="c15b9-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="c15b9-114">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="c15b9-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c15b9-115">2. példa: nyomtatási ütemtervek beszerzése szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="c15b9-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
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

<span data-ttu-id="c15b9-116">Ez a parancs a *szűrési* paraméter megadásával beilleszti az összes olyan munkabeosztást, amelynek a feladattal kezdődő azonosítói vannak.</span><span class="sxs-lookup"><span data-stu-id="c15b9-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="c15b9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c15b9-117">PARAMETERS</span></span>

### <span data-ttu-id="c15b9-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c15b9-118">-BatchContext</span></span>
<span data-ttu-id="c15b9-119">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="c15b9-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c15b9-120">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="c15b9-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c15b9-121">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="c15b9-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c15b9-122">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="c15b9-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c15b9-123">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="c15b9-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c15b9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c15b9-124">-DefaultProfile</span></span>
<span data-ttu-id="c15b9-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c15b9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c15b9-126">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="c15b9-126">-Expand</span></span>
<span data-ttu-id="c15b9-127">Az Open Data Protocol (OData) kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c15b9-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="c15b9-128">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz tartozó társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="c15b9-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="c15b9-129">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="c15b9-129">-Filter</span></span>
<span data-ttu-id="c15b9-130">Egy OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c15b9-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="c15b9-131">Ez a parancsmag olyan munkabeosztásokat ad eredményül, amelyek megfelelnek a paraméter által megadott szűrőnek.</span><span class="sxs-lookup"><span data-stu-id="c15b9-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="c15b9-132">Ha nem ad meg szűrőt, ez a parancsmag a köteg környezetéhez tartozó összes nyomtatási ütemtervet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c15b9-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="c15b9-133">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="c15b9-133">-Id</span></span>
<span data-ttu-id="c15b9-134">A parancsmag által beolvasott ütemterv AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c15b9-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="c15b9-135">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="c15b9-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="c15b9-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c15b9-136">-MaxCount</span></span>
<span data-ttu-id="c15b9-137">Az eredményül adott munkabeosztások maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c15b9-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="c15b9-138">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="c15b9-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="c15b9-139">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="c15b9-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="c15b9-140">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="c15b9-140">-Select</span></span>
<span data-ttu-id="c15b9-141">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c15b9-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="c15b9-142">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="c15b9-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="c15b9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15b9-143">CommonParameters</span></span>
<span data-ttu-id="c15b9-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c15b9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15b9-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c15b9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15b9-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c15b9-146">INPUTS</span></span>

### <span data-ttu-id="c15b9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c15b9-147">System.String</span></span>

### <span data-ttu-id="c15b9-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c15b9-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c15b9-149">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c15b9-149">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c15b9-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c15b9-150">OUTPUTS</span></span>

### <span data-ttu-id="c15b9-151">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c15b9-151">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="c15b9-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c15b9-152">NOTES</span></span>

## <span data-ttu-id="c15b9-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c15b9-153">RELATED LINKS</span></span>

[<span data-ttu-id="c15b9-154">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c15b9-154">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c15b9-155">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c15b9-155">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c15b9-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c15b9-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c15b9-157">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c15b9-157">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="c15b9-158">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c15b9-158">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="c15b9-159">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c15b9-159">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="c15b9-160">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c15b9-160">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


