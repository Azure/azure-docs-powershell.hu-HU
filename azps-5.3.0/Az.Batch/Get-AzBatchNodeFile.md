---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: db8ef62a158edaa3a697af9f77e7932dfa18c096
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478349"
---
# <span data-ttu-id="2a3f3-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="2a3f3-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="2a3f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3f3-103">A Batch-csomópontfájlok tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="2a3f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2a3f3-104">SYNTAX</span></span>

### <span data-ttu-id="2a3f3-105">ComputeNode_Id (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a3f3-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3f3-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="2a3f3-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3f3-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="2a3f3-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3f3-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="2a3f3-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3f3-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="2a3f3-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a3f3-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="2a3f3-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a3f3-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2a3f3-111">DESCRIPTION</span></span>
<span data-ttu-id="2a3f3-112">A **Get-AzBatchNodeFile** parancsmag begyűjte egy feladat vagy számítási csomópont Azure Batch-csomópontfájljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="2a3f3-113">Az eredmények szűkítéséhez OData-szűrőt is megadhat.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="2a3f3-114">Ha egy feladatot ad meg, szűrőt azonban nem, ez a parancsmag az adott feladat összes csomópontfájljának tulajdonságait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="2a3f3-115">Ha egy számítási csomópontot ad meg, szűrőt azonban nem, ez a parancsmag az adott számítási csomópont összes csomópontfájljának tulajdonságait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="2a3f3-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2a3f3-116">EXAMPLES</span></span>

### <span data-ttu-id="2a3f3-117">1. példa: A feladathoz társított csomópontfájl tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="2a3f3-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="2a3f3-118">Ez a parancs annak a StdOut.txt csomópontfájlnak a tulajdonságait kapja meg, amely a Feladat26 azonosítót tartalmazza a 000001 azonosítójú feladatban.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="2a3f3-119">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-119">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2a3f3-120">2. példa: A feladathoz társított csomópontfájlok tulajdonságainak lekérte egy szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="2a3f3-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="2a3f3-121">Ez a parancs azoknak a csomópontfájloknak a tulajdonságait kapja meg, amelyeknek a neve st-nek kezdődik, és olyan feladathoz van társítva, amelynek feladatazonosítója Feladat26 azonosítót tartalmaz 00002-es azonosítójú feladat alatt.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="2a3f3-122">3. példa: A feladathoz társított csomópontfájlok tulajdonságainak rekurzív be szerezze</span><span class="sxs-lookup"><span data-stu-id="2a3f3-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
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

<span data-ttu-id="2a3f3-123">Ez a parancs a Feladat 00003-as feladatban lévő Feladat31 azonosítóval társított feladathoz társított összes fájl tulajdonságait beveszi.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="2a3f3-124">Ez a parancs a *rekurzív paramétert adja* meg.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="2a3f3-125">Ezért a parancsmag rekurzív fájlkeresést hajt végre, és visszaadja a wd\newFile.txt csomópontfájlt.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="2a3f3-126">4. példa: Egyetlen fájl lekérte egy számítási csomópontból</span><span class="sxs-lookup"><span data-stu-id="2a3f3-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="2a3f3-127">Ez a parancs a Startup\StdOut.txt az id ComputeNode01 azonosítóval rendelkezik a készletben, amely az azonosítókészletet22 tartalmazza, a számítási csomópontból kapja meg a Startup\StdOut.txt nevű fájlt.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="2a3f3-128">5. példa: Az összes fájl bekérte egy mappa alá egy számítási csomópontból</span><span class="sxs-lookup"><span data-stu-id="2a3f3-128">Example 5: Get all files under a folder from a compute node</span></span>
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

<span data-ttu-id="2a3f3-129">Ez a parancs az indítómappa alatt található összes fájlt abból a számítási csomópontból kapja meg, amelynél a ComputeNode01 azonosító található az azonosítókészletet tartalmazó készletben22.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="2a3f3-130">Ez a parancsmag megadja a *rekurzív* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="2a3f3-131">6. példa: Fájlok letöltése egy számítási csomópont gyökérmappába</span><span class="sxs-lookup"><span data-stu-id="2a3f3-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso...
True        startup                         https://cmdletexample.westus.Batch.contoso...
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="2a3f3-132">Ez a parancs annak a számítási csomópontnak a gyökérmappában lévő összes fájlt begyakorlja, amelynél a ComputeNode01 azonosító található az azonosítókészletet tartalmazó készletben22.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="2a3f3-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a3f3-133">PARAMETERS</span></span>

### <span data-ttu-id="2a3f3-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2a3f3-134">-BatchContext</span></span>
<span data-ttu-id="2a3f3-135">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2a3f3-136">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2a3f3-137">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-137">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2a3f3-138">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2a3f3-139">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2a3f3-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="2a3f3-140">-ComputeNode</span></span>
<span data-ttu-id="2a3f3-141">A Batch csomópontfájlokat tartalmazó számítási csomópontOT adja meg **PSComputeNode-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="2a3f3-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="2a3f3-142">Számítási csomópontobjektum beszerzéséhez használja a Get-AzBatchComputeNode parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="2a3f3-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="2a3f3-143">-ComputeNodeId</span></span>
<span data-ttu-id="2a3f3-144">A Batch csomópontfájlokat tartalmazó számítási csomópont azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

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

### <span data-ttu-id="2a3f3-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a3f3-145">-DefaultProfile</span></span>
<span data-ttu-id="2a3f3-146">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a3f3-147">-Filter</span><span class="sxs-lookup"><span data-stu-id="2a3f3-147">-Filter</span></span>
<span data-ttu-id="2a3f3-148">OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="2a3f3-149">Ez a parancsmag a paraméter által megadott szűrőnek megfelelő csomópontfájlok tulajdonságait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a3f3-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="2a3f3-150">-JobId</span></span>
<span data-ttu-id="2a3f3-151">A cél tevékenységet tartalmazó feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-151">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="2a3f3-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2a3f3-152">-MaxCount</span></span>
<span data-ttu-id="2a3f3-153">Azt adja meg, hogy legfeljebb hány csomópontfájlt ad vissza a parancsmag.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="2a3f3-154">Ha nullát (0) vagy kisebb értéket ad meg, a parancsmag nem használ felső korlátot.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="2a3f3-155">Az alapértelmezett érték 1000.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-155">The default value is 1000.</span></span>

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

### <span data-ttu-id="2a3f3-156">-Path</span><span class="sxs-lookup"><span data-stu-id="2a3f3-156">-Path</span></span>
<span data-ttu-id="2a3f3-157">Annak a csomópontfájlnak az elérési útját adja meg, amelynek tulajdonságait a parancsmag beolvassa.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="2a3f3-158">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-158">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="2a3f3-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="2a3f3-159">-PoolId</span></span>
<span data-ttu-id="2a3f3-160">Annak a készletnek az azonosítóját adja meg, amely azt a számítási csomópontot tartalmazza, amelyből a csomópontfájlok tulajdonságait meg szeretné kapni.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

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

### <span data-ttu-id="2a3f3-161">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="2a3f3-161">-Recursive</span></span>
<span data-ttu-id="2a3f3-162">Azt jelzi, hogy ez a parancsmag egy rekurzív fájllistát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="2a3f3-163">Ellenkező esetben csak a gyökérmappában lévő fájlokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-163">Otherwise, it returns only the files in the root folder.</span></span>

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

### <span data-ttu-id="2a3f3-164">-Task</span><span class="sxs-lookup"><span data-stu-id="2a3f3-164">-Task</span></span>
<span data-ttu-id="2a3f3-165">Azt a feladatot adja meg **PSCloudTask-objektumként,** amellyel a csomópontfájlok társítva vannak.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="2a3f3-166">Feladatobjektum beszerzéséhez használja a Get-AzBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="2a3f3-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="2a3f3-167">-TaskId</span></span>
<span data-ttu-id="2a3f3-168">Annak a feladatnak az azonosítója, amelynek a parancsmagja a csomópontfájlok tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

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

### <span data-ttu-id="2a3f3-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3f3-169">CommonParameters</span></span>
<span data-ttu-id="2a3f3-170">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a3f3-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3f3-171">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a3f3-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3f3-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a3f3-172">INPUTS</span></span>

### <span data-ttu-id="2a3f3-173">System.String</span><span class="sxs-lookup"><span data-stu-id="2a3f3-173">System.String</span></span>

### <span data-ttu-id="2a3f3-174">Microsoft.Azure.Commands.Bat. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="2a3f3-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="2a3f3-175">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="2a3f3-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="2a3f3-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2a3f3-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2a3f3-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a3f3-177">OUTPUTS</span></span>

### <span data-ttu-id="2a3f3-178">Microsoft.Azure.Commands.Bat. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="2a3f3-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="2a3f3-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2a3f3-179">NOTES</span></span>

## <span data-ttu-id="2a3f3-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a3f3-180">RELATED LINKS</span></span>

[<span data-ttu-id="2a3f3-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2a3f3-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2a3f3-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="2a3f3-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="2a3f3-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="2a3f3-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="2a3f3-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2a3f3-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="2a3f3-185">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="2a3f3-185">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
