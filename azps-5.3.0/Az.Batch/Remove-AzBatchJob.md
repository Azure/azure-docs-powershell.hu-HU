---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478226"
---
# <span data-ttu-id="f4210-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4210-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="f4210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4210-102">SYNOPSIS</span></span>
<span data-ttu-id="f4210-103">Egy kötegfájl-feladatot töröl.</span><span class="sxs-lookup"><span data-stu-id="f4210-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="f4210-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f4210-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4210-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f4210-105">DESCRIPTION</span></span>
<span data-ttu-id="f4210-106">A **Remove-AzBatch Job** parancsmag töröl egy Azure Batch-feladatot.</span><span class="sxs-lookup"><span data-stu-id="f4210-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="f4210-107">Ez a parancsmag megerősítést kér a feladat eltávolítása előtt, hacsak nem adja meg a *Force paramétert.*</span><span class="sxs-lookup"><span data-stu-id="f4210-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="f4210-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f4210-108">EXAMPLES</span></span>

### <span data-ttu-id="f4210-109">1. példa: Kötegelt feladat törlése</span><span class="sxs-lookup"><span data-stu-id="f4210-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="f4210-110">Ez a parancs törli a 000001 azonosítójú feladatot.</span><span class="sxs-lookup"><span data-stu-id="f4210-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="f4210-111">A parancs megerősítést kér a feladat törlése előtt.</span><span class="sxs-lookup"><span data-stu-id="f4210-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="f4210-112">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="f4210-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f4210-113">2. példa: Köteg-feladat törlése jóváhagyás nélkül a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="f4210-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="f4210-114">Ez a parancs a 0000002 azonosítójú feladatot kapja meg a Get-AzBatchJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f4210-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="f4210-115">A parancs a folyamat műveleti operátorával átadja a feladatot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="f4210-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f4210-116">A parancs törli ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="f4210-116">The command deletes that job.</span></span>
<span data-ttu-id="f4210-117">Mivel a parancs tartalmazza az *Kényszerítés* paramétert, nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4210-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f4210-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4210-118">PARAMETERS</span></span>

### <span data-ttu-id="f4210-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f4210-119">-BatchContext</span></span>
<span data-ttu-id="f4210-120">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="f4210-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f4210-121">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="f4210-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f4210-122">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="f4210-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f4210-123">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="f4210-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f4210-124">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="f4210-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f4210-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4210-125">-DefaultProfile</span></span>
<span data-ttu-id="f4210-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4210-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4210-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f4210-127">-Force</span></span>
<span data-ttu-id="f4210-128">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f4210-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4210-129">-Id</span><span class="sxs-lookup"><span data-stu-id="f4210-129">-Id</span></span>
<span data-ttu-id="f4210-130">A parancsmag által törölt feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f4210-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="f4210-131">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="f4210-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="f4210-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4210-132">-Confirm</span></span>
<span data-ttu-id="f4210-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f4210-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4210-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4210-134">-WhatIf</span></span>
<span data-ttu-id="f4210-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f4210-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4210-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4210-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4210-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4210-137">CommonParameters</span></span>
<span data-ttu-id="f4210-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4210-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4210-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4210-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4210-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4210-140">INPUTS</span></span>

### <span data-ttu-id="f4210-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f4210-141">System.String</span></span>

### <span data-ttu-id="f4210-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f4210-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f4210-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4210-143">OUTPUTS</span></span>

### <span data-ttu-id="f4210-144">System.Void</span><span class="sxs-lookup"><span data-stu-id="f4210-144">System.Void</span></span>

## <span data-ttu-id="f4210-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f4210-145">NOTES</span></span>

## <span data-ttu-id="f4210-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4210-146">RELATED LINKS</span></span>

[<span data-ttu-id="f4210-147">Disable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="f4210-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="f4210-148">Enable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="f4210-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="f4210-149">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="f4210-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="f4210-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f4210-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f4210-151">New-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="f4210-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="f4210-152">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4210-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="f4210-153">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f4210-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
