---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 6200ee0d929aaadccb8e2be0e8fb646929907d73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501932"
---
# <span data-ttu-id="dc46b-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="dc46b-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="dc46b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc46b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc46b-103">Töröl egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="dc46b-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc46b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc46b-104">SYNTAX</span></span>

### <span data-ttu-id="dc46b-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="dc46b-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc46b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="dc46b-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc46b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc46b-107">DESCRIPTION</span></span>
<span data-ttu-id="dc46b-108">A **Remove-AzureBatchTask** parancsmag egy Azure-köteg-feladatot töröl.</span><span class="sxs-lookup"><span data-stu-id="dc46b-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="dc46b-109">Ez a parancsmag csak akkor kér megerősítést, ha az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc46b-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="dc46b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dc46b-110">EXAMPLES</span></span>

### <span data-ttu-id="dc46b-111">1. példa: egy köteg tevékenységének törlése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="dc46b-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="dc46b-112">Ez a parancs törli azt a feladatot, amely a Task23 AZONOSÍTÓval rendelkezik a 000001 azonosítójú projektben.</span><span class="sxs-lookup"><span data-stu-id="dc46b-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="dc46b-113">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="dc46b-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="dc46b-114">A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="dc46b-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="dc46b-115">2. példa: a kötegelt feladat törlése megerősítés nélküli csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="dc46b-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="dc46b-116">Ez a parancs azt a kötegelt feladatot kapja meg, amely a Task26 azonosítójú projekt azonosítóját tartalmazza a **Get-AzureBatchTask** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="dc46b-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="dc46b-117">A parancs a tevékenységet a pipeline operátorral továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dc46b-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dc46b-118">A parancs törli a feladatot.</span><span class="sxs-lookup"><span data-stu-id="dc46b-118">The command deletes that task.</span></span>
<span data-ttu-id="dc46b-119">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc46b-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="dc46b-120">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc46b-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="dc46b-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc46b-121">PARAMETERS</span></span>

### <span data-ttu-id="dc46b-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dc46b-122">-BatchContext</span></span>
<span data-ttu-id="dc46b-123">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="dc46b-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dc46b-124">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dc46b-124">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="dc46b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="dc46b-125">-Force</span></span>
<span data-ttu-id="dc46b-126">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="dc46b-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc46b-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="dc46b-127">-Id</span></span>
<span data-ttu-id="dc46b-128">A parancsmag által törölt tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc46b-128">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="dc46b-129">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="dc46b-129">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="dc46b-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc46b-130">-InputObject</span></span>
<span data-ttu-id="dc46b-131">A parancsmag által törölt feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc46b-131">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="dc46b-132">**PSCloudTask** objektum beolvasásához használja az Get-AzureBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dc46b-132">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="dc46b-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="dc46b-133">-JobId</span></span>
<span data-ttu-id="dc46b-134">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc46b-134">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="dc46b-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dc46b-135">-Confirm</span></span>
<span data-ttu-id="dc46b-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc46b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc46b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc46b-137">-WhatIf</span></span>
<span data-ttu-id="dc46b-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dc46b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc46b-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc46b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc46b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc46b-140">-DefaultProfile</span></span>
<span data-ttu-id="dc46b-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc46b-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc46b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc46b-142">CommonParameters</span></span>
<span data-ttu-id="dc46b-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc46b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc46b-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc46b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc46b-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc46b-145">INPUTS</span></span>

### <span data-ttu-id="dc46b-146">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dc46b-146">BatchAccountContext</span></span>
<span data-ttu-id="dc46b-147">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dc46b-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="dc46b-148">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="dc46b-148">PSCloudTask</span></span>
<span data-ttu-id="dc46b-149">A ' InputObject ' paraméter az "PSCloudTask" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dc46b-149">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="dc46b-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc46b-150">OUTPUTS</span></span>

## <span data-ttu-id="dc46b-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc46b-151">NOTES</span></span>

## <span data-ttu-id="dc46b-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc46b-152">RELATED LINKS</span></span>

[<span data-ttu-id="dc46b-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dc46b-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="dc46b-154">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="dc46b-154">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="dc46b-155">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="dc46b-155">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="dc46b-156">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="dc46b-156">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="dc46b-157">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="dc46b-157">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="dc46b-158">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dc46b-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


