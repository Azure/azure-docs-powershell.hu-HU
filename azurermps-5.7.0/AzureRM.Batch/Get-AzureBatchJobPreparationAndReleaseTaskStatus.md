---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 5f24e55042a8be7f36b1a9946c4bd5b87209a0f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502619"
---
# <span data-ttu-id="dc16f-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="dc16f-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="dc16f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc16f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc16f-103">Beolvassa a kötegelt feldolgozást, és felszabadítja a tevékenység állapotát.</span><span class="sxs-lookup"><span data-stu-id="dc16f-103">Gets Batch job preparation and release task status.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc16f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc16f-104">SYNTAX</span></span>

### <span data-ttu-id="dc16f-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc16f-105">Id (Default)</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc16f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="dc16f-106">InputObject</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc16f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc16f-107">DESCRIPTION</span></span>
<span data-ttu-id="dc16f-108">A **Get-AzureBatchJobPreparationAndReleaseTaskStatus** parancsmag az Azure kötegelt feladat-előkészítési és kiadási tevékenység állapotát kapja meg egy kötegelt feldolgozáshoz.</span><span class="sxs-lookup"><span data-stu-id="dc16f-108">The **Get-AzureBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="dc16f-109">Ebben a parancsmagban meg kell adnia az *azonosító* paramétert vagy egy **PSCloudJob** -példányt.</span><span class="sxs-lookup"><span data-stu-id="dc16f-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="dc16f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dc16f-110">EXAMPLES</span></span>

### <span data-ttu-id="dc16f-111">Példa 1: a projekt felkészítési és kiadási állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="dc16f-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="dc16f-112">Ez a parancs beilleszti a feladat-előkészítési és kiadási tevékenység állapotát a "teszt" állásba.</span><span class="sxs-lookup"><span data-stu-id="dc16f-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="dc16f-113">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="dc16f-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="dc16f-114">2. példa: a projekt előkészítési és kiadási állapotának beszerzése szűrővel, majd a megadott elem választása</span><span class="sxs-lookup"><span data-stu-id="dc16f-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="dc16f-115">Ez a parancs beolvassa a feladat-előkészítési és kiadási tevékenység állapotát a "TVM-2316545714_1-20170613t201733z" ("teszt") csomóponton, és a Select záradékot használja az JobPreparationTaskExecutionInformation adatok visszaadására.</span><span class="sxs-lookup"><span data-stu-id="dc16f-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="dc16f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc16f-116">PARAMETERS</span></span>

### <span data-ttu-id="dc16f-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dc16f-117">-BatchContext</span></span>
<span data-ttu-id="dc16f-118">A kötegelt szolgáltatással való interakció során használandó BatchAccountContext-példány.</span><span class="sxs-lookup"><span data-stu-id="dc16f-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="dc16f-119">A Get-AzureRmBatchAccountKeys parancsmag segítségével BatchAccountContext-objektumot kaphat a hozzá tartozó elérési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="dc16f-119">Use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc16f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc16f-120">-DefaultProfile</span></span>
<span data-ttu-id="dc16f-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc16f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc16f-122">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="dc16f-122">-Expand</span></span>
<span data-ttu-id="dc16f-123">Az Open Data Protocol (OData) kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc16f-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="dc16f-124">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz tartozó társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="dc16f-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc16f-125">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="dc16f-125">-Filter</span></span>
<span data-ttu-id="dc16f-126">Egy OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="dc16f-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="dc16f-127">Ha nem ad meg szűrőt, ez a parancsmag visszaadja a projekthez tartozó összes feladat-előkészítési és kiadási tevékenység állapotát.</span><span class="sxs-lookup"><span data-stu-id="dc16f-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc16f-128">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="dc16f-128">-Id</span></span>
<span data-ttu-id="dc16f-129">Annak a feladatnak az AZONOSÍTÓját adja meg, amelynek az előkészítési és kiadási feladatait le kell olvasni.</span><span class="sxs-lookup"><span data-stu-id="dc16f-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="dc16f-130">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="dc16f-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc16f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc16f-131">-InputObject</span></span>
<span data-ttu-id="dc16f-132">Itt adhatja meg azt a **PSCloudJob** -objektumot, amely a feladatra vonatkozó előkészítő és kiadási tevékenység állapotát reprezentálja.</span><span class="sxs-lookup"><span data-stu-id="dc16f-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="dc16f-133">**PSCloudJob** objektum beolvasásához használja az Get-AzureBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dc16f-133">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc16f-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="dc16f-134">-MaxCount</span></span>
<span data-ttu-id="dc16f-135">Megadja, hogy a program a munkafolyamatok elkészítési és kiadási tevékenységének maximális számát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="dc16f-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="dc16f-136">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="dc16f-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="dc16f-137">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="dc16f-137">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc16f-138">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="dc16f-138">-Select</span></span>
<span data-ttu-id="dc16f-139">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="dc16f-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="dc16f-140">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="dc16f-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc16f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc16f-141">CommonParameters</span></span>
<span data-ttu-id="dc16f-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc16f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc16f-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc16f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc16f-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc16f-144">INPUTS</span></span>

### <span data-ttu-id="dc16f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="dc16f-145">System.String</span></span>
<span data-ttu-id="dc16f-146">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dc16f-146">Microsoft.Azure.Commands.Batch.Models.PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dc16f-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc16f-147">OUTPUTS</span></span>

### <span data-ttu-id="dc16f-148">Microsoft.Azure.Commands.BatCH. Modellek. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="dc16f-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="dc16f-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc16f-149">NOTES</span></span>

## <span data-ttu-id="dc16f-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc16f-150">RELATED LINKS</span></span>

[<span data-ttu-id="dc16f-151">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc16f-151">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="dc16f-152">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dc16f-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
