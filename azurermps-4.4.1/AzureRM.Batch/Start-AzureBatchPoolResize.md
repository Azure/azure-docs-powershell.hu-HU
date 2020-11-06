---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499200"
---
# <span data-ttu-id="3b911-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="3b911-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="3b911-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b911-102">SYNOPSIS</span></span>
<span data-ttu-id="3b911-103">Elkezdi átméretezni a készletet.</span><span class="sxs-lookup"><span data-stu-id="3b911-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b911-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b911-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b911-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b911-105">DESCRIPTION</span></span>
<span data-ttu-id="3b911-106">A **Start-AzureBatchPoolResize** parancsmag az Azure köteg-átméretezési műveletet kezdi a készletre.</span><span class="sxs-lookup"><span data-stu-id="3b911-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="3b911-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b911-107">EXAMPLES</span></span>

### <span data-ttu-id="3b911-108">1. példa: a készlet átméretezése 12 csomópontra</span><span class="sxs-lookup"><span data-stu-id="3b911-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

<span data-ttu-id="3b911-109">A parancs átméretezési műveletet indít az azonosító ContosoPool06 tartalmazó készleten.</span><span class="sxs-lookup"><span data-stu-id="3b911-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="3b911-110">A művelet célja 12 dedikált kiszámított csomópont.</span><span class="sxs-lookup"><span data-stu-id="3b911-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="3b911-111">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="3b911-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3b911-112">2. példa: a készlet átméretezése kifoglalási beállítás használatával</span><span class="sxs-lookup"><span data-stu-id="3b911-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="3b911-113">Ez a parancsmag átméretezi a készletet öt dedikált kiszámított csomópontra.</span><span class="sxs-lookup"><span data-stu-id="3b911-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="3b911-114">A parancs a Get-AzureBatchPool parancsmag használatával az azonosító ContosoPool06 tartalmazó készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="3b911-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="3b911-115">A parancs a pipeline operátorral továbbítja a készlet objektumát az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3b911-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3b911-116">A parancs átméretezési műveletet indít a készleten.</span><span class="sxs-lookup"><span data-stu-id="3b911-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="3b911-117">A cél öt külön kiszámított csomópont.</span><span class="sxs-lookup"><span data-stu-id="3b911-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="3b911-118">A parancs egy óra elteltével adja meg az időtúllépési időszakot.</span><span class="sxs-lookup"><span data-stu-id="3b911-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="3b911-119">A parancs a leállítási lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b911-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="3b911-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b911-120">PARAMETERS</span></span>

### <span data-ttu-id="3b911-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3b911-121">-BatchContext</span></span>
<span data-ttu-id="3b911-122">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="3b911-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3b911-123">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3b911-123">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="3b911-124">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="3b911-124">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="3b911-125">A parancsmag által elinduló átméretezési művelet kiosztási beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b911-125">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="3b911-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="3b911-126">-Id</span></span>
<span data-ttu-id="3b911-127">A parancsmag által átméretezett készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b911-127">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="3b911-128">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="3b911-128">-ResizeTimeout</span></span>
<span data-ttu-id="3b911-129">Az átméretezési művelet időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b911-129">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="3b911-130">Ha a készlet jelenleg nem éri el a cél méretét, az átméretezés művelet leáll.</span><span class="sxs-lookup"><span data-stu-id="3b911-130">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="3b911-131">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="3b911-131">-TargetDedicated</span></span>
<span data-ttu-id="3b911-132">A dedikált számítási csomópontok cél számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b911-132">Specifies the target number of dedicated compute nodes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b911-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b911-133">-DefaultProfile</span></span>
<span data-ttu-id="3b911-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b911-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b911-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b911-135">CommonParameters</span></span>
<span data-ttu-id="3b911-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b911-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b911-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b911-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b911-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b911-138">INPUTS</span></span>

### <span data-ttu-id="3b911-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3b911-139">BatchAccountContext</span></span>
<span data-ttu-id="3b911-140">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3b911-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="3b911-141">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="3b911-141">String</span></span>
<span data-ttu-id="3b911-142">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="3b911-142">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3b911-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b911-143">OUTPUTS</span></span>

## <span data-ttu-id="3b911-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b911-144">NOTES</span></span>

## <span data-ttu-id="3b911-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b911-145">RELATED LINKS</span></span>

[<span data-ttu-id="3b911-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3b911-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3b911-147">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="3b911-147">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="3b911-148">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="3b911-148">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="3b911-149">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3b911-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


