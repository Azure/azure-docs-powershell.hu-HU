---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 719c743281102f83c08f55093d221856be4194bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672174"
---
# <span data-ttu-id="9462d-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9462d-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="9462d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9462d-102">SYNOPSIS</span></span>
<span data-ttu-id="9462d-103">Befejezi a kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="9462d-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9462d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9462d-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9462d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9462d-105">DESCRIPTION</span></span>
<span data-ttu-id="9462d-106">A **stop-AzureBatchJobSchedule** parancsmag az Azure kötegelt feladatok ütemtervét leállítja.</span><span class="sxs-lookup"><span data-stu-id="9462d-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="9462d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9462d-107">EXAMPLES</span></span>

### <span data-ttu-id="9462d-108">1. példa: munkabeosztás leállítása</span><span class="sxs-lookup"><span data-stu-id="9462d-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="9462d-109">Ez a parancs leállítja a JobSchedule17 AZONOSÍTÓJÚ munkabeosztást.</span><span class="sxs-lookup"><span data-stu-id="9462d-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="9462d-110">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="9462d-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="9462d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9462d-111">PARAMETERS</span></span>

### <span data-ttu-id="9462d-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9462d-112">-BatchContext</span></span>
<span data-ttu-id="9462d-113">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="9462d-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9462d-114">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="9462d-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9462d-115">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="9462d-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9462d-116">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="9462d-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9462d-117">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="9462d-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9462d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9462d-118">-DefaultProfile</span></span>
<span data-ttu-id="9462d-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9462d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9462d-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9462d-120">-Id</span></span>
<span data-ttu-id="9462d-121">Annak a munkaütemezésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="9462d-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="9462d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9462d-122">CommonParameters</span></span>
<span data-ttu-id="9462d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9462d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9462d-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9462d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9462d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9462d-125">INPUTS</span></span>

### <span data-ttu-id="9462d-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9462d-126">BatchAccountContext</span></span>
<span data-ttu-id="9462d-127">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9462d-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="9462d-128">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="9462d-128">String</span></span>
<span data-ttu-id="9462d-129">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="9462d-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="9462d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9462d-130">OUTPUTS</span></span>

## <span data-ttu-id="9462d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9462d-131">NOTES</span></span>

## <span data-ttu-id="9462d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9462d-132">RELATED LINKS</span></span>

[<span data-ttu-id="9462d-133">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9462d-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="9462d-134">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9462d-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="9462d-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9462d-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9462d-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9462d-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="9462d-137">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9462d-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="9462d-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9462d-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="9462d-139">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9462d-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


