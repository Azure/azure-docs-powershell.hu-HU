---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: a25c31c0b73a42e0d64b567b6bc2529bf4ebf258
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205407"
---
# <span data-ttu-id="85176-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="85176-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="85176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85176-102">SYNOPSIS</span></span>
<span data-ttu-id="85176-103">Letilt egy köteg-feladatot.</span><span class="sxs-lookup"><span data-stu-id="85176-103">Disables a Batch job.</span></span>

## <span data-ttu-id="85176-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="85176-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85176-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="85176-105">DESCRIPTION</span></span>
<span data-ttu-id="85176-106">A **Disable-AzBatch Job** parancsmag letiltja az Azure Batch-feladatot.</span><span class="sxs-lookup"><span data-stu-id="85176-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="85176-107">A feladat engedélyezése után az új feladatok futtathatók.</span><span class="sxs-lookup"><span data-stu-id="85176-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="85176-108">A letiltott feladatok nem futtatnak új feladatokat.</span><span class="sxs-lookup"><span data-stu-id="85176-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="85176-109">Később engedélyezheti a letiltott feladatot.</span><span class="sxs-lookup"><span data-stu-id="85176-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="85176-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="85176-110">EXAMPLES</span></span>

### <span data-ttu-id="85176-111">1. példa: Kötegelt feladat letiltása</span><span class="sxs-lookup"><span data-stu-id="85176-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="85176-112">Ez a parancs letiltja a 000001 azonosítójú feladatot.</span><span class="sxs-lookup"><span data-stu-id="85176-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="85176-113">A parancs megszakítja a feladat aktív feladatait.</span><span class="sxs-lookup"><span data-stu-id="85176-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="85176-114">A **Get-AzBatchAccountKey** parancsmaggal kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="85176-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="85176-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85176-115">PARAMETERS</span></span>

### <span data-ttu-id="85176-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="85176-116">-BatchContext</span></span>
<span data-ttu-id="85176-117">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="85176-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="85176-118">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="85176-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="85176-119">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot, és töltse ki a hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="85176-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="85176-120">Megosztott kulcsú hitelesítés használata esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="85176-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="85176-121">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="85176-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="85176-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85176-122">-DefaultProfile</span></span>
<span data-ttu-id="85176-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85176-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85176-124">-DisableOption</span><span class="sxs-lookup"><span data-stu-id="85176-124">-DisableJobOption</span></span>
<span data-ttu-id="85176-125">Meghatározza, hogy mit kell tenni a parancsmag által letiltott feladathoz társított aktív feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="85176-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="85176-126">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="85176-126">Valid values are:</span></span>
- <span data-ttu-id="85176-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="85176-127">Requeue</span></span>
- <span data-ttu-id="85176-128">Lezárás</span><span class="sxs-lookup"><span data-stu-id="85176-128">Terminate</span></span>
- <span data-ttu-id="85176-129">várj</span><span class="sxs-lookup"><span data-stu-id="85176-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85176-130">-Id</span><span class="sxs-lookup"><span data-stu-id="85176-130">-Id</span></span>
<span data-ttu-id="85176-131">A parancsmag által letiltott feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="85176-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="85176-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85176-132">CommonParameters</span></span>
<span data-ttu-id="85176-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85176-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85176-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85176-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85176-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85176-135">INPUTS</span></span>

### <span data-ttu-id="85176-136">System.String</span><span class="sxs-lookup"><span data-stu-id="85176-136">System.String</span></span>

### <span data-ttu-id="85176-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="85176-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="85176-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85176-138">OUTPUTS</span></span>

### <span data-ttu-id="85176-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="85176-139">System.Void</span></span>

## <span data-ttu-id="85176-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="85176-140">NOTES</span></span>

## <span data-ttu-id="85176-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85176-141">RELATED LINKS</span></span>

[<span data-ttu-id="85176-142">Enable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="85176-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="85176-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="85176-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="85176-144">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="85176-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="85176-145">New-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="85176-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="85176-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="85176-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="85176-147">Stop-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="85176-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="85176-148">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="85176-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
