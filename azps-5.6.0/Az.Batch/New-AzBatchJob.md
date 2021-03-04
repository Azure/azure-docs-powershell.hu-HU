---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: 97b6d2c332b4bc59df165599fe49d38fe496008c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936305"
---
# <span data-ttu-id="99639-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="99639-101">New-AzBatchJob</span></span>

## <span data-ttu-id="99639-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99639-102">SYNOPSIS</span></span>
<span data-ttu-id="99639-103">Létrehozza a feladatot a Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="99639-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="99639-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="99639-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99639-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="99639-105">DESCRIPTION</span></span>
<span data-ttu-id="99639-106">A **New-AzBatch Job parancsmag** létrehoz egy feladatot az Azure Batch szolgáltatásban a *BatchAccountContext* paraméterrel megadott fiókban.</span><span class="sxs-lookup"><span data-stu-id="99639-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="99639-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="99639-107">EXAMPLES</span></span>

### <span data-ttu-id="99639-108">1. példa: Feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="99639-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $PoolInformation.PoolId = "Pool22"
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="99639-109">Az első parancs egy **PSPoolInformation** objektumot hoz létre a New-Object parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="99639-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="99639-110">A parancs az objektumot a $PoolInformation tárolja.</span><span class="sxs-lookup"><span data-stu-id="99639-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="99639-111">A második parancs hozzárendeli az ID  Pool22-t a $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="99639-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="99639-112">Az utolsó parancs létrehoz egy feladatot, amely Contoso Job35 azonosítóval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="99639-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="99639-113">A feladathoz adott tevékenységek az azonosítókészletet22-es készleten futtatják.</span><span class="sxs-lookup"><span data-stu-id="99639-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="99639-114">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="99639-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="99639-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99639-115">PARAMETERS</span></span>

### <span data-ttu-id="99639-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="99639-116">-BatchContext</span></span>
<span data-ttu-id="99639-117">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="99639-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="99639-118">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="99639-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="99639-119">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="99639-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="99639-120">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="99639-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="99639-121">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="99639-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="99639-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="99639-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="99639-123">Ez a parancsmag a feladat összes tevékenységéhez beállítja a gyakori környezeti változókat kulcs/érték párokként.</span><span class="sxs-lookup"><span data-stu-id="99639-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="99639-124">A kulcs a környezeti változó neve.</span><span class="sxs-lookup"><span data-stu-id="99639-124">The key is the environment variable name.</span></span>
<span data-ttu-id="99639-125">Az érték a környezeti változó értéke.</span><span class="sxs-lookup"><span data-stu-id="99639-125">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99639-126">-Constraints</span><span class="sxs-lookup"><span data-stu-id="99639-126">-Constraints</span></span>
<span data-ttu-id="99639-127">A feladat végrehajtási kényszerét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="99639-127">Specifies the execution constraints for the job.</span></span>

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

### <span data-ttu-id="99639-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99639-128">-DefaultProfile</span></span>
<span data-ttu-id="99639-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99639-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99639-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="99639-130">-DisplayName</span></span>
<span data-ttu-id="99639-131">A feladat megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99639-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="99639-132">-Id</span><span class="sxs-lookup"><span data-stu-id="99639-132">-Id</span></span>
<span data-ttu-id="99639-133">Megadja a feladat azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="99639-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="99639-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="99639-134">-JobManagerTask</span></span>
<span data-ttu-id="99639-135">A Feladatkezelő feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="99639-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="99639-136">A Batch szolgáltatás futtatja a Feladatkezelő feladatot a feladat végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="99639-136">The Batch service runs the Job Manager task when the job is started.</span></span>

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

### <span data-ttu-id="99639-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="99639-137">-JobPreparationTask</span></span>
<span data-ttu-id="99639-138">A Feladat előkészítése tevékenységet adja meg.</span><span class="sxs-lookup"><span data-stu-id="99639-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="99639-139">A Batch szolgáltatás futtatja a feladat előkészítése feladatot egy számítási csomóponton, mielőtt elindítja a feladat bármely feladatát az adott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="99639-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

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

### <span data-ttu-id="99639-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="99639-140">-JobReleaseTask</span></span>
<span data-ttu-id="99639-141">Megadja a "Job Release" tevékenységet.</span><span class="sxs-lookup"><span data-stu-id="99639-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="99639-142">A Batch szolgáltatás futtatja a Feladat kiadása feladatot, amikor a feladat véget ér.</span><span class="sxs-lookup"><span data-stu-id="99639-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="99639-143">A Batch szolgáltatás minden olyan számítási csomóponton futtatja a Job Release feladatot, ahol a feladat bármely feladatát futtatta.</span><span class="sxs-lookup"><span data-stu-id="99639-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

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

### <span data-ttu-id="99639-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="99639-144">-Metadata</span></span>
<span data-ttu-id="99639-145">Megadja a feladathoz hozzáadni a metaadatokat kulcs-érték párokként.</span><span class="sxs-lookup"><span data-stu-id="99639-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="99639-146">A kulcs a metaadatok neve.</span><span class="sxs-lookup"><span data-stu-id="99639-146">The key is the metadata name.</span></span>
<span data-ttu-id="99639-147">Az érték a metaadatérték.</span><span class="sxs-lookup"><span data-stu-id="99639-147">The value is the metadata value.</span></span>

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

### <span data-ttu-id="99639-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="99639-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="99639-149">Azt a műveletet adja meg, amit a Batch szolgáltatás akkor végez, ha a feladat összes feladata befejezett állapotban van.</span><span class="sxs-lookup"><span data-stu-id="99639-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

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

### <span data-ttu-id="99639-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="99639-150">-OnTaskFailure</span></span>
<span data-ttu-id="99639-151">Azt a műveletet adja meg, amit a Batch szolgáltatás akkor végez, ha a feladat bármelyik feladata meghiúsul.</span><span class="sxs-lookup"><span data-stu-id="99639-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

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

### <span data-ttu-id="99639-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="99639-152">-PoolInformation</span></span>
<span data-ttu-id="99639-153">Megadja annak a készletnek a részleteit, amelyen a Batch szolgáltatás futtatja a feladat feladatait.</span><span class="sxs-lookup"><span data-stu-id="99639-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

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

### <span data-ttu-id="99639-154">-Priority</span><span class="sxs-lookup"><span data-stu-id="99639-154">-Priority</span></span>
<span data-ttu-id="99639-155">A feladat prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="99639-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="99639-156">Érvényes értékek: -1000 és 1000 között.</span><span class="sxs-lookup"><span data-stu-id="99639-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="99639-157">A -1000-es érték a legalacsonyabb prioritás.</span><span class="sxs-lookup"><span data-stu-id="99639-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="99639-158">Az 1000-es érték a legmagasabb prioritás.</span><span class="sxs-lookup"><span data-stu-id="99639-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="99639-159">Az alapértelmezett érték 0.</span><span class="sxs-lookup"><span data-stu-id="99639-159">The default value is 0.</span></span>

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

### <span data-ttu-id="99639-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="99639-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="99639-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99639-161">CommonParameters</span></span>
<span data-ttu-id="99639-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99639-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99639-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99639-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99639-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99639-164">INPUTS</span></span>

### <span data-ttu-id="99639-165">System.String</span><span class="sxs-lookup"><span data-stu-id="99639-165">System.String</span></span>

### <span data-ttu-id="99639-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="99639-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="99639-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99639-167">OUTPUTS</span></span>

### <span data-ttu-id="99639-168">System.Void</span><span class="sxs-lookup"><span data-stu-id="99639-168">System.Void</span></span>

## <span data-ttu-id="99639-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="99639-169">NOTES</span></span>

## <span data-ttu-id="99639-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99639-170">RELATED LINKS</span></span>

[<span data-ttu-id="99639-171">Disable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="99639-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="99639-172">Enable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="99639-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="99639-173">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="99639-173">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="99639-174">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="99639-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="99639-175">Get-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="99639-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="99639-176">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="99639-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="99639-177">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="99639-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="99639-178">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="99639-178">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
