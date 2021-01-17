---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478321"
---
# <span data-ttu-id="31f4b-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="31f4b-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="31f4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="31f4b-103">RdP-fájlt kap egy számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="31f4b-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="31f4b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31f4b-104">SYNTAX</span></span>

### <span data-ttu-id="31f4b-105">Id_Path (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31f4b-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31f4b-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="31f4b-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31f4b-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="31f4b-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31f4b-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="31f4b-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31f4b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31f4b-109">DESCRIPTION</span></span>
<span data-ttu-id="31f4b-110">A **Get-AzBatchRemoteDesktopProtocolFile** parancsmag egy RDP-fájlt kap egy számítási csomópontból, és fájlként vagy egy felhasználó által megadott adatfolyamba menti.</span><span class="sxs-lookup"><span data-stu-id="31f4b-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="31f4b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31f4b-111">EXAMPLES</span></span>

### <span data-ttu-id="31f4b-112">1. példa: RDP-fájl lekérte egy megadott számítási csomópontból, és mentse a fájlt</span><span class="sxs-lookup"><span data-stu-id="31f4b-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="31f4b-113">Ez a parancs egy RDP-fájlt kap abból a számítási csomópontból, amelynél az ID ComputeNode01 azonosító található a Készletazonosító készletben.</span><span class="sxs-lookup"><span data-stu-id="31f4b-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="31f4b-114">A parancs a .rdp fájlt C:\PowerShell\MyComputeNode.rdp formátumban menti.</span><span class="sxs-lookup"><span data-stu-id="31f4b-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="31f4b-115">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="31f4b-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="31f4b-116">2. példa: RDP-fájl lekérte egy számítási csomópontból, és a folyamat használatával mentheti a fájlt</span><span class="sxs-lookup"><span data-stu-id="31f4b-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="31f4b-117">Ez a parancs lekérte azt a számítási csomópontot, amelynél a ComputeNode02 azonosító található a készletben, amely az ID Pool06 azonosítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="31f4b-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="31f4b-118">A parancs a csomópontot a folyamat műveleti operátorával átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="31f4b-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="31f4b-119">Az aktuális parancsmag egy .rpd fájlt kap a számítási csomópontból, majd a tartalmat C:\PowerShell\MyComputeNode02.rdp nevű fájlként menti.</span><span class="sxs-lookup"><span data-stu-id="31f4b-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="31f4b-120">3. példa: RDP-fájl lekérte egy adott számítási csomópontból, és egy adatfolyamhoz irányította</span><span class="sxs-lookup"><span data-stu-id="31f4b-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="31f4b-121">Az első parancs egy adatfolyamot hoz létre a New-Object parancsmag használatával, majd a $Stream tárolja.</span><span class="sxs-lookup"><span data-stu-id="31f4b-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="31f4b-122">A második parancs egy .rdp fájlt kap abból a számítási csomópontból, amelynél a ComputeNode03 azonosító található a Készletazonosító készletben.</span><span class="sxs-lookup"><span data-stu-id="31f4b-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="31f4b-123">A parancs a fájl tartalmát a $Stream.</span><span class="sxs-lookup"><span data-stu-id="31f4b-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="31f4b-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31f4b-124">PARAMETERS</span></span>

### <span data-ttu-id="31f4b-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="31f4b-125">-BatchContext</span></span>
<span data-ttu-id="31f4b-126">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="31f4b-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="31f4b-127">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="31f4b-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="31f4b-128">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="31f4b-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="31f4b-129">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="31f4b-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="31f4b-130">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="31f4b-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="31f4b-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="31f4b-131">-ComputeNode</span></span>
<span data-ttu-id="31f4b-132">Egy olyan számítási csomópontot **(PSComputeNode-objektumot)** ad meg, amelyre az .rdp fájl mutat.</span><span class="sxs-lookup"><span data-stu-id="31f4b-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="31f4b-133">Számítási csomópontobjektum beszerzéséhez használja a Get-AzBatchComputeNode parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="31f4b-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31f4b-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="31f4b-134">-ComputeNodeId</span></span>
<span data-ttu-id="31f4b-135">Annak a számítási csomópontnak az azonosítója, amelyre az .rdp fájl mutat.</span><span class="sxs-lookup"><span data-stu-id="31f4b-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f4b-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f4b-136">-DefaultProfile</span></span>
<span data-ttu-id="31f4b-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31f4b-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31f4b-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="31f4b-138">-DestinationPath</span></span>
<span data-ttu-id="31f4b-139">Megadja azt a fájl elérési útját, ahová a parancsmag az .rdp fájlt menti.</span><span class="sxs-lookup"><span data-stu-id="31f4b-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f4b-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="31f4b-140">-DestinationStream</span></span>
<span data-ttu-id="31f4b-141">Azt az adatfolyamot adja meg, amelybe ez a parancsmag az RDP-adatokat irányítja.</span><span class="sxs-lookup"><span data-stu-id="31f4b-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="31f4b-142">Ez a parancsmag nem zárja be és nem tekeri vissza az adatfolyamot.</span><span class="sxs-lookup"><span data-stu-id="31f4b-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f4b-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="31f4b-143">-PoolId</span></span>
<span data-ttu-id="31f4b-144">Annak a készletnek az azonosítója, amely azt a számítási csomópontot tartalmazza, amelyből a parancsmag .rdp fájlt kap.</span><span class="sxs-lookup"><span data-stu-id="31f4b-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f4b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f4b-145">CommonParameters</span></span>
<span data-ttu-id="31f4b-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f4b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f4b-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31f4b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f4b-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31f4b-148">INPUTS</span></span>

### <span data-ttu-id="31f4b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="31f4b-149">System.String</span></span>

### <span data-ttu-id="31f4b-150">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="31f4b-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="31f4b-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="31f4b-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="31f4b-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31f4b-152">OUTPUTS</span></span>

### <span data-ttu-id="31f4b-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="31f4b-153">System.Void</span></span>

## <span data-ttu-id="31f4b-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31f4b-154">NOTES</span></span>

## <span data-ttu-id="31f4b-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31f4b-155">RELATED LINKS</span></span>

[<span data-ttu-id="31f4b-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="31f4b-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="31f4b-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="31f4b-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="31f4b-158">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="31f4b-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
