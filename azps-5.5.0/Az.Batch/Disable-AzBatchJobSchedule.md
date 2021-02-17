---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: f874432bc26ae2a579a54e4068c719b236ad4c45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205406"
---
# <span data-ttu-id="0b234-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b234-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="0b234-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b234-102">SYNOPSIS</span></span>
<span data-ttu-id="0b234-103">Letiltja a köteg feladatütemtervét.</span><span class="sxs-lookup"><span data-stu-id="0b234-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="0b234-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b234-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b234-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b234-105">DESCRIPTION</span></span>
<span data-ttu-id="0b234-106">A **Disable-AzBatch JobSchedule** parancsmag letiltja az Azure Batch-feladat ütemezését.</span><span class="sxs-lookup"><span data-stu-id="0b234-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="0b234-107">Ha letilt egy ütemtervet, a feladatok nem az ütemezésnek megfelelően jön létre.</span><span class="sxs-lookup"><span data-stu-id="0b234-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="0b234-108">A letiltott ütemezést később is engedélyezheti.</span><span class="sxs-lookup"><span data-stu-id="0b234-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="0b234-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b234-109">EXAMPLES</span></span>

### <span data-ttu-id="0b234-110">1. példa: Munkabeosztás letiltása</span><span class="sxs-lookup"><span data-stu-id="0b234-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="0b234-111">Ez a parancs letiltja azt a munkabeosztást, amely a JobSchedule17 azonosítóval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="0b234-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="0b234-112">A **Get-AzBatchAccountKey** parancsmaggal kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="0b234-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="0b234-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b234-113">PARAMETERS</span></span>

### <span data-ttu-id="0b234-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0b234-114">-BatchContext</span></span>
<span data-ttu-id="0b234-115">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="0b234-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0b234-116">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="0b234-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0b234-117">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="0b234-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0b234-118">Megosztott kulcsú hitelesítés használata esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="0b234-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0b234-119">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="0b234-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0b234-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b234-120">-DefaultProfile</span></span>
<span data-ttu-id="0b234-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b234-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b234-122">-Id</span><span class="sxs-lookup"><span data-stu-id="0b234-122">-Id</span></span>
<span data-ttu-id="0b234-123">A parancsmag által letiltott feladatütemterv azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0b234-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="0b234-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b234-124">CommonParameters</span></span>
<span data-ttu-id="0b234-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b234-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b234-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b234-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b234-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b234-127">INPUTS</span></span>

### <span data-ttu-id="0b234-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0b234-128">System.String</span></span>

### <span data-ttu-id="0b234-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0b234-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0b234-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b234-130">OUTPUTS</span></span>

### <span data-ttu-id="0b234-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="0b234-131">System.Void</span></span>

## <span data-ttu-id="0b234-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b234-132">NOTES</span></span>

## <span data-ttu-id="0b234-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b234-133">RELATED LINKS</span></span>

[<span data-ttu-id="0b234-134">Enable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b234-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="0b234-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0b234-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0b234-136">Get-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b234-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="0b234-137">New-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b234-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="0b234-138">Remove-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b234-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="0b234-139">Stop-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b234-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="0b234-140">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0b234-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
