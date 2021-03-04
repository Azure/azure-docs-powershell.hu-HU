---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 902c7ab5f6125716e03e846a4f1ebc3925aae43f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937162"
---
# <span data-ttu-id="3c86e-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3c86e-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="3c86e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c86e-102">SYNOPSIS</span></span>
<span data-ttu-id="3c86e-103">Tevékenység újraaktiválása.</span><span class="sxs-lookup"><span data-stu-id="3c86e-103">Reactivates a task.</span></span>

## <span data-ttu-id="3c86e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3c86e-104">SYNTAX</span></span>

### <span data-ttu-id="3c86e-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="3c86e-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c86e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3c86e-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c86e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3c86e-107">DESCRIPTION</span></span>
<span data-ttu-id="3c86e-108">Az **Enable-AzBatchTask** parancsmag újraaktivál egy feladatot.</span><span class="sxs-lookup"><span data-stu-id="3c86e-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="3c86e-109">Ha egy feladat elhasználta az újrapróbálkozási számát, ez a parancsmag ennek ellenére lehetővé teszi a futtatását.</span><span class="sxs-lookup"><span data-stu-id="3c86e-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="3c86e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3c86e-110">EXAMPLES</span></span>

### <span data-ttu-id="3c86e-111">1. példa: Tevékenység újraaktiválása</span><span class="sxs-lookup"><span data-stu-id="3c86e-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="3c86e-112">Ez a parancs újraaktiválja a Feladat2 feladatot a Job7 feladatban.</span><span class="sxs-lookup"><span data-stu-id="3c86e-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="3c86e-113">2. példa: Tevékenység újraaktiválása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="3c86e-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="3c86e-114">Ez a parancs a 8-as azonosítójú feladathoz az azonosító feladat3 azonosítóját használó kötegfeladatot kapja meg a Get-AzBatchTask parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="3c86e-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="3c86e-115">A parancs a folyamat műveleti operátorával átadja a feladatot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="3c86e-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3c86e-116">A parancs újraaktiválja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="3c86e-116">The command reactivates that task.</span></span>

## <span data-ttu-id="3c86e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c86e-117">PARAMETERS</span></span>

### <span data-ttu-id="3c86e-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3c86e-118">-BatchContext</span></span>
<span data-ttu-id="3c86e-119">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="3c86e-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3c86e-120">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="3c86e-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3c86e-121">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="3c86e-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3c86e-122">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="3c86e-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3c86e-123">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="3c86e-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3c86e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c86e-124">-DefaultProfile</span></span>
<span data-ttu-id="3c86e-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c86e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c86e-126">-Id</span><span class="sxs-lookup"><span data-stu-id="3c86e-126">-Id</span></span>
<span data-ttu-id="3c86e-127">Az újraaktiválható tevékenység azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3c86e-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="3c86e-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="3c86e-128">-JobId</span></span>
<span data-ttu-id="3c86e-129">A tevékenységet tartalmazó feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3c86e-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="3c86e-130">-Task</span><span class="sxs-lookup"><span data-stu-id="3c86e-130">-Task</span></span>
<span data-ttu-id="3c86e-131">A parancsmag újraaktiválható feladata.</span><span class="sxs-lookup"><span data-stu-id="3c86e-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="3c86e-132">**PSCloudTask-objektum** beszerzéséhez használja a Get-AzBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3c86e-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="3c86e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c86e-133">-Confirm</span></span>
<span data-ttu-id="3c86e-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3c86e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c86e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c86e-135">-WhatIf</span></span>
<span data-ttu-id="3c86e-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3c86e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c86e-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c86e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c86e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c86e-138">CommonParameters</span></span>
<span data-ttu-id="3c86e-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c86e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c86e-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c86e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c86e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c86e-141">INPUTS</span></span>

### <span data-ttu-id="3c86e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3c86e-142">System.String</span></span>

### <span data-ttu-id="3c86e-143">Microsoft.Azure.Commands.Bat. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="3c86e-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="3c86e-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3c86e-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3c86e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c86e-145">OUTPUTS</span></span>

### <span data-ttu-id="3c86e-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="3c86e-146">System.Void</span></span>

## <span data-ttu-id="3c86e-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3c86e-147">NOTES</span></span>

## <span data-ttu-id="3c86e-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c86e-148">RELATED LINKS</span></span>

[<span data-ttu-id="3c86e-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3c86e-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3c86e-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3c86e-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="3c86e-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3c86e-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="3c86e-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3c86e-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="3c86e-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3c86e-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="3c86e-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3c86e-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


