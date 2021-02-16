---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: e067eea86e3a4350d08c5c0f9ec34b4af65b07f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168219"
---
# <span data-ttu-id="18cb0-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="18cb0-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="18cb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="18cb0-103">Egy kötegfeladat törlése.</span><span class="sxs-lookup"><span data-stu-id="18cb0-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="18cb0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18cb0-104">SYNTAX</span></span>

### <span data-ttu-id="18cb0-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="18cb0-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18cb0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="18cb0-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18cb0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18cb0-107">DESCRIPTION</span></span>
<span data-ttu-id="18cb0-108">A **Remove-AzBatchTask** parancsmag töröl egy Azure Batch-feladatot.</span><span class="sxs-lookup"><span data-stu-id="18cb0-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="18cb0-109">Ez a parancsmag megerősítést kér, hacsak nem adja meg a *Force paramétert.*</span><span class="sxs-lookup"><span data-stu-id="18cb0-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="18cb0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18cb0-110">EXAMPLES</span></span>

### <span data-ttu-id="18cb0-111">1. példa: Batch-feladat törlése azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="18cb0-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="18cb0-112">Ez a parancs törli a 000001 azonosítójú feladat alatt az Azonosító Tevékenység23 azonosítót.</span><span class="sxs-lookup"><span data-stu-id="18cb0-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="18cb0-113">A parancs megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="18cb0-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="18cb0-114">A **Get-AzBatchAccountKey** parancsmaggal kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="18cb0-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="18cb0-115">2. példa: Kötegfeladat törlése a folyamat használatával megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="18cb0-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="18cb0-116">Ez a parancs a **Get-AzBatchTask** parancsmagot használva kapja meg azt a kötegtevékenységet, amely a 000001-es azonosítófeladatot használó feladatban az Azonosító feladat26 feladatot használja.</span><span class="sxs-lookup"><span data-stu-id="18cb0-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="18cb0-117">A parancs a folyamat műveleti operátorával átadja a feladatot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="18cb0-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="18cb0-118">A parancs törli ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="18cb0-118">The command deletes that task.</span></span>
<span data-ttu-id="18cb0-119">Ez a parancs a *Force paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="18cb0-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="18cb0-120">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="18cb0-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="18cb0-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18cb0-121">PARAMETERS</span></span>

### <span data-ttu-id="18cb0-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="18cb0-122">-BatchContext</span></span>
<span data-ttu-id="18cb0-123">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="18cb0-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="18cb0-124">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="18cb0-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="18cb0-125">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot, és töltse ki a hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="18cb0-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="18cb0-126">Megosztott kulcsú hitelesítés használata esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="18cb0-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="18cb0-127">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="18cb0-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="18cb0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cb0-128">-DefaultProfile</span></span>
<span data-ttu-id="18cb0-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18cb0-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18cb0-130">-Force</span><span class="sxs-lookup"><span data-stu-id="18cb0-130">-Force</span></span>
<span data-ttu-id="18cb0-131">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="18cb0-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18cb0-132">-Id</span><span class="sxs-lookup"><span data-stu-id="18cb0-132">-Id</span></span>
<span data-ttu-id="18cb0-133">A parancsmag által törölt feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="18cb0-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="18cb0-134">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="18cb0-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="18cb0-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18cb0-135">-InputObject</span></span>
<span data-ttu-id="18cb0-136">A parancsmag által törölt feladat.</span><span class="sxs-lookup"><span data-stu-id="18cb0-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="18cb0-137">**PSCloudTask-objektum** beszerzéséhez használja a Get-AzBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="18cb0-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="18cb0-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="18cb0-138">-JobId</span></span>
<span data-ttu-id="18cb0-139">A tevékenységet tartalmazó feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="18cb0-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="18cb0-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18cb0-140">-Confirm</span></span>
<span data-ttu-id="18cb0-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="18cb0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18cb0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18cb0-142">-WhatIf</span></span>
<span data-ttu-id="18cb0-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="18cb0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18cb0-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18cb0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18cb0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cb0-145">CommonParameters</span></span>
<span data-ttu-id="18cb0-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18cb0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cb0-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18cb0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cb0-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18cb0-148">INPUTS</span></span>

### <span data-ttu-id="18cb0-149">System.String</span><span class="sxs-lookup"><span data-stu-id="18cb0-149">System.String</span></span>

### <span data-ttu-id="18cb0-150">Microsoft.Azure.Commands.Bat. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="18cb0-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="18cb0-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="18cb0-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="18cb0-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18cb0-152">OUTPUTS</span></span>

### <span data-ttu-id="18cb0-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="18cb0-153">System.Void</span></span>

## <span data-ttu-id="18cb0-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18cb0-154">NOTES</span></span>

## <span data-ttu-id="18cb0-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18cb0-155">RELATED LINKS</span></span>

[<span data-ttu-id="18cb0-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="18cb0-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="18cb0-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="18cb0-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="18cb0-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="18cb0-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="18cb0-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="18cb0-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="18cb0-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="18cb0-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="18cb0-161">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="18cb0-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
