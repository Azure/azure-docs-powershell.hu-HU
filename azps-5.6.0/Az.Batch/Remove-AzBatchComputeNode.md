---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 7e2b2bca042573ec96fefdf85e5077ec1138d1da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920626"
---
# <span data-ttu-id="6a7b6-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6a7b6-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="6a7b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7b6-103">Eltávolítja a számítási csomópontokat egy készletből.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="6a7b6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a7b6-104">SYNTAX</span></span>

### <span data-ttu-id="6a7b6-105">Id (Default)</span><span class="sxs-lookup"><span data-stu-id="6a7b6-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a7b6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6a7b6-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a7b6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a7b6-107">DESCRIPTION</span></span>
<span data-ttu-id="6a7b6-108">A **Remove-AzBatchComputeNode** parancsmag eltávolítja az Azure Batch számítási csomópontokat a készletből.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="6a7b6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a7b6-109">EXAMPLES</span></span>

### <span data-ttu-id="6a7b6-110">1. példa: Számítási csomópont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6a7b6-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="6a7b6-111">Ez a parancs eltávolítja azt a számítási csomópontot, amely a megadott azonosítót tartalmazza a Készletazonosító készletből.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="6a7b6-112">A parancs az elosztás megszüntetése lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="6a7b6-113">Az időkorrektás átméretezése 10 perc.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="6a7b6-114">2. példa: Számítási csomópont eltávolítása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="6a7b6-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="6a7b6-115">Ez a parancs lekérte azt a számítási csomópontot, amely a készletből az id Pool07 azonosítóval rendelkezik a Get-AzBatchComputeNode parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="6a7b6-116">A parancs a folyamat segítségével átadja a csomópontot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="6a7b6-117">Az aktuális parancsmag eltávolítja a számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="6a7b6-118">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6a7b6-119">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="6a7b6-120">3. példa: Több csomópont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6a7b6-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="6a7b6-121">Ez a parancs eltávolít két számítási csomópontot abból a készletből, amely az ID Pool07 azonosítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="6a7b6-122">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6a7b6-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a7b6-123">PARAMETERS</span></span>

### <span data-ttu-id="6a7b6-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6a7b6-124">-BatchContext</span></span>
<span data-ttu-id="6a7b6-125">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6a7b6-126">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6a7b6-127">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6a7b6-128">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6a7b6-129">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6a7b6-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="6a7b6-130">-ComputeNode</span></span>
<span data-ttu-id="6a7b6-131">A parancsmag által eltávolított számítási csomópontot képviselő **PSComputeNode-objektumot** adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6a7b6-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="6a7b6-132">-DeallocationOption</span></span>
<span data-ttu-id="6a7b6-133">Megadja a parancsmag eltávolítási műveletének áthelyezési beállítását.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="6a7b6-134">Az alapértelmezett érték az Újrarekesz.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="6a7b6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a7b6-135">-DefaultProfile</span></span>
<span data-ttu-id="6a7b6-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a7b6-137">-Force</span><span class="sxs-lookup"><span data-stu-id="6a7b6-137">-Force</span></span>
<span data-ttu-id="6a7b6-138">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6a7b6-139">-Ids</span><span class="sxs-lookup"><span data-stu-id="6a7b6-139">-Ids</span></span>
<span data-ttu-id="6a7b6-140">A parancsmag által a készletből eltávolítandó számítási csomópontok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="6a7b6-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="6a7b6-141">-PoolId</span></span>
<span data-ttu-id="6a7b6-142">Annak a készletnek az azonosítóját adja meg, amely a parancsmag által eltávolított számítási csomópontokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6a7b6-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="6a7b6-143">-ResizeTimeout</span></span>
<span data-ttu-id="6a7b6-144">A számítási csomópontok készletből való eltávolításának idő-időintervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="6a7b6-145">Az alapértelmezett érték 10 perc.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="6a7b6-146">A minimális érték 5 perc.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="6a7b6-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a7b6-147">-Confirm</span></span>
<span data-ttu-id="6a7b6-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a7b6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a7b6-149">-WhatIf</span></span>
<span data-ttu-id="6a7b6-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a7b6-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a7b6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7b6-152">CommonParameters</span></span>
<span data-ttu-id="6a7b6-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a7b6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7b6-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a7b6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7b6-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a7b6-155">INPUTS</span></span>

### <span data-ttu-id="6a7b6-156">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="6a7b6-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="6a7b6-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6a7b6-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6a7b6-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a7b6-158">OUTPUTS</span></span>

### <span data-ttu-id="6a7b6-159">System.Void</span><span class="sxs-lookup"><span data-stu-id="6a7b6-159">System.Void</span></span>

## <span data-ttu-id="6a7b6-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a7b6-160">NOTES</span></span>

## <span data-ttu-id="6a7b6-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a7b6-161">RELATED LINKS</span></span>

[<span data-ttu-id="6a7b6-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6a7b6-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6a7b6-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6a7b6-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="6a7b6-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6a7b6-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


