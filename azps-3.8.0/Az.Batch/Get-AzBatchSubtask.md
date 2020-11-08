---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 4a1278734e6c9f40dc7495acb92f847d7b2cd32d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013003"
---
# <span data-ttu-id="bf579-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="bf579-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="bf579-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf579-102">SYNOPSIS</span></span>
<span data-ttu-id="bf579-103">A megadott tevékenység altevékenység-információit kapja.</span><span class="sxs-lookup"><span data-stu-id="bf579-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="bf579-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf579-104">SYNTAX</span></span>

### <span data-ttu-id="bf579-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf579-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf579-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="bf579-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf579-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf579-107">DESCRIPTION</span></span>
<span data-ttu-id="bf579-108">A **Get-AzBatchSubtask** parancsmag kikeresi a megadott tevékenység altevékenységi adatait.</span><span class="sxs-lookup"><span data-stu-id="bf579-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="bf579-109">Az altevékenységek párhuzamos feldolgozást biztosítanak az egyes tevékenységekhez, és lehetővé teszik a tevékenységek végrehajtásának és előrehaladásának pontos figyelését.</span><span class="sxs-lookup"><span data-stu-id="bf579-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="bf579-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bf579-110">EXAMPLES</span></span>

### <span data-ttu-id="bf579-111">Példa 1: adott tevékenység összes altevékenységének visszaadása</span><span class="sxs-lookup"><span data-stu-id="bf579-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="bf579-112">Ezek a parancsok a tevékenységhez tartozó összes altevékenységet visszaadja az azonosító myTask.</span><span class="sxs-lookup"><span data-stu-id="bf579-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="bf579-113">Ehhez a példa első parancsa létrehoz egy objektumot a kötegelt fiók contosobatchaccount tartozó fiók kulcsaihoz.</span><span class="sxs-lookup"><span data-stu-id="bf579-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="bf579-114">Ez az objektum hivatkozás a $context nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="bf579-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="bf579-115">A második parancs ezt követően az Object Reference és a **Get-AzBatchSubtask** parancsmagot használja az myTask összes altevékenységének visszaadására, egy olyan tevékenységre, amely a projektfeladat-01 részeként fut.</span><span class="sxs-lookup"><span data-stu-id="bf579-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="bf579-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf579-116">PARAMETERS</span></span>

### <span data-ttu-id="bf579-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bf579-117">-BatchContext</span></span>
<span data-ttu-id="bf579-118">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="bf579-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bf579-119">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="bf579-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bf579-120">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="bf579-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bf579-121">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="bf579-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bf579-122">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="bf579-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bf579-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf579-123">-DefaultProfile</span></span>
<span data-ttu-id="bf579-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf579-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf579-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="bf579-125">-JobId</span></span>
<span data-ttu-id="bf579-126">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amely a parancsmag altevékenységeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bf579-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="bf579-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bf579-127">-MaxCount</span></span>
<span data-ttu-id="bf579-128">A visszaadni kívánt altevékenységek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf579-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="bf579-129">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="bf579-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="bf579-130">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="bf579-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="bf579-131">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="bf579-131">-Task</span></span>
<span data-ttu-id="bf579-132">Megadja az objektum hivatkozását arra a tevékenységre, amely a parancsmag által visszaadott altevékenységeket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bf579-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="bf579-133">Ez az objektum hivatkozás az Get-AzBatchTask parancsmag használatával jön létre, és a visszaadott objektumot egy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bf579-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="bf579-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="bf579-134">-TaskId</span></span>
<span data-ttu-id="bf579-135">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amelynek az altevékenysége ezt a parancsmagot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bf579-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="bf579-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf579-136">CommonParameters</span></span>
<span data-ttu-id="bf579-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf579-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf579-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bf579-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf579-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf579-139">INPUTS</span></span>

### <span data-ttu-id="bf579-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bf579-140">System.String</span></span>

### <span data-ttu-id="bf579-141">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="bf579-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="bf579-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bf579-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bf579-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf579-143">OUTPUTS</span></span>

### <span data-ttu-id="bf579-144">Microsoft.Azure.Commands.BatCH. Modellek. PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="bf579-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="bf579-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf579-145">NOTES</span></span>

## <span data-ttu-id="bf579-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf579-146">RELATED LINKS</span></span>

[<span data-ttu-id="bf579-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bf579-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


