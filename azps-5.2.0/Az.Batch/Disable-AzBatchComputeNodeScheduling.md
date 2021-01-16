---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353910"
---
# <span data-ttu-id="7068c-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="7068c-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="7068c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7068c-102">SYNOPSIS</span></span>
<span data-ttu-id="7068c-103">Letiltja a tevékenységütemezést a megadott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="7068c-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="7068c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7068c-104">SYNTAX</span></span>

### <span data-ttu-id="7068c-105">Id (Default)</span><span class="sxs-lookup"><span data-stu-id="7068c-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7068c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7068c-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7068c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7068c-107">DESCRIPTION</span></span>
<span data-ttu-id="7068c-108">A **Disable-AzBatchComputeNodeScheduling** parancsmag letiltja a feladatütemezést a megadott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="7068c-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="7068c-109">A számítási csomópont egy adott alkalmazásterheléshez dedikált Azure virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="7068c-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="7068c-110">Ha egy számítási csomóponton letiltja a tevékenységütemezést, eldöntheti azt is, hogy mit kell tenni a csomópont feladatsorában lévő feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="7068c-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="7068c-111">**Az Disable-AzBatchComputeNodeScheduling** segítségével az alábbi lehetőségek közül választhat:</span><span class="sxs-lookup"><span data-stu-id="7068c-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="7068c-112">Bontsa le a tevékenységeket, és helyezze vissza őket a várólistára.</span><span class="sxs-lookup"><span data-stu-id="7068c-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="7068c-113">Ez lehetővé teszi, hogy ezeket a feladatokat átütemezték egy másik számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="7068c-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="7068c-114">Bontsa le a feladatokat, és távolítsa el őket a várólistáról.</span><span class="sxs-lookup"><span data-stu-id="7068c-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="7068c-115">Az ily módon leállított tevékenységeket a projekt nem ütemezi át.</span><span class="sxs-lookup"><span data-stu-id="7068c-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="7068c-116">Várja meg, amíg az összes jelenleg végrehajtott feladat befejeződik, majd tiltsa le a tevékenységütemezést a számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="7068c-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="7068c-117">Várja meg, amíg az összes futó feladat befejeződik, az adatmegőrzési időszakok lejárnak, majd tiltsa le a tevékenységütemezést a számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="7068c-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="7068c-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7068c-118">EXAMPLES</span></span>

### <span data-ttu-id="7068c-119">1. példa: Feladatütemezés letiltása számítási csomóponton</span><span class="sxs-lookup"><span data-stu-id="7068c-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="7068c-120">Ezek a parancsok letiltják a tevékenység ütemezését a számítási csomópont tvm-1783593343_34-20151117t22514z.</span><span class="sxs-lookup"><span data-stu-id="7068c-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="7068c-121">Ehhez a példában az első parancs létrehoz egy objektumhivatkozást a contosobatchaccount kötegfiók fiókkulcsára.</span><span class="sxs-lookup"><span data-stu-id="7068c-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="7068c-122">Ezt az objektumhivatkozást egy $context.</span><span class="sxs-lookup"><span data-stu-id="7068c-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="7068c-123">A második parancs ezután ezt az objektumhivatkozást és a **Disable-AzBatchComputeNodeScheduling** parancsmagot használva csatlakozik a sajátPool készlethez, és letiltja a feladatok ütemezését a node tvm-1783593343_34-20151117t22514z.</span><span class="sxs-lookup"><span data-stu-id="7068c-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="7068c-124">Mivel a *DisableComputeNodeSchedulingOptions* paraméter nem tartalmazta a számítási csomóponton jelenleg futó feladatokat, a rendszer újra le fogja tiltani.</span><span class="sxs-lookup"><span data-stu-id="7068c-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="7068c-125">2. példa: Tevékenységütemezés letiltása egy készlet összes számítási csomópontja számára</span><span class="sxs-lookup"><span data-stu-id="7068c-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="7068c-126">Ezek a parancsok letiltják a tevékenység ütemezését a készlet Pool06 összes számítógépcsomópontját.</span><span class="sxs-lookup"><span data-stu-id="7068c-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="7068c-127">A feladat végrehajtásához a példában az első parancs létrehoz egy objektumhivatkozást a contosobatchaccount kötegfiók fiókkulcsára.</span><span class="sxs-lookup"><span data-stu-id="7068c-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="7068c-128">Ezt az objektumhivatkozást egy $context.</span><span class="sxs-lookup"><span data-stu-id="7068c-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="7068c-129">A példában a második parancs ezt az objektumhivatkozást és **a Get-AzBatchComputeNode-ot** használva visszaadja a Pool06-ban található összes számítási csomópont gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="7068c-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="7068c-130">Ezt a gyűjteményt ezután a **Disable-AzBatchComputeNodeScheduling** parancsmagra kapcsolja a rendszer, hogy letiltsa a feladatütemezést a gyűjtemény minden egyes számítási csomópontján.</span><span class="sxs-lookup"><span data-stu-id="7068c-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="7068c-131">Mivel a *DisableComputeNodeSchedulingOptions* paraméter nem tartalmazta a számítási csomópontokon jelenleg futó feladatokat, a rendszer újraszámít.</span><span class="sxs-lookup"><span data-stu-id="7068c-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="7068c-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7068c-132">PARAMETERS</span></span>

### <span data-ttu-id="7068c-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7068c-133">-BatchContext</span></span>
<span data-ttu-id="7068c-134">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="7068c-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7068c-135">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="7068c-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7068c-136">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="7068c-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7068c-137">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="7068c-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7068c-138">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="7068c-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7068c-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="7068c-139">-ComputeNode</span></span>
<span data-ttu-id="7068c-140">Objektumhivatkozást ad meg arra a számítási csomópontra, ahol a tevékenységütemezés le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="7068c-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="7068c-141">Ez az objektumhivatkozás a Get-AzBatchComputeNode segítségével jön létre, és a visszaadott számítási csomópont-objektumot egy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7068c-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="7068c-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7068c-142">-DefaultProfile</span></span>
<span data-ttu-id="7068c-143">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7068c-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7068c-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="7068c-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="7068c-145">Azt adja meg, hogy ez a parancsmag hogyan foglalkozik a számítógép csomópontján jelenleg futó olyan feladatokkal, amelyekben az ütemezés le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="7068c-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="7068c-146">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="7068c-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7068c-147">Újraérték.</span><span class="sxs-lookup"><span data-stu-id="7068c-147">Requeue.</span></span>
<span data-ttu-id="7068c-148">A feladatok azonnal leállnak, és visszakerülnek a várólistára.</span><span class="sxs-lookup"><span data-stu-id="7068c-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="7068c-149">Ez lehetővé teszi a feladatok átütemezét egy másik számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="7068c-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="7068c-150">Ez az alapértelmezett érték.</span><span class="sxs-lookup"><span data-stu-id="7068c-150">This is the default value.</span></span> 
- <span data-ttu-id="7068c-151">Lezárás.</span><span class="sxs-lookup"><span data-stu-id="7068c-151">Terminate.</span></span>
<span data-ttu-id="7068c-152">A tevékenységeket a rendszer azonnal leállja, és eltávolítja őket a várólistáról.</span><span class="sxs-lookup"><span data-stu-id="7068c-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="7068c-153">Ezek a tevékenységek nem lesznek átütemezve.</span><span class="sxs-lookup"><span data-stu-id="7068c-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="7068c-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="7068c-154">TaskCompletion.</span></span>
<span data-ttu-id="7068c-155">A jelenleg futó feladatok még azelőtt befejeződnek, hogy a tevékenységütemezés le lenne tiltva a számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="7068c-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="7068c-156">Ezen a csomóponton nem lesznek új feladatok ütemezve.</span><span class="sxs-lookup"><span data-stu-id="7068c-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="7068c-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="7068c-157">RetainedData.</span></span>
<span data-ttu-id="7068c-158">A jelenleg futó feladatok befejeződnek, az adatmegőrzési időszakok pedig le fognak járni, mielőtt a tevékenységütemezés le lenne tiltva a számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="7068c-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="7068c-159">Ezen a csomóponton nem lesznek új feladatok ütemezve.</span><span class="sxs-lookup"><span data-stu-id="7068c-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7068c-160">-Id</span><span class="sxs-lookup"><span data-stu-id="7068c-160">-Id</span></span>
<span data-ttu-id="7068c-161">Annak a számítási csomópontnak az azonosítója, ahol a tevékenységütemezés le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="7068c-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="7068c-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="7068c-162">-PoolId</span></span>
<span data-ttu-id="7068c-163">Annak a kötegkészletnek az azonosítója, amely azt a számítási csomópontot tartalmazza, ahol a tevékenységütemezés le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="7068c-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="7068c-164">Ha a *PoolId paramétert használja,* ne használja a *ComputeNode* paramétert ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="7068c-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="7068c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7068c-165">CommonParameters</span></span>
<span data-ttu-id="7068c-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7068c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7068c-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7068c-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7068c-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7068c-168">INPUTS</span></span>

### <span data-ttu-id="7068c-169">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="7068c-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="7068c-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7068c-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7068c-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7068c-171">OUTPUTS</span></span>

### <span data-ttu-id="7068c-172">System.Void</span><span class="sxs-lookup"><span data-stu-id="7068c-172">System.Void</span></span>

## <span data-ttu-id="7068c-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7068c-173">NOTES</span></span>

## <span data-ttu-id="7068c-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7068c-174">RELATED LINKS</span></span>

[<span data-ttu-id="7068c-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7068c-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7068c-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="7068c-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


