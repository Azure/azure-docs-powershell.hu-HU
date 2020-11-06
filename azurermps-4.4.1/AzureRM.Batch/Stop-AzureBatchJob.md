---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 8893ed4002e576e257cd9b885d5773c5851edde0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500104"
---
# <span data-ttu-id="0089b-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0089b-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="0089b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0089b-102">SYNOPSIS</span></span>
<span data-ttu-id="0089b-103">Leállít egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="0089b-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0089b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0089b-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0089b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0089b-105">DESCRIPTION</span></span>
<span data-ttu-id="0089b-106">A **stop-AzureBatchJob** parancsmag leállítja az Azure kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="0089b-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="0089b-107">Ez a parancs befejezettként jelöli meg a feladatot.</span><span class="sxs-lookup"><span data-stu-id="0089b-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="0089b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0089b-108">EXAMPLES</span></span>

### <span data-ttu-id="0089b-109">Példa 1: kötegelt feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="0089b-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="0089b-110">Ez a parancs leállítja a 000001 AZONOSÍTÓJÚ munkát.</span><span class="sxs-lookup"><span data-stu-id="0089b-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="0089b-111">A parancs azt a lehetőséget adja meg, amely a feladat leállítását választotta.</span><span class="sxs-lookup"><span data-stu-id="0089b-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="0089b-112">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="0089b-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="0089b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0089b-113">PARAMETERS</span></span>

### <span data-ttu-id="0089b-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0089b-114">-BatchContext</span></span>
<span data-ttu-id="0089b-115">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="0089b-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0089b-116">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0089b-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="0089b-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="0089b-117">-Id</span></span>
<span data-ttu-id="0089b-118">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="0089b-118">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0089b-119">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="0089b-119">-TerminateReason</span></span>
<span data-ttu-id="0089b-120">Itt adhatja meg, hogy miért döntött a feladat leállítására.</span><span class="sxs-lookup"><span data-stu-id="0089b-120">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="0089b-121">Ez a parancsmag a következő szöveget tárolja a projekt **TerminateReason** tulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="0089b-121">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="0089b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0089b-122">-DefaultProfile</span></span>
<span data-ttu-id="0089b-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0089b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0089b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0089b-124">CommonParameters</span></span>
<span data-ttu-id="0089b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0089b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0089b-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0089b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0089b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0089b-127">INPUTS</span></span>

### <span data-ttu-id="0089b-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0089b-128">BatchAccountContext</span></span>
<span data-ttu-id="0089b-129">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0089b-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0089b-130">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="0089b-130">String</span></span>
<span data-ttu-id="0089b-131">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="0089b-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="0089b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0089b-132">OUTPUTS</span></span>

## <span data-ttu-id="0089b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0089b-133">NOTES</span></span>

## <span data-ttu-id="0089b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0089b-134">RELATED LINKS</span></span>

[<span data-ttu-id="0089b-135">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0089b-135">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="0089b-136">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0089b-136">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="0089b-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0089b-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0089b-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0089b-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="0089b-139">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0089b-139">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="0089b-140">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0089b-140">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="0089b-141">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0089b-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


