---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 2ab8ca197c1d78980e1683f9572f6d3f6d4d55fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672074"
---
# <span data-ttu-id="8cb91-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8cb91-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="8cb91-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cb91-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb91-103">Az automatikus méretezési képlet eredményét kapja a készletben.</span><span class="sxs-lookup"><span data-stu-id="8cb91-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cb91-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cb91-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cb91-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cb91-105">DESCRIPTION</span></span>
<span data-ttu-id="8cb91-106">A **teszt-AzureBatchAutoScale** parancsmag a megadott készlet automatikus méretezési képletének eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="8cb91-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="8cb91-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8cb91-107">EXAMPLES</span></span>

### <span data-ttu-id="8cb91-108">Példa 1: automéretarányos képlet kiértékelése egy készleten</span><span class="sxs-lookup"><span data-stu-id="8cb91-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="8cb91-109">Az első parancs a példában szereplő képletet tárolja a $Formula változóban.</span><span class="sxs-lookup"><span data-stu-id="8cb91-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="8cb91-110">A második parancs kiértékeli az autoscale képletet az azonosító ContosoPool tartalmazó készletben.</span><span class="sxs-lookup"><span data-stu-id="8cb91-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="8cb91-111">A végleges parancs a normál pont szintaxis használatával jeleníti meg az **eredményeket** .</span><span class="sxs-lookup"><span data-stu-id="8cb91-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="8cb91-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cb91-112">PARAMETERS</span></span>

### <span data-ttu-id="8cb91-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="8cb91-113">-AutoScaleFormula</span></span>
<span data-ttu-id="8cb91-114">Megadja a készletben a számítási csomópontok kívánt számának képletét.</span><span class="sxs-lookup"><span data-stu-id="8cb91-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="8cb91-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8cb91-115">-BatchContext</span></span>
<span data-ttu-id="8cb91-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="8cb91-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8cb91-117">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8cb91-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="8cb91-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8cb91-118">-Id</span></span>
<span data-ttu-id="8cb91-119">Annak a készletnek az objektum-AZONOSÍTÓját adja meg, amelynél az automatikus méretezést ellenőrizni szeretné.</span><span class="sxs-lookup"><span data-stu-id="8cb91-119">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="8cb91-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb91-120">-DefaultProfile</span></span>
<span data-ttu-id="8cb91-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8cb91-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cb91-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb91-122">CommonParameters</span></span>
<span data-ttu-id="8cb91-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cb91-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb91-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cb91-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb91-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cb91-125">INPUTS</span></span>

### <span data-ttu-id="8cb91-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8cb91-126">BatchAccountContext</span></span>
<span data-ttu-id="8cb91-127">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8cb91-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="8cb91-128">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="8cb91-128">String</span></span>
<span data-ttu-id="8cb91-129">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="8cb91-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8cb91-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cb91-130">OUTPUTS</span></span>

### <span data-ttu-id="8cb91-131">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="8cb91-131">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="8cb91-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cb91-132">NOTES</span></span>

## <span data-ttu-id="8cb91-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cb91-133">RELATED LINKS</span></span>

[<span data-ttu-id="8cb91-134">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8cb91-134">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="8cb91-135">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8cb91-135">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="8cb91-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8cb91-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8cb91-137">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8cb91-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


