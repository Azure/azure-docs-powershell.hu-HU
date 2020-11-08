---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182619"
---
# <span data-ttu-id="15cb0-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="15cb0-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="15cb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="15cb0-103">Beolvassa a köteg-csomópontot tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="15cb0-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="15cb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15cb0-104">SYNTAX</span></span>

### <span data-ttu-id="15cb0-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="15cb0-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15cb0-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="15cb0-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15cb0-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="15cb0-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15cb0-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="15cb0-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15cb0-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="15cb0-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15cb0-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="15cb0-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15cb0-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="15cb0-111">DESCRIPTION</span></span>
<span data-ttu-id="15cb0-112">A **Get-AzBatchNodeFileContent** parancsmag egy Azure batch csomópontot tartalmazó fájlt kap, és fájlként vagy adatfolyamként menti.</span><span class="sxs-lookup"><span data-stu-id="15cb0-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="15cb0-113">Példák</span><span class="sxs-lookup"><span data-stu-id="15cb0-113">EXAMPLES</span></span>

### <span data-ttu-id="15cb0-114">Példa 1: egy tevékenységhez társított köteg-csomópont beszerzése és a fájl mentése</span><span class="sxs-lookup"><span data-stu-id="15cb0-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="15cb0-115">Ez a parancs beilleszti a StdOut.txt nevű csomópontot, és a helyi számítógép E:\PowerShell\StdOut.txt elérési útjára menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="15cb0-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="15cb0-116">A StdOut.txt csomópont-fájl társítva van egy olyan tevékenységhez, amelynek azonosító Task01 az azonosító Job01 tartalmazó projekthez tartozik.</span><span class="sxs-lookup"><span data-stu-id="15cb0-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="15cb0-117">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="15cb0-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="15cb0-118">2. példa: kötegfájl-fájl beszerzése és mentése a megadott fájlelérési útra a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="15cb0-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="15cb0-119">Ez a parancs a Get-AzBatchNodeFile parancsmaggal StdErr.txt nevű csomópontot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="15cb0-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="15cb0-120">A parancs átadja a fájlt az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="15cb0-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="15cb0-121">Az aktuális parancsmag a fájlt a helyi számítógép E:\PowerShell\StdOut.txt fájlelérési útjára menti.</span><span class="sxs-lookup"><span data-stu-id="15cb0-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="15cb0-122">A StdOut.txt csomópont-fájl társítva van azzal a tevékenységgel, amelynek azonosító Task02 az azonosító Job02 tartalmazó projekthez tartozik.</span><span class="sxs-lookup"><span data-stu-id="15cb0-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="15cb0-123">3. példa: egy tevékenységhez társított köteg-csomópont beszerzése és az adatfolyamhoz irányítása</span><span class="sxs-lookup"><span data-stu-id="15cb0-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="15cb0-124">Az első parancs az New-Object parancsmag segítségével hoz létre adatfolyamot, és a $Stream változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="15cb0-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="15cb0-125">A második parancs beolvassa az StdOut.txt nevű csomópontot az azonosítót tartalmazó Task11 az azonosító Job03 tartalmazó feladathoz.</span><span class="sxs-lookup"><span data-stu-id="15cb0-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="15cb0-126">A parancs a fájl tartalmát az adatfolyamra irányítja a $Streamban.</span><span class="sxs-lookup"><span data-stu-id="15cb0-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="15cb0-127">Példa 4: node-fájl beszerzése egy számítási csomópontról és mentése</span><span class="sxs-lookup"><span data-stu-id="15cb0-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="15cb0-128">Ez a parancs a csomópontot Startup\StdOut.txt a számítási csomópontról, amelynek azonosító ComputeNode01 az azonosító Pool01 tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="15cb0-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="15cb0-129">A parancs a fájlt a helyi számítógép E:\PowerShell\StdOut.txt fájlelérési útjára menti.</span><span class="sxs-lookup"><span data-stu-id="15cb0-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="15cb0-130">Példa 5: csomópont kinyerése a számítási csomópontból, és mentése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="15cb0-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="15cb0-131">Ez a parancs a csomópont-fájlt Startup\StdOut.txt Get-AzBatchNodeFile segítségével az ID ComputeNode01 tartalmazó számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="15cb0-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="15cb0-132">A számítási csomópont abban a készletben található, amely az azonosító Pool01 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="15cb0-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="15cb0-133">A parancs átadja ezt a csomópont-fájlt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="15cb0-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="15cb0-134">Ez a parancsmag a fájlt a helyi számítógép E:\PowerShell\StdOut.txt fájlelérési útjára menti.</span><span class="sxs-lookup"><span data-stu-id="15cb0-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="15cb0-135">Példa 6: a csomópontok kinyerése a számítási csomópontból és az adatfolyamhoz való közvetlen átvétele</span><span class="sxs-lookup"><span data-stu-id="15cb0-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="15cb0-136">Az első parancs az New-Object parancsmag segítségével hoz létre adatfolyamot, és a $Stream változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="15cb0-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="15cb0-137">A második parancs beolvassa az StdOut.txt nevű csomópontot a számítási csomópontról, amelynek azonosító ComputeNode01 az azonosító Pool01 tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="15cb0-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="15cb0-138">A parancs a fájl tartalmát az adatfolyamra irányítja a $Streamban.</span><span class="sxs-lookup"><span data-stu-id="15cb0-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="15cb0-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15cb0-139">PARAMETERS</span></span>

### <span data-ttu-id="15cb0-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="15cb0-140">-BatchContext</span></span>
<span data-ttu-id="15cb0-141">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="15cb0-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="15cb0-142">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="15cb0-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="15cb0-143">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="15cb0-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="15cb0-144">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="15cb0-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="15cb0-145">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="15cb0-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="15cb0-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="15cb0-146">-ByteRangeEnd</span></span>
<span data-ttu-id="15cb0-147">A letöltendő bájtok hatókörének vége.</span><span class="sxs-lookup"><span data-stu-id="15cb0-147">The end of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15cb0-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="15cb0-148">-ByteRangeStart</span></span>
<span data-ttu-id="15cb0-149">A letöltendő bájtok hatókörének kezdete.</span><span class="sxs-lookup"><span data-stu-id="15cb0-149">The start of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15cb0-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="15cb0-150">-ComputeNodeId</span></span>
<span data-ttu-id="15cb0-151">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amely a parancsmag által megadott csomópont-fájlt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="15cb0-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15cb0-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15cb0-152">-DefaultProfile</span></span>
<span data-ttu-id="15cb0-153">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15cb0-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15cb0-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="15cb0-154">-DestinationPath</span></span>
<span data-ttu-id="15cb0-155">Annak a fájlnak az elérési útját adja meg, ahol ez a parancsmag menti a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="15cb0-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15cb0-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="15cb0-156">-DestinationStream</span></span>
<span data-ttu-id="15cb0-157">Azt a adatfolyamot adja meg, amelybe ez a parancsmag a csomópont-fájl tartalmát írja be.</span><span class="sxs-lookup"><span data-stu-id="15cb0-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="15cb0-158">Ez a parancsmag nem zárja be vagy hagyja vissza az adatfolyamot.</span><span class="sxs-lookup"><span data-stu-id="15cb0-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15cb0-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15cb0-159">-InputObject</span></span>
<span data-ttu-id="15cb0-160">Azt a fájlt adja meg, amelyet a parancsmag **PSNodeFile** objektumként kap.</span><span class="sxs-lookup"><span data-stu-id="15cb0-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="15cb0-161">A Node file objektum beolvasásához használja az Get-AzBatchNodeFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="15cb0-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15cb0-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="15cb0-162">-JobId</span></span>
<span data-ttu-id="15cb0-163">Annak a feladatnak az AZONOSÍTÓját adja meg, amely a célként megadott feladatot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="15cb0-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15cb0-164">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="15cb0-164">-Path</span></span>
<span data-ttu-id="15cb0-165">A letöltendő csomópont elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="15cb0-165">The path of the node file to download.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15cb0-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="15cb0-166">-PoolId</span></span>
<span data-ttu-id="15cb0-167">Annak a készletnek az AZONOSÍTÓját adja meg, amely a parancsmagot tartalmazó csomópontot tartalmazó csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="15cb0-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15cb0-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="15cb0-168">-TaskId</span></span>
<span data-ttu-id="15cb0-169">A tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="15cb0-169">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15cb0-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15cb0-170">CommonParameters</span></span>
<span data-ttu-id="15cb0-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15cb0-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15cb0-172">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="15cb0-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15cb0-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15cb0-173">INPUTS</span></span>

### <span data-ttu-id="15cb0-174">System. String</span><span class="sxs-lookup"><span data-stu-id="15cb0-174">System.String</span></span>

### <span data-ttu-id="15cb0-175">Microsoft.Azure.Commands.BatCH. Modellek. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="15cb0-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="15cb0-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="15cb0-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="15cb0-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15cb0-177">OUTPUTS</span></span>

### <span data-ttu-id="15cb0-178">System. Void</span><span class="sxs-lookup"><span data-stu-id="15cb0-178">System.Void</span></span>

## <span data-ttu-id="15cb0-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15cb0-179">NOTES</span></span>

## <span data-ttu-id="15cb0-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15cb0-180">RELATED LINKS</span></span>

[<span data-ttu-id="15cb0-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="15cb0-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="15cb0-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="15cb0-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="15cb0-183">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="15cb0-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
