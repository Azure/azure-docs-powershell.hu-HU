---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 58bed6fda4040c1af48469f4aa85f717c26c898c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505651"
---
# <span data-ttu-id="003c5-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="003c5-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="003c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="003c5-102">SYNOPSIS</span></span>
<span data-ttu-id="003c5-103">A megadott tevékenység altevékenység-információit kapja.</span><span class="sxs-lookup"><span data-stu-id="003c5-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="003c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="003c5-104">SYNTAX</span></span>

### <span data-ttu-id="003c5-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="003c5-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="003c5-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="003c5-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="003c5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="003c5-107">DESCRIPTION</span></span>
<span data-ttu-id="003c5-108">A **Get-AzureBatchSubtask** parancsmag kikeresi a megadott tevékenység altevékenységi adatait.</span><span class="sxs-lookup"><span data-stu-id="003c5-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="003c5-109">Az altevékenységek párhuzamos feldolgozást biztosítanak az egyes tevékenységekhez, és lehetővé teszik a tevékenységek végrehajtásának és előrehaladásának pontos figyelését.</span><span class="sxs-lookup"><span data-stu-id="003c5-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="003c5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="003c5-110">EXAMPLES</span></span>

### <span data-ttu-id="003c5-111">Példa 1: adott tevékenység összes altevékenységének visszaadása</span><span class="sxs-lookup"><span data-stu-id="003c5-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="003c5-112">Ezek a parancsok a tevékenységhez tartozó összes altevékenységet visszaadja az azonosító myTask.</span><span class="sxs-lookup"><span data-stu-id="003c5-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="003c5-113">Ehhez a példa első parancsa létrehoz egy objektumot a kötegelt fiók contosobatchaccount tartozó fiók kulcsaihoz.</span><span class="sxs-lookup"><span data-stu-id="003c5-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="003c5-114">Ez az objektum hivatkozás a $context nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="003c5-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="003c5-115">A második parancs ezt követően az Object Reference és a **Get-AzureBatchSubtask** parancsmagot használja az myTask összes altevékenységének visszaadására, egy olyan tevékenységre, amely a projektfeladat-01 részeként fut.</span><span class="sxs-lookup"><span data-stu-id="003c5-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="003c5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="003c5-116">PARAMETERS</span></span>

### <span data-ttu-id="003c5-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="003c5-117">-BatchContext</span></span>
<span data-ttu-id="003c5-118">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="003c5-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="003c5-119">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="003c5-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="003c5-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="003c5-120">-JobId</span></span>
<span data-ttu-id="003c5-121">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amely a parancsmag altevékenységeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="003c5-121">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="003c5-122">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="003c5-122">-MaxCount</span></span>
<span data-ttu-id="003c5-123">A visszaadni kívánt altevékenységek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="003c5-123">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="003c5-124">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="003c5-124">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="003c5-125">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="003c5-125">The default value is 1000.</span></span>

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

### <span data-ttu-id="003c5-126">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="003c5-126">-Task</span></span>
<span data-ttu-id="003c5-127">Megadja az objektum hivatkozását arra a tevékenységre, amely a parancsmag által visszaadott altevékenységeket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="003c5-127">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="003c5-128">Ez az objektum hivatkozás az Get-AzureBatchTask parancsmag használatával jön létre, és a visszaadott objektumot egy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="003c5-128">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="003c5-129">-TaskId</span><span class="sxs-lookup"><span data-stu-id="003c5-129">-TaskId</span></span>
<span data-ttu-id="003c5-130">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amelynek az altevékenysége ezt a parancsmagot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="003c5-130">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="003c5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003c5-131">-DefaultProfile</span></span>
<span data-ttu-id="003c5-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="003c5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="003c5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003c5-133">CommonParameters</span></span>
<span data-ttu-id="003c5-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="003c5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003c5-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="003c5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003c5-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="003c5-136">INPUTS</span></span>

### <span data-ttu-id="003c5-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="003c5-137">BatchAccountContext</span></span>
<span data-ttu-id="003c5-138">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="003c5-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="003c5-139">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="003c5-139">PSCloudTask</span></span>
<span data-ttu-id="003c5-140">A "tevékenység" paraméter elfogadja a "PSCloudTask" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="003c5-140">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="003c5-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="003c5-141">OUTPUTS</span></span>

###  
<span data-ttu-id="003c5-142">Ez a parancsmag a **PSSubtaskInformation** objektum példányait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="003c5-142">This cmdlet returns instances of the **PSSubtaskInformation** object.</span></span>

## <span data-ttu-id="003c5-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="003c5-143">NOTES</span></span>

## <span data-ttu-id="003c5-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="003c5-144">RELATED LINKS</span></span>

[<span data-ttu-id="003c5-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="003c5-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


