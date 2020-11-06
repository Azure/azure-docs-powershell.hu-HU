---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 58ac726d722959e3ee32bce84c0abe3c771fcbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500103"
---
# <span data-ttu-id="feacf-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="feacf-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="feacf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="feacf-102">SYNOPSIS</span></span>
<span data-ttu-id="feacf-103">Befejezi a kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="feacf-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="feacf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="feacf-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feacf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="feacf-105">DESCRIPTION</span></span>
<span data-ttu-id="feacf-106">A **stop-AzureBatchJobSchedule** parancsmag az Azure kötegelt feladatok ütemtervét leállítja.</span><span class="sxs-lookup"><span data-stu-id="feacf-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="feacf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="feacf-107">EXAMPLES</span></span>

### <span data-ttu-id="feacf-108">1. példa: munkabeosztás leállítása</span><span class="sxs-lookup"><span data-stu-id="feacf-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="feacf-109">Ez a parancs leállítja a JobSchedule17 AZONOSÍTÓJÚ munkabeosztást.</span><span class="sxs-lookup"><span data-stu-id="feacf-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="feacf-110">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="feacf-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="feacf-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="feacf-111">PARAMETERS</span></span>

### <span data-ttu-id="feacf-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="feacf-112">-BatchContext</span></span>
<span data-ttu-id="feacf-113">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="feacf-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="feacf-114">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="feacf-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="feacf-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="feacf-115">-Id</span></span>
<span data-ttu-id="feacf-116">Annak a munkaütemezésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="feacf-116">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="feacf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feacf-117">-DefaultProfile</span></span>
<span data-ttu-id="feacf-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="feacf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feacf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feacf-119">CommonParameters</span></span>
<span data-ttu-id="feacf-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="feacf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feacf-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feacf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feacf-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="feacf-122">INPUTS</span></span>

### <span data-ttu-id="feacf-123">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="feacf-123">BatchAccountContext</span></span>
<span data-ttu-id="feacf-124">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="feacf-124">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="feacf-125">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="feacf-125">String</span></span>
<span data-ttu-id="feacf-126">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="feacf-126">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="feacf-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="feacf-127">OUTPUTS</span></span>

## <span data-ttu-id="feacf-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="feacf-128">NOTES</span></span>

## <span data-ttu-id="feacf-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="feacf-129">RELATED LINKS</span></span>

[<span data-ttu-id="feacf-130">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="feacf-130">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="feacf-131">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="feacf-131">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="feacf-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="feacf-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="feacf-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="feacf-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="feacf-134">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="feacf-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="feacf-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="feacf-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="feacf-136">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="feacf-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


