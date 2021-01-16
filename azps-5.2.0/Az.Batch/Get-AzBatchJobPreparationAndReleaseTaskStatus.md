---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363255"
---
# <span data-ttu-id="8da1b-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="8da1b-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="8da1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8da1b-102">SYNOPSIS</span></span>
<span data-ttu-id="8da1b-103">Kötegfeladat-előkészítést és feladatállapotot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="8da1b-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="8da1b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8da1b-104">SYNTAX</span></span>

### <span data-ttu-id="8da1b-105">Id (Default)</span><span class="sxs-lookup"><span data-stu-id="8da1b-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8da1b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8da1b-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8da1b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8da1b-107">DESCRIPTION</span></span>
<span data-ttu-id="8da1b-108">A **Get-AzBatchPreparationAndReleaseTaskStatus** parancsmag megkapja az Azure Batch-feladat előkészítését és egy batch-feladat feladatállapotának kiadását.</span><span class="sxs-lookup"><span data-stu-id="8da1b-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="8da1b-109">Ehhez a parancsmaghoz meg kell adnunk az *Id* paramétert vagy egy **PSCloudSzolgáltatás-példányt.**</span><span class="sxs-lookup"><span data-stu-id="8da1b-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="8da1b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8da1b-110">EXAMPLES</span></span>

### <span data-ttu-id="8da1b-111">1. példa: A feladat előkészítésének és kiadásának állapota</span><span class="sxs-lookup"><span data-stu-id="8da1b-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="8da1b-112">Ez a parancs a "Teszt" feladathoz beveszi a feladat előkészítését és kiadását.</span><span class="sxs-lookup"><span data-stu-id="8da1b-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="8da1b-113">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="8da1b-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8da1b-114">2. példa: A feladat előkészítésének és kiadásának állapota a megadott Szűrő és kijelölés beállítással</span><span class="sxs-lookup"><span data-stu-id="8da1b-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="8da1b-115">Ez a parancs a "Tvm-2316545714_1-20170613t201733z" csomópont "Test" feladatának "Tesztelés" állapotát kapja meg, és a Select záradékot használva csak a JobPreparationTaskExecutionInformation információt adja vissza.</span><span class="sxs-lookup"><span data-stu-id="8da1b-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="8da1b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8da1b-116">PARAMETERS</span></span>

### <span data-ttu-id="8da1b-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8da1b-117">-BatchContext</span></span>
<span data-ttu-id="8da1b-118">A BatchAccountContext példány, amely a Batch szolgáltatás használata során használható.</span><span class="sxs-lookup"><span data-stu-id="8da1b-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="8da1b-119">A Get-AzBatchAccountKey parancsmaggal be tud szerezni egy BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="8da1b-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="8da1b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da1b-120">-DefaultProfile</span></span>
<span data-ttu-id="8da1b-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8da1b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8da1b-122">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="8da1b-122">-Expand</span></span>
<span data-ttu-id="8da1b-123">OData-kibontó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8da1b-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="8da1b-124">Adjon meg egy értéket a paraméterhez a bejő fő entitás társított entitásának lekérthez.</span><span class="sxs-lookup"><span data-stu-id="8da1b-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="8da1b-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="8da1b-125">-Filter</span></span>
<span data-ttu-id="8da1b-126">OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8da1b-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="8da1b-127">Ha nem ad meg szűrőt, ez a parancsmag a feladatra vonatkozó összes feladat előkészítését és kiadását visszaadja.</span><span class="sxs-lookup"><span data-stu-id="8da1b-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="8da1b-128">-Id</span><span class="sxs-lookup"><span data-stu-id="8da1b-128">-Id</span></span>
<span data-ttu-id="8da1b-129">Annak a feladatnak az azonosítója, amelynek az előkészítési és kibocsátási feladatait le kellkérni.</span><span class="sxs-lookup"><span data-stu-id="8da1b-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="8da1b-130">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="8da1b-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da1b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8da1b-131">-InputObject</span></span>
<span data-ttu-id="8da1b-132">Egy **PSCloud Job** objektumot ad meg, amely a feladat előkészítésének és kiadásának állapotát jelzi.</span><span class="sxs-lookup"><span data-stu-id="8da1b-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="8da1b-133">**PSCloudFeladat-objektum** beszerzéséhez használja a Get-AzBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8da1b-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8da1b-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8da1b-134">-MaxCount</span></span>
<span data-ttu-id="8da1b-135">Azt adja meg, hogy legfeljebb hány feladat előkészítését és kiadását kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="8da1b-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="8da1b-136">Ha nullát (0) vagy kisebb értéket ad meg, a parancsmag nem használ felső korlátot.</span><span class="sxs-lookup"><span data-stu-id="8da1b-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8da1b-137">Az alapértelmezett érték 1000.</span><span class="sxs-lookup"><span data-stu-id="8da1b-137">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da1b-138">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="8da1b-138">-Select</span></span>
<span data-ttu-id="8da1b-139">OData-választó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8da1b-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="8da1b-140">A paraméter értékét megadva az összes objektumtulajdonság helyett konkrét tulajdonságokat kap.</span><span class="sxs-lookup"><span data-stu-id="8da1b-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="8da1b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da1b-141">CommonParameters</span></span>
<span data-ttu-id="8da1b-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da1b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da1b-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8da1b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da1b-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8da1b-144">INPUTS</span></span>

### <span data-ttu-id="8da1b-145">Microsoft.Azure.Commands.Bat. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="8da1b-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="8da1b-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8da1b-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8da1b-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8da1b-147">OUTPUTS</span></span>

### <span data-ttu-id="8da1b-148">Microsoft.Azure.Commands.Bat. Models.PSPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="8da1b-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="8da1b-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8da1b-149">NOTES</span></span>

## <span data-ttu-id="8da1b-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8da1b-150">RELATED LINKS</span></span>

[<span data-ttu-id="8da1b-151">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="8da1b-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="8da1b-152">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8da1b-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
