---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a85ac52622bb752b2e3437eb096f229c4d8e762
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505264"
---
# <span data-ttu-id="dc711-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="dc711-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="dc711-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc711-102">SYNOPSIS</span></span>
<span data-ttu-id="dc711-103">Lehetővé teszi a készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="dc711-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc711-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc711-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc711-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc711-105">DESCRIPTION</span></span>
<span data-ttu-id="dc711-106">Az **enable-AzureBatchAutoScale** parancsmag lehetővé teszi a megadott készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="dc711-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="dc711-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dc711-107">EXAMPLES</span></span>

### <span data-ttu-id="dc711-108">1. példa: a készlet automatikus méretezésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="dc711-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="dc711-109">Az első parancs a képletet definiálja, majd a $Formula változóra menti.</span><span class="sxs-lookup"><span data-stu-id="dc711-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="dc711-110">A második parancs engedélyezi a MyPool nevű alkalmazáskészlet automatikus méretezését az $Formula képlet használatával.</span><span class="sxs-lookup"><span data-stu-id="dc711-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="dc711-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc711-111">PARAMETERS</span></span>

### <span data-ttu-id="dc711-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="dc711-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="dc711-113">Itt adhatja meg, hogy a program mennyi ideig (percben) adja meg, hogy mennyi időt kell eltelnie, mielőtt a program automatikusan kiigazítja a készlet méretét.</span><span class="sxs-lookup"><span data-stu-id="dc711-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="dc711-114">Az alapértelmezett érték 15 perc, és a minimális érték 5 perc.</span><span class="sxs-lookup"><span data-stu-id="dc711-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="dc711-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="dc711-115">-AutoScaleFormula</span></span>
<span data-ttu-id="dc711-116">Megadja a készletben a számítási csomópontok kívánt számának képletét.</span><span class="sxs-lookup"><span data-stu-id="dc711-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="dc711-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dc711-117">-BatchContext</span></span>
<span data-ttu-id="dc711-118">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="dc711-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dc711-119">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dc711-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="dc711-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="dc711-120">-Id</span></span>
<span data-ttu-id="dc711-121">Annak a készletnek az objektum-AZONOSÍTÓját adja meg, amelyhez engedélyezni szeretné az automatikus méretezést.</span><span class="sxs-lookup"><span data-stu-id="dc711-121">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="dc711-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc711-122">-DefaultProfile</span></span>
<span data-ttu-id="dc711-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc711-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc711-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc711-124">CommonParameters</span></span>
<span data-ttu-id="dc711-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc711-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc711-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc711-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc711-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc711-127">INPUTS</span></span>

### <span data-ttu-id="dc711-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dc711-128">BatchAccountContext</span></span>
<span data-ttu-id="dc711-129">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dc711-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="dc711-130">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="dc711-130">String</span></span>
<span data-ttu-id="dc711-131">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="dc711-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="dc711-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc711-132">OUTPUTS</span></span>

## <span data-ttu-id="dc711-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc711-133">NOTES</span></span>

## <span data-ttu-id="dc711-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc711-134">RELATED LINKS</span></span>

[<span data-ttu-id="dc711-135">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="dc711-135">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="dc711-136">Teszt-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="dc711-136">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="dc711-137">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dc711-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


