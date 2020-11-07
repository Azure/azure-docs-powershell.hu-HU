---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: c2b198359bbd793353c9b416a631d94cad0709fa
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671833"
---
# <span data-ttu-id="69174-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="69174-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="69174-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69174-102">SYNOPSIS</span></span>
<span data-ttu-id="69174-103">Töröl egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="69174-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="69174-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69174-104">SYNTAX</span></span>

### <span data-ttu-id="69174-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="69174-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69174-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="69174-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69174-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="69174-107">DESCRIPTION</span></span>
<span data-ttu-id="69174-108">A **Remove-AzBatchTask** parancsmag egy Azure-köteg-feladatot töröl.</span><span class="sxs-lookup"><span data-stu-id="69174-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="69174-109">Ez a parancsmag csak akkor kér megerősítést, ha az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="69174-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="69174-110">Példák</span><span class="sxs-lookup"><span data-stu-id="69174-110">EXAMPLES</span></span>

### <span data-ttu-id="69174-111">1. példa: egy köteg tevékenységének törlése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="69174-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="69174-112">Ez a parancs törli azt a feladatot, amely a Task23 AZONOSÍTÓval rendelkezik a 000001 azonosítójú projektben.</span><span class="sxs-lookup"><span data-stu-id="69174-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="69174-113">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="69174-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="69174-114">A **Get-AzBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="69174-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="69174-115">2. példa: a kötegelt feladat törlése megerősítés nélküli csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="69174-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="69174-116">Ez a parancs azt a kötegelt feladatot kapja meg, amely a Task26 azonosítójú projekt azonosítóját tartalmazza a **Get-AzBatchTask** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="69174-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="69174-117">A parancs a tevékenységet a pipeline operátorral továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="69174-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="69174-118">A parancs törli a feladatot.</span><span class="sxs-lookup"><span data-stu-id="69174-118">The command deletes that task.</span></span>
<span data-ttu-id="69174-119">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="69174-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="69174-120">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69174-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="69174-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69174-121">PARAMETERS</span></span>

### <span data-ttu-id="69174-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="69174-122">-BatchContext</span></span>
<span data-ttu-id="69174-123">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="69174-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="69174-124">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="69174-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="69174-125">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="69174-125">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="69174-126">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="69174-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="69174-127">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="69174-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="69174-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69174-128">-DefaultProfile</span></span>
<span data-ttu-id="69174-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69174-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69174-130">-Force</span><span class="sxs-lookup"><span data-stu-id="69174-130">-Force</span></span>
<span data-ttu-id="69174-131">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="69174-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="69174-132">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="69174-132">-Id</span></span>
<span data-ttu-id="69174-133">A parancsmag által törölt tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="69174-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="69174-134">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="69174-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="69174-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69174-135">-InputObject</span></span>
<span data-ttu-id="69174-136">A parancsmag által törölt feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="69174-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="69174-137">**PSCloudTask** objektum beolvasásához használja az Get-AzBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="69174-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="69174-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="69174-138">-JobId</span></span>
<span data-ttu-id="69174-139">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="69174-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="69174-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69174-140">-Confirm</span></span>
<span data-ttu-id="69174-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69174-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69174-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69174-142">-WhatIf</span></span>
<span data-ttu-id="69174-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69174-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69174-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69174-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69174-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69174-145">CommonParameters</span></span>
<span data-ttu-id="69174-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69174-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69174-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69174-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69174-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69174-148">INPUTS</span></span>

### <span data-ttu-id="69174-149">System. String</span><span class="sxs-lookup"><span data-stu-id="69174-149">System.String</span></span>

### <span data-ttu-id="69174-150">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="69174-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="69174-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="69174-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="69174-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69174-152">OUTPUTS</span></span>

### <span data-ttu-id="69174-153">System. Void</span><span class="sxs-lookup"><span data-stu-id="69174-153">System.Void</span></span>

## <span data-ttu-id="69174-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69174-154">NOTES</span></span>

## <span data-ttu-id="69174-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69174-155">RELATED LINKS</span></span>

[<span data-ttu-id="69174-156">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="69174-156">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="69174-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="69174-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="69174-158">Új – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="69174-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="69174-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="69174-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="69174-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="69174-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="69174-161">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="69174-161">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


