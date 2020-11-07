---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: 6350505efe3f3e7c571fee6940cf678706c4fc7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679893"
---
# <span data-ttu-id="2a8cd-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="2a8cd-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="2a8cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a8cd-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8cd-103">Eltávolítja a kiszámított csomópontokat a készletből.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a8cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a8cd-104">SYNTAX</span></span>

### <span data-ttu-id="2a8cd-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a8cd-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a8cd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2a8cd-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a8cd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a8cd-107">DESCRIPTION</span></span>
<span data-ttu-id="2a8cd-108">A **Remove-AzureBatchComputeNode** parancsmag eltávolítja az Azure batch-számítási csomópontokat egy készletből.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="2a8cd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2a8cd-109">EXAMPLES</span></span>

### <span data-ttu-id="2a8cd-110">1. példa: számítási csomópont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2a8cd-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="2a8cd-111">Ez a parancs eltávolítja az azonosító Pool07 tartalmazó készletből a megadott azonosítót tartalmazó számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="2a8cd-112">A parancs a lezáró visszafoglalási lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="2a8cd-113">Az átméretezési időtúllépés 10 perc.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="2a8cd-114">2. példa: számítási csomópont eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="2a8cd-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="2a8cd-115">Ez a parancs azt a számítási csomópontot adja eredményül, amely a megadott azonosítót tartalmazza a Pool07 AZONOSÍTÓJÚ készletből, és az Get-AzureBatchComputeNode parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="2a8cd-116">A parancs a csővezetéken keresztül továbbítja a csomópontot az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="2a8cd-117">Az aktuális parancsmag eltávolítja a számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="2a8cd-118">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2a8cd-119">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="2a8cd-120">3. példa: több csomópont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2a8cd-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="2a8cd-121">Ez a parancs eltávolítja a két számítási csomópontot az azonosító Pool07 tartalmazó készletből.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="2a8cd-122">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2a8cd-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a8cd-123">PARAMETERS</span></span>

### <span data-ttu-id="2a8cd-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2a8cd-124">-BatchContext</span></span>
<span data-ttu-id="2a8cd-125">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2a8cd-126">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2a8cd-127">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2a8cd-128">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2a8cd-129">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2a8cd-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="2a8cd-130">-ComputeNode</span></span>
<span data-ttu-id="2a8cd-131">Azt a **PSComputeNode** -objektumot adja meg, amely a parancsmag által eltávolított számítási csomópontot jelöli.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2a8cd-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="2a8cd-132">-DeallocationOption</span></span>
<span data-ttu-id="2a8cd-133">A parancsmag által elinduló eltávolítási művelet kiosztási beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="2a8cd-134">Az alapértelmezett érték az újravárólista.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-134">The default value is Requeue.</span></span>

```yaml
Type: ComputeNodeDeallocationOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8cd-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8cd-135">-DefaultProfile</span></span>
<span data-ttu-id="2a8cd-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a8cd-137">-Force</span><span class="sxs-lookup"><span data-stu-id="2a8cd-137">-Force</span></span>
<span data-ttu-id="2a8cd-138">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8cd-139">-IDS</span><span class="sxs-lookup"><span data-stu-id="2a8cd-139">-Ids</span></span>
<span data-ttu-id="2a8cd-140">A számítási csomópontok tömbök sorát adja meg, amelyeket a parancsmag eltávolít a készletből.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8cd-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="2a8cd-141">-PoolId</span></span>
<span data-ttu-id="2a8cd-142">A parancsmag által eltávolított számítási csomópontokat tartalmazó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2a8cd-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="2a8cd-143">-ResizeTimeout</span></span>
<span data-ttu-id="2a8cd-144">A számítási csomópontoknak a készletből való eltávolításának időtúllépési intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="2a8cd-145">Az alapértelmezett érték 10 perc.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="2a8cd-146">A minimális érték 5 perc.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-146">The minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8cd-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2a8cd-147">-Confirm</span></span>
<span data-ttu-id="2a8cd-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8cd-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a8cd-149">-WhatIf</span></span>
<span data-ttu-id="2a8cd-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a8cd-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a8cd-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8cd-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8cd-152">CommonParameters</span></span>
<span data-ttu-id="2a8cd-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a8cd-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8cd-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a8cd-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8cd-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a8cd-155">INPUTS</span></span>

### <span data-ttu-id="2a8cd-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2a8cd-156">BatchAccountContext</span></span>
<span data-ttu-id="2a8cd-157">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2a8cd-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2a8cd-158">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="2a8cd-158">PSComputeNode</span></span>
<span data-ttu-id="2a8cd-159">A ' ComputeNode ' paraméter az "PSComputeNode" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2a8cd-159">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="2a8cd-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a8cd-160">OUTPUTS</span></span>

## <span data-ttu-id="2a8cd-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a8cd-161">NOTES</span></span>

## <span data-ttu-id="2a8cd-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a8cd-162">RELATED LINKS</span></span>

[<span data-ttu-id="2a8cd-163">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2a8cd-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2a8cd-164">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="2a8cd-164">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="2a8cd-165">Újraindítás – AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="2a8cd-165">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)


