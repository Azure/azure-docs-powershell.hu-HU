---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: fb1f9cf884b3443ec9746eca7cef603c7b9f3a38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505796"
---
# <span data-ttu-id="cf6b5-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf6b5-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="cf6b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf6b5-102">SYNOPSIS</span></span>
<span data-ttu-id="cf6b5-103">Letilt egy kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf6b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf6b5-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf6b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf6b5-105">DESCRIPTION</span></span>
<span data-ttu-id="cf6b5-106">A **disable-AzureBatchJobSchedule** parancsmag letiltja az Azure-alapú kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="cf6b5-107">Ha letiltja az ütemtervet, a feladatok nem az adott ütemterv szerint jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="cf6b5-108">Később is engedélyezheti a letiltott ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="cf6b5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cf6b5-109">EXAMPLES</span></span>

### <span data-ttu-id="cf6b5-110">1. példa: munkabeosztás letiltása</span><span class="sxs-lookup"><span data-stu-id="cf6b5-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="cf6b5-111">Ez a parancs letiltja a JobSchedule17 azonosító munkabeosztást.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="cf6b5-112">A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="cf6b5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf6b5-113">PARAMETERS</span></span>

### <span data-ttu-id="cf6b5-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cf6b5-114">-BatchContext</span></span>
<span data-ttu-id="cf6b5-115">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cf6b5-116">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cf6b5-117">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cf6b5-118">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cf6b5-119">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cf6b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf6b5-120">-DefaultProfile</span></span>
<span data-ttu-id="cf6b5-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf6b5-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="cf6b5-122">-Id</span></span>
<span data-ttu-id="cf6b5-123">Annak az ütemezésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="cf6b5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf6b5-124">CommonParameters</span></span>
<span data-ttu-id="cf6b5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf6b5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf6b5-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf6b5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf6b5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf6b5-127">INPUTS</span></span>

### <span data-ttu-id="cf6b5-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cf6b5-128">BatchAccountContext</span></span>
<span data-ttu-id="cf6b5-129">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cf6b5-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="cf6b5-130">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="cf6b5-130">String</span></span>
<span data-ttu-id="cf6b5-131">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="cf6b5-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="cf6b5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf6b5-132">OUTPUTS</span></span>

## <span data-ttu-id="cf6b5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf6b5-133">NOTES</span></span>

## <span data-ttu-id="cf6b5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf6b5-134">RELATED LINKS</span></span>

[<span data-ttu-id="cf6b5-135">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf6b5-135">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf6b5-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cf6b5-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cf6b5-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf6b5-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf6b5-138">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf6b5-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf6b5-139">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf6b5-139">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf6b5-140">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf6b5-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf6b5-141">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="cf6b5-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


