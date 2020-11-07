---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: a81d77ac1761c37dc3042394a4a70bda6848cc83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672487"
---
# <span data-ttu-id="75164-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="75164-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="75164-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75164-102">SYNOPSIS</span></span>
<span data-ttu-id="75164-103">Törli a tevékenység vagy a számítási csomópont csomópont-fájlját.</span><span class="sxs-lookup"><span data-stu-id="75164-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75164-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75164-104">SYNTAX</span></span>

### <span data-ttu-id="75164-105">Tevékenység</span><span class="sxs-lookup"><span data-stu-id="75164-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75164-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="75164-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75164-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="75164-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75164-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="75164-108">DESCRIPTION</span></span>
<span data-ttu-id="75164-109">A **Remove-AzureBatchNodeFile** parancsmag egy Azure kötegfájl-csomópontot töröl egy tevékenységhez vagy egy kiszámított csomóponthoz.</span><span class="sxs-lookup"><span data-stu-id="75164-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="75164-110">Példák</span><span class="sxs-lookup"><span data-stu-id="75164-110">EXAMPLES</span></span>

### <span data-ttu-id="75164-111">1. példa: assocated tartalmazó fájl törlése</span><span class="sxs-lookup"><span data-stu-id="75164-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="75164-112">Ez a parancs törli a wd\testFile.txt nevű csomópontot.</span><span class="sxs-lookup"><span data-stu-id="75164-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="75164-113">A fájl társítva van azzal a tevékenységgel, amelynek azonosító Task26 a Job Job-000001.</span><span class="sxs-lookup"><span data-stu-id="75164-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="75164-114">2. példa: fájl törlése egy számítási csomópontból</span><span class="sxs-lookup"><span data-stu-id="75164-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="75164-115">Ez a parancs törli a startup\testFile.txt nevű csomópontot az azonosító Pool07 tartalmazó készlet meghatározott számítási csomópontról.</span><span class="sxs-lookup"><span data-stu-id="75164-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="75164-116">3. példa: fájl eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="75164-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="75164-117">Ez a parancs a **Get-AzureBatchNodeFile** használatával kapja meg a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="75164-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="75164-118">A fájl társítva van azzal a tevékenységgel, amelynek azonosító Task26 a Job Job-000001.</span><span class="sxs-lookup"><span data-stu-id="75164-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="75164-119">A parancs a fájlt átadja az aktuális parancsmagnak a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="75164-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="75164-120">Az aktuális parancsmag eltávolítja a csomópontot tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="75164-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="75164-121">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="75164-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="75164-122">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="75164-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="75164-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75164-123">PARAMETERS</span></span>

### <span data-ttu-id="75164-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="75164-124">-BatchContext</span></span>
<span data-ttu-id="75164-125">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="75164-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="75164-126">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="75164-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="75164-127">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="75164-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="75164-128">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="75164-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="75164-129">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="75164-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="75164-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="75164-130">-ComputeNodeId</span></span>
<span data-ttu-id="75164-131">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amely a parancsmag által törölt köteg csomópont-fájlt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="75164-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="75164-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75164-132">-DefaultProfile</span></span>
<span data-ttu-id="75164-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75164-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75164-134">-Force</span><span class="sxs-lookup"><span data-stu-id="75164-134">-Force</span></span>
<span data-ttu-id="75164-135">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="75164-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75164-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75164-136">-InputObject</span></span>
<span data-ttu-id="75164-137">Azt a **PSNodeFile** objektumot adja meg, amely a parancsmag által törölt csomópont-fájlt jelképezi.</span><span class="sxs-lookup"><span data-stu-id="75164-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="75164-138">Ha **PSNodeFile** szeretne beolvasni, használja az Get-AzureBatchNodeFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="75164-138">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="75164-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="75164-139">-JobId</span></span>
<span data-ttu-id="75164-140">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="75164-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="75164-141">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="75164-141">-Path</span></span>
<span data-ttu-id="75164-142">A törlendő csomópont fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="75164-142">The file path of the node file to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75164-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="75164-143">-PoolId</span></span>
<span data-ttu-id="75164-144">Annak a készletnek az AZONOSÍTÓját adja meg, amely azokat a számítási csomópontokat tartalmazza, amelyeknek a parancsmagja eltávolítja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="75164-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="75164-145">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="75164-145">-Recursive</span></span>
<span data-ttu-id="75164-146">Azt jelzi, hogy ez a parancsmag törli a mappát és az összes almappát és fájlt a megadott elérési úttal.</span><span class="sxs-lookup"><span data-stu-id="75164-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="75164-147">Ez a parancsmag csak akkor érvényes, ha az elérési út egy mappa.</span><span class="sxs-lookup"><span data-stu-id="75164-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="75164-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="75164-148">-TaskId</span></span>
<span data-ttu-id="75164-149">A tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="75164-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="75164-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="75164-150">-Confirm</span></span>
<span data-ttu-id="75164-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="75164-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75164-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75164-152">-WhatIf</span></span>
<span data-ttu-id="75164-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="75164-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75164-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75164-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75164-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75164-155">CommonParameters</span></span>
<span data-ttu-id="75164-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75164-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75164-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75164-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75164-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75164-158">INPUTS</span></span>

### <span data-ttu-id="75164-159">System. String</span><span class="sxs-lookup"><span data-stu-id="75164-159">System.String</span></span>

### <span data-ttu-id="75164-160">Microsoft.Azure.Commands.BatCH. Modellek. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="75164-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>
<span data-ttu-id="75164-161">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75164-161">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="75164-162">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="75164-162">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="75164-163">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75164-163">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="75164-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75164-164">OUTPUTS</span></span>

### <span data-ttu-id="75164-165">System. Void</span><span class="sxs-lookup"><span data-stu-id="75164-165">System.Void</span></span>

## <span data-ttu-id="75164-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75164-166">NOTES</span></span>

## <span data-ttu-id="75164-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75164-167">RELATED LINKS</span></span>

[<span data-ttu-id="75164-168">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="75164-168">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="75164-169">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="75164-169">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="75164-170">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="75164-170">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


