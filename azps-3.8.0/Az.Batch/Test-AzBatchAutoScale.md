---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: ca78cd5fc5103b2c9589dc4a84ccf0de0ac3f171
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017229"
---
# <span data-ttu-id="6f104-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="6f104-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="6f104-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f104-102">SYNOPSIS</span></span>
<span data-ttu-id="6f104-103">Az automatikus méretezési képlet eredményét kapja a készletben.</span><span class="sxs-lookup"><span data-stu-id="6f104-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="6f104-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f104-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f104-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f104-105">DESCRIPTION</span></span>
<span data-ttu-id="6f104-106">A **teszt-AzBatchAutoScale** parancsmag a megadott készlet automatikus méretezési képletének eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="6f104-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="6f104-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6f104-107">EXAMPLES</span></span>

### <span data-ttu-id="6f104-108">Példa 1: automéretarányos képlet kiértékelése egy készleten</span><span class="sxs-lookup"><span data-stu-id="6f104-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="6f104-109">Az első parancs a példában szereplő képletet tárolja a $Formula változóban.</span><span class="sxs-lookup"><span data-stu-id="6f104-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="6f104-110">A második parancs kiértékeli az autoscale képletet az azonosító ContosoPool tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="6f104-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="6f104-111">A végleges parancs a normál pont szintaxis használatával jeleníti meg az **eredményeket** .</span><span class="sxs-lookup"><span data-stu-id="6f104-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="6f104-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f104-112">PARAMETERS</span></span>

### <span data-ttu-id="6f104-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="6f104-113">-AutoScaleFormula</span></span>
<span data-ttu-id="6f104-114">Megadja a készletben a számítási csomópontok kívánt számának képletét.</span><span class="sxs-lookup"><span data-stu-id="6f104-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="6f104-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6f104-115">-BatchContext</span></span>
<span data-ttu-id="6f104-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="6f104-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6f104-117">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="6f104-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6f104-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="6f104-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6f104-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="6f104-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6f104-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="6f104-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6f104-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f104-121">-DefaultProfile</span></span>
<span data-ttu-id="6f104-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f104-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f104-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="6f104-123">-Id</span></span>
<span data-ttu-id="6f104-124">Annak a készletnek az objektum-AZONOSÍTÓját adja meg, amelynél az automatikus méretezést ellenőrizni szeretné.</span><span class="sxs-lookup"><span data-stu-id="6f104-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="6f104-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f104-125">CommonParameters</span></span>
<span data-ttu-id="6f104-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f104-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f104-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6f104-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f104-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f104-128">INPUTS</span></span>

### <span data-ttu-id="6f104-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6f104-129">System.String</span></span>

### <span data-ttu-id="6f104-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6f104-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6f104-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f104-131">OUTPUTS</span></span>

### <span data-ttu-id="6f104-132">Microsoft.Azure.Commands.BatCH. Modellek. PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="6f104-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="6f104-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f104-133">NOTES</span></span>

## <span data-ttu-id="6f104-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f104-134">RELATED LINKS</span></span>

[<span data-ttu-id="6f104-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="6f104-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="6f104-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="6f104-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="6f104-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6f104-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6f104-138">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="6f104-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


