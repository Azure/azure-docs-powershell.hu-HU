---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194933"
---
# <span data-ttu-id="16d57-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="16d57-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="16d57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16d57-102">SYNOPSIS</span></span>
<span data-ttu-id="16d57-103">Elkezdi átméretezni a készletet.</span><span class="sxs-lookup"><span data-stu-id="16d57-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="16d57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16d57-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16d57-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="16d57-105">DESCRIPTION</span></span>
<span data-ttu-id="16d57-106">A **Start-AzBatchPoolResize** parancsmag az Azure köteg-átméretezési műveletet kezdi a készletre.</span><span class="sxs-lookup"><span data-stu-id="16d57-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="16d57-107">Példák</span><span class="sxs-lookup"><span data-stu-id="16d57-107">EXAMPLES</span></span>

### <span data-ttu-id="16d57-108">1. példa: a készlet átméretezése 12 csomópontra</span><span class="sxs-lookup"><span data-stu-id="16d57-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="16d57-109">A parancs átméretezési műveletet indít az azonosító ContosoPool06 tartalmazó készleten.</span><span class="sxs-lookup"><span data-stu-id="16d57-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="16d57-110">A művelet célja 12 dedikált kiszámított csomópont.</span><span class="sxs-lookup"><span data-stu-id="16d57-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="16d57-111">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="16d57-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="16d57-112">2. példa: a készlet átméretezése kifoglalási beállítás használatával</span><span class="sxs-lookup"><span data-stu-id="16d57-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="16d57-113">Ez a parancsmag átméretezi a készletet öt dedikált kiszámított csomópontra.</span><span class="sxs-lookup"><span data-stu-id="16d57-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="16d57-114">A parancs a Get-AzBatchPool parancsmag használatával az azonosító ContosoPool06 tartalmazó készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="16d57-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="16d57-115">A parancs a pipeline operátorral továbbítja a készlet objektumát az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="16d57-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="16d57-116">A parancs átméretezési műveletet indít a készleten.</span><span class="sxs-lookup"><span data-stu-id="16d57-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="16d57-117">A cél öt külön kiszámított csomópont.</span><span class="sxs-lookup"><span data-stu-id="16d57-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="16d57-118">A parancs egy óra elteltével adja meg az időtúllépési időszakot.</span><span class="sxs-lookup"><span data-stu-id="16d57-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="16d57-119">A parancs a leállítási lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d57-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="16d57-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16d57-120">PARAMETERS</span></span>

### <span data-ttu-id="16d57-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="16d57-121">-BatchContext</span></span>
<span data-ttu-id="16d57-122">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="16d57-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="16d57-123">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="16d57-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="16d57-124">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="16d57-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="16d57-125">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="16d57-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="16d57-126">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="16d57-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="16d57-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="16d57-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="16d57-128">A parancsmag által elinduló átméretezési művelet kiosztási beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d57-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="16d57-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d57-129">-DefaultProfile</span></span>
<span data-ttu-id="16d57-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16d57-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16d57-131">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="16d57-131">-Id</span></span>
<span data-ttu-id="16d57-132">A parancsmag által átméretezett készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d57-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="16d57-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="16d57-133">-ResizeTimeout</span></span>
<span data-ttu-id="16d57-134">Az átméretezési művelet időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d57-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="16d57-135">Ha a készlet jelenleg nem éri el a cél méretét, az átméretezés művelet leáll.</span><span class="sxs-lookup"><span data-stu-id="16d57-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="16d57-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="16d57-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="16d57-137">A célhoz rendelt számítási csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="16d57-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="16d57-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="16d57-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="16d57-139">Az alacsony prioritású számítási csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="16d57-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="16d57-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d57-140">CommonParameters</span></span>
<span data-ttu-id="16d57-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16d57-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d57-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="16d57-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d57-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16d57-143">INPUTS</span></span>

### <span data-ttu-id="16d57-144">System. String</span><span class="sxs-lookup"><span data-stu-id="16d57-144">System.String</span></span>

### <span data-ttu-id="16d57-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="16d57-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="16d57-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16d57-146">OUTPUTS</span></span>

### <span data-ttu-id="16d57-147">System. Void</span><span class="sxs-lookup"><span data-stu-id="16d57-147">System.Void</span></span>

## <span data-ttu-id="16d57-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16d57-148">NOTES</span></span>

## <span data-ttu-id="16d57-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16d57-149">RELATED LINKS</span></span>

[<span data-ttu-id="16d57-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="16d57-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="16d57-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="16d57-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="16d57-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="16d57-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="16d57-153">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="16d57-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
