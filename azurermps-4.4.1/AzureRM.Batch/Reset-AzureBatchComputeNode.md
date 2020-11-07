---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: b90a70bb6b4a8104597056715c75f5699db5a24e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672882"
---
# <span data-ttu-id="da489-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="da489-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="da489-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da489-102">SYNOPSIS</span></span>
<span data-ttu-id="da489-103">Újratelepíti az operációs rendszert a megadott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="da489-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da489-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da489-104">SYNTAX</span></span>

### <span data-ttu-id="da489-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da489-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da489-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="da489-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da489-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="da489-107">DESCRIPTION</span></span>
<span data-ttu-id="da489-108">A **reset-AzureBatchComputeNode** parancsmag a megadott számítási csomóponton újratelepíti az operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="da489-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="da489-109">Példák</span><span class="sxs-lookup"><span data-stu-id="da489-109">EXAMPLES</span></span>

### <span data-ttu-id="da489-110">Példa 1: csomópont átméretezése</span><span class="sxs-lookup"><span data-stu-id="da489-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="da489-111">Ez a parancs a MyPool nevű alkalmazáskészletben a "TVM-3257026573_2-20150813t200938z" AZONOSÍTÓJÚ számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="da489-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="da489-112">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="da489-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="da489-113">2. példa: a készlet minden csomópontjának átrendezése</span><span class="sxs-lookup"><span data-stu-id="da489-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="da489-114">Ez a parancs a MyPool nevű készlet minden számítási csomópontját újra felszámolja.</span><span class="sxs-lookup"><span data-stu-id="da489-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="da489-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da489-115">PARAMETERS</span></span>

### <span data-ttu-id="da489-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="da489-116">-BatchContext</span></span>
<span data-ttu-id="da489-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="da489-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="da489-118">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="da489-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="da489-119">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="da489-119">-ComputeNode</span></span>
<span data-ttu-id="da489-120">Azt a **PSComputeNode** -objektumot adja meg, amely a számítási csomópontot ábrázolja.</span><span class="sxs-lookup"><span data-stu-id="da489-120">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="da489-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="da489-121">-Id</span></span>
<span data-ttu-id="da489-122">A számítási csomópont AZONOSÍTÓját adja meg a visszaképhez.</span><span class="sxs-lookup"><span data-stu-id="da489-122">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="da489-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="da489-123">-PoolId</span></span>
<span data-ttu-id="da489-124">A számítási csomópontot tartalmazó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="da489-124">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="da489-125">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="da489-125">-ReimageOption</span></span>
<span data-ttu-id="da489-126">Meghatározza, hogy mikor kell a csomópontot áttekinteni, és mi a teendő a jelenleg futó tevékenységekkel.</span><span class="sxs-lookup"><span data-stu-id="da489-126">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="da489-127">Az alapértelmezett beállítás az újravárólista.</span><span class="sxs-lookup"><span data-stu-id="da489-127">The default is Requeue.</span></span>

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

### <span data-ttu-id="da489-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da489-128">-DefaultProfile</span></span>
<span data-ttu-id="da489-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da489-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da489-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da489-130">CommonParameters</span></span>
<span data-ttu-id="da489-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da489-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da489-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da489-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da489-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da489-133">INPUTS</span></span>

### <span data-ttu-id="da489-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="da489-134">BatchAccountContext</span></span>
<span data-ttu-id="da489-135">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="da489-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="da489-136">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="da489-136">PSComputeNode</span></span>
<span data-ttu-id="da489-137">A ' ComputeNode ' paraméter az "PSComputeNode" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="da489-137">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="da489-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da489-138">OUTPUTS</span></span>

## <span data-ttu-id="da489-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da489-139">NOTES</span></span>

## <span data-ttu-id="da489-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da489-140">RELATED LINKS</span></span>

[<span data-ttu-id="da489-141">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="da489-141">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="da489-142">Újraindítás – AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="da489-142">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="da489-143">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="da489-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


