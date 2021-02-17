---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 73e7e9e0e4020f284b26e720e0f34ec7f11fd04f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205383"
---
# <span data-ttu-id="dea8a-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="dea8a-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="dea8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dea8a-102">SYNOPSIS</span></span>
<span data-ttu-id="dea8a-103">Engedélyezi a készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="dea8a-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="dea8a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dea8a-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dea8a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dea8a-105">DESCRIPTION</span></span>
<span data-ttu-id="dea8a-106">Az **Enable-AzBatchAutoScale** parancsmag lehetővé teszi a megadott készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="dea8a-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="dea8a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dea8a-107">EXAMPLES</span></span>

### <span data-ttu-id="dea8a-108">1. példa: A készlet automatikus méretezésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="dea8a-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="dea8a-109">Az első parancs definiál egy képletet, majd menti azt a $Formula változóba.</span><span class="sxs-lookup"><span data-stu-id="dea8a-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="dea8a-110">A második parancs engedélyezi az automatikus méretezést a MyPool nevű készleten a $Formula.</span><span class="sxs-lookup"><span data-stu-id="dea8a-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="dea8a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dea8a-111">PARAMETERS</span></span>

### <span data-ttu-id="dea8a-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="dea8a-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="dea8a-113">Azt az időt adja meg (percben), amely alatt a készlet mérete automatikusan módosul az automatikus skálázási képletnek megfelelően.</span><span class="sxs-lookup"><span data-stu-id="dea8a-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="dea8a-114">Az alapértelmezett érték 15 perc, a minimális érték pedig 5 perc.</span><span class="sxs-lookup"><span data-stu-id="dea8a-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea8a-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="dea8a-115">-AutoScaleFormula</span></span>
<span data-ttu-id="dea8a-116">A készletben található számítási csomópontok kívánt számának képletét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dea8a-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea8a-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dea8a-117">-BatchContext</span></span>
<span data-ttu-id="dea8a-118">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="dea8a-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dea8a-119">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="dea8a-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dea8a-120">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot, és töltse ki a hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="dea8a-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dea8a-121">Megosztott kulcsú hitelesítés használata esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="dea8a-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dea8a-122">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="dea8a-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dea8a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea8a-123">-DefaultProfile</span></span>
<span data-ttu-id="dea8a-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dea8a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dea8a-125">-Id</span><span class="sxs-lookup"><span data-stu-id="dea8a-125">-Id</span></span>
<span data-ttu-id="dea8a-126">Annak a készletnek az objektumazonosítóját adja meg, amelyhez engedélyezni szeretné az automatikus méretezést.</span><span class="sxs-lookup"><span data-stu-id="dea8a-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="dea8a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea8a-127">CommonParameters</span></span>
<span data-ttu-id="dea8a-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dea8a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea8a-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dea8a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea8a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dea8a-130">INPUTS</span></span>

### <span data-ttu-id="dea8a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="dea8a-131">System.String</span></span>

### <span data-ttu-id="dea8a-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dea8a-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dea8a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dea8a-133">OUTPUTS</span></span>

### <span data-ttu-id="dea8a-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="dea8a-134">System.Void</span></span>

## <span data-ttu-id="dea8a-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dea8a-135">NOTES</span></span>

## <span data-ttu-id="dea8a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dea8a-136">RELATED LINKS</span></span>

[<span data-ttu-id="dea8a-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="dea8a-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="dea8a-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="dea8a-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="dea8a-139">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dea8a-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
