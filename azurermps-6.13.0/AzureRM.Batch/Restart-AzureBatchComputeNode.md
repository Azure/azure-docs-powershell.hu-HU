---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/restart-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: 2b604b1bedf7843d21c9595227ab1ff446028133
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492861"
---
# <span data-ttu-id="d9e32-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d9e32-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="d9e32-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9e32-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e32-103">Újraindítja a megadott számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="d9e32-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9e32-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9e32-104">SYNTAX</span></span>

### <span data-ttu-id="d9e32-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9e32-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9e32-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d9e32-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9e32-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9e32-107">DESCRIPTION</span></span>
<span data-ttu-id="d9e32-108">Az **Újraindítás – AzureBatchComputeNode** parancsmag újraindítja a megadott számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="d9e32-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="d9e32-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d9e32-109">EXAMPLES</span></span>

### <span data-ttu-id="d9e32-110">Példa 1: számítási csomópont újraindítása</span><span class="sxs-lookup"><span data-stu-id="d9e32-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="d9e32-111">Ez a parancs újraindítja a számítási csomópontot az "TVM-3257026573_2-20150813t200938z" AZONOSÍTÓval a Pool MyPool.</span><span class="sxs-lookup"><span data-stu-id="d9e32-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="d9e32-112">2. példa: az összes számítási csomópont újraindítása a készletben</span><span class="sxs-lookup"><span data-stu-id="d9e32-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="d9e32-113">Ez a parancs újraindítja az összes számítási csomópontot a Pool MyPool.</span><span class="sxs-lookup"><span data-stu-id="d9e32-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="d9e32-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9e32-114">PARAMETERS</span></span>

### <span data-ttu-id="d9e32-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d9e32-115">-BatchContext</span></span>
<span data-ttu-id="d9e32-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="d9e32-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d9e32-117">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="d9e32-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d9e32-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="d9e32-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d9e32-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="d9e32-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d9e32-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="d9e32-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d9e32-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d9e32-121">-ComputeNode</span></span>
<span data-ttu-id="d9e32-122">Azt a **PSComputeNode** -objektumot adja meg, amely a számítási csomópontot az újraindításra jelöli.</span><span class="sxs-lookup"><span data-stu-id="d9e32-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="d9e32-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e32-123">-DefaultProfile</span></span>
<span data-ttu-id="d9e32-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9e32-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9e32-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d9e32-125">-Id</span></span>
<span data-ttu-id="d9e32-126">A számítási csomópont AZONOSÍTÓját adja meg újraindításhoz.</span><span class="sxs-lookup"><span data-stu-id="d9e32-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="d9e32-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d9e32-127">-PoolId</span></span>
<span data-ttu-id="d9e32-128">A számítási csomópontot tartalmazó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9e32-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="d9e32-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="d9e32-129">-RebootOption</span></span>
<span data-ttu-id="d9e32-130">Megadja, hogy mikor indítsa újra a csomópontot, és mi a teendő a jelenleg futó feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="d9e32-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="d9e32-131">Az alapértelmezett beállítás az újravárólista.</span><span class="sxs-lookup"><span data-stu-id="d9e32-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="d9e32-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e32-132">CommonParameters</span></span>
<span data-ttu-id="d9e32-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9e32-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e32-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9e32-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e32-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9e32-135">INPUTS</span></span>

### <span data-ttu-id="d9e32-136">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d9e32-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="d9e32-137">Paraméterek: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9e32-137">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="d9e32-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d9e32-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="d9e32-139">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9e32-139">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="d9e32-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9e32-140">OUTPUTS</span></span>

### <span data-ttu-id="d9e32-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="d9e32-141">System.Void</span></span>

## <span data-ttu-id="d9e32-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9e32-142">NOTES</span></span>

## <span data-ttu-id="d9e32-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9e32-143">RELATED LINKS</span></span>

[<span data-ttu-id="d9e32-144">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d9e32-144">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="d9e32-145">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d9e32-145">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="d9e32-146">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d9e32-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


