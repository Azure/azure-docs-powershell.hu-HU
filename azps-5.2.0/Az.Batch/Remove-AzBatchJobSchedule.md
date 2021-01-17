---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323760"
---
# <span data-ttu-id="2ae4e-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2ae4e-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="2ae4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ae4e-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae4e-103">Eltávolítja a köteg feladatütemtervét.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="2ae4e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2ae4e-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ae4e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2ae4e-105">DESCRIPTION</span></span>
<span data-ttu-id="2ae4e-106">A **Remove-AzBatch JobSchedule** parancsmag eltávolít egy Azure Batch-feladatütemtervet.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="2ae4e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2ae4e-107">EXAMPLES</span></span>

### <span data-ttu-id="2ae4e-108">1. példa: Kötegelt feladat ütemezésének törlése</span><span class="sxs-lookup"><span data-stu-id="2ae4e-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="2ae4e-109">Ez a parancs törli a MySchedule azonosítójú munkabeosztást.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="2ae4e-110">A parancs megerősítést kér a feladat törlése előtt.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="2ae4e-111">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2ae4e-112">2. példa: Köteg-feladat törlése jóváhagyás nélkül a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="2ae4e-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="2ae4e-113">Ez a parancs a my JobSchedule azonosítót használó munkabeosztást a Get-AzBatchJobSchedule parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="2ae4e-114">A parancs a folyamat műveleti operátorával átadja ezt a feladatütemtervet az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2ae4e-115">A parancs törli az ütemezést.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="2ae4e-116">Mivel a parancs tartalmazza az *Kényszerítés* paramétert, nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2ae4e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ae4e-117">PARAMETERS</span></span>

### <span data-ttu-id="2ae4e-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2ae4e-118">-BatchContext</span></span>
<span data-ttu-id="2ae4e-119">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2ae4e-120">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2ae4e-121">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2ae4e-122">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2ae4e-123">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2ae4e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ae4e-124">-DefaultProfile</span></span>
<span data-ttu-id="2ae4e-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ae4e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="2ae4e-126">-Force</span></span>
<span data-ttu-id="2ae4e-127">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2ae4e-128">-Id</span><span class="sxs-lookup"><span data-stu-id="2ae4e-128">-Id</span></span>
<span data-ttu-id="2ae4e-129">Az eltávolítható feladatütemterv azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="2ae4e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ae4e-130">-Confirm</span></span>
<span data-ttu-id="2ae4e-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ae4e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ae4e-132">-WhatIf</span></span>
<span data-ttu-id="2ae4e-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ae4e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ae4e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae4e-135">CommonParameters</span></span>
<span data-ttu-id="2ae4e-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ae4e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae4e-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ae4e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae4e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ae4e-138">INPUTS</span></span>

### <span data-ttu-id="2ae4e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2ae4e-139">System.String</span></span>

### <span data-ttu-id="2ae4e-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2ae4e-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2ae4e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ae4e-141">OUTPUTS</span></span>

### <span data-ttu-id="2ae4e-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="2ae4e-142">System.Void</span></span>

## <span data-ttu-id="2ae4e-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2ae4e-143">NOTES</span></span>

## <span data-ttu-id="2ae4e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ae4e-144">RELATED LINKS</span></span>

[<span data-ttu-id="2ae4e-145">Disable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2ae4e-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="2ae4e-146">Enable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2ae4e-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="2ae4e-147">Get-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2ae4e-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="2ae4e-148">New-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2ae4e-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="2ae4e-149">Set-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2ae4e-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="2ae4e-150">Stop-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2ae4e-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


