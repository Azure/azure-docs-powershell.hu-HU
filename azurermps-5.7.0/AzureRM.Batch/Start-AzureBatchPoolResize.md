---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/start-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: b460eb4377f06cfa7348f06cdd60f2013e5b5e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493254"
---
# <span data-ttu-id="d0157-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="d0157-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="d0157-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0157-102">SYNOPSIS</span></span>
<span data-ttu-id="d0157-103">Elkezdi átméretezni a készletet.</span><span class="sxs-lookup"><span data-stu-id="d0157-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0157-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0157-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0157-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0157-105">DESCRIPTION</span></span>
<span data-ttu-id="d0157-106">A **Start-AzureBatchPoolResize** parancsmag az Azure köteg-átméretezési műveletet kezdi a készletre.</span><span class="sxs-lookup"><span data-stu-id="d0157-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="d0157-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d0157-107">EXAMPLES</span></span>

### <span data-ttu-id="d0157-108">1. példa: a készlet átméretezése 12 csomópontra</span><span class="sxs-lookup"><span data-stu-id="d0157-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="d0157-109">A parancs átméretezési műveletet indít az azonosító ContosoPool06 tartalmazó készleten.</span><span class="sxs-lookup"><span data-stu-id="d0157-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="d0157-110">A művelet célja 12 dedikált kiszámított csomópont.</span><span class="sxs-lookup"><span data-stu-id="d0157-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="d0157-111">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="d0157-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d0157-112">2. példa: a készlet átméretezése kifoglalási beállítás használatával</span><span class="sxs-lookup"><span data-stu-id="d0157-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="d0157-113">Ez a parancsmag átméretezi a készletet öt dedikált kiszámított csomópontra.</span><span class="sxs-lookup"><span data-stu-id="d0157-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="d0157-114">A parancs a Get-AzureBatchPool parancsmag használatával az azonosító ContosoPool06 tartalmazó készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="d0157-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="d0157-115">A parancs a pipeline operátorral továbbítja a készlet objektumát az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d0157-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d0157-116">A parancs átméretezési műveletet indít a készleten.</span><span class="sxs-lookup"><span data-stu-id="d0157-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="d0157-117">A cél öt külön kiszámított csomópont.</span><span class="sxs-lookup"><span data-stu-id="d0157-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="d0157-118">A parancs egy óra elteltével adja meg az időtúllépési időszakot.</span><span class="sxs-lookup"><span data-stu-id="d0157-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="d0157-119">A parancs a leállítási lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0157-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="d0157-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0157-120">PARAMETERS</span></span>

### <span data-ttu-id="d0157-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d0157-121">-BatchContext</span></span>
<span data-ttu-id="d0157-122">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="d0157-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d0157-123">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="d0157-123">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d0157-124">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="d0157-124">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d0157-125">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="d0157-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d0157-126">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="d0157-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d0157-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="d0157-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="d0157-128">A parancsmag által elinduló átméretezési művelet kiosztási beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0157-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d0157-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0157-129">-DefaultProfile</span></span>
<span data-ttu-id="d0157-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0157-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0157-131">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d0157-131">-Id</span></span>
<span data-ttu-id="d0157-132">A parancsmag által átméretezett készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0157-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0157-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="d0157-133">-ResizeTimeout</span></span>
<span data-ttu-id="d0157-134">Az átméretezési művelet időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0157-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="d0157-135">Ha a készlet jelenleg nem éri el a cél méretét, az átméretezés művelet leáll.</span><span class="sxs-lookup"><span data-stu-id="d0157-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="d0157-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="d0157-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="d0157-137">A célhoz rendelt számítási csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="d0157-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0157-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="d0157-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="d0157-139">Az alacsony prioritású számítási csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="d0157-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0157-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0157-140">CommonParameters</span></span>
<span data-ttu-id="d0157-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0157-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0157-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0157-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0157-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0157-143">INPUTS</span></span>

### <span data-ttu-id="d0157-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d0157-144">BatchAccountContext</span></span>
<span data-ttu-id="d0157-145">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d0157-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d0157-146">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="d0157-146">String</span></span>
<span data-ttu-id="d0157-147">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="d0157-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d0157-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0157-148">OUTPUTS</span></span>

## <span data-ttu-id="d0157-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0157-149">NOTES</span></span>

## <span data-ttu-id="d0157-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0157-150">RELATED LINKS</span></span>

[<span data-ttu-id="d0157-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d0157-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d0157-152">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="d0157-152">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="d0157-153">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="d0157-153">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="d0157-154">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d0157-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


