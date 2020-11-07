---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: 530db3d911d0300e1bd587cd953fb357ca810c9c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847985"
---
# <span data-ttu-id="76ffb-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="76ffb-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="76ffb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="76ffb-103">Újratelepíti az operációs rendszert a megadott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="76ffb-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="76ffb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76ffb-104">SYNTAX</span></span>

### <span data-ttu-id="76ffb-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76ffb-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76ffb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="76ffb-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76ffb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="76ffb-107">DESCRIPTION</span></span>
<span data-ttu-id="76ffb-108">A **reset-AzBatchComputeNode** parancsmag a megadott számítási csomóponton újratelepíti az operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="76ffb-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="76ffb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="76ffb-109">EXAMPLES</span></span>

### <span data-ttu-id="76ffb-110">Példa 1: csomópont átméretezése</span><span class="sxs-lookup"><span data-stu-id="76ffb-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="76ffb-111">Ez a parancs a MyPool nevű alkalmazáskészletben a "TVM-3257026573_2-20150813t200938z" AZONOSÍTÓJÚ számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="76ffb-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="76ffb-112">A Get-AzBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="76ffb-112">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="76ffb-113">2. példa: a készlet minden csomópontjának átrendezése</span><span class="sxs-lookup"><span data-stu-id="76ffb-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="76ffb-114">Ez a parancs a MyPool nevű készlet minden számítási csomópontját újra felszámolja.</span><span class="sxs-lookup"><span data-stu-id="76ffb-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="76ffb-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76ffb-115">PARAMETERS</span></span>

### <span data-ttu-id="76ffb-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="76ffb-116">-BatchContext</span></span>
<span data-ttu-id="76ffb-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="76ffb-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="76ffb-118">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="76ffb-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="76ffb-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="76ffb-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="76ffb-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="76ffb-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="76ffb-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="76ffb-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="76ffb-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="76ffb-122">-ComputeNode</span></span>
<span data-ttu-id="76ffb-123">Azt a **PSComputeNode** -objektumot adja meg, amely a számítási csomópontot ábrázolja.</span><span class="sxs-lookup"><span data-stu-id="76ffb-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="76ffb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ffb-124">-DefaultProfile</span></span>
<span data-ttu-id="76ffb-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76ffb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76ffb-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="76ffb-126">-Id</span></span>
<span data-ttu-id="76ffb-127">A számítási csomópont AZONOSÍTÓját adja meg a visszaképhez.</span><span class="sxs-lookup"><span data-stu-id="76ffb-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="76ffb-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="76ffb-128">-PoolId</span></span>
<span data-ttu-id="76ffb-129">A számítási csomópontot tartalmazó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="76ffb-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="76ffb-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="76ffb-130">-ReimageOption</span></span>
<span data-ttu-id="76ffb-131">Meghatározza, hogy mikor kell a csomópontot áttekinteni, és mi a teendő a jelenleg futó tevékenységekkel.</span><span class="sxs-lookup"><span data-stu-id="76ffb-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="76ffb-132">Az alapértelmezett beállítás az újravárólista.</span><span class="sxs-lookup"><span data-stu-id="76ffb-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="76ffb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ffb-133">CommonParameters</span></span>
<span data-ttu-id="76ffb-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76ffb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ffb-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76ffb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ffb-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76ffb-136">INPUTS</span></span>

### <span data-ttu-id="76ffb-137">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="76ffb-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="76ffb-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="76ffb-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="76ffb-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76ffb-139">OUTPUTS</span></span>

### <span data-ttu-id="76ffb-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="76ffb-140">System.Void</span></span>

## <span data-ttu-id="76ffb-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76ffb-141">NOTES</span></span>

## <span data-ttu-id="76ffb-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76ffb-142">RELATED LINKS</span></span>

[<span data-ttu-id="76ffb-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="76ffb-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="76ffb-144">Újraindítás – AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="76ffb-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="76ffb-145">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="76ffb-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

