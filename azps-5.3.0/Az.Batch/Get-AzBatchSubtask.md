---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 4a1278734e6c9f40dc7495acb92f847d7b2cd32d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478317"
---
# <span data-ttu-id="bcd6b-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="bcd6b-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="bcd6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcd6b-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd6b-103">A megadott tevékenység altevékenység-információinak lekérte.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="bcd6b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bcd6b-104">SYNTAX</span></span>

### <span data-ttu-id="bcd6b-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bcd6b-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcd6b-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="bcd6b-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcd6b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bcd6b-107">DESCRIPTION</span></span>
<span data-ttu-id="bcd6b-108">A **Get-AzBatchSubtask** parancsmag beolvassa az altevékenység adatait a megadott tevékenységről.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="bcd6b-109">Az altevékenységek párhuzamos feldolgozást biztosítanak az egyes tevékenységekhez, és lehetővé teszik a tevékenységek végrehajtásának és előrehaladásának pontos nyomon követését.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="bcd6b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bcd6b-110">EXAMPLES</span></span>

### <span data-ttu-id="bcd6b-111">1. példa: Egy adott tevékenység összes altevékenységének visszaadott száma</span><span class="sxs-lookup"><span data-stu-id="bcd6b-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="bcd6b-112">Ezek a parancsok a myTask azonosítóval visszaadják a tevékenység összes altevékenységét.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="bcd6b-113">Ehhez a példában az első parancs létrehoz egy objektumhivatkozást a contosobatchaccount kötegfiók fiókkulcsára.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="bcd6b-114">Ezt az objektumhivatkozást egy $context.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="bcd6b-115">A második parancs ezután az objektumhivatkozást és a **Get-AzBatchSubtask** parancsmagot használva visszaadja a MyTask altevékenységét, a Job-01 feladat részeként futtatott feladatot.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="bcd6b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcd6b-116">PARAMETERS</span></span>

### <span data-ttu-id="bcd6b-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bcd6b-117">-BatchContext</span></span>
<span data-ttu-id="bcd6b-118">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bcd6b-119">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bcd6b-120">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bcd6b-121">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bcd6b-122">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bcd6b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd6b-123">-DefaultProfile</span></span>
<span data-ttu-id="bcd6b-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcd6b-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="bcd6b-125">-JobId</span></span>
<span data-ttu-id="bcd6b-126">Annak a feladatnak az azonosítója, amely azt a feladatot tartalmazza, amelynek altevékenységei ezt a parancsmagot kapják.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="bcd6b-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bcd6b-127">-MaxCount</span></span>
<span data-ttu-id="bcd6b-128">Azt adja meg, hogy legfeljebb hány altevékenységet kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="bcd6b-129">Ha nullát (0) vagy kisebb értéket ad meg, a parancsmag nem használ felső korlátot.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="bcd6b-130">Az alapértelmezett érték 1000.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="bcd6b-131">-Task</span><span class="sxs-lookup"><span data-stu-id="bcd6b-131">-Task</span></span>
<span data-ttu-id="bcd6b-132">A parancsmag által visszaadott altevékenységeket tartalmazó tevékenységre való objektumhivatkozást ad meg.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="bcd6b-133">Ez az objektumhivatkozás a Get-AzBatchTask használatával jön létre, és a visszaadott objektumot egy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="bcd6b-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="bcd6b-134">-TaskId</span></span>
<span data-ttu-id="bcd6b-135">Annak a tevékenységnek az azonosítója, amelynek altevékenységei ezt a parancsmagot visszaadják.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="bcd6b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd6b-136">CommonParameters</span></span>
<span data-ttu-id="bcd6b-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcd6b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd6b-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcd6b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd6b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcd6b-139">INPUTS</span></span>

### <span data-ttu-id="bcd6b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bcd6b-140">System.String</span></span>

### <span data-ttu-id="bcd6b-141">Microsoft.Azure.Commands.Bat. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="bcd6b-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="bcd6b-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bcd6b-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bcd6b-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcd6b-143">OUTPUTS</span></span>

### <span data-ttu-id="bcd6b-144">Microsoft.Azure.Commands.Bat. Models.PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="bcd6b-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="bcd6b-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bcd6b-145">NOTES</span></span>

## <span data-ttu-id="bcd6b-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcd6b-146">RELATED LINKS</span></span>

[<span data-ttu-id="bcd6b-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bcd6b-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


