---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: b572a7aefc3076671e78895f5fea531929858873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503256"
---
# <span data-ttu-id="b8dcb-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8dcb-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="b8dcb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="b8dcb-103">Frissíti a tevékenység tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b8dcb-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8dcb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8dcb-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8dcb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8dcb-105">DESCRIPTION</span></span>
<span data-ttu-id="b8dcb-106">A **set-AzureBatchTask** parancsmag frissíti egy tevékenység tulajdonságait az Azure kötegfájl-szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="b8dcb-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="b8dcb-107">A Get-AzureBatchTask parancsmaggal **PSCloudTask** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="b8dcb-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="b8dcb-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="b8dcb-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="b8dcb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b8dcb-109">EXAMPLES</span></span>

### <span data-ttu-id="b8dcb-110">Példa 1: tevékenység frissítése</span><span class="sxs-lookup"><span data-stu-id="b8dcb-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="b8dcb-111">Az első parancs **beolvassa a feladatot a Get-AzureBatchTask** függvénnyel, majd a $Task változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b8dcb-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="b8dcb-112">A következő két parancs módosítja a tevékenység korlátozásait a $Taskban.</span><span class="sxs-lookup"><span data-stu-id="b8dcb-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="b8dcb-113">A végleges parancs frissíti a kötegfájlt a $Task helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="b8dcb-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="b8dcb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8dcb-114">PARAMETERS</span></span>

### <span data-ttu-id="b8dcb-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b8dcb-115">-BatchContext</span></span>
<span data-ttu-id="b8dcb-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="b8dcb-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b8dcb-117">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b8dcb-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b8dcb-118">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="b8dcb-118">-Task</span></span>
<span data-ttu-id="b8dcb-119">Azt a **PSCloudTask** adja meg, amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b8dcb-119">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dcb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8dcb-120">-DefaultProfile</span></span>
<span data-ttu-id="b8dcb-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8dcb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8dcb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8dcb-122">CommonParameters</span></span>
<span data-ttu-id="b8dcb-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8dcb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8dcb-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8dcb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8dcb-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8dcb-125">INPUTS</span></span>

### <span data-ttu-id="b8dcb-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b8dcb-126">BatchAccountContext</span></span>
<span data-ttu-id="b8dcb-127">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b8dcb-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b8dcb-128">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="b8dcb-128">PSCloudTask</span></span>
<span data-ttu-id="b8dcb-129">A "tevékenység" paraméter elfogadja a "PSCloudTask" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b8dcb-129">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="b8dcb-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8dcb-130">OUTPUTS</span></span>

## <span data-ttu-id="b8dcb-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8dcb-131">NOTES</span></span>

## <span data-ttu-id="b8dcb-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8dcb-132">RELATED LINKS</span></span>

[<span data-ttu-id="b8dcb-133">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8dcb-133">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="b8dcb-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b8dcb-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b8dcb-135">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8dcb-135">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="b8dcb-136">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8dcb-136">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="b8dcb-137">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8dcb-137">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="b8dcb-138">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b8dcb-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


