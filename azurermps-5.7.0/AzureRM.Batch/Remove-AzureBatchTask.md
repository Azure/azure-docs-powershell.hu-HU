---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 775425b0da46ef6c2b22e1c28725b323b3071974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503075"
---
# <span data-ttu-id="5a1e6-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5a1e6-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="5a1e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a1e6-102">SYNOPSIS</span></span>
<span data-ttu-id="5a1e6-103">Töröl egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a1e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a1e6-104">SYNTAX</span></span>

### <span data-ttu-id="5a1e6-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="5a1e6-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a1e6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5a1e6-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a1e6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a1e6-107">DESCRIPTION</span></span>
<span data-ttu-id="5a1e6-108">A **Remove-AzureBatchTask** parancsmag egy Azure-köteg-feladatot töröl.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="5a1e6-109">Ez a parancsmag csak akkor kér megerősítést, ha az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="5a1e6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5a1e6-110">EXAMPLES</span></span>

### <span data-ttu-id="5a1e6-111">1. példa: egy köteg tevékenységének törlése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="5a1e6-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="5a1e6-112">Ez a parancs törli azt a feladatot, amely a Task23 AZONOSÍTÓval rendelkezik a 000001 azonosítójú projektben.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="5a1e6-113">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="5a1e6-114">A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5a1e6-115">2. példa: a kötegelt feladat törlése megerősítés nélküli csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="5a1e6-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="5a1e6-116">Ez a parancs azt a kötegelt feladatot kapja meg, amely a Task26 azonosítójú projekt azonosítóját tartalmazza a **Get-AzureBatchTask** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="5a1e6-117">A parancs a tevékenységet a pipeline operátorral továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5a1e6-118">A parancs törli a feladatot.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-118">The command deletes that task.</span></span>
<span data-ttu-id="5a1e6-119">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="5a1e6-120">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5a1e6-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a1e6-121">PARAMETERS</span></span>

### <span data-ttu-id="5a1e6-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5a1e6-122">-BatchContext</span></span>
<span data-ttu-id="5a1e6-123">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5a1e6-124">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5a1e6-125">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5a1e6-126">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5a1e6-127">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5a1e6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a1e6-128">-DefaultProfile</span></span>
<span data-ttu-id="5a1e6-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a1e6-130">-Force</span><span class="sxs-lookup"><span data-stu-id="5a1e6-130">-Force</span></span>
<span data-ttu-id="5a1e6-131">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e6-132">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5a1e6-132">-Id</span></span>
<span data-ttu-id="5a1e6-133">A parancsmag által törölt tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="5a1e6-134">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="5a1e6-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a1e6-135">-InputObject</span></span>
<span data-ttu-id="5a1e6-136">A parancsmag által törölt feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="5a1e6-137">**PSCloudTask** objektum beolvasásához használja az Get-AzureBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="5a1e6-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="5a1e6-138">-JobId</span></span>
<span data-ttu-id="5a1e6-139">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="5a1e6-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5a1e6-140">-Confirm</span></span>
<span data-ttu-id="5a1e6-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a1e6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a1e6-142">-WhatIf</span></span>
<span data-ttu-id="5a1e6-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a1e6-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a1e6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a1e6-145">CommonParameters</span></span>
<span data-ttu-id="5a1e6-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a1e6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a1e6-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a1e6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a1e6-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a1e6-148">INPUTS</span></span>

### <span data-ttu-id="5a1e6-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5a1e6-149">BatchAccountContext</span></span>
<span data-ttu-id="5a1e6-150">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5a1e6-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5a1e6-151">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="5a1e6-151">PSCloudTask</span></span>
<span data-ttu-id="5a1e6-152">A ' InputObject ' paraméter az "PSCloudTask" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5a1e6-152">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="5a1e6-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a1e6-153">OUTPUTS</span></span>

## <span data-ttu-id="5a1e6-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a1e6-154">NOTES</span></span>

## <span data-ttu-id="5a1e6-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a1e6-155">RELATED LINKS</span></span>

[<span data-ttu-id="5a1e6-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5a1e6-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5a1e6-157">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5a1e6-157">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="5a1e6-158">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5a1e6-158">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="5a1e6-159">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5a1e6-159">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="5a1e6-160">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5a1e6-160">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="5a1e6-161">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5a1e6-161">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


