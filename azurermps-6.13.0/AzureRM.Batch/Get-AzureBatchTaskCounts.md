---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: 9010ec1d15958f5198c25fd0ef9e8a5ecfe6a39e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502232"
---
# <span data-ttu-id="43fc5-101">Get-AzureBatchTaskCounts</span><span class="sxs-lookup"><span data-stu-id="43fc5-101">Get-AzureBatchTaskCounts</span></span>

## <span data-ttu-id="43fc5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="43fc5-103">A tevékenység megszámlálása a megadott feladatra.</span><span class="sxs-lookup"><span data-stu-id="43fc5-103">Gets the task counts for the specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43fc5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43fc5-104">SYNTAX</span></span>

### <span data-ttu-id="43fc5-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="43fc5-105">Id</span></span>
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43fc5-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="43fc5-106">ParentObject</span></span>
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43fc5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="43fc5-107">DESCRIPTION</span></span>
<span data-ttu-id="43fc5-108">A **Get-AzureBatchTaskCounts** parancsmag az Azure-köteg feladatok számát kapja meg egy kötegelt feladatban.</span><span class="sxs-lookup"><span data-stu-id="43fc5-108">The **Get-AzureBatchTaskCounts** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="43fc5-109">Adjon meg egy feladatot a *JobId* vagy a *Job* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="43fc5-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="43fc5-110">A tevékenységek száma az aktív, a futó vagy a befejezett tevékenység állapota, valamint a sikertelen vagy sikertelen tevékenységekkel kapcsolatos tevékenységek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="43fc5-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="43fc5-111">Az előkészítő állapotú feladatok futása számításba kerülnek.</span><span class="sxs-lookup"><span data-stu-id="43fc5-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="43fc5-112">Ha a validationStatus nincs ellenőrizve, akkor a kötegelt szolgáltatás nem tudta ellenőrizni az állam számát a tevékenységekkel kapcsolatban, amint azt a lista feladatok API-ban közölte.</span><span class="sxs-lookup"><span data-stu-id="43fc5-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="43fc5-113">Előfordulhat, hogy a validationStatus nem ellenőrizhető, ha a feladat több mint 200 000 feladatot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="43fc5-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="43fc5-114">Példák</span><span class="sxs-lookup"><span data-stu-id="43fc5-114">EXAMPLES</span></span>

### <span data-ttu-id="43fc5-115">Példa 1: tevékenység számlálása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="43fc5-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="43fc5-116">Ez a parancs a tevékenység Job01 számítja ki a tevékenységet.</span><span class="sxs-lookup"><span data-stu-id="43fc5-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="43fc5-117">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="43fc5-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="43fc5-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43fc5-118">PARAMETERS</span></span>

### <span data-ttu-id="43fc5-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="43fc5-119">-BatchContext</span></span>
<span data-ttu-id="43fc5-120">A kötegelt szolgáltatással való interakció során használandó BatchAccountContext-példány.</span><span class="sxs-lookup"><span data-stu-id="43fc5-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="43fc5-121">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="43fc5-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="43fc5-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="43fc5-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="43fc5-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="43fc5-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="43fc5-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="43fc5-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="43fc5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43fc5-125">-DefaultProfile</span></span>
<span data-ttu-id="43fc5-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43fc5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43fc5-127">-Job</span><span class="sxs-lookup"><span data-stu-id="43fc5-127">-Job</span></span>
<span data-ttu-id="43fc5-128">Azt a feladatot adja meg, amely a parancsmag által kapott feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="43fc5-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="43fc5-129">**PSCloudJob** objektum beolvasásához használja az Get-AzureBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="43fc5-129">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="43fc5-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="43fc5-130">-JobId</span></span>
<span data-ttu-id="43fc5-131">Annak a projektnek az azonosítója, amelyhez a tevékenységhez tartozó adatok számítanak.</span><span class="sxs-lookup"><span data-stu-id="43fc5-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="43fc5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43fc5-132">CommonParameters</span></span>
<span data-ttu-id="43fc5-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43fc5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43fc5-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43fc5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43fc5-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43fc5-135">INPUTS</span></span>

### <span data-ttu-id="43fc5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="43fc5-136">System.String</span></span>

### <span data-ttu-id="43fc5-137">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="43fc5-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="43fc5-138">Paraméterek: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43fc5-138">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="43fc5-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="43fc5-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="43fc5-140">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43fc5-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="43fc5-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43fc5-141">OUTPUTS</span></span>

### <span data-ttu-id="43fc5-142">Microsoft.Azure.Commands.BatCH. Modellek. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="43fc5-142">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="43fc5-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43fc5-143">NOTES</span></span>

## <span data-ttu-id="43fc5-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43fc5-144">RELATED LINKS</span></span>

[<span data-ttu-id="43fc5-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="43fc5-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="43fc5-146">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43fc5-146">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="43fc5-147">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="43fc5-147">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
