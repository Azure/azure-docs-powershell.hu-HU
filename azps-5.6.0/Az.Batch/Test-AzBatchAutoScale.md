---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: a048e7bd2a013bd5d8526feead3b38483a1f61b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922514"
---
# <span data-ttu-id="3f984-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3f984-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="3f984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f984-102">SYNOPSIS</span></span>
<span data-ttu-id="3f984-103">Egy automatikus méretezési képlet eredményét kapja egy készleten.</span><span class="sxs-lookup"><span data-stu-id="3f984-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="3f984-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f984-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f984-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f984-105">DESCRIPTION</span></span>
<span data-ttu-id="3f984-106">A **Test-AzBatchAutoScale** parancsmag egy automatikus méretezési képlet eredményét kapja a megadott készleten.</span><span class="sxs-lookup"><span data-stu-id="3f984-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="3f984-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f984-107">EXAMPLES</span></span>

### <span data-ttu-id="3f984-108">1. példa: Automatikus skálázási képlet kiértékelése készleten</span><span class="sxs-lookup"><span data-stu-id="3f984-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="3f984-109">Az első parancs egy képletet tárol a $Formula változóban a példában való használatra.</span><span class="sxs-lookup"><span data-stu-id="3f984-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="3f984-110">A második parancs kiértékeli a ContosoPool azonosítójú készlet automatikus skálázási képletét.</span><span class="sxs-lookup"><span data-stu-id="3f984-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="3f984-111">Az utolsó parancs  a normál pontszintaxissal jeleníti meg az Eredményeket.</span><span class="sxs-lookup"><span data-stu-id="3f984-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="3f984-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f984-112">PARAMETERS</span></span>

### <span data-ttu-id="3f984-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="3f984-113">-AutoScaleFormula</span></span>
<span data-ttu-id="3f984-114">A készletben található számítási csomópontok kívánt számának képletét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f984-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f984-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3f984-115">-BatchContext</span></span>
<span data-ttu-id="3f984-116">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="3f984-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3f984-117">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="3f984-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3f984-118">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="3f984-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3f984-119">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="3f984-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3f984-120">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="3f984-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3f984-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f984-121">-DefaultProfile</span></span>
<span data-ttu-id="3f984-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f984-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f984-123">-Id</span><span class="sxs-lookup"><span data-stu-id="3f984-123">-Id</span></span>
<span data-ttu-id="3f984-124">Annak a készletnek az objektumazonosítóját adja meg, amelynek az automatikus méretezését tesztelni kell.</span><span class="sxs-lookup"><span data-stu-id="3f984-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="3f984-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f984-125">CommonParameters</span></span>
<span data-ttu-id="3f984-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f984-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f984-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f984-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f984-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f984-128">INPUTS</span></span>

### <span data-ttu-id="3f984-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3f984-129">System.String</span></span>

### <span data-ttu-id="3f984-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3f984-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3f984-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f984-131">OUTPUTS</span></span>

### <span data-ttu-id="3f984-132">Microsoft.Azure.Commands.Bat. Models.PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="3f984-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="3f984-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f984-133">NOTES</span></span>

## <span data-ttu-id="3f984-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f984-134">RELATED LINKS</span></span>

[<span data-ttu-id="3f984-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3f984-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="3f984-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3f984-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="3f984-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3f984-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3f984-138">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3f984-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
