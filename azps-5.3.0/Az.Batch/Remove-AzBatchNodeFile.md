---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 7e9aeebebfc5720ab006d43071eadeabe6bcf655
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478225"
---
# <span data-ttu-id="02600-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="02600-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="02600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02600-102">SYNOPSIS</span></span>
<span data-ttu-id="02600-103">Egy feladat vagy számítási csomópont csomópontfájljának törlése.</span><span class="sxs-lookup"><span data-stu-id="02600-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="02600-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="02600-104">SYNTAX</span></span>

### <span data-ttu-id="02600-105">Tevékenység</span><span class="sxs-lookup"><span data-stu-id="02600-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02600-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="02600-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02600-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="02600-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02600-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="02600-108">DESCRIPTION</span></span>
<span data-ttu-id="02600-109">A **Remove-AzBatchNodeFile** parancsmag töröl egy Azure Batch-csomópontfájlt egy feladathoz vagy számítási csomóponthoz.</span><span class="sxs-lookup"><span data-stu-id="02600-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="02600-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="02600-110">EXAMPLES</span></span>

### <span data-ttu-id="02600-111">1. példa: Feladathoz társított fájl törlése</span><span class="sxs-lookup"><span data-stu-id="02600-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="02600-112">Ez a parancs törli a csomópontfájlt, amely neve wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="02600-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="02600-113">Ez a fájl a Feladat-000001 feladat alatt a 26-os azonosítójú tevékenységhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="02600-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="02600-114">2. példa: Fájl törlése egy számítási csomópontból</span><span class="sxs-lookup"><span data-stu-id="02600-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="02600-115">Ez a parancs törli a startup\testFile.txt az id Pool07 azonosítójú készlet megadott számítási csomópontjának csomópontját.</span><span class="sxs-lookup"><span data-stu-id="02600-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="02600-116">3. példa: Fájl eltávolítása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="02600-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="02600-117">Ez a parancs a **Get-AzBatchNodeFile** használatával kapja meg a csomópontfájlt.</span><span class="sxs-lookup"><span data-stu-id="02600-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="02600-118">Ez a fájl a Feladat-000001 feladat alatt a 26-os azonosítójú tevékenységhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="02600-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="02600-119">A parancs a folyamat segítségével átadja a fájlt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="02600-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="02600-120">Az aktuális parancsmag eltávolítja a csomópontfájlt.</span><span class="sxs-lookup"><span data-stu-id="02600-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="02600-121">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="02600-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="02600-122">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02600-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="02600-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02600-123">PARAMETERS</span></span>

### <span data-ttu-id="02600-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="02600-124">-BatchContext</span></span>
<span data-ttu-id="02600-125">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="02600-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="02600-126">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="02600-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="02600-127">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="02600-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="02600-128">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="02600-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="02600-129">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="02600-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="02600-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="02600-130">-ComputeNodeId</span></span>
<span data-ttu-id="02600-131">Annak a számítási csomópontnak az azonosítója, amely a parancsmag által törölt Batch csomópontfájlt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="02600-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="02600-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02600-132">-DefaultProfile</span></span>
<span data-ttu-id="02600-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02600-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02600-134">-Force</span><span class="sxs-lookup"><span data-stu-id="02600-134">-Force</span></span>
<span data-ttu-id="02600-135">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="02600-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02600-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02600-136">-InputObject</span></span>
<span data-ttu-id="02600-137">A parancsmag által törölt csomópontfájlt képviselő **PSNodeFile-objektumot** adja meg.</span><span class="sxs-lookup"><span data-stu-id="02600-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="02600-138">**PSNodeFile beszerzéséhez** használja a Get-AzBatchNodeFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="02600-138">To obtain a **PSNodeFile**, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="02600-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="02600-139">-JobId</span></span>
<span data-ttu-id="02600-140">A tevékenységet tartalmazó feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="02600-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="02600-141">-Path</span><span class="sxs-lookup"><span data-stu-id="02600-141">-Path</span></span>
<span data-ttu-id="02600-142">A törölni kívánt csomópontfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="02600-142">The file path of the node file to delete.</span></span>

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

### <span data-ttu-id="02600-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="02600-143">-PoolId</span></span>
<span data-ttu-id="02600-144">Annak a készletnek az azonosítóját adja meg, amely azokat a számítási csomópontokat tartalmazza, amelyekből a parancsmag eltávolít egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="02600-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="02600-145">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="02600-145">-Recursive</span></span>
<span data-ttu-id="02600-146">Azt jelzi, hogy ez a parancsmag törli a mappát, valamint a megadott elérési út alatti almappákat és fájlokat.</span><span class="sxs-lookup"><span data-stu-id="02600-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="02600-147">Ez a parancsmag csak akkor releváns, ha az elérési út egy mappa.</span><span class="sxs-lookup"><span data-stu-id="02600-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="02600-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="02600-148">-TaskId</span></span>
<span data-ttu-id="02600-149">A tevékenység azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02600-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="02600-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02600-150">-Confirm</span></span>
<span data-ttu-id="02600-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="02600-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02600-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02600-152">-WhatIf</span></span>
<span data-ttu-id="02600-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="02600-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02600-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02600-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02600-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02600-155">CommonParameters</span></span>
<span data-ttu-id="02600-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02600-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02600-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02600-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02600-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02600-158">INPUTS</span></span>

### <span data-ttu-id="02600-159">System.String</span><span class="sxs-lookup"><span data-stu-id="02600-159">System.String</span></span>

### <span data-ttu-id="02600-160">Microsoft.Azure.Commands.Bat. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="02600-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="02600-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="02600-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="02600-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02600-162">OUTPUTS</span></span>

### <span data-ttu-id="02600-163">System.Void</span><span class="sxs-lookup"><span data-stu-id="02600-163">System.Void</span></span>

## <span data-ttu-id="02600-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="02600-164">NOTES</span></span>

## <span data-ttu-id="02600-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02600-165">RELATED LINKS</span></span>

[<span data-ttu-id="02600-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="02600-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="02600-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="02600-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="02600-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="02600-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


