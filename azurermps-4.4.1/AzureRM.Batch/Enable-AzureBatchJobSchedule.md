---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: c012fe266bc25752729b14192c4d9c0a42cd8961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505259"
---
# <span data-ttu-id="a1a59-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1a59-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="a1a59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1a59-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a59-103">Lehetővé teszi a kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="a1a59-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1a59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1a59-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1a59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1a59-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a59-106">Az **enable-AzureBatchJobSchedule** parancsmag az Azure kötegelt feladatok ütemtervét engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="a1a59-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="a1a59-107">Miután engedélyezte a projekt ütemezését, a munkahelyeket az adott ütemterv szerint hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="a1a59-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="a1a59-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a1a59-108">EXAMPLES</span></span>

### <span data-ttu-id="a1a59-109">1. példa: projekt-ütemezés engedélyezése</span><span class="sxs-lookup"><span data-stu-id="a1a59-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="a1a59-110">Ez a parancs engedélyezi az ID JobSchedule17 tartalmazó ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="a1a59-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="a1a59-111">A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="a1a59-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a1a59-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1a59-112">PARAMETERS</span></span>

### <span data-ttu-id="a1a59-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a1a59-113">-BatchContext</span></span>
<span data-ttu-id="a1a59-114">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="a1a59-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a1a59-115">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a1a59-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a1a59-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a1a59-116">-Id</span></span>
<span data-ttu-id="a1a59-117">Annak az ütemezésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="a1a59-117">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="a1a59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a59-118">-DefaultProfile</span></span>
<span data-ttu-id="a1a59-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1a59-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1a59-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a59-120">CommonParameters</span></span>
<span data-ttu-id="a1a59-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1a59-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a59-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a59-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a59-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1a59-123">INPUTS</span></span>

### <span data-ttu-id="a1a59-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a1a59-124">BatchAccountContext</span></span>
<span data-ttu-id="a1a59-125">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a1a59-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a1a59-126">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="a1a59-126">String</span></span>
<span data-ttu-id="a1a59-127">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="a1a59-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a1a59-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1a59-128">OUTPUTS</span></span>

## <span data-ttu-id="a1a59-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1a59-129">NOTES</span></span>

## <span data-ttu-id="a1a59-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1a59-130">RELATED LINKS</span></span>

[<span data-ttu-id="a1a59-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1a59-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="a1a59-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a1a59-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a1a59-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1a59-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="a1a59-134">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1a59-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="a1a59-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1a59-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="a1a59-136">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1a59-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="a1a59-137">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a1a59-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


