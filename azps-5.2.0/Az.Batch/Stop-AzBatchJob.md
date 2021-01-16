---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357067"
---
# <span data-ttu-id="8d499-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="8d499-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="8d499-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d499-102">SYNOPSIS</span></span>
<span data-ttu-id="8d499-103">Egy köteg-feladat leállítja.</span><span class="sxs-lookup"><span data-stu-id="8d499-103">Stops a Batch job.</span></span>

## <span data-ttu-id="8d499-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d499-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d499-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d499-105">DESCRIPTION</span></span>
<span data-ttu-id="8d499-106">A **Stop-AzBatch Job parancsmag** leállít egy Azure Batch-feladatot.</span><span class="sxs-lookup"><span data-stu-id="8d499-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="8d499-107">Ez a parancs befejezettként jelöli meg a feladatot.</span><span class="sxs-lookup"><span data-stu-id="8d499-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="8d499-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d499-108">EXAMPLES</span></span>

### <span data-ttu-id="8d499-109">1. példa: Kötegelt feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="8d499-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="8d499-110">Ez a parancs leállítja a 000001-es azonosítójú feladatot.</span><span class="sxs-lookup"><span data-stu-id="8d499-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="8d499-111">A parancs megadja a feladat leállításának okát.</span><span class="sxs-lookup"><span data-stu-id="8d499-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="8d499-112">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="8d499-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="8d499-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d499-113">PARAMETERS</span></span>

### <span data-ttu-id="8d499-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8d499-114">-BatchContext</span></span>
<span data-ttu-id="8d499-115">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="8d499-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8d499-116">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="8d499-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8d499-117">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="8d499-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8d499-118">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="8d499-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8d499-119">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="8d499-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8d499-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d499-120">-DefaultProfile</span></span>
<span data-ttu-id="8d499-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d499-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d499-122">-Id</span><span class="sxs-lookup"><span data-stu-id="8d499-122">-Id</span></span>
<span data-ttu-id="8d499-123">Annak a feladatnak az azonosítóját adja meg, amely leállítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8d499-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="8d499-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="8d499-124">-TerminateReason</span></span>
<span data-ttu-id="8d499-125">Megadja, hogy miért döntött úgy, hogy leállítja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="8d499-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="8d499-126">Ez a parancsmag a feladat **TerminateReason tulajdonságaként** tárolja ezt a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8d499-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="8d499-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d499-127">CommonParameters</span></span>
<span data-ttu-id="8d499-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d499-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d499-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d499-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d499-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d499-130">INPUTS</span></span>

### <span data-ttu-id="8d499-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8d499-131">System.String</span></span>

### <span data-ttu-id="8d499-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8d499-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8d499-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d499-133">OUTPUTS</span></span>

### <span data-ttu-id="8d499-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="8d499-134">System.Void</span></span>

## <span data-ttu-id="8d499-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d499-135">NOTES</span></span>

## <span data-ttu-id="8d499-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d499-136">RELATED LINKS</span></span>

[<span data-ttu-id="8d499-137">Disable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="8d499-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="8d499-138">Enable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="8d499-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="8d499-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8d499-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8d499-140">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="8d499-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="8d499-141">New-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="8d499-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="8d499-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="8d499-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="8d499-143">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8d499-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
