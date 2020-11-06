---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 0f33807c112ea770e3d02d972d52ca7a166bb791
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493251"
---
# <span data-ttu-id="a0a0c-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0a0c-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="a0a0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a0c-103">Leállít egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0a0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0a0c-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0a0c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0a0c-105">DESCRIPTION</span></span>
<span data-ttu-id="a0a0c-106">A **stop-AzureBatchJob** parancsmag leállítja az Azure kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="a0a0c-107">Ez a parancs befejezettként jelöli meg a feladatot.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="a0a0c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a0a0c-108">EXAMPLES</span></span>

### <span data-ttu-id="a0a0c-109">Példa 1: kötegelt feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="a0a0c-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="a0a0c-110">Ez a parancs leállítja a 000001 AZONOSÍTÓJÚ munkát.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a0a0c-111">A parancs azt a lehetőséget adja meg, amely a feladat leállítását választotta.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="a0a0c-112">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a0a0c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0a0c-113">PARAMETERS</span></span>

### <span data-ttu-id="a0a0c-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a0a0c-114">-BatchContext</span></span>
<span data-ttu-id="a0a0c-115">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a0a0c-116">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a0a0c-117">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a0a0c-118">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a0a0c-119">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a0a0c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a0c-120">-DefaultProfile</span></span>
<span data-ttu-id="a0a0c-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0a0c-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a0a0c-122">-Id</span></span>
<span data-ttu-id="a0a0c-123">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="a0a0c-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="a0a0c-124">-TerminateReason</span></span>
<span data-ttu-id="a0a0c-125">Itt adhatja meg, hogy miért döntött a feladat leállítására.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="a0a0c-126">Ez a parancsmag a következő szöveget tárolja a projekt **TerminateReason** tulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a0c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a0c-127">CommonParameters</span></span>
<span data-ttu-id="a0a0c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0a0c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a0c-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0a0c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a0c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0a0c-130">INPUTS</span></span>

### <span data-ttu-id="a0a0c-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a0a0c-131">BatchAccountContext</span></span>
<span data-ttu-id="a0a0c-132">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a0a0c-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a0a0c-133">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="a0a0c-133">String</span></span>
<span data-ttu-id="a0a0c-134">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a0a0c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0a0c-135">OUTPUTS</span></span>

## <span data-ttu-id="a0a0c-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0a0c-136">NOTES</span></span>

## <span data-ttu-id="a0a0c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0a0c-137">RELATED LINKS</span></span>

[<span data-ttu-id="a0a0c-138">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0a0c-138">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="a0a0c-139">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0a0c-139">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="a0a0c-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a0a0c-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a0a0c-141">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0a0c-141">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a0a0c-142">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0a0c-142">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="a0a0c-143">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0a0c-143">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a0a0c-144">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a0a0c-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


