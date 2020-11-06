---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497899"
---
# <span data-ttu-id="d6710-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d6710-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="d6710-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6710-102">SYNOPSIS</span></span>
<span data-ttu-id="d6710-103">Kötegelt feladatot hoz létre a projektben.</span><span class="sxs-lookup"><span data-stu-id="d6710-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6710-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6710-104">SYNTAX</span></span>

### <span data-ttu-id="d6710-105">JobId_Single (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6710-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6710-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="d6710-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6710-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="d6710-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6710-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="d6710-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6710-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6710-109">DESCRIPTION</span></span>
<span data-ttu-id="d6710-110">A **New-AzureBatchTask** parancsmag egy Azure-köteg feladatot hoz létre a *JobId* paraméterben vagy a *Job* paraméterben megadott munkához.</span><span class="sxs-lookup"><span data-stu-id="d6710-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="d6710-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d6710-111">EXAMPLES</span></span>

### <span data-ttu-id="d6710-112">1. példa: köteg-tevékenység létrehozása</span><span class="sxs-lookup"><span data-stu-id="d6710-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="d6710-113">Ez a parancs létrehoz egy feladatot, amely a Task23 AZONOSÍTÓval rendelkezik a 000001 azonosítójú projektben.</span><span class="sxs-lookup"><span data-stu-id="d6710-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d6710-114">A tevékenység futtatja a megadott parancsot.</span><span class="sxs-lookup"><span data-stu-id="d6710-114">The task runs the specified command.</span></span>
<span data-ttu-id="d6710-115">A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="d6710-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d6710-116">2. példa: köteg-tevékenység létrehozása</span><span class="sxs-lookup"><span data-stu-id="d6710-116">Example 2: Create a Batch task</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

<span data-ttu-id="d6710-117">Ez a parancs a **Get-AzureBatchJob** parancsmaggal kapja meg a 000001 azonosítójú kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="d6710-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="d6710-118">A parancs a munkafolyamatot a csővezeték-kezelő használatával továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d6710-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d6710-119">A parancs létrehoz egy feladatot, amely az azonosító Task26 tartalmazza az adott feladatban.</span><span class="sxs-lookup"><span data-stu-id="d6710-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="d6710-120">A feladat a megadott parancsot a magasabb szintű engedélyek használatával futtatja.</span><span class="sxs-lookup"><span data-stu-id="d6710-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="d6710-121">3. példa: tevékenység-gyűjtemény felvétele a megadott feladatba a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="d6710-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="d6710-122">Az első parancs a **Get-AzureRmBatchAccountKeys** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="d6710-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="d6710-123">A parancs a $Context változóban tárolja az objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="d6710-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="d6710-124">A következő két parancs **PSCloudTask** -objektumokat hoz létre a New-Object parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="d6710-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="d6710-125">A parancsok a $Task 01 és $Task 02 változóban található feladatokat tárolják.</span><span class="sxs-lookup"><span data-stu-id="d6710-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="d6710-126">A végleges parancs a **Get-AzureBatchJob** segítségével a 000001 azonosítójú kötegelt feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="d6710-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="d6710-127">Ezután a parancs átadja ezt a feladatot az aktuális parancsmagnak a pipeline operátorral.</span><span class="sxs-lookup"><span data-stu-id="d6710-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d6710-128">A parancs felveszi a feladatok gyűjteményét az adott feladatba.</span><span class="sxs-lookup"><span data-stu-id="d6710-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="d6710-129">A parancs a $Contextban tárolt környezetet használja.</span><span class="sxs-lookup"><span data-stu-id="d6710-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="d6710-130">4. példa: tevékenység-gyűjtemény felvétele a megadott feladatba</span><span class="sxs-lookup"><span data-stu-id="d6710-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="d6710-131">Az első parancs a **Get-AzureRmBatchAccountKeys** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="d6710-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="d6710-132">A parancs a $Context változóban tárolja az objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="d6710-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="d6710-133">A következő két parancs **PSCloudTask** -objektumokat hoz létre a New-Object parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="d6710-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="d6710-134">A parancsok a $Task 01 és $Task 02 változóban található feladatokat tárolják.</span><span class="sxs-lookup"><span data-stu-id="d6710-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="d6710-135">A végleges parancs felveszi a $Task 01-ben tárolt feladatokat, és a "000001" AZONOSÍTÓJÚ munkahelyhez $Task a 02-et.</span><span class="sxs-lookup"><span data-stu-id="d6710-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

## <span data-ttu-id="d6710-136">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6710-136">PARAMETERS</span></span>

### <span data-ttu-id="d6710-137">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="d6710-137">-AffinityInformation</span></span>
<span data-ttu-id="d6710-138">Itt adhatja meg azt a területi célzást, amellyel a kötegelt szolgáltatás kijelöli a feladatot futtató csomópontot.</span><span class="sxs-lookup"><span data-stu-id="d6710-138">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-139">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="d6710-139">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d6710-140">-BatchContext</span></span>
<span data-ttu-id="d6710-141">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="d6710-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d6710-142">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d6710-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d6710-143">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="d6710-143">-CommandLine</span></span>
<span data-ttu-id="d6710-144">A tevékenységhez tartozó parancssort adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6710-144">Specifies the command line for the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-145">-Kényszerek</span><span class="sxs-lookup"><span data-stu-id="d6710-145">-Constraints</span></span>
<span data-ttu-id="d6710-146">A feladatra vonatkozó végrehajtási kényszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6710-146">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-147">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="d6710-147">-DependsOn</span></span>
<span data-ttu-id="d6710-148">Azt adja meg, hogy a tevékenység más tevékenységtől függ.</span><span class="sxs-lookup"><span data-stu-id="d6710-148">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="d6710-149">A tevékenység addig nem lesz ütemezve, amíg az összes függő tevékenység sikeresen el nem fejeződött.</span><span class="sxs-lookup"><span data-stu-id="d6710-149">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-150">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d6710-150">-DisplayName</span></span>
<span data-ttu-id="d6710-151">A tevékenység megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6710-151">Specifies the display name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-152">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="d6710-152">-EnvironmentSettings</span></span>
<span data-ttu-id="d6710-153">A környezeti beállításokat adja meg kulcs/érték párokként, hogy a parancsmag hozzáadja a tevékenységhez.</span><span class="sxs-lookup"><span data-stu-id="d6710-153">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="d6710-154">A kulcs a környezet beállításának neve.</span><span class="sxs-lookup"><span data-stu-id="d6710-154">The key is the environment setting name.</span></span>
<span data-ttu-id="d6710-155">Az érték a környezet beállítása.</span><span class="sxs-lookup"><span data-stu-id="d6710-155">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-156">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="d6710-156">-ExitConditions</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-157">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d6710-157">-Id</span></span>
<span data-ttu-id="d6710-158">A tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6710-158">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-159">-Job</span><span class="sxs-lookup"><span data-stu-id="d6710-159">-Job</span></span>
<span data-ttu-id="d6710-160">Azt a feladatot adja meg, amely alatt a parancsmag létrehozta a feladatot.</span><span class="sxs-lookup"><span data-stu-id="d6710-160">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="d6710-161">**PSCloudJob** objektum beolvasásához használja az Get-AzureBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d6710-161">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="d6710-162">-JobId</span></span>
<span data-ttu-id="d6710-163">Annak a feladatnak az AZONOSÍTÓját adja meg, amely alatt a parancsmag létrehozta a feladatot.</span><span class="sxs-lookup"><span data-stu-id="d6710-163">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-164">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="d6710-164">-MultiInstanceSettings</span></span>
<span data-ttu-id="d6710-165">Itt adhatja meg, hogy miként futtathat több példányos tevékenységet.</span><span class="sxs-lookup"><span data-stu-id="d6710-165">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-166">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="d6710-166">-ResourceFiles</span></span>
<span data-ttu-id="d6710-167">A tevékenységhez szükséges erőforrás-fájlokat (kulcs/érték párokként) adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6710-167">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="d6710-168">A kulcs az erőforrás fájlelérési útja.</span><span class="sxs-lookup"><span data-stu-id="d6710-168">The key is the resource file path.</span></span>
<span data-ttu-id="d6710-169">Az érték az erőforrás fájl blob-forrása.</span><span class="sxs-lookup"><span data-stu-id="d6710-169">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-170">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="d6710-170">-RunElevated</span></span>
<span data-ttu-id="d6710-171">Azt jelzi, hogy a tevékenység folyamata rendszergazdai jogosultságokkal fut.</span><span class="sxs-lookup"><span data-stu-id="d6710-171">Indicates that the task process runs with administrator privileges.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-172">-Feladatok</span><span class="sxs-lookup"><span data-stu-id="d6710-172">-Tasks</span></span>
<span data-ttu-id="d6710-173">A felvenni kívánt feladatok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6710-173">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="d6710-174">Minden tevékenységhez egyedi AZONOSÍTÓval kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="d6710-174">Each task must have a unique ID.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6710-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6710-175">-DefaultProfile</span></span>
<span data-ttu-id="d6710-176">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6710-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6710-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6710-177">CommonParameters</span></span>
<span data-ttu-id="d6710-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6710-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6710-179">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6710-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6710-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6710-180">INPUTS</span></span>

### <span data-ttu-id="d6710-181">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d6710-181">BatchAccountContext</span></span>
<span data-ttu-id="d6710-182">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d6710-182">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d6710-183">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="d6710-183">PSCloudJob</span></span>
<span data-ttu-id="d6710-184">A ' Job ' paraméter elfogadja a "PSCloudJob" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d6710-184">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="d6710-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6710-185">OUTPUTS</span></span>

## <span data-ttu-id="d6710-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6710-186">NOTES</span></span>

## <span data-ttu-id="d6710-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6710-187">RELATED LINKS</span></span>

[<span data-ttu-id="d6710-188">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d6710-188">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d6710-189">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d6710-189">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="d6710-190">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d6710-190">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="d6710-191">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d6710-191">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="d6710-192">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d6710-192">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="d6710-193">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d6710-193">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="d6710-194">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d6710-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


