---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: a50329620944aa18458c3bb667e3a95ff45bc21f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025551"
---
# <span data-ttu-id="8f110-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8f110-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="8f110-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f110-102">SYNOPSIS</span></span>
<span data-ttu-id="8f110-103">Egy köteg számítási csomópontját a készletből kapja.</span><span class="sxs-lookup"><span data-stu-id="8f110-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="8f110-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f110-104">SYNTAX</span></span>

### <span data-ttu-id="8f110-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8f110-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f110-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="8f110-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f110-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="8f110-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f110-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f110-108">DESCRIPTION</span></span>
<span data-ttu-id="8f110-109">A **Get-AzBatchComputeNode** parancsmag Azure-köteg-számítási csomópontokat kap a készletből.</span><span class="sxs-lookup"><span data-stu-id="8f110-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="8f110-110">Adja meg a *PoolID* vagy a *Pool* paramétert.</span><span class="sxs-lookup"><span data-stu-id="8f110-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="8f110-111">Adja meg az *azonosító* paramétert egyetlen számítási csomópont beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="8f110-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="8f110-112">Adja meg a *szűrő* paramétert a nyitott adatprotokoll-(Open Data Protocol) OData megfelelő számítási csomópontok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="8f110-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="8f110-113">Példák</span><span class="sxs-lookup"><span data-stu-id="8f110-113">EXAMPLES</span></span>

### <span data-ttu-id="8f110-114">Példa 1: számítási csomópont beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="8f110-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="8f110-115">Ez a parancs beilleszti a TVM-2316545714_1-20150725t213220z AZONOSÍTÓJÚ számítási csomópontot az id-Pool06 tartalmazó készletből.</span><span class="sxs-lookup"><span data-stu-id="8f110-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="8f110-116">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="8f110-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8f110-117">2. példa: az összes tétlen számítási csomópont lekérése egy készletből</span><span class="sxs-lookup"><span data-stu-id="8f110-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :

Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM
IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="8f110-118">Ez a parancs a Pool06 AZONOSÍTÓJÚ készletben található összes tétlen számítási csomópontot megkapja.</span><span class="sxs-lookup"><span data-stu-id="8f110-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="8f110-119">A parancs a *szűrő* paraméter használatával adja meg az üresjárat állapotát.</span><span class="sxs-lookup"><span data-stu-id="8f110-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="8f110-120">3. példa: a megadott készlet minden számítási csomópontjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="8f110-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzBatchPool -Id "Pool07" -BatchContext $Context | Get-AzBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :


Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM

IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="8f110-121">Ez a parancs a Get-AzBatchPool parancsmag használatával az azonosító Pool07 tartalmazó készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="8f110-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="8f110-122">A parancs a csővezeték-kezelő segítségével átadja az adott készletet az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="8f110-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8f110-123">Ez a parancsmag a készlet összes csomópontját kiszámítja.</span><span class="sxs-lookup"><span data-stu-id="8f110-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="8f110-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f110-124">PARAMETERS</span></span>

### <span data-ttu-id="8f110-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8f110-125">-BatchContext</span></span>
<span data-ttu-id="8f110-126">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="8f110-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8f110-127">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="8f110-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8f110-128">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="8f110-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8f110-129">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="8f110-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8f110-130">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="8f110-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8f110-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f110-131">-DefaultProfile</span></span>
<span data-ttu-id="8f110-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f110-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f110-133">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="8f110-133">-Filter</span></span>
<span data-ttu-id="8f110-134">Egy OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8f110-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="8f110-135">Ez a parancsmag olyan számítási csomópontokat ad eredményül, amelyek megfelelnek a paraméter által megadott szűrőnek.</span><span class="sxs-lookup"><span data-stu-id="8f110-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="8f110-136">Ha nem ad meg szűrőt, ez a parancsmag a készlet összes számítási csomópontját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8f110-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f110-137">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8f110-137">-Id</span></span>
<span data-ttu-id="8f110-138">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyre a parancsmag a készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="8f110-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="8f110-139">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="8f110-139">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f110-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8f110-140">-MaxCount</span></span>
<span data-ttu-id="8f110-141">Az eredményül kapott számítási csomópontok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f110-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="8f110-142">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="8f110-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8f110-143">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="8f110-143">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f110-144">-Pool (Pool)</span><span class="sxs-lookup"><span data-stu-id="8f110-144">-Pool</span></span>
<span data-ttu-id="8f110-145">Itt adhatja meg a **PSCloudPool** objektumhoz tartozó medencét, amely a számítási csomópontokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8f110-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="8f110-146">**PSCloudPool** objektum beolvasásához használja az Get-AzBatchPool parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8f110-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f110-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="8f110-147">-PoolId</span></span>
<span data-ttu-id="8f110-148">A számítási csomópontokat tartalmazó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f110-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f110-149">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="8f110-149">-Select</span></span>
<span data-ttu-id="8f110-150">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8f110-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="8f110-151">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="8f110-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f110-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f110-152">CommonParameters</span></span>
<span data-ttu-id="8f110-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f110-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f110-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8f110-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f110-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f110-155">INPUTS</span></span>

### <span data-ttu-id="8f110-156">System. String</span><span class="sxs-lookup"><span data-stu-id="8f110-156">System.String</span></span>

### <span data-ttu-id="8f110-157">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="8f110-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="8f110-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8f110-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8f110-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f110-159">OUTPUTS</span></span>

### <span data-ttu-id="8f110-160">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="8f110-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="8f110-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f110-161">NOTES</span></span>

## <span data-ttu-id="8f110-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f110-162">RELATED LINKS</span></span>

[<span data-ttu-id="8f110-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8f110-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="8f110-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="8f110-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="8f110-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="8f110-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="8f110-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8f110-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="8f110-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8f110-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="8f110-168">Újraindítás – AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8f110-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="8f110-169">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8f110-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
