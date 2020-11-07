---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 92c485a743372eff7ddb8725172ac4d9bb030d22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679795"
---
# <span data-ttu-id="0b838-101">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="0b838-101">Get-AzureBatchNodeFileContent</span></span>

## <span data-ttu-id="0b838-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b838-102">SYNOPSIS</span></span>
<span data-ttu-id="0b838-103">Beolvassa a köteg-csomópontot tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="0b838-103">Gets a Batch node file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b838-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b838-104">SYNTAX</span></span>

### <span data-ttu-id="0b838-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="0b838-105">Task_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b838-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="0b838-106">Task_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b838-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="0b838-107">ComputeNode_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b838-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="0b838-108">ComputeNode_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b838-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="0b838-109">InputObject_Path</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b838-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="0b838-110">InputObject_Stream</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b838-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b838-111">DESCRIPTION</span></span>
<span data-ttu-id="0b838-112">A **Get-AzureBatchNodeFileContent** parancsmag egy Azure batch csomópontot tartalmazó fájlt kap, és fájlként vagy adatfolyamként menti.</span><span class="sxs-lookup"><span data-stu-id="0b838-112">The **Get-AzureBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="0b838-113">Példák</span><span class="sxs-lookup"><span data-stu-id="0b838-113">EXAMPLES</span></span>

### <span data-ttu-id="0b838-114">Példa 1: egy tevékenységhez társított köteg-csomópont beszerzése és a fájl mentése</span><span class="sxs-lookup"><span data-stu-id="0b838-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Name "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="0b838-115">Ez a parancs beilleszti a StdOut.txt nevű csomópontot, és a helyi számítógép E:\PowerShell\StdOut.txt elérési útjára menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="0b838-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="0b838-116">A StdOut.txt csomópont-fájl társítva van egy olyan tevékenységhez, amelynek azonosító Task01 az azonosító Job01 tartalmazó projekthez tartozik.</span><span class="sxs-lookup"><span data-stu-id="0b838-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="0b838-117">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="0b838-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0b838-118">2. példa: kötegfájl-fájl beszerzése és mentése a megadott fájlelérési útra a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="0b838-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Name "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="0b838-119">Ez a parancs a Get-AzureBatchNodeFile parancsmaggal StdErr.txt nevű csomópontot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0b838-119">This command gets the node file that is named StdErr.txt by using the Get-AzureBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="0b838-120">A parancs átadja a fájlt az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="0b838-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0b838-121">Az aktuális parancsmag a fájlt a helyi számítógép E:\PowerShell\StdOut.txt fájlelérési útjára menti.</span><span class="sxs-lookup"><span data-stu-id="0b838-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="0b838-122">A StdOut.txt csomópont-fájl társítva van azzal a tevékenységgel, amelynek azonosító Task02 az azonosító Job02 tartalmazó projekthez tartozik.</span><span class="sxs-lookup"><span data-stu-id="0b838-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="0b838-123">3. példa: egy tevékenységhez társított köteg-csomópont beszerzése és az adatfolyamhoz irányítása</span><span class="sxs-lookup"><span data-stu-id="0b838-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Name "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="0b838-124">Az első parancs az New-Object parancsmag segítségével hoz létre adatfolyamot, és a $Stream változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0b838-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="0b838-125">A második parancs beolvassa az StdOut.txt nevű csomópontot az azonosítót tartalmazó Task11 az azonosító Job03 tartalmazó feladathoz.</span><span class="sxs-lookup"><span data-stu-id="0b838-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="0b838-126">A parancs a fájl tartalmát az adatfolyamra irányítja a $Streamban.</span><span class="sxs-lookup"><span data-stu-id="0b838-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="0b838-127">Példa 4: node-fájl beszerzése egy számítási csomópontról és mentése</span><span class="sxs-lookup"><span data-stu-id="0b838-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="0b838-128">Ez a parancs a csomópontot Startup\StdOut.txt a számítási csomópontról, amelynek azonosító ComputeNode01 az azonosító Pool01 tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="0b838-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="0b838-129">A parancs a fájlt a helyi számítógép E:\PowerShell\StdOut.txt fájlelérési útjára menti.</span><span class="sxs-lookup"><span data-stu-id="0b838-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="0b838-130">Példa 5: csomópont kinyerése a számítási csomópontból, és mentése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="0b838-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="0b838-131">Ez a parancs a csomópont-fájlt Startup\StdOut.txt Get-AzureBatchNodeFile segítségével az ID ComputeNode01 tartalmazó számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="0b838-131">This command gets the node file Startup\StdOut.txt by using Get-AzureBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="0b838-132">A számítási csomópont abban a készletben található, amely az azonosító Pool01 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0b838-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="0b838-133">A parancs átadja ezt a csomópont-fájlt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="0b838-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="0b838-134">Ez a parancsmag a fájlt a helyi számítógép E:\PowerShell\StdOut.txt fájlelérési útjára menti.</span><span class="sxs-lookup"><span data-stu-id="0b838-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="0b838-135">Példa 6: a csomópontok kinyerése a számítási csomópontból és az adatfolyamhoz való közvetlen átvétele</span><span class="sxs-lookup"><span data-stu-id="0b838-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="0b838-136">Az első parancs az New-Object parancsmag segítségével hoz létre adatfolyamot, és a $Stream változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0b838-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="0b838-137">A második parancs beolvassa az StdOut.txt nevű csomópontot a számítási csomópontról, amelynek azonosító ComputeNode01 az azonosító Pool01 tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="0b838-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="0b838-138">A parancs a fájl tartalmát az adatfolyamra irányítja a $Streamban.</span><span class="sxs-lookup"><span data-stu-id="0b838-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="0b838-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b838-139">PARAMETERS</span></span>

### <span data-ttu-id="0b838-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0b838-140">-BatchContext</span></span>
<span data-ttu-id="0b838-141">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="0b838-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0b838-142">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0b838-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="0b838-143">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="0b838-143">-ByteRangeEnd</span></span>
<span data-ttu-id="0b838-144">A letöltendő bájtok hatókörének vége.</span><span class="sxs-lookup"><span data-stu-id="0b838-144">The end of the byte range to be downloaded.</span></span>
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

### <span data-ttu-id="0b838-145">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="0b838-145">-ByteRangeStart</span></span>
<span data-ttu-id="0b838-146">A letöltendő bájtok hatókörének kezdete.</span><span class="sxs-lookup"><span data-stu-id="0b838-146">The start of the byte range to be downloaded.</span></span>
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

### <span data-ttu-id="0b838-147">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="0b838-147">-ComputeNodeId</span></span>
<span data-ttu-id="0b838-148">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amely a parancsmag által megadott csomópont-fájlt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0b838-148">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="0b838-149">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="0b838-149">-DestinationPath</span></span>
<span data-ttu-id="0b838-150">Annak a fájlnak az elérési útját adja meg, ahol ez a parancsmag menti a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="0b838-150">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="0b838-151">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="0b838-151">-DestinationStream</span></span>
<span data-ttu-id="0b838-152">Azt a adatfolyamot adja meg, amelybe ez a parancsmag a csomópont-fájl tartalmát írja be.</span><span class="sxs-lookup"><span data-stu-id="0b838-152">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="0b838-153">Ez a parancsmag nem zárja be vagy hagyja vissza az adatfolyamot.</span><span class="sxs-lookup"><span data-stu-id="0b838-153">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="0b838-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b838-154">-InputObject</span></span>
<span data-ttu-id="0b838-155">Azt a fájlt adja meg, amelyet a parancsmag **PSNodeFile** objektumként kap.</span><span class="sxs-lookup"><span data-stu-id="0b838-155">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="0b838-156">A Node file objektum beolvasásához használja az Get-AzureBatchNodeFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0b838-156">To obtain a node file object, use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="0b838-157">-JobId</span><span class="sxs-lookup"><span data-stu-id="0b838-157">-JobId</span></span>
<span data-ttu-id="0b838-158">Annak a feladatnak az AZONOSÍTÓját adja meg, amely a célként megadott feladatot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0b838-158">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="0b838-159">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0b838-159">-Name</span></span>
<span data-ttu-id="0b838-160">Annak a csomópontnak a nevét adja meg, amelyre a parancsmag bekéri.</span><span class="sxs-lookup"><span data-stu-id="0b838-160">Specifies the name of the node file that this cmdlet retrieves.</span></span>
<span data-ttu-id="0b838-161">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="0b838-161">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b838-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="0b838-162">-PoolId</span></span>
<span data-ttu-id="0b838-163">Annak a készletnek az AZONOSÍTÓját adja meg, amely a parancsmagot tartalmazó csomópontot tartalmazó csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0b838-163">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0b838-164">-TaskId</span><span class="sxs-lookup"><span data-stu-id="0b838-164">-TaskId</span></span>
<span data-ttu-id="0b838-165">A tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b838-165">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="0b838-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b838-166">-DefaultProfile</span></span>
<span data-ttu-id="0b838-167">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b838-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b838-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b838-168">CommonParameters</span></span>
<span data-ttu-id="0b838-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b838-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b838-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b838-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b838-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b838-171">INPUTS</span></span>

### <span data-ttu-id="0b838-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0b838-172">BatchAccountContext</span></span>
<span data-ttu-id="0b838-173">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0b838-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0b838-174">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="0b838-174">PSNodeFile</span></span>
<span data-ttu-id="0b838-175">A ' InputObject ' paraméter az "PSNodeFile" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0b838-175">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="0b838-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b838-176">OUTPUTS</span></span>

## <span data-ttu-id="0b838-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b838-177">NOTES</span></span>

## <span data-ttu-id="0b838-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b838-178">RELATED LINKS</span></span>

[<span data-ttu-id="0b838-179">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0b838-179">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0b838-180">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="0b838-180">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="0b838-181">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0b838-181">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


