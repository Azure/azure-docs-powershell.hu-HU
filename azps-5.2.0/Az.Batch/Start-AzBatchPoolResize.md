---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352229"
---
# <span data-ttu-id="ef57e-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="ef57e-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="ef57e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef57e-102">SYNOPSIS</span></span>
<span data-ttu-id="ef57e-103">Kezd átméretezni egy készletet.</span><span class="sxs-lookup"><span data-stu-id="ef57e-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="ef57e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef57e-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef57e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef57e-105">DESCRIPTION</span></span>
<span data-ttu-id="ef57e-106">A **Start-AzBatchPoolResize** parancsmag elindít egy Azure Batch-átméretezési műveletet egy készleten.</span><span class="sxs-lookup"><span data-stu-id="ef57e-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="ef57e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef57e-107">EXAMPLES</span></span>

### <span data-ttu-id="ef57e-108">1. példa: Készlet átméretezése 12 csomópontra</span><span class="sxs-lookup"><span data-stu-id="ef57e-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="ef57e-109">Ez a parancs egy átméretezési műveletet kezd a ContosoPool06 azonosítójú készleten.</span><span class="sxs-lookup"><span data-stu-id="ef57e-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="ef57e-110">A művelet célja 12 dedikált számítási csomópont.</span><span class="sxs-lookup"><span data-stu-id="ef57e-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="ef57e-111">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="ef57e-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ef57e-112">2. példa: Készlet átméretezése áthelyezési beállítással</span><span class="sxs-lookup"><span data-stu-id="ef57e-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="ef57e-113">Ez a parancsmag átméretez egy készletet öt dedikált számítási csomópontra.</span><span class="sxs-lookup"><span data-stu-id="ef57e-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="ef57e-114">A parancs a ContosoPool06 azonosítót használó készletet a Get-AzBatchPool parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ef57e-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="ef57e-115">A parancs a folyamat műveleti operátorával átadja az objektumot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="ef57e-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ef57e-116">A parancs átméretezést kezd a készleten.</span><span class="sxs-lookup"><span data-stu-id="ef57e-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="ef57e-117">A cél öt dedikált számítási csomópont.</span><span class="sxs-lookup"><span data-stu-id="ef57e-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="ef57e-118">A parancs egyórás időkorrektot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ef57e-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="ef57e-119">A parancs a Terminate (Lezárás) elosztási lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef57e-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="ef57e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef57e-120">PARAMETERS</span></span>

### <span data-ttu-id="ef57e-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ef57e-121">-BatchContext</span></span>
<span data-ttu-id="ef57e-122">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="ef57e-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ef57e-123">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="ef57e-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ef57e-124">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="ef57e-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ef57e-125">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="ef57e-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ef57e-126">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="ef57e-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ef57e-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="ef57e-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="ef57e-128">Megadja a parancsmag által elindított átméretezési művelet áthelyezési beállítását.</span><span class="sxs-lookup"><span data-stu-id="ef57e-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ef57e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef57e-129">-DefaultProfile</span></span>
<span data-ttu-id="ef57e-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef57e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef57e-131">-Id</span><span class="sxs-lookup"><span data-stu-id="ef57e-131">-Id</span></span>
<span data-ttu-id="ef57e-132">A parancsmag által átméretezett készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef57e-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef57e-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="ef57e-133">-ResizeTimeout</span></span>
<span data-ttu-id="ef57e-134">Az átméretezési művelet időkorrekciós időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef57e-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="ef57e-135">Ha a készlet ez idő alatt nem éri el a célméretet, az átméretezés leáll.</span><span class="sxs-lookup"><span data-stu-id="ef57e-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="ef57e-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="ef57e-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="ef57e-137">A célként dedikált számítási csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="ef57e-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef57e-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="ef57e-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="ef57e-139">Az alacsony prioritású cél számítási csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="ef57e-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef57e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef57e-140">CommonParameters</span></span>
<span data-ttu-id="ef57e-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef57e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef57e-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef57e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef57e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef57e-143">INPUTS</span></span>

### <span data-ttu-id="ef57e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ef57e-144">System.String</span></span>

### <span data-ttu-id="ef57e-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ef57e-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ef57e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef57e-146">OUTPUTS</span></span>

### <span data-ttu-id="ef57e-147">System.Void</span><span class="sxs-lookup"><span data-stu-id="ef57e-147">System.Void</span></span>

## <span data-ttu-id="ef57e-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef57e-148">NOTES</span></span>

## <span data-ttu-id="ef57e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef57e-149">RELATED LINKS</span></span>

[<span data-ttu-id="ef57e-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ef57e-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ef57e-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ef57e-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="ef57e-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="ef57e-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="ef57e-153">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ef57e-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
