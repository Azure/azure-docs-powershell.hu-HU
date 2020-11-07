---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/reset-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: 8e1fd78c51a6a41f1f455fc3672a0c340309f76c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680432"
---
# <span data-ttu-id="5eb7e-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5eb7e-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="5eb7e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5eb7e-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb7e-103">Újratelepíti az operációs rendszert a megadott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5eb7e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5eb7e-104">SYNTAX</span></span>

### <span data-ttu-id="5eb7e-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5eb7e-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eb7e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5eb7e-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eb7e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5eb7e-107">DESCRIPTION</span></span>
<span data-ttu-id="5eb7e-108">A **reset-AzureBatchComputeNode** parancsmag a megadott számítási csomóponton újratelepíti az operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="5eb7e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5eb7e-109">EXAMPLES</span></span>

### <span data-ttu-id="5eb7e-110">Példa 1: csomópont átméretezése</span><span class="sxs-lookup"><span data-stu-id="5eb7e-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="5eb7e-111">Ez a parancs a MyPool nevű alkalmazáskészletben a "TVM-3257026573_2-20150813t200938z" AZONOSÍTÓJÚ számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="5eb7e-112">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5eb7e-113">2. példa: a készlet minden csomópontjának átrendezése</span><span class="sxs-lookup"><span data-stu-id="5eb7e-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="5eb7e-114">Ez a parancs a MyPool nevű készlet minden számítási csomópontját újra felszámolja.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="5eb7e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5eb7e-115">PARAMETERS</span></span>

### <span data-ttu-id="5eb7e-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5eb7e-116">-BatchContext</span></span>
<span data-ttu-id="5eb7e-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5eb7e-118">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5eb7e-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5eb7e-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5eb7e-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb7e-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="5eb7e-122">-ComputeNode</span></span>
<span data-ttu-id="5eb7e-123">Azt a **PSComputeNode** -objektumot adja meg, amely a számítási csomópontot ábrázolja.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb7e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb7e-124">-DefaultProfile</span></span>
<span data-ttu-id="5eb7e-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb7e-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5eb7e-126">-Id</span></span>
<span data-ttu-id="5eb7e-127">A számítási csomópont AZONOSÍTÓját adja meg a visszaképhez.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-127">Specifies the ID of the compute node to reimage.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb7e-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="5eb7e-128">-PoolId</span></span>
<span data-ttu-id="5eb7e-129">A számítási csomópontot tartalmazó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-129">Specifies the ID of the pool that contains the compute node.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb7e-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="5eb7e-130">-ReimageOption</span></span>
<span data-ttu-id="5eb7e-131">Meghatározza, hogy mikor kell a csomópontot áttekinteni, és mi a teendő a jelenleg futó tevékenységekkel.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="5eb7e-132">Az alapértelmezett beállítás az újravárólista.</span><span class="sxs-lookup"><span data-stu-id="5eb7e-132">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeReimageOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb7e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb7e-133">CommonParameters</span></span>
<span data-ttu-id="5eb7e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5eb7e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb7e-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eb7e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb7e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5eb7e-136">INPUTS</span></span>

### <span data-ttu-id="5eb7e-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5eb7e-137">BatchAccountContext</span></span>
<span data-ttu-id="5eb7e-138">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5eb7e-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5eb7e-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="5eb7e-139">PSComputeNode</span></span>
<span data-ttu-id="5eb7e-140">A ' ComputeNode ' paraméter az "PSComputeNode" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5eb7e-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="5eb7e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5eb7e-141">OUTPUTS</span></span>

## <span data-ttu-id="5eb7e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5eb7e-142">NOTES</span></span>

## <span data-ttu-id="5eb7e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5eb7e-143">RELATED LINKS</span></span>

[<span data-ttu-id="5eb7e-144">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5eb7e-144">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="5eb7e-145">Újraindítás – AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5eb7e-145">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="5eb7e-146">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5eb7e-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


