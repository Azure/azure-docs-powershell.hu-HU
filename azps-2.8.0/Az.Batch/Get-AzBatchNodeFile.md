---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: 3337cfa2423d6bc3a26c96ea734ce517f2707a04
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847917"
---
# <span data-ttu-id="e356e-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="e356e-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="e356e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e356e-102">SYNOPSIS</span></span>
<span data-ttu-id="e356e-103">A kötegfájl-fájlok tulajdonságainak lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="e356e-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="e356e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e356e-104">SYNTAX</span></span>

### <span data-ttu-id="e356e-105">ComputeNode_Id (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e356e-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e356e-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="e356e-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e356e-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="e356e-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e356e-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="e356e-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e356e-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="e356e-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e356e-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="e356e-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e356e-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="e356e-111">DESCRIPTION</span></span>
<span data-ttu-id="e356e-112">A **Get-AzBatchNodeFile** parancsmag a tevékenység vagy a számítási csomópont Azure batch csomópont-fájljainak tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e356e-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="e356e-113">Ha szűkíteni szeretné az eredményeket, megadhat egy Open Data Protocol (OData) szűrőt.</span><span class="sxs-lookup"><span data-stu-id="e356e-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="e356e-114">Ha olyan tevékenységet ad meg, amely nem szűrő, akkor ez a parancsmag a tevékenységhez tartozó összes csomópont-fájl tulajdonságait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e356e-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="e356e-115">Ha olyan számítási csomópontot ad meg, amely nem szűrő, akkor ez a parancsmag a számítási csomópont összes csomópont-fájljának tulajdonságait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e356e-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="e356e-116">Példák</span><span class="sxs-lookup"><span data-stu-id="e356e-116">EXAMPLES</span></span>

### <span data-ttu-id="e356e-117">Példa 1: a tevékenységhez társított csomópont-fájl tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="e356e-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="e356e-118">Ez a parancs beolvassa a tevékenységhez társított StdOut.txt csomópont-fájl tulajdonságait, amely a Task26 azonosítóval rendelkezik – 000001.</span><span class="sxs-lookup"><span data-stu-id="e356e-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e356e-119">A Get-AzBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="e356e-119">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e356e-120">2. példa: a tevékenységhez társított csomópont-fájlok tulajdonságainak lekérdezése szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="e356e-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="e356e-121">Ez a parancs beolvassa a St-val kezdődő csomópontok tulajdonságait, és társítva van egy olyan feladathoz, amely a Task26-00002 azonosítójú projekthez tartozik.</span><span class="sxs-lookup"><span data-stu-id="e356e-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="e356e-122">3. példa: egy tevékenységhez társított csomópont-fájlok tulajdonságainak rekurzív beolvasása</span><span class="sxs-lookup"><span data-stu-id="e356e-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="e356e-123">Ez a parancs beolvassa a tevékenységhez társított összes fájl tulajdonságait a Job Job-00003 AZONOSÍTÓJÚ Task31.</span><span class="sxs-lookup"><span data-stu-id="e356e-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="e356e-124">Ez a parancs a *rekurzív* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="e356e-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="e356e-125">A parancsmag ezért végrehajt egy rekurzív fájlok keresését, és a wd\newFile.txt csomópontot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e356e-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="e356e-126">Példa 4: egyetlen fájl beszerzése egy számítási csomópontból</span><span class="sxs-lookup"><span data-stu-id="e356e-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="e356e-127">Ez a parancs beilleszti az Startup\StdOut.txt nevű fájlt a számítási csomópontról, amelynek azonosító ComputeNode01 az azonosító Pool22 tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="e356e-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="e356e-128">5. példa: a mappa alatti fájlok beolvasása egy számítási csomópontból</span><span class="sxs-lookup"><span data-stu-id="e356e-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="e356e-129">Ez a parancs beilleszti az indítási mappa alatti összes fájlt a számítási csomópontból, amely az id-Pool22 tartalmazó készlet ComputeNode01 rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="e356e-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="e356e-130">Ez a parancsmag a *rekurzív* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="e356e-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="e356e-131">6. példa: fájlok beolvasása a számítási csomópont gyökérkönyvtárába</span><span class="sxs-lookup"><span data-stu-id="e356e-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="e356e-132">Ez a parancs beolvassa a számítási csomópont gyökerének minden fájlját, amely az id-Pool22 tartalmazó készlet ComputeNode01 rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="e356e-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="e356e-133">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e356e-133">PARAMETERS</span></span>

### <span data-ttu-id="e356e-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e356e-134">-BatchContext</span></span>
<span data-ttu-id="e356e-135">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="e356e-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e356e-136">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="e356e-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e356e-137">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="e356e-137">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e356e-138">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="e356e-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e356e-139">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="e356e-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e356e-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="e356e-140">-ComputeNode</span></span>
<span data-ttu-id="e356e-141">A **PSComputeNode** -objektum számítási csomópontját adja meg, amely a köteg csomópont-fájlokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e356e-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="e356e-142">A számítási csomópont objektum beolvasásához használja az Get-AzBatchComputeNode parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e356e-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentComputeNode
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e356e-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="e356e-143">-ComputeNodeId</span></span>
<span data-ttu-id="e356e-144">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amely a köteg csomópont-fájlokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e356e-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e356e-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e356e-145">-DefaultProfile</span></span>
<span data-ttu-id="e356e-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e356e-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e356e-147">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="e356e-147">-Filter</span></span>
<span data-ttu-id="e356e-148">Egy OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e356e-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="e356e-149">Ez a parancsmag azokat a csomópont-fájlokat adja meg, amelyek megfelelnek a paraméter által megadott szűrőnek.</span><span class="sxs-lookup"><span data-stu-id="e356e-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e356e-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="e356e-150">-JobId</span></span>
<span data-ttu-id="e356e-151">Annak a feladatnak az AZONOSÍTÓját adja meg, amely a célként megadott feladatot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e356e-151">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e356e-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e356e-152">-MaxCount</span></span>
<span data-ttu-id="e356e-153">Annak a csomópontnak a maximális számát adja meg, amelyre a parancsmag tulajdonságot ad.</span><span class="sxs-lookup"><span data-stu-id="e356e-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="e356e-154">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="e356e-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="e356e-155">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="e356e-155">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e356e-156">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="e356e-156">-Path</span></span>
<span data-ttu-id="e356e-157">Annak a csomópontnak az elérési útját adja meg, amelynek a parancsmagja a tulajdonságokat lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="e356e-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="e356e-158">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="e356e-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e356e-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e356e-159">-PoolId</span></span>
<span data-ttu-id="e356e-160">Annak a készletnek az AZONOSÍTÓját adja meg, amely a csomópont-fájlok tulajdonságainak beolvasására szolgáló számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e356e-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e356e-161">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="e356e-161">-Recursive</span></span>
<span data-ttu-id="e356e-162">Azt jelzi, hogy ez a parancsmag a fájlok rekurzív listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e356e-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="e356e-163">Ellenkező esetben csak a gyökérmappa fájljait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e356e-163">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e356e-164">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="e356e-164">-Task</span></span>
<span data-ttu-id="e356e-165">Azt a feladatot adja meg **PSCloudTask** objektumként, amellyel a csomópontok fájljait társította.</span><span class="sxs-lookup"><span data-stu-id="e356e-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="e356e-166">Tevékenység-objektum beolvasásához használja az Get-AzBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e356e-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentTask
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e356e-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="e356e-167">-TaskId</span></span>
<span data-ttu-id="e356e-168">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag a csomópont-fájlok tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="e356e-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e356e-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e356e-169">CommonParameters</span></span>
<span data-ttu-id="e356e-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e356e-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e356e-171">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e356e-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e356e-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e356e-172">INPUTS</span></span>

### <span data-ttu-id="e356e-173">System. String</span><span class="sxs-lookup"><span data-stu-id="e356e-173">System.String</span></span>

### <span data-ttu-id="e356e-174">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="e356e-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="e356e-175">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="e356e-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="e356e-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e356e-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e356e-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e356e-177">OUTPUTS</span></span>

### <span data-ttu-id="e356e-178">Microsoft.Azure.Commands.BatCH. Modellek. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="e356e-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="e356e-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e356e-179">NOTES</span></span>

## <span data-ttu-id="e356e-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e356e-180">RELATED LINKS</span></span>

[<span data-ttu-id="e356e-181">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e356e-181">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e356e-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e356e-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="e356e-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="e356e-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="e356e-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e356e-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="e356e-185">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e356e-185">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


