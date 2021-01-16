---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: ff8c758b5e384fbab8f690030eb8a7fbe35c79f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333762"
---
# <span data-ttu-id="0b67e-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="0b67e-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="0b67e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b67e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b67e-103">Újratelepíti az operációs rendszert a megadott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="0b67e-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="0b67e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b67e-104">SYNTAX</span></span>

### <span data-ttu-id="0b67e-105">Id (Default)</span><span class="sxs-lookup"><span data-stu-id="0b67e-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b67e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0b67e-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b67e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b67e-107">DESCRIPTION</span></span>
<span data-ttu-id="0b67e-108">A **Reset-AzBatchComputeNode** parancsmag újratelepíti az operációs rendszert a megadott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="0b67e-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="0b67e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b67e-109">EXAMPLES</span></span>

### <span data-ttu-id="0b67e-110">1. példa: Csomópont újraimálása</span><span class="sxs-lookup"><span data-stu-id="0b67e-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="0b67e-111">Ez a parancs újragondolja a számítási csomópontot a MyPool nevű készlet "tvm-3257026573_2-20150813t200938z" azonosítójával.</span><span class="sxs-lookup"><span data-stu-id="0b67e-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="0b67e-112">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="0b67e-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0b67e-113">2. példa: A készlet összes csomópontja újraimálása</span><span class="sxs-lookup"><span data-stu-id="0b67e-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="0b67e-114">Ez a parancs újragondolja a MyPool nevű készlet összes számítási csomópontját.</span><span class="sxs-lookup"><span data-stu-id="0b67e-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="0b67e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b67e-115">PARAMETERS</span></span>

### <span data-ttu-id="0b67e-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0b67e-116">-BatchContext</span></span>
<span data-ttu-id="0b67e-117">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="0b67e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0b67e-118">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="0b67e-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0b67e-119">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="0b67e-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0b67e-120">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="0b67e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0b67e-121">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="0b67e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0b67e-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="0b67e-122">-ComputeNode</span></span>
<span data-ttu-id="0b67e-123">Azt a **PSComputeNode** objektumot adja meg, amely a reimage-nak megfelelő számítási csomópontot jelöli.</span><span class="sxs-lookup"><span data-stu-id="0b67e-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="0b67e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b67e-124">-DefaultProfile</span></span>
<span data-ttu-id="0b67e-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b67e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b67e-126">-Id</span><span class="sxs-lookup"><span data-stu-id="0b67e-126">-Id</span></span>
<span data-ttu-id="0b67e-127">A visszaimálható számítási csomópont azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b67e-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="0b67e-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="0b67e-128">-PoolId</span></span>
<span data-ttu-id="0b67e-129">A számítási csomópontot tartalmazó készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0b67e-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="0b67e-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="0b67e-130">-ReimageOption</span></span>
<span data-ttu-id="0b67e-131">Azt adja meg, hogy mikor kell újraimálni a csomópontot, és hogy mit kell tenni az éppen futó feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="0b67e-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="0b67e-132">Az alapértelmezett érték az Újrarekesz.</span><span class="sxs-lookup"><span data-stu-id="0b67e-132">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeReimageOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b67e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b67e-133">CommonParameters</span></span>
<span data-ttu-id="0b67e-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b67e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b67e-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b67e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b67e-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b67e-136">INPUTS</span></span>

### <span data-ttu-id="0b67e-137">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="0b67e-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="0b67e-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0b67e-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0b67e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b67e-139">OUTPUTS</span></span>

### <span data-ttu-id="0b67e-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="0b67e-140">System.Void</span></span>

## <span data-ttu-id="0b67e-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b67e-141">NOTES</span></span>

## <span data-ttu-id="0b67e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b67e-142">RELATED LINKS</span></span>

[<span data-ttu-id="0b67e-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="0b67e-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="0b67e-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="0b67e-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="0b67e-145">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0b67e-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
