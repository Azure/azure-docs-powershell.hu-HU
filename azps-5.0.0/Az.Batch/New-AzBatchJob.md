---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: f997c1574a81badf9d97bb4afecc104990aa725b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299699"
---
# <span data-ttu-id="41161-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41161-101">New-AzBatchJob</span></span>

## <span data-ttu-id="41161-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41161-102">SYNOPSIS</span></span>
<span data-ttu-id="41161-103">Feladatot hoz létre a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="41161-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="41161-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41161-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41161-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="41161-105">DESCRIPTION</span></span>
<span data-ttu-id="41161-106">A **New-AzBatchJob** parancsmag létrehoz egy feladatot az Azure kötegelt szolgáltatásban a *BatchAccountContext* paraméterrel megadott fiókban.</span><span class="sxs-lookup"><span data-stu-id="41161-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="41161-107">Példák</span><span class="sxs-lookup"><span data-stu-id="41161-107">EXAMPLES</span></span>

### <span data-ttu-id="41161-108">Példa 1: feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="41161-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $PoolInformation.PoolId = "Pool22"
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="41161-109">Az első parancs az New-Object parancsmag segítségével hoz létre **PSPoolInformation** -objektumokat.</span><span class="sxs-lookup"><span data-stu-id="41161-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="41161-110">A parancs az objektumot a $PoolInformation változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="41161-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="41161-111">A második parancs az azonosító Pool22 az objektum **PoolId** tulajdonságához rendeli az $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="41161-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="41161-112">A végleges parancs létrehoz egy olyan feladatot, amely az azonosító ContosoJob35 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="41161-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="41161-113">A feladathoz hozzáadott feladatok az azonosító Pool22 tartalmazó készleten futnak.</span><span class="sxs-lookup"><span data-stu-id="41161-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="41161-114">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="41161-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="41161-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41161-115">PARAMETERS</span></span>

### <span data-ttu-id="41161-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="41161-116">-BatchContext</span></span>
<span data-ttu-id="41161-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="41161-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="41161-118">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="41161-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="41161-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="41161-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="41161-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="41161-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="41161-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="41161-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="41161-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="41161-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="41161-123">A gyakori környezeti változók (kulcs/érték párok) meghatározása a projekt összes tevékenységéhez.</span><span class="sxs-lookup"><span data-stu-id="41161-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="41161-124">A kulcs a környezeti változók neve.</span><span class="sxs-lookup"><span data-stu-id="41161-124">The key is the environment variable name.</span></span>
<span data-ttu-id="41161-125">Az érték a környezeti változó értéke.</span><span class="sxs-lookup"><span data-stu-id="41161-125">The value is the environment variable value.</span></span>

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

### <span data-ttu-id="41161-126">-Kényszerek</span><span class="sxs-lookup"><span data-stu-id="41161-126">-Constraints</span></span>
<span data-ttu-id="41161-127">A projekt végrehajtási korlátozásait adja meg.</span><span class="sxs-lookup"><span data-stu-id="41161-127">Specifies the execution constraints for the job.</span></span>

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

### <span data-ttu-id="41161-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41161-128">-DefaultProfile</span></span>
<span data-ttu-id="41161-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41161-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41161-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="41161-130">-DisplayName</span></span>
<span data-ttu-id="41161-131">A feladat megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41161-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="41161-132">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="41161-132">-Id</span></span>
<span data-ttu-id="41161-133">A feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="41161-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="41161-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="41161-134">-JobManagerTask</span></span>
<span data-ttu-id="41161-135">A Feladatkezelő feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41161-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="41161-136">A kötegelt szolgáltatás a feladat indításakor a Feladatkezelő feladatot futtatja.</span><span class="sxs-lookup"><span data-stu-id="41161-136">The Batch service runs the Job Manager task when the job is started.</span></span>

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

### <span data-ttu-id="41161-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="41161-137">-JobPreparationTask</span></span>
<span data-ttu-id="41161-138">A projekt előkészületi tevékenysége.</span><span class="sxs-lookup"><span data-stu-id="41161-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="41161-139">A kötegelt szolgáltatás egy számítási csomóponton futtatja a projekt-előkészítési feladatot, mielőtt az adott feladatot a számítási csomóponton elindítja.</span><span class="sxs-lookup"><span data-stu-id="41161-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

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

### <span data-ttu-id="41161-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="41161-140">-JobReleaseTask</span></span>
<span data-ttu-id="41161-141">A projekt kiadási feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41161-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="41161-142">A kötegelt szolgáltatás a feladat befejezését követően futtatja a projekt kiadási feladatot.</span><span class="sxs-lookup"><span data-stu-id="41161-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="41161-143">A kötegelt szolgáltatás minden olyan számítási csomóponton futtatja a projekt kiadási feladatot, amely a feladat bármely tevékenységét futtatta.</span><span class="sxs-lookup"><span data-stu-id="41161-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

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

### <span data-ttu-id="41161-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="41161-144">-Metadata</span></span>
<span data-ttu-id="41161-145">A feladatba felvenni kívánt metaadatokat adja meg kulcs/érték párokként.</span><span class="sxs-lookup"><span data-stu-id="41161-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="41161-146">A kulcs a metaadat neve.</span><span class="sxs-lookup"><span data-stu-id="41161-146">The key is the metadata name.</span></span>
<span data-ttu-id="41161-147">Az érték a metaadat-érték.</span><span class="sxs-lookup"><span data-stu-id="41161-147">The value is the metadata value.</span></span>

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

### <span data-ttu-id="41161-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="41161-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="41161-149">Megadja, hogy a kötegelt szolgáltatás milyen műveletet hajtson végre, ha a feladatban szereplő összes tevékenység a befejezett állapotba kerül.</span><span class="sxs-lookup"><span data-stu-id="41161-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

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

### <span data-ttu-id="41161-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="41161-150">-OnTaskFailure</span></span>
<span data-ttu-id="41161-151">Megadja, hogy a kötegelt szolgáltatás milyen műveletet hajtson végre, ha a feladatban bármely tevékenység nem működik.</span><span class="sxs-lookup"><span data-stu-id="41161-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

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

### <span data-ttu-id="41161-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="41161-152">-PoolInformation</span></span>
<span data-ttu-id="41161-153">Annak a készletnek a részletét adja meg, amelyen a kötegelt szolgáltatás végrehajtja a feladat feladatait.</span><span class="sxs-lookup"><span data-stu-id="41161-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

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

### <span data-ttu-id="41161-154">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="41161-154">-Priority</span></span>
<span data-ttu-id="41161-155">A feladat prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="41161-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="41161-156">Az érvényes értékek:-1000-től 1000-ig terjedő egész számok.</span><span class="sxs-lookup"><span data-stu-id="41161-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="41161-157">A-1000 értéke a legalacsonyabb prioritás.</span><span class="sxs-lookup"><span data-stu-id="41161-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="41161-158">A 1000 értéke a legmagasabb prioritás.</span><span class="sxs-lookup"><span data-stu-id="41161-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="41161-159">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="41161-159">The default value is 0.</span></span>

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

### <span data-ttu-id="41161-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="41161-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="41161-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41161-161">CommonParameters</span></span>
<span data-ttu-id="41161-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41161-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41161-163">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="41161-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41161-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41161-164">INPUTS</span></span>

### <span data-ttu-id="41161-165">System. String</span><span class="sxs-lookup"><span data-stu-id="41161-165">System.String</span></span>

### <span data-ttu-id="41161-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="41161-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="41161-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41161-167">OUTPUTS</span></span>

### <span data-ttu-id="41161-168">System. Void</span><span class="sxs-lookup"><span data-stu-id="41161-168">System.Void</span></span>

## <span data-ttu-id="41161-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41161-169">NOTES</span></span>

## <span data-ttu-id="41161-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41161-170">RELATED LINKS</span></span>

[<span data-ttu-id="41161-171">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41161-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="41161-172">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41161-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="41161-173">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="41161-173">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="41161-174">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41161-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="41161-175">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="41161-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="41161-176">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41161-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="41161-177">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41161-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="41161-178">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="41161-178">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
