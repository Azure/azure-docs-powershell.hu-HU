---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: ff8c758b5e384fbab8f690030eb8a7fbe35c79f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187848"
---
# <span data-ttu-id="a488c-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a488c-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="a488c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a488c-102">SYNOPSIS</span></span>
<span data-ttu-id="a488c-103">Újratelepíti az operációs rendszert a megadott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="a488c-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="a488c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a488c-104">SYNTAX</span></span>

### <span data-ttu-id="a488c-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a488c-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a488c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a488c-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a488c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a488c-107">DESCRIPTION</span></span>
<span data-ttu-id="a488c-108">A **reset-AzBatchComputeNode** parancsmag a megadott számítási csomóponton újratelepíti az operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="a488c-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="a488c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a488c-109">EXAMPLES</span></span>

### <span data-ttu-id="a488c-110">Példa 1: csomópont átméretezése</span><span class="sxs-lookup"><span data-stu-id="a488c-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="a488c-111">Ez a parancs a MyPool nevű alkalmazáskészletben a "TVM-3257026573_2-20150813t200938z" AZONOSÍTÓJÚ számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="a488c-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="a488c-112">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="a488c-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a488c-113">2. példa: a készlet minden csomópontjának átrendezése</span><span class="sxs-lookup"><span data-stu-id="a488c-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="a488c-114">Ez a parancs a MyPool nevű készlet minden számítási csomópontját újra felszámolja.</span><span class="sxs-lookup"><span data-stu-id="a488c-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="a488c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a488c-115">PARAMETERS</span></span>

### <span data-ttu-id="a488c-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a488c-116">-BatchContext</span></span>
<span data-ttu-id="a488c-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="a488c-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a488c-118">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="a488c-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a488c-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="a488c-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a488c-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="a488c-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a488c-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="a488c-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a488c-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a488c-122">-ComputeNode</span></span>
<span data-ttu-id="a488c-123">Azt a **PSComputeNode** -objektumot adja meg, amely a számítási csomópontot ábrázolja.</span><span class="sxs-lookup"><span data-stu-id="a488c-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="a488c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a488c-124">-DefaultProfile</span></span>
<span data-ttu-id="a488c-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a488c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a488c-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a488c-126">-Id</span></span>
<span data-ttu-id="a488c-127">A számítási csomópont AZONOSÍTÓját adja meg a visszaképhez.</span><span class="sxs-lookup"><span data-stu-id="a488c-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="a488c-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a488c-128">-PoolId</span></span>
<span data-ttu-id="a488c-129">A számítási csomópontot tartalmazó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a488c-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="a488c-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="a488c-130">-ReimageOption</span></span>
<span data-ttu-id="a488c-131">Meghatározza, hogy mikor kell a csomópontot áttekinteni, és mi a teendő a jelenleg futó tevékenységekkel.</span><span class="sxs-lookup"><span data-stu-id="a488c-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="a488c-132">Az alapértelmezett beállítás az újravárólista.</span><span class="sxs-lookup"><span data-stu-id="a488c-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="a488c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a488c-133">CommonParameters</span></span>
<span data-ttu-id="a488c-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a488c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a488c-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a488c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a488c-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a488c-136">INPUTS</span></span>

### <span data-ttu-id="a488c-137">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a488c-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="a488c-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a488c-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a488c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a488c-139">OUTPUTS</span></span>

### <span data-ttu-id="a488c-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="a488c-140">System.Void</span></span>

## <span data-ttu-id="a488c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a488c-141">NOTES</span></span>

## <span data-ttu-id="a488c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a488c-142">RELATED LINKS</span></span>

[<span data-ttu-id="a488c-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a488c-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="a488c-144">Újraindítás – AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a488c-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="a488c-145">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a488c-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
