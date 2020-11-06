---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: f67660cdc64c814d04ec4a987b711c802ca222d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498396"
---
# <span data-ttu-id="5e36f-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e36f-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="5e36f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e36f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e36f-103">Leállít egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="5e36f-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e36f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e36f-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e36f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e36f-105">DESCRIPTION</span></span>
<span data-ttu-id="5e36f-106">A **stop-AzureBatchJob** parancsmag leállítja az Azure kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="5e36f-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="5e36f-107">Ez a parancs befejezettként jelöli meg a feladatot.</span><span class="sxs-lookup"><span data-stu-id="5e36f-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="5e36f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5e36f-108">EXAMPLES</span></span>

### <span data-ttu-id="5e36f-109">Példa 1: kötegelt feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="5e36f-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="5e36f-110">Ez a parancs leállítja a 000001 AZONOSÍTÓJÚ munkát.</span><span class="sxs-lookup"><span data-stu-id="5e36f-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="5e36f-111">A parancs azt a lehetőséget adja meg, amely a feladat leállítását választotta.</span><span class="sxs-lookup"><span data-stu-id="5e36f-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="5e36f-112">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="5e36f-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5e36f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e36f-113">PARAMETERS</span></span>

### <span data-ttu-id="5e36f-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5e36f-114">-BatchContext</span></span>
<span data-ttu-id="5e36f-115">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="5e36f-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5e36f-116">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="5e36f-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5e36f-117">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="5e36f-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5e36f-118">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="5e36f-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5e36f-119">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5e36f-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5e36f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e36f-120">-DefaultProfile</span></span>
<span data-ttu-id="5e36f-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e36f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e36f-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5e36f-122">-Id</span></span>
<span data-ttu-id="5e36f-123">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="5e36f-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="5e36f-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="5e36f-124">-TerminateReason</span></span>
<span data-ttu-id="5e36f-125">Itt adhatja meg, hogy miért döntött a feladat leállítására.</span><span class="sxs-lookup"><span data-stu-id="5e36f-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="5e36f-126">Ez a parancsmag a következő szöveget tárolja a projekt **TerminateReason** tulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="5e36f-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="5e36f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e36f-127">CommonParameters</span></span>
<span data-ttu-id="5e36f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e36f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e36f-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e36f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e36f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e36f-130">INPUTS</span></span>

### <span data-ttu-id="5e36f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5e36f-131">System.String</span></span>

### <span data-ttu-id="5e36f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5e36f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="5e36f-133">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5e36f-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="5e36f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e36f-134">OUTPUTS</span></span>

### <span data-ttu-id="5e36f-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="5e36f-135">System.Void</span></span>

## <span data-ttu-id="5e36f-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e36f-136">NOTES</span></span>

## <span data-ttu-id="5e36f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e36f-137">RELATED LINKS</span></span>

[<span data-ttu-id="5e36f-138">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e36f-138">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="5e36f-139">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e36f-139">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="5e36f-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5e36f-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5e36f-141">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e36f-141">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="5e36f-142">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e36f-142">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="5e36f-143">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e36f-143">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="5e36f-144">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5e36f-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


