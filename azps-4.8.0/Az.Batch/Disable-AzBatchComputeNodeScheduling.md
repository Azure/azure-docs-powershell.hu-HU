---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180626"
---
# <span data-ttu-id="79aa7-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="79aa7-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="79aa7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="79aa7-103">A megadott számítási csomóponton letiltja a tevékenység ütemezését.</span><span class="sxs-lookup"><span data-stu-id="79aa7-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="79aa7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79aa7-104">SYNTAX</span></span>

### <span data-ttu-id="79aa7-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79aa7-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79aa7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="79aa7-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79aa7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="79aa7-107">DESCRIPTION</span></span>
<span data-ttu-id="79aa7-108">A **disable-AzBatchComputeNodeScheduling** parancsmag letiltja a tevékenység ütemezését a megadott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="79aa7-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="79aa7-109">A számítási csomópont egy olyan Azure Virtual Machine, amely egy adott alkalmazási munkaterheléshez van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="79aa7-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="79aa7-110">Ha egy számítási csomóponton letiltja a tevékenységek ütemezését, akkor azt is megadhatja, hogy mit szeretne tenni a csomópont tevékenység-várólistájában lévő munkahelyekről.</span><span class="sxs-lookup"><span data-stu-id="79aa7-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="79aa7-111">A **disable-AzBatchComputeNodeScheduling** segítségével az alábbiakat végezheti el:</span><span class="sxs-lookup"><span data-stu-id="79aa7-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="79aa7-112">A feladatok megszüntetése és visszahelyezése a projekt várólistájába.</span><span class="sxs-lookup"><span data-stu-id="79aa7-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="79aa7-113">Ez lehetővé teszi, hogy ezek a feladatok egy másik számítási csomóponton átütemezve legyenek.</span><span class="sxs-lookup"><span data-stu-id="79aa7-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="79aa7-114">A feladatok megszüntetése és eltávolítása a projekt várólistájából.</span><span class="sxs-lookup"><span data-stu-id="79aa7-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="79aa7-115">Az ilyen módon leállított feladatok nem lesznek átütemezve.</span><span class="sxs-lookup"><span data-stu-id="79aa7-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="79aa7-116">Várjon, amíg a program végrehajtja az összes folyamatban lévő feladatot, majd tiltsa le a tevékenységek ütemezését a számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="79aa7-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="79aa7-117">Várjon, amíg az összes futó tevékenység le nem fejeződik, és az összes adatmegőrzési időszak lejár, majd tiltsa le a tevékenység ütemezése beállítást a számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="79aa7-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="79aa7-118">Példák</span><span class="sxs-lookup"><span data-stu-id="79aa7-118">EXAMPLES</span></span>

### <span data-ttu-id="79aa7-119">1. példa: a tevékenység ütemezése le van tiltva egy számítási csomóponton</span><span class="sxs-lookup"><span data-stu-id="79aa7-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="79aa7-120">Ezek a parancsok letiltják a tevékenységek ütemtervét a számítási csomópont TVM – 1783593343_34 – 20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="79aa7-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="79aa7-121">Ehhez a példa első parancsa létrehoz egy objektumot a kötegelt fiók contosobatchaccount tartozó fiók kulcsaihoz.</span><span class="sxs-lookup"><span data-stu-id="79aa7-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="79aa7-122">Ez az objektum hivatkozás a $context nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="79aa7-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="79aa7-123">A második parancs ezt az objektumot használja, és a **disable-AzBatchComputeNodeScheduling** parancsmag segítségével csatlakozik a Pool myPool, és letilthatja a TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="79aa7-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="79aa7-124">Mivel a *DisableComputeNodeSchedulingOptions* paraméter nem szerepel a számítási csomóponton jelenleg futó feladatok újravárólistájában.</span><span class="sxs-lookup"><span data-stu-id="79aa7-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="79aa7-125">2. példa: a tevékenységek ütemezésének letiltása a teljes számítási csomóponton a készletben</span><span class="sxs-lookup"><span data-stu-id="79aa7-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="79aa7-126">Ezekkel a parancsokkal letilthatja a tevékenységek ütemezését a köteg-Pool06 lévő összes számítógép-csomóponton.</span><span class="sxs-lookup"><span data-stu-id="79aa7-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="79aa7-127">A feladat végrehajtásához a példa első parancsa létrehoz egy objektumot a kötegelt fiók contosobatchaccount tartozó fiók kulcsaihoz.</span><span class="sxs-lookup"><span data-stu-id="79aa7-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="79aa7-128">Ez az objektum hivatkozás a $context nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="79aa7-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="79aa7-129">A példában szereplő második parancs az objektum-hivatkozással és a **Get-AzBatchComputeNode** a Pool06 található összes számítási csomópont gyűjteményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="79aa7-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="79aa7-130">A gyűjtemény ezután a **Letiltva, majd a le-AzBatchComputeNodeScheduling** parancsmaggal letilthatja a tevékenységek ütemezését a gyűjtemény egyes számítási csomópontjain.</span><span class="sxs-lookup"><span data-stu-id="79aa7-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="79aa7-131">Mivel a *DisableComputeNodeSchedulingOptions* paraméter nem szerepel a számítási csomópontokon jelenleg futó feladatok újravárólistájában.</span><span class="sxs-lookup"><span data-stu-id="79aa7-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="79aa7-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79aa7-132">PARAMETERS</span></span>

### <span data-ttu-id="79aa7-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="79aa7-133">-BatchContext</span></span>
<span data-ttu-id="79aa7-134">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="79aa7-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="79aa7-135">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="79aa7-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="79aa7-136">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="79aa7-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="79aa7-137">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="79aa7-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="79aa7-138">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="79aa7-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="79aa7-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="79aa7-139">-ComputeNode</span></span>
<span data-ttu-id="79aa7-140">A számítási csomópontra mutató objektum hivatkozását adja meg, ahol a tevékenység ütemezése le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="79aa7-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="79aa7-141">Ez az objektum hivatkozás az Get-AzBatchComputeNode parancsmag használatával jön létre, és a visszaadott számítási csomópont objektumát egy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="79aa7-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="79aa7-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79aa7-142">-DefaultProfile</span></span>
<span data-ttu-id="79aa7-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79aa7-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79aa7-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="79aa7-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="79aa7-145">Itt adhatja meg, hogy ez a parancsmag hogyan foglalkozik az ütemezés letiltására szolgáló számítógép-csomóponton jelenleg futó feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="79aa7-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="79aa7-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="79aa7-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79aa7-147">Újravárólista.</span><span class="sxs-lookup"><span data-stu-id="79aa7-147">Requeue.</span></span>
<span data-ttu-id="79aa7-148">A feladatok azonnal leálltak, és visszatért a projekt várólistájába.</span><span class="sxs-lookup"><span data-stu-id="79aa7-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="79aa7-149">Ezzel lehetővé teszi, hogy a tevékenységeket egy másik számítási csomóponton át lehessen ütemezni.</span><span class="sxs-lookup"><span data-stu-id="79aa7-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="79aa7-150">Ez az alapértelmezett érték.</span><span class="sxs-lookup"><span data-stu-id="79aa7-150">This is the default value.</span></span> 
- <span data-ttu-id="79aa7-151">Lezáró.</span><span class="sxs-lookup"><span data-stu-id="79aa7-151">Terminate.</span></span>
<span data-ttu-id="79aa7-152">A feladatok azonnal megszűnnek, és törlődnek a projekt várólistájáról.</span><span class="sxs-lookup"><span data-stu-id="79aa7-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="79aa7-153">Ezek a feladatok nem lesznek átütemezve.</span><span class="sxs-lookup"><span data-stu-id="79aa7-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="79aa7-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="79aa7-154">TaskCompletion.</span></span>
<span data-ttu-id="79aa7-155">A jelenleg futó feladatok csak akkor fognak megjelenni, ha a tevékenység ütemezése le van tiltva a számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="79aa7-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="79aa7-156">Ebben a csomópontban nem lesz új tevékenység ütemezve.</span><span class="sxs-lookup"><span data-stu-id="79aa7-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="79aa7-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="79aa7-157">RetainedData.</span></span>
<span data-ttu-id="79aa7-158">A jelenleg futó feladatok teljes körűek és az adatmegőrzési időszakok a számítási csomóponton le lesznek tiltva, mielőtt a tevékenység ütemezése le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="79aa7-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="79aa7-159">Ebben a csomópontban nem lesz új tevékenység ütemezve.</span><span class="sxs-lookup"><span data-stu-id="79aa7-159">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="79aa7-160">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="79aa7-160">-Id</span></span>
<span data-ttu-id="79aa7-161">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, ahol a tevékenység ütemezése le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="79aa7-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="79aa7-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="79aa7-162">-PoolId</span></span>
<span data-ttu-id="79aa7-163">Annak a kötegelt készletnek az AZONOSÍTÓját adja meg, amely a tevékenység ütemezése letiltott számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="79aa7-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="79aa7-164">Ha a *PoolId* paramétert használja, a *ComputeNode* paramétert ne használja ugyanezt a parancsot.</span><span class="sxs-lookup"><span data-stu-id="79aa7-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="79aa7-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79aa7-165">CommonParameters</span></span>
<span data-ttu-id="79aa7-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79aa7-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79aa7-167">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="79aa7-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79aa7-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79aa7-168">INPUTS</span></span>

### <span data-ttu-id="79aa7-169">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="79aa7-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="79aa7-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="79aa7-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="79aa7-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79aa7-171">OUTPUTS</span></span>

### <span data-ttu-id="79aa7-172">System. Void</span><span class="sxs-lookup"><span data-stu-id="79aa7-172">System.Void</span></span>

## <span data-ttu-id="79aa7-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79aa7-173">NOTES</span></span>

## <span data-ttu-id="79aa7-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79aa7-174">RELATED LINKS</span></span>

[<span data-ttu-id="79aa7-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="79aa7-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="79aa7-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="79aa7-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


