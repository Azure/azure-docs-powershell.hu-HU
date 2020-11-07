---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 0f9d20cdd1d2acabbd644fda91f5f8d22ff1ccd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680610"
---
# <span data-ttu-id="033c0-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="033c0-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="033c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="033c0-102">SYNOPSIS</span></span>
<span data-ttu-id="033c0-103">Ütemtervet állít be.</span><span class="sxs-lookup"><span data-stu-id="033c0-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="033c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="033c0-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="033c0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="033c0-105">DESCRIPTION</span></span>
<span data-ttu-id="033c0-106">A **set-AzureBatchJobSchedule** parancsmag az Azure kötegelt szolgáltatásban végez ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="033c0-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="033c0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="033c0-107">EXAMPLES</span></span>

## <span data-ttu-id="033c0-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="033c0-108">PARAMETERS</span></span>

### <span data-ttu-id="033c0-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="033c0-109">-BatchContext</span></span>
<span data-ttu-id="033c0-110">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="033c0-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="033c0-111">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="033c0-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="033c0-112">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="033c0-112">-JobSchedule</span></span>
<span data-ttu-id="033c0-113">Olyan **PSCloudJobSchedule** -objektumot ad meg, amely egy projekt ütemtervét képviseli.</span><span class="sxs-lookup"><span data-stu-id="033c0-113">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="033c0-114">**PSCloudJobSchedule** objektum beolvasásához használja az Get-AzureBatchJobSchedule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="033c0-114">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="033c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="033c0-115">-DefaultProfile</span></span>
<span data-ttu-id="033c0-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="033c0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="033c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="033c0-117">CommonParameters</span></span>
<span data-ttu-id="033c0-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="033c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="033c0-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="033c0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="033c0-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="033c0-120">INPUTS</span></span>

### <span data-ttu-id="033c0-121">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="033c0-121">BatchAccountContext</span></span>
<span data-ttu-id="033c0-122">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="033c0-122">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="033c0-123">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="033c0-123">PSCloudJobSchedule</span></span>
<span data-ttu-id="033c0-124">A ' JobSchedule ' paraméter az "PSCloudJobSchedule" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="033c0-124">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="033c0-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="033c0-125">OUTPUTS</span></span>

## <span data-ttu-id="033c0-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="033c0-126">NOTES</span></span>

## <span data-ttu-id="033c0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="033c0-127">RELATED LINKS</span></span>

[<span data-ttu-id="033c0-128">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="033c0-128">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="033c0-129">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="033c0-129">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="033c0-130">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="033c0-130">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="033c0-131">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="033c0-131">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="033c0-132">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="033c0-132">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="033c0-133">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="033c0-133">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


