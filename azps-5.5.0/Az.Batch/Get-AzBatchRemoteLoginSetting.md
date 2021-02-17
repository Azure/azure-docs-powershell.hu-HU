---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205247"
---
# <span data-ttu-id="aa1ad-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="aa1ad-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="aa1ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="aa1ad-103">Távoli bejelentkezési beállításokat kap egy számítási csomóponthoz.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="aa1ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aa1ad-104">SYNTAX</span></span>

### <span data-ttu-id="aa1ad-105">Id (Default)</span><span class="sxs-lookup"><span data-stu-id="aa1ad-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa1ad-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="aa1ad-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa1ad-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aa1ad-107">DESCRIPTION</span></span>
<span data-ttu-id="aa1ad-108">A **Get-AzBatchRemoteLoginSetting** parancsmag távoli bejelentkezési beállításokat kap egy számítási csomóponthoz egy virtuális gép infrastruktúrán alapuló készletében.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="aa1ad-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aa1ad-109">EXAMPLES</span></span>

### <span data-ttu-id="aa1ad-110">1. példa: Távoli bejelentkezési beállítások lekérte a készlet összes csomópontját</span><span class="sxs-lookup"><span data-stu-id="aa1ad-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="aa1ad-111">Az első parancs a **Get-AzBatchAccountKey** használatával kap egy kötegfiók környezetét, amely az előfizetés hozzáférési kulcsait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="aa1ad-112">A parancs a következő parancsban $Context változóban tárolja a környezetét.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="aa1ad-113">A második parancs a **Get-AzBatchComputeNode** használatával bekérte a ContosoPool azonosítójú számítási csomópontokat a készletbe.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="aa1ad-114">A parancs minden egyes számítógépcsomópontot az aktuális parancsmagnak ad át a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="aa1ad-115">A parancs az egyes számítási csomópontok távoli bejelentkezési beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="aa1ad-116">2. példa: Távoli bejelentkezési beállítások lekérte egy csomóponthoz</span><span class="sxs-lookup"><span data-stu-id="aa1ad-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="aa1ad-117">Az első parancs egy kötegfiók környezetét kapja meg, amely tartalmazza az előfizetés hozzáférési kulcsait, majd azt a $Context változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="aa1ad-118">A második parancs annak a számítási csomópontnak a távoli bejelentkezési beállításait kapja meg, amely a ContosoPool azonosítót tartalmazza a megadott azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="aa1ad-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa1ad-119">PARAMETERS</span></span>

### <span data-ttu-id="aa1ad-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aa1ad-120">-BatchContext</span></span>
<span data-ttu-id="aa1ad-121">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aa1ad-122">Az előfizetés hozzáférési kulcsait tartalmazó **BatchAccountContext** fájl beszerzéséhez használja a Get-AzBatchAccountKey parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

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

### <span data-ttu-id="aa1ad-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="aa1ad-123">-ComputeNode</span></span>
<span data-ttu-id="aa1ad-124">Egy olyan számítási csomópontot ad meg **PSComputeNode-objektumként,** amelyhez ez a parancsmag távoli bejelentkezési beállításokat kap.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="aa1ad-125">Számítási csomópontobjektum beszerzéséhez használja a Get-AzBatchComputeNode parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa1ad-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="aa1ad-126">-ComputeNodeId</span></span>
<span data-ttu-id="aa1ad-127">Annak a számítási csomópontnak az azonosítója, amelynek a távoli bejelentkezési beállításait meg szeretné kapni.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="aa1ad-128">amelynek a parancsmagja távoli bejelentkezési beállításokat kap.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa1ad-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa1ad-129">-DefaultProfile</span></span>
<span data-ttu-id="aa1ad-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa1ad-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="aa1ad-131">-PoolId</span></span>
<span data-ttu-id="aa1ad-132">A virtuális gépet tartalmazó készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa1ad-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa1ad-133">CommonParameters</span></span>
<span data-ttu-id="aa1ad-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa1ad-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa1ad-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa1ad-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa1ad-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa1ad-136">INPUTS</span></span>

### <span data-ttu-id="aa1ad-137">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="aa1ad-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="aa1ad-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aa1ad-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="aa1ad-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa1ad-139">OUTPUTS</span></span>

### <span data-ttu-id="aa1ad-140">Microsoft.Azure.Commands.Bat. Models.PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="aa1ad-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="aa1ad-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aa1ad-141">NOTES</span></span>

## <span data-ttu-id="aa1ad-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa1ad-142">RELATED LINKS</span></span>

[<span data-ttu-id="aa1ad-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="aa1ad-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="aa1ad-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="aa1ad-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="aa1ad-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="aa1ad-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="aa1ad-146">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa1ad-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
