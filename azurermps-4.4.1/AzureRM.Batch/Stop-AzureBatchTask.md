---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: ac63bbdb95551ff5ff08661a92f0924d5853ade5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500096"
---
# <span data-ttu-id="00f0d-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="00f0d-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="00f0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="00f0d-103">Leállít egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="00f0d-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00f0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00f0d-104">SYNTAX</span></span>

### <span data-ttu-id="00f0d-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="00f0d-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00f0d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="00f0d-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00f0d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="00f0d-107">DESCRIPTION</span></span>
<span data-ttu-id="00f0d-108">A **stop-AzureBatchTask** parancsmag egy Azure-köteg-feladatot leáll.</span><span class="sxs-lookup"><span data-stu-id="00f0d-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="00f0d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="00f0d-109">EXAMPLES</span></span>

### <span data-ttu-id="00f0d-110">1. példa: egy köteg tevékenységének törlése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="00f0d-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="00f0d-111">Ez a parancs leállítja azt a feladatot, amely a Task23 AZONOSÍTÓval rendelkezik a 000001 azonosítójú projektben.</span><span class="sxs-lookup"><span data-stu-id="00f0d-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="00f0d-112">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="00f0d-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="00f0d-113">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="00f0d-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="00f0d-114">2. példa: a kötegelt feladat leállítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="00f0d-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="00f0d-115">Ez a parancs azt a kötegelt feladatot kapja meg, amely a Task26 azonosító 000001 tartalmazó projekt azonosítóját tartalmazza a Get-AzureBatchTask parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="00f0d-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="00f0d-116">A parancs a tevékenységet a pipeline operátorral továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="00f0d-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="00f0d-117">A parancs leállítja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="00f0d-117">The command stops that task.</span></span>

## <span data-ttu-id="00f0d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00f0d-118">PARAMETERS</span></span>

### <span data-ttu-id="00f0d-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="00f0d-119">-BatchContext</span></span>
<span data-ttu-id="00f0d-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="00f0d-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="00f0d-121">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="00f0d-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="00f0d-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="00f0d-122">-Id</span></span>
<span data-ttu-id="00f0d-123">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="00f0d-123">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00f0d-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="00f0d-124">-JobId</span></span>
<span data-ttu-id="00f0d-125">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="00f0d-125">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="00f0d-126">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="00f0d-126">-Task</span></span>
<span data-ttu-id="00f0d-127">Azt a feladatot adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="00f0d-127">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="00f0d-128">**PSCloudTask** objektum beolvasásához használja az Get-AzureBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="00f0d-128">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00f0d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f0d-129">-DefaultProfile</span></span>
<span data-ttu-id="00f0d-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00f0d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00f0d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f0d-131">CommonParameters</span></span>
<span data-ttu-id="00f0d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00f0d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f0d-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f0d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f0d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00f0d-134">INPUTS</span></span>

### <span data-ttu-id="00f0d-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="00f0d-135">BatchAccountContext</span></span>
<span data-ttu-id="00f0d-136">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="00f0d-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="00f0d-137">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="00f0d-137">PSCloudTask</span></span>
<span data-ttu-id="00f0d-138">A "tevékenység" paraméter elfogadja a "PSCloudTask" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="00f0d-138">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="00f0d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00f0d-139">OUTPUTS</span></span>

## <span data-ttu-id="00f0d-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00f0d-140">NOTES</span></span>

## <span data-ttu-id="00f0d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00f0d-141">RELATED LINKS</span></span>

[<span data-ttu-id="00f0d-142">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="00f0d-142">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="00f0d-143">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="00f0d-143">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="00f0d-144">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="00f0d-144">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="00f0d-145">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="00f0d-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


