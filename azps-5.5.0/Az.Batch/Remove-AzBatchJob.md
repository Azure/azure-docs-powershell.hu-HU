---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166770"
---
# <span data-ttu-id="95d3a-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="95d3a-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="95d3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="95d3a-103">Egy kötegfájl-feladatot töröl.</span><span class="sxs-lookup"><span data-stu-id="95d3a-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="95d3a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="95d3a-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d3a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="95d3a-105">DESCRIPTION</span></span>
<span data-ttu-id="95d3a-106">A **Remove-AzBatch Job** parancsmag töröl egy Azure Batch-feladatot.</span><span class="sxs-lookup"><span data-stu-id="95d3a-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="95d3a-107">Ez a parancsmag megerősítést kér a feladat eltávolítása előtt, hacsak meg nem adja a *Force paramétert.*</span><span class="sxs-lookup"><span data-stu-id="95d3a-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="95d3a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="95d3a-108">EXAMPLES</span></span>

### <span data-ttu-id="95d3a-109">1. példa: Kötegelt feladat törlése</span><span class="sxs-lookup"><span data-stu-id="95d3a-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="95d3a-110">Ez a parancs törli a 000001 azonosítójú feladatot.</span><span class="sxs-lookup"><span data-stu-id="95d3a-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="95d3a-111">A parancs megerősítést kér a feladat törlése előtt.</span><span class="sxs-lookup"><span data-stu-id="95d3a-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="95d3a-112">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="95d3a-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="95d3a-113">2. példa: Köteg-feladat törlése jóváhagyás nélkül a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="95d3a-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="95d3a-114">Ez a parancs a 0000002 azonosítójú feladatot kapja meg a Get-AzBatchJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="95d3a-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="95d3a-115">A parancs a folyamat műveleti operátorával átadja a feladatot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="95d3a-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="95d3a-116">A parancs törli ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="95d3a-116">The command deletes that job.</span></span>
<span data-ttu-id="95d3a-117">Mivel a parancs tartalmazza az *Kényszerítés* paramétert, nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="95d3a-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="95d3a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95d3a-118">PARAMETERS</span></span>

### <span data-ttu-id="95d3a-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="95d3a-119">-BatchContext</span></span>
<span data-ttu-id="95d3a-120">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="95d3a-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="95d3a-121">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="95d3a-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="95d3a-122">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot, és töltse ki a hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="95d3a-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="95d3a-123">Megosztott kulcsú hitelesítés használata esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="95d3a-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="95d3a-124">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="95d3a-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="95d3a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d3a-125">-DefaultProfile</span></span>
<span data-ttu-id="95d3a-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95d3a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95d3a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="95d3a-127">-Force</span></span>
<span data-ttu-id="95d3a-128">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="95d3a-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95d3a-129">-Id</span><span class="sxs-lookup"><span data-stu-id="95d3a-129">-Id</span></span>
<span data-ttu-id="95d3a-130">A parancsmag által törölt feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="95d3a-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="95d3a-131">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="95d3a-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d3a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95d3a-132">-Confirm</span></span>
<span data-ttu-id="95d3a-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="95d3a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d3a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d3a-134">-WhatIf</span></span>
<span data-ttu-id="95d3a-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="95d3a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95d3a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95d3a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d3a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d3a-137">CommonParameters</span></span>
<span data-ttu-id="95d3a-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d3a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d3a-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95d3a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d3a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95d3a-140">INPUTS</span></span>

### <span data-ttu-id="95d3a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="95d3a-141">System.String</span></span>

### <span data-ttu-id="95d3a-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="95d3a-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="95d3a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95d3a-143">OUTPUTS</span></span>

### <span data-ttu-id="95d3a-144">System.Void</span><span class="sxs-lookup"><span data-stu-id="95d3a-144">System.Void</span></span>

## <span data-ttu-id="95d3a-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="95d3a-145">NOTES</span></span>

## <span data-ttu-id="95d3a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95d3a-146">RELATED LINKS</span></span>

[<span data-ttu-id="95d3a-147">Disable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="95d3a-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="95d3a-148">Enable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="95d3a-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="95d3a-149">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="95d3a-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="95d3a-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="95d3a-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="95d3a-151">New-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="95d3a-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="95d3a-152">Stop-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="95d3a-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="95d3a-153">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="95d3a-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
