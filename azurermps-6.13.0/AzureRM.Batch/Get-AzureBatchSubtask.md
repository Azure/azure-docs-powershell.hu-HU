---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 5aa0ccc7da257cf20deb4a79d2b5415aa4c45885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502235"
---
# <span data-ttu-id="76f90-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="76f90-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="76f90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76f90-102">SYNOPSIS</span></span>
<span data-ttu-id="76f90-103">A megadott tevékenység altevékenység-információit kapja.</span><span class="sxs-lookup"><span data-stu-id="76f90-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76f90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76f90-104">SYNTAX</span></span>

### <span data-ttu-id="76f90-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76f90-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76f90-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="76f90-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76f90-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="76f90-107">DESCRIPTION</span></span>
<span data-ttu-id="76f90-108">A **Get-AzureBatchSubtask** parancsmag kikeresi a megadott tevékenység altevékenységi adatait.</span><span class="sxs-lookup"><span data-stu-id="76f90-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="76f90-109">Az altevékenységek párhuzamos feldolgozást biztosítanak az egyes tevékenységekhez, és lehetővé teszik a tevékenységek végrehajtásának és előrehaladásának pontos figyelését.</span><span class="sxs-lookup"><span data-stu-id="76f90-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="76f90-110">Példák</span><span class="sxs-lookup"><span data-stu-id="76f90-110">EXAMPLES</span></span>

### <span data-ttu-id="76f90-111">Példa 1: adott tevékenység összes altevékenységének visszaadása</span><span class="sxs-lookup"><span data-stu-id="76f90-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="76f90-112">Ezek a parancsok a tevékenységhez tartozó összes altevékenységet visszaadja az azonosító myTask.</span><span class="sxs-lookup"><span data-stu-id="76f90-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="76f90-113">Ehhez a példa első parancsa létrehoz egy objektumot a kötegelt fiók contosobatchaccount tartozó fiók kulcsaihoz.</span><span class="sxs-lookup"><span data-stu-id="76f90-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="76f90-114">Ez az objektum hivatkozás a $context nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="76f90-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="76f90-115">A második parancs ezt követően az Object Reference és a **Get-AzureBatchSubtask** parancsmagot használja az myTask összes altevékenységének visszaadására, egy olyan tevékenységre, amely a projektfeladat-01 részeként fut.</span><span class="sxs-lookup"><span data-stu-id="76f90-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="76f90-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76f90-116">PARAMETERS</span></span>

### <span data-ttu-id="76f90-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="76f90-117">-BatchContext</span></span>
<span data-ttu-id="76f90-118">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="76f90-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="76f90-119">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="76f90-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="76f90-120">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="76f90-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="76f90-121">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="76f90-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="76f90-122">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="76f90-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="76f90-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f90-123">-DefaultProfile</span></span>
<span data-ttu-id="76f90-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76f90-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76f90-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="76f90-125">-JobId</span></span>
<span data-ttu-id="76f90-126">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amely a parancsmag altevékenységeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="76f90-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f90-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="76f90-127">-MaxCount</span></span>
<span data-ttu-id="76f90-128">A visszaadni kívánt altevékenységek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="76f90-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="76f90-129">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="76f90-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="76f90-130">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="76f90-130">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f90-131">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="76f90-131">-Task</span></span>
<span data-ttu-id="76f90-132">Megadja az objektum hivatkozását arra a tevékenységre, amely a parancsmag által visszaadott altevékenységeket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="76f90-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="76f90-133">Ez az objektum hivatkozás az Get-AzureBatchTask parancsmag használatával jön létre, és a visszaadott objektumot egy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="76f90-133">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76f90-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="76f90-134">-TaskId</span></span>
<span data-ttu-id="76f90-135">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amelynek az altevékenysége ezt a parancsmagot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="76f90-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f90-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f90-136">CommonParameters</span></span>
<span data-ttu-id="76f90-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76f90-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f90-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76f90-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f90-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76f90-139">INPUTS</span></span>

### <span data-ttu-id="76f90-140">System. String</span><span class="sxs-lookup"><span data-stu-id="76f90-140">System.String</span></span>

### <span data-ttu-id="76f90-141">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="76f90-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="76f90-142">Paraméterek: tevékenység (ByValue)</span><span class="sxs-lookup"><span data-stu-id="76f90-142">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="76f90-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="76f90-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="76f90-144">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="76f90-144">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="76f90-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76f90-145">OUTPUTS</span></span>

### <span data-ttu-id="76f90-146">Microsoft.Azure.Commands.BatCH. Modellek. PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="76f90-146">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="76f90-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76f90-147">NOTES</span></span>

## <span data-ttu-id="76f90-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76f90-148">RELATED LINKS</span></span>

[<span data-ttu-id="76f90-149">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="76f90-149">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


