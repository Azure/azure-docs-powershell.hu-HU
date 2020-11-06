---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: 5b8797cf2f6068098d1ca407f0f97283dd171af5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497891"
---
# <span data-ttu-id="23641-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="23641-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="23641-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23641-102">SYNOPSIS</span></span>
<span data-ttu-id="23641-103">Törli a tevékenység vagy a számítási csomópont csomópont-fájlját.</span><span class="sxs-lookup"><span data-stu-id="23641-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23641-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23641-104">SYNTAX</span></span>

### <span data-ttu-id="23641-105">Tevékenység</span><span class="sxs-lookup"><span data-stu-id="23641-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23641-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="23641-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23641-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="23641-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23641-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="23641-108">DESCRIPTION</span></span>
<span data-ttu-id="23641-109">A **Remove-AzureBatchNodeFile** parancsmag egy Azure kötegfájl-csomópontot töröl egy tevékenységhez vagy egy kiszámított csomóponthoz.</span><span class="sxs-lookup"><span data-stu-id="23641-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="23641-110">Példák</span><span class="sxs-lookup"><span data-stu-id="23641-110">EXAMPLES</span></span>

### <span data-ttu-id="23641-111">1. példa: assocated tartalmazó fájl törlése</span><span class="sxs-lookup"><span data-stu-id="23641-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="23641-112">Ez a parancs törli a wd\testFile.txt nevű csomópontot.</span><span class="sxs-lookup"><span data-stu-id="23641-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="23641-113">A fájl társítva van azzal a tevékenységgel, amelynek azonosító Task26 a Job Job-000001.</span><span class="sxs-lookup"><span data-stu-id="23641-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="23641-114">2. példa: fájl törlése egy számítási csomópontból</span><span class="sxs-lookup"><span data-stu-id="23641-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Name "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="23641-115">Ez a parancs törli a startup\testFile.txt nevű csomópontot az azonosító Pool07 tartalmazó készlet meghatározott számítási csomópontról.</span><span class="sxs-lookup"><span data-stu-id="23641-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="23641-116">3. példa: fájl eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="23641-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="23641-117">Ez a parancs a **Get-AzureBatchNodeFile** használatával kapja meg a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="23641-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="23641-118">A fájl társítva van azzal a tevékenységgel, amelynek azonosító Task26 a Job Job-000001.</span><span class="sxs-lookup"><span data-stu-id="23641-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="23641-119">A parancs a fájlt átadja az aktuális parancsmagnak a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="23641-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="23641-120">Az aktuális parancsmag eltávolítja a csomópontot tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="23641-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="23641-121">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="23641-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="23641-122">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23641-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="23641-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23641-123">PARAMETERS</span></span>

### <span data-ttu-id="23641-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="23641-124">-BatchContext</span></span>
<span data-ttu-id="23641-125">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="23641-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="23641-126">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="23641-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="23641-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="23641-127">-ComputeNodeId</span></span>
<span data-ttu-id="23641-128">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amely a parancsmag által törölt köteg csomópont-fájlt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="23641-128">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23641-129">-Force</span><span class="sxs-lookup"><span data-stu-id="23641-129">-Force</span></span>
<span data-ttu-id="23641-130">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="23641-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23641-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23641-131">-InputObject</span></span>
<span data-ttu-id="23641-132">Azt a **PSNodeFile** objektumot adja meg, amely a parancsmag által törölt csomópont-fájlt jelképezi.</span><span class="sxs-lookup"><span data-stu-id="23641-132">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="23641-133">Ha **PSNodeFile** szeretne beolvasni, használja az Get-AzureBatchNodeFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="23641-133">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23641-134">-JobId</span><span class="sxs-lookup"><span data-stu-id="23641-134">-JobId</span></span>
<span data-ttu-id="23641-135">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="23641-135">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23641-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23641-136">-Name</span></span>
<span data-ttu-id="23641-137">Annak a csomópontnak a nevét adja meg, amelyre a parancsmag törli.</span><span class="sxs-lookup"><span data-stu-id="23641-137">Specifies the name of the node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23641-138">-PoolId</span><span class="sxs-lookup"><span data-stu-id="23641-138">-PoolId</span></span>
<span data-ttu-id="23641-139">Annak a készletnek az AZONOSÍTÓját adja meg, amely azokat a számítási csomópontokat tartalmazza, amelyeknek a parancsmagja eltávolítja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="23641-139">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23641-140">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="23641-140">-Recursive</span></span>
<span data-ttu-id="23641-141">Azt jelzi, hogy ez a parancsmag törli a mappát és az összes almappát és fájlt a megadott elérési úttal.</span><span class="sxs-lookup"><span data-stu-id="23641-141">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="23641-142">Ez a parancsmag csak akkor érvényes, ha az elérési út egy mappa.</span><span class="sxs-lookup"><span data-stu-id="23641-142">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="23641-143">-TaskId</span><span class="sxs-lookup"><span data-stu-id="23641-143">-TaskId</span></span>
<span data-ttu-id="23641-144">A tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="23641-144">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23641-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="23641-145">-Confirm</span></span>
<span data-ttu-id="23641-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23641-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23641-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23641-147">-WhatIf</span></span>
<span data-ttu-id="23641-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="23641-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23641-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23641-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23641-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23641-150">-DefaultProfile</span></span>
<span data-ttu-id="23641-151">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23641-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23641-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23641-152">CommonParameters</span></span>
<span data-ttu-id="23641-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23641-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23641-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23641-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23641-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23641-155">INPUTS</span></span>

### <span data-ttu-id="23641-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="23641-156">BatchAccountContext</span></span>
<span data-ttu-id="23641-157">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="23641-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="23641-158">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="23641-158">PSNodeFile</span></span>
<span data-ttu-id="23641-159">A ' InputObject ' paraméter az "PSNodeFile" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="23641-159">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="23641-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23641-160">OUTPUTS</span></span>

## <span data-ttu-id="23641-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23641-161">NOTES</span></span>

## <span data-ttu-id="23641-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23641-162">RELATED LINKS</span></span>

[<span data-ttu-id="23641-163">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="23641-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="23641-164">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="23641-164">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="23641-165">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="23641-165">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


