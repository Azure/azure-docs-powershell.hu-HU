---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 812edce5ba6a9c1aa4582538c3fda510efdb7175
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673176"
---
# <span data-ttu-id="22e0c-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="22e0c-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="22e0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="22e0c-103">RDP-fájlt kap egy számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="22e0c-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22e0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22e0c-104">SYNTAX</span></span>

### <span data-ttu-id="22e0c-105">Id_Path (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22e0c-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22e0c-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="22e0c-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22e0c-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="22e0c-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22e0c-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="22e0c-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22e0c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="22e0c-109">DESCRIPTION</span></span>
<span data-ttu-id="22e0c-110">A **Get-AzureBatchRemoteDesktopProtocolFile** parancsmag egy Remote Desktop Protocol (RDP) fájlt kap egy számítási csomópontból, és fájlként vagy egy felhasználó által szolgáltatott adatfolyamként menti.</span><span class="sxs-lookup"><span data-stu-id="22e0c-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="22e0c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="22e0c-111">EXAMPLES</span></span>

### <span data-ttu-id="22e0c-112">Példa 1: RDP-fájl kérése meghatározott számítási csomópontról és a fájl mentése</span><span class="sxs-lookup"><span data-stu-id="22e0c-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="22e0c-113">Ez a parancs egy RDP-fájlt kap a számítási csomópontból, amelynek azonosító ComputeNode01 az azonosító Pool06 tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="22e0c-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="22e0c-114">A parancs az. rdp fájlt C:\PowerShell\MyComputeNode.rdp.-ként menti.</span><span class="sxs-lookup"><span data-stu-id="22e0c-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="22e0c-115">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="22e0c-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="22e0c-116">2. példa: RDP-fájl kérése egy számítási csomópontról és a fájl mentése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="22e0c-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="22e0c-117">Ez a parancs azt a számítási csomópontot adja eredményül, amely a ComputeNode02 azonosító Pool06 tartalmazó készlet AZONOSÍTÓját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="22e0c-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="22e0c-118">A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmaghoz tartozó csomópontot.</span><span class="sxs-lookup"><span data-stu-id="22e0c-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="22e0c-119">Az aktuális parancsmag. RPD fájlt kap a számítási csomópontból, majd a tartalmat a C:\PowerShell\MyComputeNode02.rdp. nevű fájlként menti.</span><span class="sxs-lookup"><span data-stu-id="22e0c-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="22e0c-120">3. példa: a megadott számítási csomópont RDP-fájljának beszerzése és az adatfolyamhoz irányítása</span><span class="sxs-lookup"><span data-stu-id="22e0c-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="22e0c-121">Az első parancs az New-Object parancsmag segítségével hoz létre adatfolyamot, és a $Stream változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="22e0c-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="22e0c-122">A második parancs egy. rdp kiterjesztésű fájlt kap a számítási csomópontból, amelynek azonosító ComputeNode03 az azonosító Pool06 tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="22e0c-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="22e0c-123">A parancs a fájl tartalmát az adatfolyamra irányítja a $Streamban.</span><span class="sxs-lookup"><span data-stu-id="22e0c-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="22e0c-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22e0c-124">PARAMETERS</span></span>

### <span data-ttu-id="22e0c-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="22e0c-125">-BatchContext</span></span>
<span data-ttu-id="22e0c-126">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="22e0c-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="22e0c-127">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="22e0c-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="22e0c-128">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="22e0c-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="22e0c-129">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="22e0c-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="22e0c-130">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="22e0c-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="22e0c-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="22e0c-131">-ComputeNode</span></span>
<span data-ttu-id="22e0c-132">A számítási csomópontot adja meg **PSComputeNode** objektumként, amely az. rdp fájlok pontja.</span><span class="sxs-lookup"><span data-stu-id="22e0c-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="22e0c-133">A számítási csomópont objektum beolvasásához használja az Get-AzureBatchComputeNode parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="22e0c-133">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="22e0c-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="22e0c-134">-ComputeNodeId</span></span>
<span data-ttu-id="22e0c-135">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyre az. rdp fájlok mutatnak.</span><span class="sxs-lookup"><span data-stu-id="22e0c-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="22e0c-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e0c-136">-DefaultProfile</span></span>
<span data-ttu-id="22e0c-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22e0c-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22e0c-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="22e0c-138">-DestinationPath</span></span>
<span data-ttu-id="22e0c-139">Annak a fájlnak az elérési útját adja meg, ahol a parancsmag menti az. rdp fájlt.</span><span class="sxs-lookup"><span data-stu-id="22e0c-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="22e0c-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="22e0c-140">-DestinationStream</span></span>
<span data-ttu-id="22e0c-141">Azt a adatfolyamot adja meg, amelybe a parancsmag az RDP-adatot irányítja.</span><span class="sxs-lookup"><span data-stu-id="22e0c-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="22e0c-142">Ez a parancsmag nem zárja be vagy hagyja vissza az adatfolyamot.</span><span class="sxs-lookup"><span data-stu-id="22e0c-142">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="22e0c-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="22e0c-143">-PoolId</span></span>
<span data-ttu-id="22e0c-144">Annak a készletnek az AZONOSÍTÓját adja meg, amely azt a számítási csomópontot tartalmazza, amelyből a parancsmag. rdp fájlt kap.</span><span class="sxs-lookup"><span data-stu-id="22e0c-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="22e0c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e0c-145">CommonParameters</span></span>
<span data-ttu-id="22e0c-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22e0c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e0c-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22e0c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e0c-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22e0c-148">INPUTS</span></span>

### <span data-ttu-id="22e0c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="22e0c-149">System.String</span></span>

### <span data-ttu-id="22e0c-150">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="22e0c-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="22e0c-151">Paraméterek: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22e0c-151">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="22e0c-152">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="22e0c-152">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="22e0c-153">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22e0c-153">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="22e0c-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22e0c-154">OUTPUTS</span></span>

### <span data-ttu-id="22e0c-155">System. Void</span><span class="sxs-lookup"><span data-stu-id="22e0c-155">System.Void</span></span>

## <span data-ttu-id="22e0c-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22e0c-156">NOTES</span></span>

## <span data-ttu-id="22e0c-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22e0c-157">RELATED LINKS</span></span>

[<span data-ttu-id="22e0c-158">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="22e0c-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="22e0c-159">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="22e0c-159">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="22e0c-160">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="22e0c-160">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


