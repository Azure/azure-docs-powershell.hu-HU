---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 823d04fc0b6dda97b1ad6d50957a2b78c999f789
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847830"
---
# <span data-ttu-id="9d77c-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="9d77c-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="9d77c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d77c-102">SYNOPSIS</span></span>
<span data-ttu-id="9d77c-103">Törli a tevékenység vagy a számítási csomópont csomópont-fájlját.</span><span class="sxs-lookup"><span data-stu-id="9d77c-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="9d77c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d77c-104">SYNTAX</span></span>

### <span data-ttu-id="9d77c-105">Tevékenység</span><span class="sxs-lookup"><span data-stu-id="9d77c-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d77c-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="9d77c-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d77c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9d77c-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d77c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d77c-108">DESCRIPTION</span></span>
<span data-ttu-id="9d77c-109">A **Remove-AzBatchNodeFile** parancsmag egy Azure kötegfájl-csomópontot töröl egy tevékenységhez vagy egy kiszámított csomóponthoz.</span><span class="sxs-lookup"><span data-stu-id="9d77c-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="9d77c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9d77c-110">EXAMPLES</span></span>

### <span data-ttu-id="9d77c-111">Példa 1: egy tevékenységhez társított fájl törlése</span><span class="sxs-lookup"><span data-stu-id="9d77c-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="9d77c-112">Ez a parancs törli a wd\testFile.txt nevű csomópontot.</span><span class="sxs-lookup"><span data-stu-id="9d77c-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="9d77c-113">A fájl társítva van azzal a tevékenységgel, amelynek azonosító Task26 a Job Job-000001.</span><span class="sxs-lookup"><span data-stu-id="9d77c-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="9d77c-114">2. példa: fájl törlése egy számítási csomópontból</span><span class="sxs-lookup"><span data-stu-id="9d77c-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="9d77c-115">Ez a parancs törli a startup\testFile.txt nevű csomópontot az azonosító Pool07 tartalmazó készlet meghatározott számítási csomópontról.</span><span class="sxs-lookup"><span data-stu-id="9d77c-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="9d77c-116">3. példa: fájl eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="9d77c-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="9d77c-117">Ez a parancs a **Get-AzBatchNodeFile** használatával kapja meg a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="9d77c-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="9d77c-118">A fájl társítva van azzal a tevékenységgel, amelynek azonosító Task26 a Job Job-000001.</span><span class="sxs-lookup"><span data-stu-id="9d77c-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="9d77c-119">A parancs a fájlt átadja az aktuális parancsmagnak a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="9d77c-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="9d77c-120">Az aktuális parancsmag eltávolítja a csomópontot tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="9d77c-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="9d77c-121">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d77c-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9d77c-122">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9d77c-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9d77c-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d77c-123">PARAMETERS</span></span>

### <span data-ttu-id="9d77c-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9d77c-124">-BatchContext</span></span>
<span data-ttu-id="9d77c-125">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="9d77c-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9d77c-126">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="9d77c-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9d77c-127">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="9d77c-127">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9d77c-128">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="9d77c-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9d77c-129">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="9d77c-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9d77c-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="9d77c-130">-ComputeNodeId</span></span>
<span data-ttu-id="9d77c-131">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amely a parancsmag által törölt köteg csomópont-fájlt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9d77c-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="9d77c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d77c-132">-DefaultProfile</span></span>
<span data-ttu-id="9d77c-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d77c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d77c-134">-Force</span><span class="sxs-lookup"><span data-stu-id="9d77c-134">-Force</span></span>
<span data-ttu-id="9d77c-135">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9d77c-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9d77c-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d77c-136">-InputObject</span></span>
<span data-ttu-id="9d77c-137">Azt a **PSNodeFile** objektumot adja meg, amely a parancsmag által törölt csomópont-fájlt jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9d77c-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="9d77c-138">Ha **PSNodeFile** szeretne beolvasni, használja az Get-AzBatchNodeFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9d77c-138">To obtain a **PSNodeFile** , use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="9d77c-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="9d77c-139">-JobId</span></span>
<span data-ttu-id="9d77c-140">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d77c-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="9d77c-141">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="9d77c-141">-Path</span></span>
<span data-ttu-id="9d77c-142">A törlendő csomópont fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9d77c-142">The file path of the node file to delete.</span></span>

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

### <span data-ttu-id="9d77c-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="9d77c-143">-PoolId</span></span>
<span data-ttu-id="9d77c-144">Annak a készletnek az AZONOSÍTÓját adja meg, amely azokat a számítási csomópontokat tartalmazza, amelyeknek a parancsmagja eltávolítja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="9d77c-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="9d77c-145">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="9d77c-145">-Recursive</span></span>
<span data-ttu-id="9d77c-146">Azt jelzi, hogy ez a parancsmag törli a mappát és az összes almappát és fájlt a megadott elérési úttal.</span><span class="sxs-lookup"><span data-stu-id="9d77c-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="9d77c-147">Ez a parancsmag csak akkor érvényes, ha az elérési út egy mappa.</span><span class="sxs-lookup"><span data-stu-id="9d77c-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="9d77c-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="9d77c-148">-TaskId</span></span>
<span data-ttu-id="9d77c-149">A tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d77c-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="9d77c-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9d77c-150">-Confirm</span></span>
<span data-ttu-id="9d77c-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9d77c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d77c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d77c-152">-WhatIf</span></span>
<span data-ttu-id="9d77c-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9d77c-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d77c-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d77c-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d77c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d77c-155">CommonParameters</span></span>
<span data-ttu-id="9d77c-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d77c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d77c-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d77c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d77c-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d77c-158">INPUTS</span></span>

### <span data-ttu-id="9d77c-159">System. String</span><span class="sxs-lookup"><span data-stu-id="9d77c-159">System.String</span></span>

### <span data-ttu-id="9d77c-160">Microsoft.Azure.Commands.BatCH. Modellek. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="9d77c-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="9d77c-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9d77c-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9d77c-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d77c-162">OUTPUTS</span></span>

### <span data-ttu-id="9d77c-163">System. Void</span><span class="sxs-lookup"><span data-stu-id="9d77c-163">System.Void</span></span>

## <span data-ttu-id="9d77c-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d77c-164">NOTES</span></span>

## <span data-ttu-id="9d77c-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d77c-165">RELATED LINKS</span></span>

[<span data-ttu-id="9d77c-166">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9d77c-166">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9d77c-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="9d77c-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="9d77c-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="9d77c-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


