---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: a25c31c0b73a42e0d64b567b6bc2529bf4ebf258
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353897"
---
# <span data-ttu-id="fb998-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fb998-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="fb998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb998-102">SYNOPSIS</span></span>
<span data-ttu-id="fb998-103">Letilt egy köteg-feladatot.</span><span class="sxs-lookup"><span data-stu-id="fb998-103">Disables a Batch job.</span></span>

## <span data-ttu-id="fb998-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb998-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb998-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb998-105">DESCRIPTION</span></span>
<span data-ttu-id="fb998-106">A **Disable-AzBatch Job parancsmag** letiltja az Azure Batch-feladatot.</span><span class="sxs-lookup"><span data-stu-id="fb998-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="fb998-107">A feladat engedélyezése után az új feladatok futtathatók.</span><span class="sxs-lookup"><span data-stu-id="fb998-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="fb998-108">A letiltott feladatok nem futtatnak új feladatokat.</span><span class="sxs-lookup"><span data-stu-id="fb998-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="fb998-109">Később engedélyezheti a letiltott feladatot.</span><span class="sxs-lookup"><span data-stu-id="fb998-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="fb998-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb998-110">EXAMPLES</span></span>

### <span data-ttu-id="fb998-111">1. példa: Kötegelt feladat letiltása</span><span class="sxs-lookup"><span data-stu-id="fb998-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="fb998-112">Ez a parancs letiltja a 000001 azonosítójú feladatot.</span><span class="sxs-lookup"><span data-stu-id="fb998-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="fb998-113">A parancs megszakítja a feladat aktív feladatait.</span><span class="sxs-lookup"><span data-stu-id="fb998-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="fb998-114">A **Get-AzBatchAccountKey** parancsmaggal kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="fb998-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="fb998-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb998-115">PARAMETERS</span></span>

### <span data-ttu-id="fb998-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fb998-116">-BatchContext</span></span>
<span data-ttu-id="fb998-117">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="fb998-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fb998-118">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="fb998-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fb998-119">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="fb998-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fb998-120">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="fb998-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fb998-121">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="fb998-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fb998-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb998-122">-DefaultProfile</span></span>
<span data-ttu-id="fb998-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb998-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb998-124">-DisableOption</span><span class="sxs-lookup"><span data-stu-id="fb998-124">-DisableJobOption</span></span>
<span data-ttu-id="fb998-125">Meghatározza, hogy mit kell tenni a parancsmag által letiltott feladathoz társított aktív feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="fb998-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="fb998-126">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="fb998-126">Valid values are:</span></span>
- <span data-ttu-id="fb998-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="fb998-127">Requeue</span></span>
- <span data-ttu-id="fb998-128">Lezárás</span><span class="sxs-lookup"><span data-stu-id="fb998-128">Terminate</span></span>
- <span data-ttu-id="fb998-129">várj</span><span class="sxs-lookup"><span data-stu-id="fb998-129">Wait</span></span>

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

### <span data-ttu-id="fb998-130">-Id</span><span class="sxs-lookup"><span data-stu-id="fb998-130">-Id</span></span>
<span data-ttu-id="fb998-131">A parancsmag által letiltott feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fb998-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="fb998-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb998-132">CommonParameters</span></span>
<span data-ttu-id="fb998-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb998-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb998-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb998-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb998-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb998-135">INPUTS</span></span>

### <span data-ttu-id="fb998-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fb998-136">System.String</span></span>

### <span data-ttu-id="fb998-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fb998-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fb998-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb998-138">OUTPUTS</span></span>

### <span data-ttu-id="fb998-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="fb998-139">System.Void</span></span>

## <span data-ttu-id="fb998-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb998-140">NOTES</span></span>

## <span data-ttu-id="fb998-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb998-141">RELATED LINKS</span></span>

[<span data-ttu-id="fb998-142">Enable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="fb998-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="fb998-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="fb998-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fb998-144">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="fb998-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="fb998-145">New-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="fb998-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="fb998-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fb998-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="fb998-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fb998-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="fb998-148">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fb998-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
