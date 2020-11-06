---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/test-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 4258c5d83b15c2cecb6e2cd4e3edc216efec7a97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492391"
---
# <span data-ttu-id="85be5-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="85be5-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="85be5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85be5-102">SYNOPSIS</span></span>
<span data-ttu-id="85be5-103">Az automatikus méretezési képlet eredményét kapja a készletben.</span><span class="sxs-lookup"><span data-stu-id="85be5-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85be5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85be5-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85be5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="85be5-105">DESCRIPTION</span></span>
<span data-ttu-id="85be5-106">A **teszt-AzureBatchAutoScale** parancsmag a megadott készlet automatikus méretezési képletének eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="85be5-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="85be5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="85be5-107">EXAMPLES</span></span>

### <span data-ttu-id="85be5-108">Példa 1: automéretarányos képlet kiértékelése egy készleten</span><span class="sxs-lookup"><span data-stu-id="85be5-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="85be5-109">Az első parancs a példában szereplő képletet tárolja a $Formula változóban.</span><span class="sxs-lookup"><span data-stu-id="85be5-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="85be5-110">A második parancs kiértékeli az autoscale képletet az azonosító ContosoPool tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="85be5-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="85be5-111">A végleges parancs a normál pont szintaxis használatával jeleníti meg az **eredményeket** .</span><span class="sxs-lookup"><span data-stu-id="85be5-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="85be5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85be5-112">PARAMETERS</span></span>

### <span data-ttu-id="85be5-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="85be5-113">-AutoScaleFormula</span></span>
<span data-ttu-id="85be5-114">Megadja a készletben a számítási csomópontok kívánt számának képletét.</span><span class="sxs-lookup"><span data-stu-id="85be5-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be5-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="85be5-115">-BatchContext</span></span>
<span data-ttu-id="85be5-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="85be5-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="85be5-117">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="85be5-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="85be5-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="85be5-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="85be5-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="85be5-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="85be5-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="85be5-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="85be5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85be5-121">-DefaultProfile</span></span>
<span data-ttu-id="85be5-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85be5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85be5-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="85be5-123">-Id</span></span>
<span data-ttu-id="85be5-124">Annak a készletnek az objektum-AZONOSÍTÓját adja meg, amelynél az automatikus méretezést ellenőrizni szeretné.</span><span class="sxs-lookup"><span data-stu-id="85be5-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="85be5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85be5-125">CommonParameters</span></span>
<span data-ttu-id="85be5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85be5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85be5-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85be5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85be5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85be5-128">INPUTS</span></span>

### <span data-ttu-id="85be5-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="85be5-129">BatchAccountContext</span></span>
<span data-ttu-id="85be5-130">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="85be5-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="85be5-131">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="85be5-131">String</span></span>
<span data-ttu-id="85be5-132">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="85be5-132">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="85be5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85be5-133">OUTPUTS</span></span>

### <span data-ttu-id="85be5-134">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="85be5-134">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="85be5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85be5-135">NOTES</span></span>

## <span data-ttu-id="85be5-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85be5-136">RELATED LINKS</span></span>

[<span data-ttu-id="85be5-137">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="85be5-137">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="85be5-138">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="85be5-138">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="85be5-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="85be5-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="85be5-140">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="85be5-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


