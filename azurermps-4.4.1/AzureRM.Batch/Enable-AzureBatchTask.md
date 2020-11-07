---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 8e7636d83b953997ac1f9269e45fbf3c2278612f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680613"
---
# <span data-ttu-id="471da-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="471da-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="471da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="471da-102">SYNOPSIS</span></span>
<span data-ttu-id="471da-103">Tevékenység újraaktiválása</span><span class="sxs-lookup"><span data-stu-id="471da-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="471da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="471da-104">SYNTAX</span></span>

### <span data-ttu-id="471da-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="471da-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="471da-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="471da-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="471da-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="471da-107">DESCRIPTION</span></span>
<span data-ttu-id="471da-108">Az **enable-AzureBatchTask** parancsmag újraaktiválja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="471da-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="471da-109">Ha egy tevékenység kimerítette az újrapróbálkozások számát, ez a parancsmag mégis lehetővé teszi a futtatását.</span><span class="sxs-lookup"><span data-stu-id="471da-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="471da-110">Példák</span><span class="sxs-lookup"><span data-stu-id="471da-110">EXAMPLES</span></span>

### <span data-ttu-id="471da-111">1. példa: tevékenység újraaktiválása</span><span class="sxs-lookup"><span data-stu-id="471da-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="471da-112">Ez a parancs újra aktiválja a tevékenység Task2 a munkahelyi Job7.</span><span class="sxs-lookup"><span data-stu-id="471da-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="471da-113">2. példa: tevékenység újraaktiválása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="471da-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="471da-114">Ez a parancs azt a kötegelt feladatot kapja meg, amely a Task3 azonosítóval rendelkezik, és az Get-AzureBatchTask parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="471da-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="471da-115">A parancs a tevékenységet a pipeline operátorral továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="471da-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="471da-116">A parancs újra aktiválja ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="471da-116">The command reactivates that task.</span></span>

## <span data-ttu-id="471da-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="471da-117">PARAMETERS</span></span>

### <span data-ttu-id="471da-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="471da-118">-BatchContext</span></span>
<span data-ttu-id="471da-119">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="471da-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="471da-120">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="471da-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="471da-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="471da-121">-Id</span></span>
<span data-ttu-id="471da-122">Az újraaktiválni kívánt tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="471da-122">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="471da-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="471da-123">-JobId</span></span>
<span data-ttu-id="471da-124">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="471da-124">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="471da-125">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="471da-125">-Task</span></span>
<span data-ttu-id="471da-126">A parancsmag által újraaktivált feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="471da-126">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="471da-127">**PSCloudTask** objektum beolvasásához használja az Get-AzureBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="471da-127">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="471da-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="471da-128">-Confirm</span></span>
<span data-ttu-id="471da-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="471da-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="471da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="471da-130">-WhatIf</span></span>
<span data-ttu-id="471da-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="471da-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="471da-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="471da-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="471da-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="471da-133">-DefaultProfile</span></span>
<span data-ttu-id="471da-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="471da-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="471da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471da-135">CommonParameters</span></span>
<span data-ttu-id="471da-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="471da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471da-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="471da-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471da-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="471da-138">INPUTS</span></span>

### <span data-ttu-id="471da-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="471da-139">BatchAccountContext</span></span>
<span data-ttu-id="471da-140">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="471da-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="471da-141">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="471da-141">PSCloudTask</span></span>
<span data-ttu-id="471da-142">A "tevékenység" paraméter elfogadja a "PSCloudTask" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="471da-142">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="471da-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="471da-143">OUTPUTS</span></span>

## <span data-ttu-id="471da-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="471da-144">NOTES</span></span>

## <span data-ttu-id="471da-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="471da-145">RELATED LINKS</span></span>

[<span data-ttu-id="471da-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="471da-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="471da-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="471da-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="471da-148">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="471da-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="471da-149">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="471da-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="471da-150">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="471da-150">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="471da-151">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="471da-151">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


