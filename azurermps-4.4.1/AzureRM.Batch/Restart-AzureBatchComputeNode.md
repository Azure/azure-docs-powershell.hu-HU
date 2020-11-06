---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: eff141494c2b34622f35b687dd1803c449e8b727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500943"
---
# <span data-ttu-id="50434-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="50434-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="50434-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50434-102">SYNOPSIS</span></span>
<span data-ttu-id="50434-103">Újraindítja a megadott számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="50434-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50434-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50434-104">SYNTAX</span></span>

### <span data-ttu-id="50434-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="50434-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50434-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="50434-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50434-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="50434-107">DESCRIPTION</span></span>
<span data-ttu-id="50434-108">Az **Újraindítás – AzureBatchComputeNode** parancsmag újraindítja a megadott számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="50434-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="50434-109">Példák</span><span class="sxs-lookup"><span data-stu-id="50434-109">EXAMPLES</span></span>

### <span data-ttu-id="50434-110">Példa 1: számítási csomópont újraindítása</span><span class="sxs-lookup"><span data-stu-id="50434-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="50434-111">Ez a parancs újraindítja a számítási csomópontot az "TVM-3257026573_2-20150813t200938z" AZONOSÍTÓval a Pool MyPool.</span><span class="sxs-lookup"><span data-stu-id="50434-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="50434-112">2. példa: az összes számítási csomópont újraindítása a készletben</span><span class="sxs-lookup"><span data-stu-id="50434-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="50434-113">Ez a parancs újraindítja az összes számítási csomópontot a Pool MyPool.</span><span class="sxs-lookup"><span data-stu-id="50434-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="50434-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50434-114">PARAMETERS</span></span>

### <span data-ttu-id="50434-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="50434-115">-BatchContext</span></span>
<span data-ttu-id="50434-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="50434-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="50434-117">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="50434-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="50434-118">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="50434-118">-ComputeNode</span></span>
<span data-ttu-id="50434-119">Azt a **PSComputeNode** -objektumot adja meg, amely a számítási csomópontot az újraindításra jelöli.</span><span class="sxs-lookup"><span data-stu-id="50434-119">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="50434-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="50434-120">-Id</span></span>
<span data-ttu-id="50434-121">A számítási csomópont AZONOSÍTÓját adja meg újraindításhoz.</span><span class="sxs-lookup"><span data-stu-id="50434-121">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="50434-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="50434-122">-PoolId</span></span>
<span data-ttu-id="50434-123">A számítási csomópontot tartalmazó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="50434-123">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="50434-124">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="50434-124">-RebootOption</span></span>
<span data-ttu-id="50434-125">Megadja, hogy mikor indítsa újra a csomópontot, és mi a teendő a jelenleg futó feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="50434-125">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="50434-126">Az alapértelmezett beállítás az újravárólista.</span><span class="sxs-lookup"><span data-stu-id="50434-126">The default is Requeue.</span></span>

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

### <span data-ttu-id="50434-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50434-127">-DefaultProfile</span></span>
<span data-ttu-id="50434-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50434-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50434-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50434-129">CommonParameters</span></span>
<span data-ttu-id="50434-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50434-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50434-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50434-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50434-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50434-132">INPUTS</span></span>

### <span data-ttu-id="50434-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="50434-133">BatchAccountContext</span></span>
<span data-ttu-id="50434-134">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="50434-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="50434-135">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="50434-135">PSComputeNode</span></span>
<span data-ttu-id="50434-136">A ' ComputeNode ' paraméter az "PSComputeNode" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="50434-136">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="50434-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50434-137">OUTPUTS</span></span>

## <span data-ttu-id="50434-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50434-138">NOTES</span></span>

## <span data-ttu-id="50434-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50434-139">RELATED LINKS</span></span>

[<span data-ttu-id="50434-140">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="50434-140">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="50434-141">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="50434-141">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="50434-142">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="50434-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


