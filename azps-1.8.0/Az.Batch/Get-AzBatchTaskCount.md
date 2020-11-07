---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: 51e9053737b95113144d5421492f64623b425ff6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671869"
---
# <span data-ttu-id="ab37d-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="ab37d-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="ab37d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab37d-102">SYNOPSIS</span></span>
<span data-ttu-id="ab37d-103">A tevékenység megszámlálása a megadott feladatra.</span><span class="sxs-lookup"><span data-stu-id="ab37d-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="ab37d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab37d-104">SYNTAX</span></span>

### <span data-ttu-id="ab37d-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="ab37d-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab37d-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ab37d-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab37d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab37d-107">DESCRIPTION</span></span>
<span data-ttu-id="ab37d-108">A **Get-AzBatchTaskCount** parancsmag az Azure-köteg feladatok számát kapja meg egy kötegelt feladatban.</span><span class="sxs-lookup"><span data-stu-id="ab37d-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="ab37d-109">Adjon meg egy feladatot a *JobId* vagy a *Job* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="ab37d-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="ab37d-110">A tevékenységek száma az aktív, a futó vagy a befejezett tevékenység állapota, valamint a sikertelen vagy sikertelen tevékenységekkel kapcsolatos tevékenységek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab37d-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="ab37d-111">Az előkészítő állapotú feladatok futása számításba kerülnek.</span><span class="sxs-lookup"><span data-stu-id="ab37d-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="ab37d-112">Ha a validationStatus nincs ellenőrizve, akkor a kötegelt szolgáltatás nem tudta ellenőrizni az állam számát a tevékenységekkel kapcsolatban, amint azt a lista feladatok API-ban közölte.</span><span class="sxs-lookup"><span data-stu-id="ab37d-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="ab37d-113">Előfordulhat, hogy a validationStatus nem ellenőrizhető, ha a feladat több mint 200 000 feladatot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ab37d-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="ab37d-114">Példák</span><span class="sxs-lookup"><span data-stu-id="ab37d-114">EXAMPLES</span></span>

### <span data-ttu-id="ab37d-115">Példa 1: tevékenység számlálása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="ab37d-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="ab37d-116">Ez a parancs a tevékenység Job01 számítja ki a tevékenységet.</span><span class="sxs-lookup"><span data-stu-id="ab37d-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="ab37d-117">A Get-AzBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="ab37d-117">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="ab37d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab37d-118">PARAMETERS</span></span>

### <span data-ttu-id="ab37d-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ab37d-119">-BatchContext</span></span>
<span data-ttu-id="ab37d-120">A kötegelt szolgáltatással való interakció során használandó BatchAccountContext-példány.</span><span class="sxs-lookup"><span data-stu-id="ab37d-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="ab37d-121">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="ab37d-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="ab37d-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="ab37d-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="ab37d-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="ab37d-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="ab37d-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="ab37d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ab37d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab37d-125">-DefaultProfile</span></span>
<span data-ttu-id="ab37d-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab37d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab37d-127">-Job</span><span class="sxs-lookup"><span data-stu-id="ab37d-127">-Job</span></span>
<span data-ttu-id="ab37d-128">Azt a feladatot adja meg, amely a parancsmag által kapott feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ab37d-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="ab37d-129">**PSCloudJob** objektum beolvasásához használja az Get-AzBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ab37d-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="ab37d-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="ab37d-130">-JobId</span></span>
<span data-ttu-id="ab37d-131">Annak a projektnek az azonosítója, amelyhez a tevékenységhez tartozó adatok számítanak.</span><span class="sxs-lookup"><span data-stu-id="ab37d-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="ab37d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab37d-132">CommonParameters</span></span>
<span data-ttu-id="ab37d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab37d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab37d-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab37d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab37d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab37d-135">INPUTS</span></span>

### <span data-ttu-id="ab37d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ab37d-136">System.String</span></span>

### <span data-ttu-id="ab37d-137">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="ab37d-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="ab37d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ab37d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ab37d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab37d-139">OUTPUTS</span></span>

### <span data-ttu-id="ab37d-140">Microsoft.Azure.Commands.BatCH. Modellek. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="ab37d-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="ab37d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab37d-141">NOTES</span></span>

## <span data-ttu-id="ab37d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab37d-142">RELATED LINKS</span></span>

[<span data-ttu-id="ab37d-143">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ab37d-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ab37d-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ab37d-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="ab37d-145">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ab37d-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
