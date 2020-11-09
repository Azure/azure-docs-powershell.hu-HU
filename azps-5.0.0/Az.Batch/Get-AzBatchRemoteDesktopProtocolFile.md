---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300407"
---
# <span data-ttu-id="5d147-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="5d147-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="5d147-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d147-102">SYNOPSIS</span></span>
<span data-ttu-id="5d147-103">RDP-fájlt kap egy számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="5d147-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="5d147-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d147-104">SYNTAX</span></span>

### <span data-ttu-id="5d147-105">Id_Path (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d147-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d147-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="5d147-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d147-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="5d147-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d147-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="5d147-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d147-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d147-109">DESCRIPTION</span></span>
<span data-ttu-id="5d147-110">A **Get-AzBatchRemoteDesktopProtocolFile** parancsmag egy Remote Desktop Protocol (RDP) fájlt kap egy számítási csomópontból, és fájlként vagy egy felhasználó által szolgáltatott adatfolyamként menti.</span><span class="sxs-lookup"><span data-stu-id="5d147-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="5d147-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5d147-111">EXAMPLES</span></span>

### <span data-ttu-id="5d147-112">Példa 1: RDP-fájl kérése meghatározott számítási csomópontról és a fájl mentése</span><span class="sxs-lookup"><span data-stu-id="5d147-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="5d147-113">Ez a parancs egy RDP-fájlt kap a számítási csomópontból, amelynek azonosító ComputeNode01 az azonosító Pool06 tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="5d147-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="5d147-114">A parancs az. rdp fájlt C:\PowerShell\MyComputeNode.rdp.-ként menti.</span><span class="sxs-lookup"><span data-stu-id="5d147-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="5d147-115">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="5d147-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5d147-116">2. példa: RDP-fájl kérése egy számítási csomópontról és a fájl mentése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="5d147-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="5d147-117">Ez a parancs azt a számítási csomópontot adja eredményül, amely a ComputeNode02 azonosító Pool06 tartalmazó készlet AZONOSÍTÓját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5d147-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="5d147-118">A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmaghoz tartozó csomópontot.</span><span class="sxs-lookup"><span data-stu-id="5d147-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5d147-119">Az aktuális parancsmag. RPD fájlt kap a számítási csomópontból, majd a tartalmat a C:\PowerShell\MyComputeNode02.rdp. nevű fájlként menti.</span><span class="sxs-lookup"><span data-stu-id="5d147-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="5d147-120">3. példa: a megadott számítási csomópont RDP-fájljának beszerzése és az adatfolyamhoz irányítása</span><span class="sxs-lookup"><span data-stu-id="5d147-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="5d147-121">Az első parancs az New-Object parancsmag segítségével hoz létre adatfolyamot, és a $Stream változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5d147-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="5d147-122">A második parancs egy. rdp kiterjesztésű fájlt kap a számítási csomópontból, amelynek azonosító ComputeNode03 az azonosító Pool06 tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="5d147-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="5d147-123">A parancs a fájl tartalmát az adatfolyamra irányítja a $Streamban.</span><span class="sxs-lookup"><span data-stu-id="5d147-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="5d147-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d147-124">PARAMETERS</span></span>

### <span data-ttu-id="5d147-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5d147-125">-BatchContext</span></span>
<span data-ttu-id="5d147-126">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="5d147-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5d147-127">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="5d147-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5d147-128">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="5d147-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5d147-129">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="5d147-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5d147-130">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5d147-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5d147-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="5d147-131">-ComputeNode</span></span>
<span data-ttu-id="5d147-132">A számítási csomópontot adja meg **PSComputeNode** objektumként, amely az. rdp fájlok pontja.</span><span class="sxs-lookup"><span data-stu-id="5d147-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="5d147-133">A számítási csomópont objektum beolvasásához használja az Get-AzBatchComputeNode parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5d147-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="5d147-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="5d147-134">-ComputeNodeId</span></span>
<span data-ttu-id="5d147-135">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyre az. rdp fájlok mutatnak.</span><span class="sxs-lookup"><span data-stu-id="5d147-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="5d147-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d147-136">-DefaultProfile</span></span>
<span data-ttu-id="5d147-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d147-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d147-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="5d147-138">-DestinationPath</span></span>
<span data-ttu-id="5d147-139">Annak a fájlnak az elérési útját adja meg, ahol a parancsmag menti az. rdp fájlt.</span><span class="sxs-lookup"><span data-stu-id="5d147-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="5d147-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="5d147-140">-DestinationStream</span></span>
<span data-ttu-id="5d147-141">Azt a adatfolyamot adja meg, amelybe a parancsmag az RDP-adatot irányítja.</span><span class="sxs-lookup"><span data-stu-id="5d147-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="5d147-142">Ez a parancsmag nem zárja be vagy hagyja vissza az adatfolyamot.</span><span class="sxs-lookup"><span data-stu-id="5d147-142">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="5d147-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="5d147-143">-PoolId</span></span>
<span data-ttu-id="5d147-144">Annak a készletnek az AZONOSÍTÓját adja meg, amely azt a számítási csomópontot tartalmazza, amelyből a parancsmag. rdp fájlt kap.</span><span class="sxs-lookup"><span data-stu-id="5d147-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="5d147-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d147-145">CommonParameters</span></span>
<span data-ttu-id="5d147-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d147-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d147-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5d147-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d147-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d147-148">INPUTS</span></span>

### <span data-ttu-id="5d147-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5d147-149">System.String</span></span>

### <span data-ttu-id="5d147-150">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="5d147-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="5d147-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5d147-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5d147-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d147-152">OUTPUTS</span></span>

### <span data-ttu-id="5d147-153">System. Void</span><span class="sxs-lookup"><span data-stu-id="5d147-153">System.Void</span></span>

## <span data-ttu-id="5d147-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d147-154">NOTES</span></span>

## <span data-ttu-id="5d147-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d147-155">RELATED LINKS</span></span>

[<span data-ttu-id="5d147-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5d147-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5d147-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5d147-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="5d147-158">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5d147-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
