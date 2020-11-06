---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: 3081721db5cb113d48417ddf28d8a96512d27f99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502627"
---
# <span data-ttu-id="5c312-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5c312-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="5c312-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c312-102">SYNOPSIS</span></span>
<span data-ttu-id="5c312-103">Lehetővé teszi a kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="5c312-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c312-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c312-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c312-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c312-105">DESCRIPTION</span></span>
<span data-ttu-id="5c312-106">Az **enable-AzureBatchJobSchedule** parancsmag az Azure kötegelt feladatok ütemtervét engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="5c312-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="5c312-107">Miután engedélyezte a projekt ütemezését, a munkahelyeket az adott ütemterv szerint hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="5c312-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="5c312-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5c312-108">EXAMPLES</span></span>

### <span data-ttu-id="5c312-109">1. példa: projekt-ütemezés engedélyezése</span><span class="sxs-lookup"><span data-stu-id="5c312-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="5c312-110">Ez a parancs engedélyezi az ID JobSchedule17 tartalmazó ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="5c312-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="5c312-111">A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="5c312-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5c312-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c312-112">PARAMETERS</span></span>

### <span data-ttu-id="5c312-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5c312-113">-BatchContext</span></span>
<span data-ttu-id="5c312-114">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="5c312-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5c312-115">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="5c312-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5c312-116">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="5c312-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5c312-117">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="5c312-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5c312-118">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5c312-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5c312-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c312-119">-DefaultProfile</span></span>
<span data-ttu-id="5c312-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c312-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c312-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5c312-121">-Id</span></span>
<span data-ttu-id="5c312-122">Annak az ütemezésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="5c312-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="5c312-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c312-123">CommonParameters</span></span>
<span data-ttu-id="5c312-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c312-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c312-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c312-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c312-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c312-126">INPUTS</span></span>

### <span data-ttu-id="5c312-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5c312-127">BatchAccountContext</span></span>
<span data-ttu-id="5c312-128">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5c312-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5c312-129">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="5c312-129">String</span></span>
<span data-ttu-id="5c312-130">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="5c312-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5c312-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c312-131">OUTPUTS</span></span>

## <span data-ttu-id="5c312-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c312-132">NOTES</span></span>

## <span data-ttu-id="5c312-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c312-133">RELATED LINKS</span></span>

[<span data-ttu-id="5c312-134">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5c312-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="5c312-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5c312-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5c312-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5c312-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="5c312-137">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5c312-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="5c312-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5c312-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="5c312-139">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5c312-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="5c312-140">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5c312-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


