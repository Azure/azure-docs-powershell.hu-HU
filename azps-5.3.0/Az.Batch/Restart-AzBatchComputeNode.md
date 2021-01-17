---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: 41c6ea8e069e03a759c04f39018e2fa3a4d16834
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478214"
---
# <span data-ttu-id="b335d-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b335d-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="b335d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b335d-102">SYNOPSIS</span></span>
<span data-ttu-id="b335d-103">A megadott számítási csomópont újraindítása.</span><span class="sxs-lookup"><span data-stu-id="b335d-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="b335d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b335d-104">SYNTAX</span></span>

### <span data-ttu-id="b335d-105">Id (Default)</span><span class="sxs-lookup"><span data-stu-id="b335d-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b335d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b335d-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b335d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b335d-107">DESCRIPTION</span></span>
<span data-ttu-id="b335d-108">Az **Restart-AzBatchComputeNode** parancsmag újraindítja a megadott számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="b335d-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="b335d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b335d-109">EXAMPLES</span></span>

### <span data-ttu-id="b335d-110">1. példa: Számítási csomópont újraindítása</span><span class="sxs-lookup"><span data-stu-id="b335d-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="b335d-111">Ez a parancs újraindítja a számítási csomópontot a MyPool készlet "tvm-3257026573_2-20150813t200938z" azonosítójával.</span><span class="sxs-lookup"><span data-stu-id="b335d-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="b335d-112">2. példa: Egy készlet összes számítási csomópontjának újraindítása</span><span class="sxs-lookup"><span data-stu-id="b335d-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="b335d-113">Ez a parancs újraindítja a MyPool készlet összes számítási csomópontját.</span><span class="sxs-lookup"><span data-stu-id="b335d-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="b335d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b335d-114">PARAMETERS</span></span>

### <span data-ttu-id="b335d-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b335d-115">-BatchContext</span></span>
<span data-ttu-id="b335d-116">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="b335d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b335d-117">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="b335d-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b335d-118">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="b335d-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b335d-119">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="b335d-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b335d-120">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="b335d-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b335d-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="b335d-121">-ComputeNode</span></span>
<span data-ttu-id="b335d-122">Azt a **PSComputeNode** objektumot adja meg, amely a újraindításhoz szükséges számítási csomópontot képviseli.</span><span class="sxs-lookup"><span data-stu-id="b335d-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="b335d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b335d-123">-DefaultProfile</span></span>
<span data-ttu-id="b335d-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b335d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b335d-125">-Id</span><span class="sxs-lookup"><span data-stu-id="b335d-125">-Id</span></span>
<span data-ttu-id="b335d-126">A újraindítható számítási csomópont azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b335d-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="b335d-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b335d-127">-PoolId</span></span>
<span data-ttu-id="b335d-128">A számítási csomópontot tartalmazó készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b335d-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="b335d-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="b335d-129">-RebootOption</span></span>
<span data-ttu-id="b335d-130">Azt adja meg, hogy mikor indítsa újra a csomópontot, és mit kell tenni az aktuálisan futó feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="b335d-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="b335d-131">Az alapértelmezett érték az Újrarekesz.</span><span class="sxs-lookup"><span data-stu-id="b335d-131">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeRebootOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b335d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b335d-132">CommonParameters</span></span>
<span data-ttu-id="b335d-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b335d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b335d-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b335d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b335d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b335d-135">INPUTS</span></span>

### <span data-ttu-id="b335d-136">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="b335d-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="b335d-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b335d-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b335d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b335d-138">OUTPUTS</span></span>

### <span data-ttu-id="b335d-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="b335d-139">System.Void</span></span>

## <span data-ttu-id="b335d-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b335d-140">NOTES</span></span>

## <span data-ttu-id="b335d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b335d-141">RELATED LINKS</span></span>

[<span data-ttu-id="b335d-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b335d-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="b335d-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b335d-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="b335d-144">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b335d-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
