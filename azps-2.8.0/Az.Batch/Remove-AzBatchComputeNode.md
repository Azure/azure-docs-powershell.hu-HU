---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: e871b32840db3802fc2bb2fb87871e37cf95dcfe
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847842"
---
# <span data-ttu-id="24a90-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="24a90-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="24a90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24a90-102">SYNOPSIS</span></span>
<span data-ttu-id="24a90-103">Eltávolítja a kiszámított csomópontokat a készletből.</span><span class="sxs-lookup"><span data-stu-id="24a90-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="24a90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24a90-104">SYNTAX</span></span>

### <span data-ttu-id="24a90-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24a90-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24a90-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="24a90-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24a90-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="24a90-107">DESCRIPTION</span></span>
<span data-ttu-id="24a90-108">A **Remove-AzBatchComputeNode** parancsmag eltávolítja az Azure batch-számítási csomópontokat egy készletből.</span><span class="sxs-lookup"><span data-stu-id="24a90-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="24a90-109">Példák</span><span class="sxs-lookup"><span data-stu-id="24a90-109">EXAMPLES</span></span>

### <span data-ttu-id="24a90-110">1. példa: számítási csomópont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="24a90-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="24a90-111">Ez a parancs eltávolítja az azonosító Pool07 tartalmazó készletből a megadott azonosítót tartalmazó számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="24a90-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="24a90-112">A parancs a lezáró visszafoglalási lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="24a90-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="24a90-113">Az átméretezési időtúllépés 10 perc.</span><span class="sxs-lookup"><span data-stu-id="24a90-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="24a90-114">2. példa: számítási csomópont eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="24a90-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="24a90-115">Ez a parancs azt a számítási csomópontot adja eredményül, amely a megadott azonosítót tartalmazza a Pool07 AZONOSÍTÓJÚ készletből, és az Get-AzBatchComputeNode parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="24a90-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="24a90-116">A parancs a csővezetéken keresztül továbbítja a csomópontot az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="24a90-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="24a90-117">Az aktuális parancsmag eltávolítja a számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="24a90-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="24a90-118">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="24a90-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="24a90-119">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24a90-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="24a90-120">3. példa: több csomópont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="24a90-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="24a90-121">Ez a parancs eltávolítja a két számítási csomópontot az azonosító Pool07 tartalmazó készletből.</span><span class="sxs-lookup"><span data-stu-id="24a90-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="24a90-122">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24a90-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="24a90-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24a90-123">PARAMETERS</span></span>

### <span data-ttu-id="24a90-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="24a90-124">-BatchContext</span></span>
<span data-ttu-id="24a90-125">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="24a90-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="24a90-126">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="24a90-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="24a90-127">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="24a90-127">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="24a90-128">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="24a90-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="24a90-129">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="24a90-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="24a90-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="24a90-130">-ComputeNode</span></span>
<span data-ttu-id="24a90-131">Azt a **PSComputeNode** -objektumot adja meg, amely a parancsmag által eltávolított számítási csomópontot jelöli.</span><span class="sxs-lookup"><span data-stu-id="24a90-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="24a90-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="24a90-132">-DeallocationOption</span></span>
<span data-ttu-id="24a90-133">A parancsmag által elinduló eltávolítási művelet kiosztási beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="24a90-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="24a90-134">Az alapértelmezett érték az újravárólista.</span><span class="sxs-lookup"><span data-stu-id="24a90-134">The default value is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a90-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a90-135">-DefaultProfile</span></span>
<span data-ttu-id="24a90-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24a90-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24a90-137">-Force</span><span class="sxs-lookup"><span data-stu-id="24a90-137">-Force</span></span>
<span data-ttu-id="24a90-138">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="24a90-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a90-139">-IDS</span><span class="sxs-lookup"><span data-stu-id="24a90-139">-Ids</span></span>
<span data-ttu-id="24a90-140">A számítási csomópontok tömbök sorát adja meg, amelyeket a parancsmag eltávolít a készletből.</span><span class="sxs-lookup"><span data-stu-id="24a90-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a90-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="24a90-141">-PoolId</span></span>
<span data-ttu-id="24a90-142">A parancsmag által eltávolított számítási csomópontokat tartalmazó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="24a90-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="24a90-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="24a90-143">-ResizeTimeout</span></span>
<span data-ttu-id="24a90-144">A számítási csomópontoknak a készletből való eltávolításának időtúllépési intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="24a90-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="24a90-145">Az alapértelmezett érték 10 perc.</span><span class="sxs-lookup"><span data-stu-id="24a90-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="24a90-146">A minimális érték 5 perc.</span><span class="sxs-lookup"><span data-stu-id="24a90-146">The minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a90-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24a90-147">-Confirm</span></span>
<span data-ttu-id="24a90-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24a90-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a90-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24a90-149">-WhatIf</span></span>
<span data-ttu-id="24a90-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24a90-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24a90-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24a90-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a90-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a90-152">CommonParameters</span></span>
<span data-ttu-id="24a90-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24a90-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a90-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a90-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a90-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a90-155">INPUTS</span></span>

### <span data-ttu-id="24a90-156">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="24a90-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="24a90-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="24a90-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="24a90-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a90-158">OUTPUTS</span></span>

### <span data-ttu-id="24a90-159">System. Void</span><span class="sxs-lookup"><span data-stu-id="24a90-159">System.Void</span></span>

## <span data-ttu-id="24a90-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24a90-160">NOTES</span></span>

## <span data-ttu-id="24a90-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24a90-161">RELATED LINKS</span></span>

[<span data-ttu-id="24a90-162">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="24a90-162">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="24a90-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="24a90-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="24a90-164">Újraindítás – AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="24a90-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

