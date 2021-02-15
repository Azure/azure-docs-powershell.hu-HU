---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 9979a0fa16b8cfbe59eb8412a76cbbebcb2fca4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166779"
---
# <span data-ttu-id="812b6-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="812b6-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="812b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="812b6-102">SYNOPSIS</span></span>
<span data-ttu-id="812b6-103">Tevékenység újraaktiválása.</span><span class="sxs-lookup"><span data-stu-id="812b6-103">Reactivates a task.</span></span>

## <span data-ttu-id="812b6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="812b6-104">SYNTAX</span></span>

### <span data-ttu-id="812b6-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="812b6-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="812b6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="812b6-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="812b6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="812b6-107">DESCRIPTION</span></span>
<span data-ttu-id="812b6-108">Az **Enable-AzBatchTask** parancsmag újraaktivál egy feladatot.</span><span class="sxs-lookup"><span data-stu-id="812b6-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="812b6-109">Ha egy feladat elhasználta az újrapróbálkozási számát, ez a parancsmag ennek ellenére lehetővé teszi a futtatását.</span><span class="sxs-lookup"><span data-stu-id="812b6-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="812b6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="812b6-110">EXAMPLES</span></span>

### <span data-ttu-id="812b6-111">1. példa: Tevékenység újraaktiválása</span><span class="sxs-lookup"><span data-stu-id="812b6-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="812b6-112">Ez a parancs újraaktiválja a Feladat2 feladatot a Job7 feladatban.</span><span class="sxs-lookup"><span data-stu-id="812b6-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="812b6-113">2. példa: Tevékenység újraaktiválása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="812b6-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="812b6-114">Ez a parancs a 8-as azonosítójú feladathoz az azonosító feladat3 azonosítóját használó kötegfeladatot kapja meg a Get-AzBatchTask parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="812b6-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="812b6-115">A parancs a folyamat műveleti operátorával átadja a feladatot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="812b6-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="812b6-116">A parancs újraaktiválja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="812b6-116">The command reactivates that task.</span></span>

## <span data-ttu-id="812b6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="812b6-117">PARAMETERS</span></span>

### <span data-ttu-id="812b6-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="812b6-118">-BatchContext</span></span>
<span data-ttu-id="812b6-119">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="812b6-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="812b6-120">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="812b6-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="812b6-121">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="812b6-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="812b6-122">Megosztott kulcsú hitelesítés használata esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="812b6-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="812b6-123">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="812b6-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="812b6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="812b6-124">-DefaultProfile</span></span>
<span data-ttu-id="812b6-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="812b6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="812b6-126">-Id</span><span class="sxs-lookup"><span data-stu-id="812b6-126">-Id</span></span>
<span data-ttu-id="812b6-127">Az újraaktiválható tevékenység azonosítója.</span><span class="sxs-lookup"><span data-stu-id="812b6-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="812b6-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="812b6-128">-JobId</span></span>
<span data-ttu-id="812b6-129">A tevékenységet tartalmazó feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="812b6-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="812b6-130">-Task</span><span class="sxs-lookup"><span data-stu-id="812b6-130">-Task</span></span>
<span data-ttu-id="812b6-131">A parancsmag újraaktiválható feladata.</span><span class="sxs-lookup"><span data-stu-id="812b6-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="812b6-132">**PSCloudTask-objektum** beszerzéséhez használja a Get-AzBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="812b6-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="812b6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="812b6-133">-Confirm</span></span>
<span data-ttu-id="812b6-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="812b6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="812b6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="812b6-135">-WhatIf</span></span>
<span data-ttu-id="812b6-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="812b6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="812b6-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="812b6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="812b6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="812b6-138">CommonParameters</span></span>
<span data-ttu-id="812b6-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="812b6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="812b6-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="812b6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="812b6-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="812b6-141">INPUTS</span></span>

### <span data-ttu-id="812b6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="812b6-142">System.String</span></span>

### <span data-ttu-id="812b6-143">Microsoft.Azure.Commands.Bat. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="812b6-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="812b6-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="812b6-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="812b6-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="812b6-145">OUTPUTS</span></span>

### <span data-ttu-id="812b6-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="812b6-146">System.Void</span></span>

## <span data-ttu-id="812b6-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="812b6-147">NOTES</span></span>

## <span data-ttu-id="812b6-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="812b6-148">RELATED LINKS</span></span>

[<span data-ttu-id="812b6-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="812b6-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="812b6-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="812b6-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="812b6-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="812b6-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="812b6-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="812b6-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="812b6-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="812b6-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="812b6-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="812b6-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


