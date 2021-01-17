---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362360"
---
# <span data-ttu-id="bf51c-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="bf51c-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="bf51c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf51c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf51c-103">A megadott feladathoz a tevékenységek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf51c-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="bf51c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bf51c-104">SYNTAX</span></span>

### <span data-ttu-id="bf51c-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="bf51c-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf51c-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="bf51c-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf51c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bf51c-107">DESCRIPTION</span></span>
<span data-ttu-id="bf51c-108">A **Get-AzBatchTaskCount** parancsmag begyűjte az Azure Batch-feladatok számát egy kötegfeladathoz.</span><span class="sxs-lookup"><span data-stu-id="bf51c-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="bf51c-109">Adjon meg egy feladatot a *JobId vagy* a *Job paraméter* alapján.</span><span class="sxs-lookup"><span data-stu-id="bf51c-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="bf51c-110">A tevékenységszámok az aktív, futó vagy befejezett tevékenységállapotok, valamint a sikeres vagy sikertelen tevékenységek számát jelentik.</span><span class="sxs-lookup"><span data-stu-id="bf51c-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="bf51c-111">Az előkészítési állapotban a feladatok futásnak számítanak.</span><span class="sxs-lookup"><span data-stu-id="bf51c-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="bf51c-112">Ha az validationStatus nincs érvényesítés nélkül, akkor a Batch szolgáltatás nem tudta ellenőrizni, hogy az állapotok a Feladatlista API-ban jelentett feladatállapotokkal vannak-e ellenőrizve.</span><span class="sxs-lookup"><span data-stu-id="bf51c-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="bf51c-113">Ha a feladat több mint 200 000 feladatot tartalmaz, előfordulhat, hogy az érvényesítésiStatus nem érvényes.</span><span class="sxs-lookup"><span data-stu-id="bf51c-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="bf51c-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bf51c-114">EXAMPLES</span></span>

### <span data-ttu-id="bf51c-115">1. példa: Tevékenységszámok lekérte azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="bf51c-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="bf51c-116">Ez a parancs a Feladat01 feladathoz megszámolandó tevékenységeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bf51c-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="bf51c-117">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="bf51c-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="bf51c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf51c-118">PARAMETERS</span></span>

### <span data-ttu-id="bf51c-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bf51c-119">-BatchContext</span></span>
<span data-ttu-id="bf51c-120">A Batch-szolgáltatáshoz használt BatchAccountContext példány.</span><span class="sxs-lookup"><span data-stu-id="bf51c-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="bf51c-121">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="bf51c-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="bf51c-122">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="bf51c-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="bf51c-123">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="bf51c-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="bf51c-124">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="bf51c-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bf51c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf51c-125">-DefaultProfile</span></span>
<span data-ttu-id="bf51c-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf51c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf51c-127">-Job</span><span class="sxs-lookup"><span data-stu-id="bf51c-127">-Job</span></span>
<span data-ttu-id="bf51c-128">Azt a feladatot adja meg, amely a parancsmag által lekért feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bf51c-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="bf51c-129">**PSCloudFeladat-objektum** beszerzéséhez használja a Get-AzBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bf51c-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf51c-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="bf51c-130">-JobId</span></span>
<span data-ttu-id="bf51c-131">Annak a feladatnak az azonosítója, amelynek a tevékenységszámát le kell számítani.</span><span class="sxs-lookup"><span data-stu-id="bf51c-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf51c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf51c-132">CommonParameters</span></span>
<span data-ttu-id="bf51c-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf51c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf51c-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf51c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf51c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf51c-135">INPUTS</span></span>

### <span data-ttu-id="bf51c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bf51c-136">System.String</span></span>

### <span data-ttu-id="bf51c-137">Microsoft.Azure.Commands.Bat. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="bf51c-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="bf51c-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bf51c-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bf51c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf51c-139">OUTPUTS</span></span>

### <span data-ttu-id="bf51c-140">Microsoft.Azure.Commands.Bat. Models.PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="bf51c-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="bf51c-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bf51c-141">NOTES</span></span>

## <span data-ttu-id="bf51c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf51c-142">RELATED LINKS</span></span>

[<span data-ttu-id="bf51c-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="bf51c-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bf51c-144">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="bf51c-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="bf51c-145">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf51c-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
