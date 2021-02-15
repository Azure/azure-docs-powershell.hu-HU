---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: a50329620944aa18458c3bb667e3a95ff45bc21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164354"
---
# <span data-ttu-id="69dc3-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="69dc3-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="69dc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="69dc3-103">Köteg számítási csomópontokat kap egy készletből.</span><span class="sxs-lookup"><span data-stu-id="69dc3-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="69dc3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69dc3-104">SYNTAX</span></span>

### <span data-ttu-id="69dc3-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69dc3-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69dc3-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="69dc3-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69dc3-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="69dc3-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69dc3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69dc3-108">DESCRIPTION</span></span>
<span data-ttu-id="69dc3-109">A **Get-AzBatchComputeNode** parancsmag az Azure Batch számítási csomópontokat kap egy készletből.</span><span class="sxs-lookup"><span data-stu-id="69dc3-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="69dc3-110">Adja meg a *PoolID* vagy *a Pool paramétert.*</span><span class="sxs-lookup"><span data-stu-id="69dc3-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="69dc3-111">Adja meg *az Azonosító* paramétert egyetlen számítási csomópont be szereznie.</span><span class="sxs-lookup"><span data-stu-id="69dc3-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="69dc3-112">Adja meg *a Szűrő* paramétert az OData-szűrőnek megfelelő számítási csomópontok be szereznie.</span><span class="sxs-lookup"><span data-stu-id="69dc3-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="69dc3-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69dc3-113">EXAMPLES</span></span>

### <span data-ttu-id="69dc3-114">1. példa: Számítási csomópont lekérte azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="69dc3-114">Example 1: Get a compute node by ID</span></span>
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

<span data-ttu-id="69dc3-115">Ez a parancs a tvm-2316545714_1-20150725t21320z azonosítójú számítási csomópontot a Pool06 azonosítókészletből kapja meg.</span><span class="sxs-lookup"><span data-stu-id="69dc3-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="69dc3-116">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="69dc3-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="69dc3-117">2. példa: Az összes üresjárati számítási csomópont behozása egy készletből</span><span class="sxs-lookup"><span data-stu-id="69dc3-117">Example 2: Get all idle compute nodes from a pool</span></span>
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

<span data-ttu-id="69dc3-118">Ez a parancs az id Pool06 azonosítót tartalmazó készletben található összes üresjárati számítási csomópontot megkapja.</span><span class="sxs-lookup"><span data-stu-id="69dc3-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="69dc3-119">A parancs az üresjárati állapotot adja meg a Szűrő *paraméter* használatával.</span><span class="sxs-lookup"><span data-stu-id="69dc3-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="69dc3-120">3. példa: Az összes számítási csomópont lekérte egy adott készletben</span><span class="sxs-lookup"><span data-stu-id="69dc3-120">Example 3: Get all compute nodes in a specified pool</span></span>
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

<span data-ttu-id="69dc3-121">Ez a parancs a készletet, amely a Pool07 azonosítót használja a Get-AzBatchPool parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="69dc3-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="69dc3-122">A parancs a folyamat műveleti operátorával átadja a készletet az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="69dc3-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="69dc3-123">Ez a parancsmag az összes számítási csomópontot ebből a készletből kapja.</span><span class="sxs-lookup"><span data-stu-id="69dc3-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="69dc3-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69dc3-124">PARAMETERS</span></span>

### <span data-ttu-id="69dc3-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="69dc3-125">-BatchContext</span></span>
<span data-ttu-id="69dc3-126">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="69dc3-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="69dc3-127">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="69dc3-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="69dc3-128">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="69dc3-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="69dc3-129">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="69dc3-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="69dc3-130">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="69dc3-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="69dc3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69dc3-131">-DefaultProfile</span></span>
<span data-ttu-id="69dc3-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69dc3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69dc3-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="69dc3-133">-Filter</span></span>
<span data-ttu-id="69dc3-134">OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="69dc3-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="69dc3-135">Ez a parancsmag olyan számítási csomópontokat ad vissza, amelyek megfelelnek a paraméter által megadott szűrőnek.</span><span class="sxs-lookup"><span data-stu-id="69dc3-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="69dc3-136">Ha nem ad meg szűrőt, ez a parancsmag a készlet összes számítási csomópontját visszaadja.</span><span class="sxs-lookup"><span data-stu-id="69dc3-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="69dc3-137">-Id</span><span class="sxs-lookup"><span data-stu-id="69dc3-137">-Id</span></span>
<span data-ttu-id="69dc3-138">Annak a számítási csomópontnak az azonosítója, amelyből a parancsmag a készletből kijön.</span><span class="sxs-lookup"><span data-stu-id="69dc3-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="69dc3-139">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="69dc3-139">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="69dc3-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="69dc3-140">-MaxCount</span></span>
<span data-ttu-id="69dc3-141">Azt adja meg, hogy legfeljebb hány számítási csomópontot kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="69dc3-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="69dc3-142">Ha nullát (0) vagy kisebb értéket ad meg, a parancsmag nem használ felső korlátot.</span><span class="sxs-lookup"><span data-stu-id="69dc3-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="69dc3-143">Az alapértelmezett érték 1000.</span><span class="sxs-lookup"><span data-stu-id="69dc3-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="69dc3-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="69dc3-144">-Pool</span></span>
<span data-ttu-id="69dc3-145">A számítási csomópontokat tartalmazó **PSCloudPool-objektumot** adja meg.</span><span class="sxs-lookup"><span data-stu-id="69dc3-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="69dc3-146">**PSCloudPool-objektum** beszerzéséhez használja a Get-AzBatchPool parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="69dc3-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="69dc3-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="69dc3-147">-PoolId</span></span>
<span data-ttu-id="69dc3-148">A számítási csomópontokat tartalmazó készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="69dc3-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="69dc3-149">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="69dc3-149">-Select</span></span>
<span data-ttu-id="69dc3-150">OData-választó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="69dc3-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="69dc3-151">A paraméter értékét megadva az összes objektumtulajdonság helyett konkrét tulajdonságokat kap.</span><span class="sxs-lookup"><span data-stu-id="69dc3-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="69dc3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69dc3-152">CommonParameters</span></span>
<span data-ttu-id="69dc3-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69dc3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69dc3-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69dc3-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69dc3-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69dc3-155">INPUTS</span></span>

### <span data-ttu-id="69dc3-156">System.String</span><span class="sxs-lookup"><span data-stu-id="69dc3-156">System.String</span></span>

### <span data-ttu-id="69dc3-157">Microsoft.Azure.Commands.Bat. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="69dc3-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="69dc3-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="69dc3-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="69dc3-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69dc3-159">OUTPUTS</span></span>

### <span data-ttu-id="69dc3-160">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="69dc3-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="69dc3-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69dc3-161">NOTES</span></span>

## <span data-ttu-id="69dc3-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69dc3-162">RELATED LINKS</span></span>

[<span data-ttu-id="69dc3-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="69dc3-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="69dc3-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="69dc3-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="69dc3-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="69dc3-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="69dc3-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="69dc3-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="69dc3-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="69dc3-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="69dc3-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="69dc3-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="69dc3-169">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="69dc3-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
