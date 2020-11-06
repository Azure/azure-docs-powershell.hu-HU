---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: bf96b5930895332de2e78ffdee71f9f6a2654b83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505536"
---
# <span data-ttu-id="e7b63-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7b63-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="e7b63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7b63-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b63-103">Feladatot hoz létre a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e7b63-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7b63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7b63-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7b63-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7b63-105">DESCRIPTION</span></span>
<span data-ttu-id="e7b63-106">A **New-AzureBatchJob** parancsmag létrehoz egy feladatot az Azure kötegelt szolgáltatásban a *BatchAccountContext* paraméterrel megadott fiókban.</span><span class="sxs-lookup"><span data-stu-id="e7b63-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="e7b63-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e7b63-107">EXAMPLES</span></span>

### <span data-ttu-id="e7b63-108">Példa 1: feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7b63-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="e7b63-109">Az első parancs az New-Object parancsmag segítségével hoz létre **PSPoolInformation** -objektumokat.</span><span class="sxs-lookup"><span data-stu-id="e7b63-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="e7b63-110">A parancs az objektumot a $PoolInformation változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e7b63-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="e7b63-111">A második parancs az azonosító Pool22 az objektum **PoolId** tulajdonságához rendeli az $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="e7b63-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="e7b63-112">A végleges parancs létrehoz egy olyan feladatot, amely az azonosító ContosoJob35 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e7b63-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="e7b63-113">A feladathoz hozzáadott feladatok az azonosító Pool22 tartalmazó készleten futnak.</span><span class="sxs-lookup"><span data-stu-id="e7b63-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="e7b63-114">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="e7b63-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e7b63-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7b63-115">PARAMETERS</span></span>

### <span data-ttu-id="e7b63-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e7b63-116">-BatchContext</span></span>
<span data-ttu-id="e7b63-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="e7b63-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e7b63-118">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="e7b63-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e7b63-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="e7b63-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e7b63-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="e7b63-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e7b63-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="e7b63-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e7b63-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="e7b63-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="e7b63-123">A gyakori környezeti változók (kulcs/érték párok) meghatározása a projekt összes tevékenységéhez.</span><span class="sxs-lookup"><span data-stu-id="e7b63-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="e7b63-124">A kulcs a környezeti változók neve.</span><span class="sxs-lookup"><span data-stu-id="e7b63-124">The key is the environment variable name.</span></span>
<span data-ttu-id="e7b63-125">Az érték a környezeti változó értéke.</span><span class="sxs-lookup"><span data-stu-id="e7b63-125">The value is the environment variable value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b63-126">-Kényszerek</span><span class="sxs-lookup"><span data-stu-id="e7b63-126">-Constraints</span></span>
<span data-ttu-id="e7b63-127">A projekt végrehajtási korlátozásait adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b63-127">Specifies the execution constraints for the job.</span></span>

```yaml
Type: PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b63-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b63-128">-DefaultProfile</span></span>
<span data-ttu-id="e7b63-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7b63-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7b63-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e7b63-130">-DisplayName</span></span>
<span data-ttu-id="e7b63-131">A feladat megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b63-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="e7b63-132">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e7b63-132">-Id</span></span>
<span data-ttu-id="e7b63-133">A feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b63-133">Specifies an ID for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b63-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="e7b63-134">-JobManagerTask</span></span>
<span data-ttu-id="e7b63-135">A Feladatkezelő feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b63-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="e7b63-136">A kötegelt szolgáltatás a feladat indításakor a Feladatkezelő feladatot futtatja.</span><span class="sxs-lookup"><span data-stu-id="e7b63-136">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b63-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="e7b63-137">-JobPreparationTask</span></span>
<span data-ttu-id="e7b63-138">A projekt előkészületi tevékenysége.</span><span class="sxs-lookup"><span data-stu-id="e7b63-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="e7b63-139">A kötegelt szolgáltatás egy számítási csomóponton futtatja a projekt-előkészítési feladatot, mielőtt az adott feladatot a számítási csomóponton elindítja.</span><span class="sxs-lookup"><span data-stu-id="e7b63-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b63-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="e7b63-140">-JobReleaseTask</span></span>
<span data-ttu-id="e7b63-141">A projekt kiadási feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b63-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="e7b63-142">A kötegelt szolgáltatás a feladat befejezését követően futtatja a projekt kiadási feladatot.</span><span class="sxs-lookup"><span data-stu-id="e7b63-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="e7b63-143">A kötegelt szolgáltatás minden olyan számítási csomóponton futtatja a projekt kiadási feladatot, amely a feladat bármely tevékenységét futtatta.</span><span class="sxs-lookup"><span data-stu-id="e7b63-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b63-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e7b63-144">-Metadata</span></span>
<span data-ttu-id="e7b63-145">A feladatba felvenni kívánt metaadatokat adja meg kulcs/érték párokként.</span><span class="sxs-lookup"><span data-stu-id="e7b63-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="e7b63-146">A kulcs a metaadat neve.</span><span class="sxs-lookup"><span data-stu-id="e7b63-146">The key is the metadata name.</span></span>
<span data-ttu-id="e7b63-147">Az érték a metaadat-érték.</span><span class="sxs-lookup"><span data-stu-id="e7b63-147">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b63-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="e7b63-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="e7b63-149">Megadja, hogy a kötegelt szolgáltatás milyen műveletet hajtson végre, ha a feladatban szereplő összes tevékenység a befejezett állapotba kerül.</span><span class="sxs-lookup"><span data-stu-id="e7b63-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: OnAllTasksComplete
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b63-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="e7b63-150">-OnTaskFailure</span></span>
<span data-ttu-id="e7b63-151">Megadja, hogy a kötegelt szolgáltatás milyen műveletet hajtson végre, ha a feladatban bármely tevékenység nem működik.</span><span class="sxs-lookup"><span data-stu-id="e7b63-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: OnTaskFailure
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b63-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="e7b63-152">-PoolInformation</span></span>
<span data-ttu-id="e7b63-153">Annak a készletnek a részletét adja meg, amelyen a kötegelt szolgáltatás végrehajtja a feladat feladatait.</span><span class="sxs-lookup"><span data-stu-id="e7b63-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b63-154">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="e7b63-154">-Priority</span></span>
<span data-ttu-id="e7b63-155">A feladat prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b63-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="e7b63-156">Az érvényes értékek:-1000-től 1000-ig terjedő egész számok.</span><span class="sxs-lookup"><span data-stu-id="e7b63-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="e7b63-157">A-1000 értéke a legalacsonyabb prioritás.</span><span class="sxs-lookup"><span data-stu-id="e7b63-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="e7b63-158">A 1000 értéke a legmagasabb prioritás.</span><span class="sxs-lookup"><span data-stu-id="e7b63-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="e7b63-159">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="e7b63-159">The default value is 0.</span></span>

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

### <span data-ttu-id="e7b63-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="e7b63-160">-UsesTaskDependencies</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b63-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b63-161">CommonParameters</span></span>
<span data-ttu-id="e7b63-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7b63-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b63-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7b63-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b63-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7b63-164">INPUTS</span></span>

### <span data-ttu-id="e7b63-165">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e7b63-165">BatchAccountContext</span></span>
<span data-ttu-id="e7b63-166">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e7b63-166">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="e7b63-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7b63-167">OUTPUTS</span></span>

## <span data-ttu-id="e7b63-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7b63-168">NOTES</span></span>

## <span data-ttu-id="e7b63-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7b63-169">RELATED LINKS</span></span>

[<span data-ttu-id="e7b63-170">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7b63-170">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="e7b63-171">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7b63-171">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="e7b63-172">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e7b63-172">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e7b63-173">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7b63-173">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="e7b63-174">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7b63-174">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="e7b63-175">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7b63-175">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="e7b63-176">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7b63-176">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="e7b63-177">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e7b63-177">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


