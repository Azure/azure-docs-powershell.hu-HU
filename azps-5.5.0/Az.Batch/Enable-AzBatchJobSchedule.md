---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205359"
---
# <span data-ttu-id="0b4a9-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b4a9-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="0b4a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b4a9-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4a9-103">Engedélyezi a köteg feladatütemtervét.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="0b4a9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b4a9-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b4a9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b4a9-105">DESCRIPTION</span></span>
<span data-ttu-id="0b4a9-106">Az **Enable-AzBatch JobSchedule** parancsmag lehetővé teszi az Azure Batch-feladat ütemezését.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="0b4a9-107">A munkabeosztás engedélyezése után a feladatok az ütemezésnek megfelelően is létrejönnek.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="0b4a9-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b4a9-108">EXAMPLES</span></span>

### <span data-ttu-id="0b4a9-109">1. példa: Munkabeosztás engedélyezése</span><span class="sxs-lookup"><span data-stu-id="0b4a9-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="0b4a9-110">Ez a parancs engedélyezi a Feladatütemterv azonosítót 17 azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="0b4a9-111">A **Get-AzBatchAccountKey** parancsmaggal kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="0b4a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b4a9-112">PARAMETERS</span></span>

### <span data-ttu-id="0b4a9-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0b4a9-113">-BatchContext</span></span>
<span data-ttu-id="0b4a9-114">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0b4a9-115">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0b4a9-116">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot, és töltse ki a hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0b4a9-117">Megosztott kulcsú hitelesítés használata esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0b4a9-118">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0b4a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4a9-119">-DefaultProfile</span></span>
<span data-ttu-id="0b4a9-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b4a9-121">-Id</span><span class="sxs-lookup"><span data-stu-id="0b4a9-121">-Id</span></span>
<span data-ttu-id="0b4a9-122">A parancsmag által lehetővé tesz feladatütemterv azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="0b4a9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4a9-123">CommonParameters</span></span>
<span data-ttu-id="0b4a9-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b4a9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4a9-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b4a9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4a9-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b4a9-126">INPUTS</span></span>

### <span data-ttu-id="0b4a9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0b4a9-127">System.String</span></span>

### <span data-ttu-id="0b4a9-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0b4a9-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0b4a9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b4a9-129">OUTPUTS</span></span>

### <span data-ttu-id="0b4a9-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="0b4a9-130">System.Void</span></span>

## <span data-ttu-id="0b4a9-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b4a9-131">NOTES</span></span>

## <span data-ttu-id="0b4a9-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b4a9-132">RELATED LINKS</span></span>

[<span data-ttu-id="0b4a9-133">Disable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b4a9-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="0b4a9-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0b4a9-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0b4a9-135">Get-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b4a9-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="0b4a9-136">New-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b4a9-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="0b4a9-137">Remove-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b4a9-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="0b4a9-138">Stop-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b4a9-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="0b4a9-139">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0b4a9-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
