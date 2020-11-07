---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 09e2c8dd4ce1eab68eb2a4237e022034696f9769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679746"
---
# <span data-ttu-id="27d0c-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="27d0c-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="27d0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="27d0c-103">Tevékenység újraaktiválása</span><span class="sxs-lookup"><span data-stu-id="27d0c-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27d0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27d0c-104">SYNTAX</span></span>

### <span data-ttu-id="27d0c-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="27d0c-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27d0c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="27d0c-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27d0c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="27d0c-107">DESCRIPTION</span></span>
<span data-ttu-id="27d0c-108">Az **enable-AzureBatchTask** parancsmag újraaktiválja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="27d0c-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="27d0c-109">Ha egy tevékenység kimerítette az újrapróbálkozások számát, ez a parancsmag mégis lehetővé teszi a futtatását.</span><span class="sxs-lookup"><span data-stu-id="27d0c-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="27d0c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="27d0c-110">EXAMPLES</span></span>

### <span data-ttu-id="27d0c-111">1. példa: tevékenység újraaktiválása</span><span class="sxs-lookup"><span data-stu-id="27d0c-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="27d0c-112">Ez a parancs újra aktiválja a tevékenység Task2 a munkahelyi Job7.</span><span class="sxs-lookup"><span data-stu-id="27d0c-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="27d0c-113">2. példa: tevékenység újraaktiválása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="27d0c-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="27d0c-114">Ez a parancs azt a kötegelt feladatot kapja meg, amely a Task3 azonosítóval rendelkezik, és az Get-AzureBatchTask parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="27d0c-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="27d0c-115">A parancs a tevékenységet a pipeline operátorral továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="27d0c-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="27d0c-116">A parancs újra aktiválja ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="27d0c-116">The command reactivates that task.</span></span>

## <span data-ttu-id="27d0c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27d0c-117">PARAMETERS</span></span>

### <span data-ttu-id="27d0c-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="27d0c-118">-BatchContext</span></span>
<span data-ttu-id="27d0c-119">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="27d0c-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="27d0c-120">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="27d0c-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="27d0c-121">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="27d0c-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="27d0c-122">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="27d0c-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="27d0c-123">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="27d0c-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27d0c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d0c-124">-DefaultProfile</span></span>
<span data-ttu-id="27d0c-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27d0c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d0c-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="27d0c-126">-Id</span></span>
<span data-ttu-id="27d0c-127">Az újraaktiválni kívánt tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="27d0c-127">Specifies the ID of the task to reactivate.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27d0c-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="27d0c-128">-JobId</span></span>
<span data-ttu-id="27d0c-129">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="27d0c-129">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27d0c-130">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="27d0c-130">-Task</span></span>
<span data-ttu-id="27d0c-131">A parancsmag által újraaktivált feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="27d0c-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="27d0c-132">**PSCloudTask** objektum beolvasásához használja az Get-AzureBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="27d0c-132">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27d0c-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27d0c-133">-Confirm</span></span>
<span data-ttu-id="27d0c-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27d0c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d0c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27d0c-135">-WhatIf</span></span>
<span data-ttu-id="27d0c-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27d0c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27d0c-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27d0c-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d0c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d0c-138">CommonParameters</span></span>
<span data-ttu-id="27d0c-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27d0c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d0c-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27d0c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d0c-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27d0c-141">INPUTS</span></span>

### <span data-ttu-id="27d0c-142">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="27d0c-142">BatchAccountContext</span></span>
<span data-ttu-id="27d0c-143">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="27d0c-143">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="27d0c-144">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="27d0c-144">PSCloudTask</span></span>
<span data-ttu-id="27d0c-145">A "tevékenység" paraméter elfogadja a "PSCloudTask" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="27d0c-145">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="27d0c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27d0c-146">OUTPUTS</span></span>

## <span data-ttu-id="27d0c-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27d0c-147">NOTES</span></span>

## <span data-ttu-id="27d0c-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27d0c-148">RELATED LINKS</span></span>

[<span data-ttu-id="27d0c-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="27d0c-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="27d0c-150">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="27d0c-150">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="27d0c-151">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="27d0c-151">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="27d0c-152">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="27d0c-152">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="27d0c-153">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="27d0c-153">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="27d0c-154">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="27d0c-154">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


