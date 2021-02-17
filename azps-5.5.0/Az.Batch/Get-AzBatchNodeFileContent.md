---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205271"
---
# <span data-ttu-id="64236-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="64236-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="64236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64236-102">SYNOPSIS</span></span>
<span data-ttu-id="64236-103">Egy Batch-csomópontfájlt kap.</span><span class="sxs-lookup"><span data-stu-id="64236-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="64236-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64236-104">SYNTAX</span></span>

### <span data-ttu-id="64236-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="64236-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64236-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="64236-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64236-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="64236-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64236-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="64236-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64236-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="64236-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64236-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="64236-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64236-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64236-111">DESCRIPTION</span></span>
<span data-ttu-id="64236-112">A **Get-AzBatchNodeFileContent** parancsmag egy Azure Batch-csomópontfájlt kap, és fájlként vagy adatfolyamként menti azt.</span><span class="sxs-lookup"><span data-stu-id="64236-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="64236-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64236-113">EXAMPLES</span></span>

### <span data-ttu-id="64236-114">1. példa: Egy feladathoz társított Batch-csomópontfájl lekérte és a fájl mentése</span><span class="sxs-lookup"><span data-stu-id="64236-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="64236-115">Ez a parancs lekérte a StdOut.txt nevű csomópontfájlt, és a helyi E:\PowerShell\StdOut.txt elérési útba menti.</span><span class="sxs-lookup"><span data-stu-id="64236-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="64236-116">A StdOut.txt csomópontfájl olyan feladathoz van társítva, amely a Feladat01 azonosítót tartalmazza a Job01 azonosítójú feladathoz.</span><span class="sxs-lookup"><span data-stu-id="64236-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="64236-117">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="64236-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="64236-118">2. példa: Egy Batch-csomópontfájl lekérte és egy megadott elérési útba mentheti a folyamattal</span><span class="sxs-lookup"><span data-stu-id="64236-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="64236-119">Ez a parancs a StdErr.txt parancsmag használatával kapja meg a Get-AzBatchNodeFile csomópontfájlt.</span><span class="sxs-lookup"><span data-stu-id="64236-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="64236-120">A parancs a folyamat műveleti operátorával átadja a fájlt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="64236-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="64236-121">Az aktuális parancsmag a fájlt a helyi E:\PowerShell\StdOut.txt elérési útba menti.</span><span class="sxs-lookup"><span data-stu-id="64236-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="64236-122">A StdOut.txt a csomópontfájl azzal a feladattal van társítva, amely a Feladatazonosító 2 azonosítóval rendelkezik a Job02 azonosítójú feladathoz.</span><span class="sxs-lookup"><span data-stu-id="64236-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="64236-123">3. példa: Egy feladathoz társított Batch-csomópontfájl lekérte és adatfolyamba irányította</span><span class="sxs-lookup"><span data-stu-id="64236-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="64236-124">Az első parancs egy adatfolyamot hoz létre a New-Object parancsmag használatával, majd a $Stream tárolja.</span><span class="sxs-lookup"><span data-stu-id="64236-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="64236-125">A második parancs lekérte a StdOut.txt nevű csomópontfájlt abból a feladatból, amely a Feladatazonosító 11 azonosítóval rendelkezik a Job03 azonosítójú feladathoz.</span><span class="sxs-lookup"><span data-stu-id="64236-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="64236-126">A parancs a fájlok tartalmát a $Stream.</span><span class="sxs-lookup"><span data-stu-id="64236-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="64236-127">4. példa: Csomópontfájl lekérte és mentve egy számítási csomópontból</span><span class="sxs-lookup"><span data-stu-id="64236-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="64236-128">Ez a parancs lekérte a Startup\StdOut.txt abból a számítási csomópontból, amelynél a ComputeNode01 azonosító található az id Pool01 készletben.</span><span class="sxs-lookup"><span data-stu-id="64236-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="64236-129">A parancs a fájlt a helyi E:\PowerShell\StdOut.txt elérési útba menti.</span><span class="sxs-lookup"><span data-stu-id="64236-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="64236-130">5. példa: Csomópontfájl létrehozása egy számítási csomópontból, és mentése a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="64236-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="64236-131">Ez a parancs a csomópontfájlt Startup\StdOut.txt a ComputeNode01 azonosítóval Get-AzBatchNodeFile csomópontból származó Get-AzBatchNodeFile használatával.</span><span class="sxs-lookup"><span data-stu-id="64236-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="64236-132">A számítási csomópont abban a készletben található, amely az ID Pool01 azonosítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="64236-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="64236-133">A parancs átadja a csomópontfájlt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="64236-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="64236-134">Ez a parancsmag a fájlt a helyi E:\PowerShell\StdOut.txt elérési útba menti.</span><span class="sxs-lookup"><span data-stu-id="64236-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="64236-135">6. példa: Csomópontfájl lekérte egy számítási csomópontról, és adatfolyamba irányította</span><span class="sxs-lookup"><span data-stu-id="64236-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="64236-136">Az első parancs egy adatfolyamot hoz létre a New-Object parancsmag használatával, majd a $Stream tárolja.</span><span class="sxs-lookup"><span data-stu-id="64236-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="64236-137">A második parancs lekérte a StdOut.txt nevű csomópontfájlt abból a számítási csomópontból, amelynél az ID ComputeNode01 azonosító található a készletben, amely az ID Pool01 azonosítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="64236-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="64236-138">A parancs a fájlok tartalmát a $Stream.</span><span class="sxs-lookup"><span data-stu-id="64236-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="64236-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64236-139">PARAMETERS</span></span>

### <span data-ttu-id="64236-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="64236-140">-BatchContext</span></span>
<span data-ttu-id="64236-141">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="64236-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="64236-142">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="64236-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="64236-143">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot, és töltse ki a hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="64236-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="64236-144">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="64236-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="64236-145">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="64236-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="64236-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="64236-146">-ByteRangeEnd</span></span>
<span data-ttu-id="64236-147">A letöltendő bájttartomány vége.</span><span class="sxs-lookup"><span data-stu-id="64236-147">The end of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="64236-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="64236-148">-ByteRangeStart</span></span>
<span data-ttu-id="64236-149">A letöltendő bájttartomány kezdete.</span><span class="sxs-lookup"><span data-stu-id="64236-149">The start of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="64236-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="64236-150">-ComputeNodeId</span></span>
<span data-ttu-id="64236-151">Annak a számítási csomópontnak az azonosítója, amely a parancsmag által visszaadott csomópontfájlt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="64236-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="64236-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64236-152">-DefaultProfile</span></span>
<span data-ttu-id="64236-153">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64236-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64236-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="64236-154">-DestinationPath</span></span>
<span data-ttu-id="64236-155">Megadja azt a fájl elérési útját, ahová a parancsmag menti a csomópontfájlt.</span><span class="sxs-lookup"><span data-stu-id="64236-155">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="64236-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="64236-156">-DestinationStream</span></span>
<span data-ttu-id="64236-157">Azt az adatfolyamot adja meg, amelybe ez a parancsmag beírja a csomópontfájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="64236-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="64236-158">Ez a parancsmag nem zárja be és nem tekeri vissza az adatfolyamot.</span><span class="sxs-lookup"><span data-stu-id="64236-158">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="64236-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64236-159">-InputObject</span></span>
<span data-ttu-id="64236-160">A parancsmag ÁLTAL **PSNodeFile-objektumként begyakorolható** fájl.</span><span class="sxs-lookup"><span data-stu-id="64236-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="64236-161">Csomópontfájl-objektum beszerzéséhez használja a Get-AzBatchNodeFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="64236-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="64236-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="64236-162">-JobId</span></span>
<span data-ttu-id="64236-163">A cél tevékenységet tartalmazó feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64236-163">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="64236-164">-Path</span><span class="sxs-lookup"><span data-stu-id="64236-164">-Path</span></span>
<span data-ttu-id="64236-165">A letölteni kívánt csomópontfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="64236-165">The path of the node file to download.</span></span>

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

### <span data-ttu-id="64236-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="64236-166">-PoolId</span></span>
<span data-ttu-id="64236-167">Annak a készletnek az azonosítója, amely a parancsmag által begyakorolt csomópontfájlt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="64236-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="64236-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="64236-168">-TaskId</span></span>
<span data-ttu-id="64236-169">A tevékenység azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64236-169">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="64236-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64236-170">CommonParameters</span></span>
<span data-ttu-id="64236-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64236-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64236-172">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64236-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64236-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64236-173">INPUTS</span></span>

### <span data-ttu-id="64236-174">System.String</span><span class="sxs-lookup"><span data-stu-id="64236-174">System.String</span></span>

### <span data-ttu-id="64236-175">Microsoft.Azure.Commands.Bat. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="64236-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="64236-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="64236-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="64236-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64236-177">OUTPUTS</span></span>

### <span data-ttu-id="64236-178">System.Void</span><span class="sxs-lookup"><span data-stu-id="64236-178">System.Void</span></span>

## <span data-ttu-id="64236-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64236-179">NOTES</span></span>

## <span data-ttu-id="64236-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64236-180">RELATED LINKS</span></span>

[<span data-ttu-id="64236-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="64236-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="64236-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="64236-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="64236-183">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="64236-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
