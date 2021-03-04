---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: cc084f276f379013125693e3314ff1eab8a7b123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925209"
---
# <span data-ttu-id="1d298-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1d298-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="1d298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d298-102">SYNOPSIS</span></span>
<span data-ttu-id="1d298-103">Egy köteg-feladat frissítése.</span><span class="sxs-lookup"><span data-stu-id="1d298-103">Updates a Batch job.</span></span>

## <span data-ttu-id="1d298-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d298-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d298-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d298-105">DESCRIPTION</span></span>
<span data-ttu-id="1d298-106">A **Set-AzBatch Job parancsmag** frissíti az Azure Batch-feladatot.</span><span class="sxs-lookup"><span data-stu-id="1d298-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="1d298-107">A Get-AzBatchJob parancsmagot használva szerezze be a **PSCloud Objectot.**</span><span class="sxs-lookup"><span data-stu-id="1d298-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="1d298-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmagot használva végleges kövesse a módosításokat a Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="1d298-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="1d298-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d298-109">EXAMPLES</span></span>

### <span data-ttu-id="1d298-110">1. példa: Feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="1d298-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="1d298-111">Az első parancs a **Get-AzBatch Paranccsal** kap feladatot, majd azt a $Job tárolja.</span><span class="sxs-lookup"><span data-stu-id="1d298-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="1d298-112">A második parancs módosítja a prioritásspecifikációt a $Job objektumon.</span><span class="sxs-lookup"><span data-stu-id="1d298-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="1d298-113">Az utolsó parancs frissíti a Batch szolgáltatást úgy, hogy megfeleljen a helyi objektumnak a $Job.</span><span class="sxs-lookup"><span data-stu-id="1d298-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="1d298-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d298-114">PARAMETERS</span></span>

### <span data-ttu-id="1d298-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1d298-115">-BatchContext</span></span>
<span data-ttu-id="1d298-116">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="1d298-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1d298-117">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="1d298-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1d298-118">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="1d298-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1d298-119">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="1d298-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1d298-120">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="1d298-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1d298-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d298-121">-DefaultProfile</span></span>
<span data-ttu-id="1d298-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d298-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d298-123">-Job</span><span class="sxs-lookup"><span data-stu-id="1d298-123">-Job</span></span>
<span data-ttu-id="1d298-124">Egy **PSCloud Parancsfájlt ad** meg, amelyre ez a parancsmag frissíti a Batch szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="1d298-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d298-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d298-125">CommonParameters</span></span>
<span data-ttu-id="1d298-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d298-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d298-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d298-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d298-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d298-128">INPUTS</span></span>

### <span data-ttu-id="1d298-129">Microsoft.Azure.Commands.Bat. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="1d298-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="1d298-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1d298-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1d298-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d298-131">OUTPUTS</span></span>

### <span data-ttu-id="1d298-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="1d298-132">System.Void</span></span>

## <span data-ttu-id="1d298-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d298-133">NOTES</span></span>

## <span data-ttu-id="1d298-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d298-134">RELATED LINKS</span></span>

[<span data-ttu-id="1d298-135">Disable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="1d298-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="1d298-136">Enable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="1d298-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="1d298-137">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="1d298-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="1d298-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1d298-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1d298-139">New-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="1d298-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="1d298-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1d298-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="1d298-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1d298-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="1d298-142">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="1d298-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
