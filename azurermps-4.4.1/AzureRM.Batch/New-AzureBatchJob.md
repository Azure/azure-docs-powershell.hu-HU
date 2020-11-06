---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: 94a35c3923debf5ea983e9d1ad276b124ae8c89c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497904"
---
# <span data-ttu-id="ccf80-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ccf80-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="ccf80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccf80-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf80-103">Feladatot hoz létre a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="ccf80-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccf80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccf80-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccf80-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccf80-105">DESCRIPTION</span></span>
<span data-ttu-id="ccf80-106">A **New-AzureBatchJob** parancsmag létrehoz egy feladatot az Azure kötegelt szolgáltatásban a *BatchAccountContext* paraméterrel megadott fiókban.</span><span class="sxs-lookup"><span data-stu-id="ccf80-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="ccf80-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ccf80-107">EXAMPLES</span></span>

### <span data-ttu-id="ccf80-108">Példa 1: feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="ccf80-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="ccf80-109">Az első parancs az New-Object parancsmag segítségével hoz létre **PSPoolInformation** -objektumokat.</span><span class="sxs-lookup"><span data-stu-id="ccf80-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="ccf80-110">A parancs az objektumot a $PoolInformation változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ccf80-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="ccf80-111">A második parancs az azonosító Pool22 az objektum **PoolId** tulajdonságához rendeli az $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="ccf80-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="ccf80-112">A végleges parancs létrehoz egy olyan feladatot, amely az azonosító ContosoJob35 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ccf80-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="ccf80-113">A feladathoz hozzáadott feladatok az azonosító Pool22 tartalmazó készleten futnak.</span><span class="sxs-lookup"><span data-stu-id="ccf80-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="ccf80-114">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="ccf80-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="ccf80-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccf80-115">PARAMETERS</span></span>

### <span data-ttu-id="ccf80-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ccf80-116">-BatchContext</span></span>
<span data-ttu-id="ccf80-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="ccf80-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ccf80-118">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ccf80-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ccf80-119">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="ccf80-119">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="ccf80-120">A gyakori környezeti változók (kulcs/érték párok) meghatározása a projekt összes tevékenységéhez.</span><span class="sxs-lookup"><span data-stu-id="ccf80-120">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="ccf80-121">A kulcs a környezeti változók neve.</span><span class="sxs-lookup"><span data-stu-id="ccf80-121">The key is the environment variable name.</span></span>
<span data-ttu-id="ccf80-122">Az érték a környezeti változó értéke.</span><span class="sxs-lookup"><span data-stu-id="ccf80-122">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf80-123">-Kényszerek</span><span class="sxs-lookup"><span data-stu-id="ccf80-123">-Constraints</span></span>
<span data-ttu-id="ccf80-124">A projekt végrehajtási korlátozásait adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccf80-124">Specifies the execution constraints for the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf80-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ccf80-125">-DisplayName</span></span>
<span data-ttu-id="ccf80-126">A feladat megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccf80-126">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="ccf80-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ccf80-127">-Id</span></span>
<span data-ttu-id="ccf80-128">A feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccf80-128">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="ccf80-129">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="ccf80-129">-JobManagerTask</span></span>
<span data-ttu-id="ccf80-130">A Feladatkezelő feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccf80-130">Specifies the Job Manager task.</span></span>
<span data-ttu-id="ccf80-131">A kötegelt szolgáltatás a feladat indításakor a Feladatkezelő feladatot futtatja.</span><span class="sxs-lookup"><span data-stu-id="ccf80-131">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf80-132">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="ccf80-132">-JobPreparationTask</span></span>
<span data-ttu-id="ccf80-133">A projekt előkészületi tevékenysége.</span><span class="sxs-lookup"><span data-stu-id="ccf80-133">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="ccf80-134">A kötegelt szolgáltatás egy számítási csomóponton futtatja a projekt-előkészítési feladatot, mielőtt az adott feladatot a számítási csomóponton elindítja.</span><span class="sxs-lookup"><span data-stu-id="ccf80-134">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf80-135">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="ccf80-135">-JobReleaseTask</span></span>
<span data-ttu-id="ccf80-136">A projekt kiadási feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccf80-136">Specifies the Job Release task.</span></span>
<span data-ttu-id="ccf80-137">A kötegelt szolgáltatás a feladat befejezését követően futtatja a projekt kiadási feladatot.</span><span class="sxs-lookup"><span data-stu-id="ccf80-137">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="ccf80-138">A kötegelt szolgáltatás minden olyan számítási csomóponton futtatja a projekt kiadási feladatot, amely a feladat bármely tevékenységét futtatta.</span><span class="sxs-lookup"><span data-stu-id="ccf80-138">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf80-139">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ccf80-139">-Metadata</span></span>
<span data-ttu-id="ccf80-140">A feladatba felvenni kívánt metaadatokat adja meg kulcs/érték párokként.</span><span class="sxs-lookup"><span data-stu-id="ccf80-140">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="ccf80-141">A kulcs a metaadat neve.</span><span class="sxs-lookup"><span data-stu-id="ccf80-141">The key is the metadata name.</span></span>
<span data-ttu-id="ccf80-142">Az érték a metaadat-érték.</span><span class="sxs-lookup"><span data-stu-id="ccf80-142">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf80-143">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="ccf80-143">-OnAllTasksComplete</span></span>
<span data-ttu-id="ccf80-144">Megadja, hogy a kötegelt szolgáltatás milyen műveletet hajtson végre, ha a feladatban szereplő összes tevékenység a befejezett állapotba kerül.</span><span class="sxs-lookup"><span data-stu-id="ccf80-144">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnAllTasksComplete]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf80-145">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="ccf80-145">-OnTaskFailure</span></span>
<span data-ttu-id="ccf80-146">Megadja, hogy a kötegelt szolgáltatás milyen műveletet hajtson végre, ha a feladatban bármely tevékenység nem működik.</span><span class="sxs-lookup"><span data-stu-id="ccf80-146">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnTaskFailure]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf80-147">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="ccf80-147">-PoolInformation</span></span>
<span data-ttu-id="ccf80-148">Annak a készletnek a részletét adja meg, amelyen a kötegelt szolgáltatás végrehajtja a feladat feladatait.</span><span class="sxs-lookup"><span data-stu-id="ccf80-148">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf80-149">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="ccf80-149">-Priority</span></span>
<span data-ttu-id="ccf80-150">A feladat prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccf80-150">Specifies the priority of the job.</span></span>
<span data-ttu-id="ccf80-151">Az érvényes értékek:-1000-től 1000-ig terjedő egész számok.</span><span class="sxs-lookup"><span data-stu-id="ccf80-151">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="ccf80-152">A-1000 értéke a legalacsonyabb prioritás.</span><span class="sxs-lookup"><span data-stu-id="ccf80-152">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="ccf80-153">A 1000 értéke a legmagasabb prioritás.</span><span class="sxs-lookup"><span data-stu-id="ccf80-153">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="ccf80-154">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="ccf80-154">The default value is 0.</span></span>

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

### <span data-ttu-id="ccf80-155">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="ccf80-155">-UsesTaskDependencies</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf80-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf80-156">-DefaultProfile</span></span>
<span data-ttu-id="ccf80-157">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccf80-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccf80-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf80-158">CommonParameters</span></span>
<span data-ttu-id="ccf80-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccf80-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf80-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccf80-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf80-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccf80-161">INPUTS</span></span>

### <span data-ttu-id="ccf80-162">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ccf80-162">BatchAccountContext</span></span>
<span data-ttu-id="ccf80-163">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ccf80-163">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="ccf80-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccf80-164">OUTPUTS</span></span>

## <span data-ttu-id="ccf80-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccf80-165">NOTES</span></span>

## <span data-ttu-id="ccf80-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccf80-166">RELATED LINKS</span></span>

[<span data-ttu-id="ccf80-167">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ccf80-167">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="ccf80-168">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ccf80-168">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="ccf80-169">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ccf80-169">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ccf80-170">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ccf80-170">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="ccf80-171">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ccf80-171">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="ccf80-172">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ccf80-172">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="ccf80-173">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ccf80-173">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="ccf80-174">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ccf80-174">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


