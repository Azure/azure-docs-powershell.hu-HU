---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: 73d80d3547ea895e5cbd35b2d514d9a757164bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505267"
---
# <span data-ttu-id="c27aa-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c27aa-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="c27aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c27aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c27aa-103">Letilt egy kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="c27aa-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c27aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c27aa-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c27aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c27aa-105">DESCRIPTION</span></span>
<span data-ttu-id="c27aa-106">A **disable-AzureBatchJobSchedule** parancsmag letiltja az Azure-alapú kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="c27aa-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="c27aa-107">Ha letiltja az ütemtervet, a feladatok nem az adott ütemterv szerint jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="c27aa-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="c27aa-108">Később is engedélyezheti a letiltott ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="c27aa-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="c27aa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c27aa-109">EXAMPLES</span></span>

### <span data-ttu-id="c27aa-110">1. példa: munkabeosztás letiltása</span><span class="sxs-lookup"><span data-stu-id="c27aa-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="c27aa-111">Ez a parancs letiltja a JobSchedule17 azonosító munkabeosztást.</span><span class="sxs-lookup"><span data-stu-id="c27aa-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="c27aa-112">A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="c27aa-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="c27aa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c27aa-113">PARAMETERS</span></span>

### <span data-ttu-id="c27aa-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c27aa-114">-BatchContext</span></span>
<span data-ttu-id="c27aa-115">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="c27aa-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c27aa-116">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c27aa-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c27aa-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="c27aa-117">-Id</span></span>
<span data-ttu-id="c27aa-118">Annak az ütemezésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="c27aa-118">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="c27aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c27aa-119">-DefaultProfile</span></span>
<span data-ttu-id="c27aa-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c27aa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c27aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c27aa-121">CommonParameters</span></span>
<span data-ttu-id="c27aa-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c27aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c27aa-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c27aa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c27aa-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c27aa-124">INPUTS</span></span>

### <span data-ttu-id="c27aa-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c27aa-125">BatchAccountContext</span></span>
<span data-ttu-id="c27aa-126">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c27aa-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c27aa-127">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="c27aa-127">String</span></span>
<span data-ttu-id="c27aa-128">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="c27aa-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c27aa-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c27aa-129">OUTPUTS</span></span>

## <span data-ttu-id="c27aa-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c27aa-130">NOTES</span></span>

## <span data-ttu-id="c27aa-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c27aa-131">RELATED LINKS</span></span>

[<span data-ttu-id="c27aa-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c27aa-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c27aa-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c27aa-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c27aa-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c27aa-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="c27aa-135">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c27aa-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="c27aa-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c27aa-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="c27aa-137">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c27aa-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="c27aa-138">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c27aa-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


