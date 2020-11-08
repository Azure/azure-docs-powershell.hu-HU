---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 043e7bf24ce994edd0ce5621d2de8b17616d43f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187083"
---
# <span data-ttu-id="f3ce9-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f3ce9-101">New-AzBatchTask</span></span>

## <span data-ttu-id="f3ce9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ce9-103">Kötegelt feladatot hoz létre a projektben.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="f3ce9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3ce9-104">SYNTAX</span></span>

### <span data-ttu-id="f3ce9-105">JobId_Single (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3ce9-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ce9-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="f3ce9-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ce9-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="f3ce9-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ce9-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="f3ce9-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3ce9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3ce9-109">DESCRIPTION</span></span>
<span data-ttu-id="f3ce9-110">A **New-AzBatchTask** parancsmag egy Azure-köteg feladatot hoz létre a *JobId* paraméterben vagy a *Job* paraméterben megadott munkához.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="f3ce9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f3ce9-111">EXAMPLES</span></span>

### <span data-ttu-id="f3ce9-112">1. példa: köteg-tevékenység létrehozása</span><span class="sxs-lookup"><span data-stu-id="f3ce9-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="f3ce9-113">Ez a parancs létrehoz egy feladatot, amely a Task23 AZONOSÍTÓval rendelkezik a 000001 azonosítójú projektben.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="f3ce9-114">A tevékenység futtatja a megadott parancsot.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-114">The task runs the specified command.</span></span>
<span data-ttu-id="f3ce9-115">A **Get-AzBatchAccountKey** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-115">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f3ce9-116">2. példa: köteg-tevékenység létrehozása</span><span class="sxs-lookup"><span data-stu-id="f3ce9-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="f3ce9-117">Ez a parancs a **Get-AzBatchJob** parancsmaggal kapja meg a 000001 azonosítójú kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="f3ce9-118">A parancs a munkafolyamatot a csővezeték-kezelő használatával továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f3ce9-119">A parancs létrehoz egy feladatot, amely az azonosító Task26 tartalmazza az adott feladatban.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="f3ce9-120">A feladat a megadott parancsot a magasabb szintű engedélyek használatával futtatja.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="f3ce9-121">3. példa: tevékenység-gyűjtemény felvétele a megadott feladatba a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="f3ce9-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="f3ce9-122">Az első parancs a **Get-AzBatchAccountKey** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="f3ce9-123">A parancs a $Context változóban tárolja az objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="f3ce9-124">A következő két parancs **PSCloudTask** -objektumokat hoz létre a New-Object parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="f3ce9-125">A parancsok a $Task 01 és $Task 02 változóban található feladatokat tárolják.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="f3ce9-126">A végleges parancs a **Get-AzBatchJob** segítségével a 000001 azonosítójú kötegelt feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="f3ce9-127">Ezután a parancs átadja ezt a feladatot az aktuális parancsmagnak a pipeline operátorral.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f3ce9-128">A parancs felveszi a feladatok gyűjteményét az adott feladatba.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="f3ce9-129">A parancs a $Contextban tárolt környezetet használja.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="f3ce9-130">4. példa: tevékenység-gyűjtemény felvétele a megadott feladatba</span><span class="sxs-lookup"><span data-stu-id="f3ce9-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="f3ce9-131">Az első parancs a **Get-AzBatchAccountKey** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="f3ce9-132">A parancs a $Context változóban tárolja az objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="f3ce9-133">A következő két parancs **PSCloudTask** -objektumokat hoz létre a New-Object parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="f3ce9-134">A parancsok a $Task 01 és $Task 02 változóban található feladatokat tárolják.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="f3ce9-135">A végleges parancs felveszi a $Task 01-ben tárolt feladatokat, és a "000001" AZONOSÍTÓJÚ munkahelyhez $Task a 02-et.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="f3ce9-136">Példa 5: tevékenység hozzáadása kimeneti fájlokkal</span><span class="sxs-lookup"><span data-stu-id="f3ce9-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="f3ce9-137">6. példa: tevékenység hozzáadása a hitelesítési jogkivonat beállításaival</span><span class="sxs-lookup"><span data-stu-id="f3ce9-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="f3ce9-138">7. példa: egy tárolóban futó tevékenység felvétele</span><span class="sxs-lookup"><span data-stu-id="f3ce9-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="f3ce9-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3ce9-139">PARAMETERS</span></span>

### <span data-ttu-id="f3ce9-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="f3ce9-140">-AffinityInformation</span></span>
<span data-ttu-id="f3ce9-141">Itt adhatja meg azt a területi célzást, amellyel a kötegelt szolgáltatás kijelöli a feladatot futtató csomópontot.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="f3ce9-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="f3ce9-142">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ce9-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="f3ce9-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="f3ce9-144">A kötegelt szolgáltatási műveletek elvégzéséhez használható hitelesítő jogkivonat beállításai.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="f3ce9-145">Ha be van állítva ez a beállítás, a köteg szolgáltatás olyan hitelesítési jogkivonattal látja el a feladatot, amely a kötegelt szolgáltatás műveleteinek hitelesítéséhez használható a fiók-hozzáférési kulcs megkövetelése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="f3ce9-146">A token a AZ_BATCH_AUTHENTICATION_TOKEN környezeti változón keresztül érhető el.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="f3ce9-147">A tevékenység által a jogkivonattal végezhető műveletek a beállításoktól függnek.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="f3ce9-148">A feladatok például kérhetik a feladatok megadását az egyéb feladatok hozzáadásához, illetve a feladat vagy más feladatok állapotát.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ce9-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f3ce9-149">-BatchContext</span></span>
<span data-ttu-id="f3ce9-150">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f3ce9-151">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f3ce9-152">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-152">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f3ce9-153">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f3ce9-154">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f3ce9-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="f3ce9-155">-CommandLine</span></span>
<span data-ttu-id="f3ce9-156">A tevékenységhez tartozó parancssort adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="f3ce9-157">-Kényszerek</span><span class="sxs-lookup"><span data-stu-id="f3ce9-157">-Constraints</span></span>
<span data-ttu-id="f3ce9-158">A feladatra vonatkozó végrehajtási kényszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="f3ce9-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="f3ce9-159">-ContainerSettings</span></span>
<span data-ttu-id="f3ce9-160">Annak a tárolónak a beállításai, amely alatt a tevékenység fut.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="f3ce9-161">Ha a feladatot futtató készlet containerConfiguration van beállítva, akkor ezt is be kell állítania.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="f3ce9-162">Ha a feladatot futtató készlet nem rendelkezik containerConfiguration beállítással, akkor ez a beállítás nem állítható be.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="f3ce9-163">Ha ez az érték van megadva, az összes olyan könyvtár, amelyet a AZ_BATCH_NODE_ROOT_DIR (az Azure-kötegek gyökerét tartalmazó kötegek gyökerében) a tárolóhoz rendelt, a tárolóhoz társít minden környezeti változót, és a program végrehajtja a feladat parancssorát a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ce9-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ce9-164">-DefaultProfile</span></span>
<span data-ttu-id="f3ce9-165">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3ce9-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="f3ce9-166">-DependsOn</span></span>
<span data-ttu-id="f3ce9-167">Azt adja meg, hogy a tevékenység más tevékenységtől függ.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="f3ce9-168">A tevékenység addig nem lesz ütemezve, amíg az összes függő tevékenység sikeresen el nem fejeződött.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="f3ce9-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3ce9-169">-DisplayName</span></span>
<span data-ttu-id="f3ce9-170">A tevékenység megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="f3ce9-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="f3ce9-171">-EnvironmentSettings</span></span>
<span data-ttu-id="f3ce9-172">A környezeti beállításokat adja meg kulcs/érték párokként, hogy a parancsmag hozzáadja a tevékenységhez.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="f3ce9-173">A kulcs a környezet beállításának neve.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-173">The key is the environment setting name.</span></span>
<span data-ttu-id="f3ce9-174">Az érték a környezet beállítása.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-174">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ce9-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="f3ce9-175">-ExitConditions</span></span>
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

### <span data-ttu-id="f3ce9-176">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f3ce9-176">-Id</span></span>
<span data-ttu-id="f3ce9-177">A tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="f3ce9-178">-Job</span><span class="sxs-lookup"><span data-stu-id="f3ce9-178">-Job</span></span>
<span data-ttu-id="f3ce9-179">Azt a feladatot adja meg, amely alatt a parancsmag létrehozta a feladatot.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="f3ce9-180">**PSCloudJob** objektum beolvasásához használja az Get-AzBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="f3ce9-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="f3ce9-181">-JobId</span></span>
<span data-ttu-id="f3ce9-182">Annak a feladatnak az AZONOSÍTÓját adja meg, amely alatt a parancsmag létrehozta a feladatot.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="f3ce9-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="f3ce9-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="f3ce9-184">Itt adhatja meg, hogy miként futtathat több példányos tevékenységet.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="f3ce9-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="f3ce9-185">-OutputFile</span></span>
<span data-ttu-id="f3ce9-186">A parancssor futtatása után megkezdi vagy beállítja a kötegelt szolgáltatás által a számítási csomópontról feltöltendő fájlok listáját.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="f3ce9-187">A többpéldányos feladatok esetében a fájlok csak arra a számítási csomópontra lesznek feltöltve, amelyen az elsődleges feladat van végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ce9-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="f3ce9-188">-ResourceFiles</span></span>
<span data-ttu-id="f3ce9-189">A tevékenységhez szükséges erőforrás-fájlokat (kulcs/érték párokként) adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="f3ce9-190">A kulcs az erőforrás fájlelérési útja.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-190">The key is the resource file path.</span></span>
<span data-ttu-id="f3ce9-191">Az érték az erőforrás fájl blob-forrása.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-191">The value is the resource file blob source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSResourceFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ce9-192">-Feladatok</span><span class="sxs-lookup"><span data-stu-id="f3ce9-192">-Tasks</span></span>
<span data-ttu-id="f3ce9-193">A felvenni kívánt feladatok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="f3ce9-194">Minden tevékenységhez egyedi AZONOSÍTÓval kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="f3ce9-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="f3ce9-195">-UserIdentity</span></span>
<span data-ttu-id="f3ce9-196">A tevékenység által futtatott felhasználó identitása.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-196">The user identity under which the task runs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ce9-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ce9-197">CommonParameters</span></span>
<span data-ttu-id="f3ce9-198">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3ce9-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ce9-199">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f3ce9-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ce9-200">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3ce9-200">INPUTS</span></span>

### <span data-ttu-id="f3ce9-201">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="f3ce9-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="f3ce9-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f3ce9-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f3ce9-203">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3ce9-203">OUTPUTS</span></span>

### <span data-ttu-id="f3ce9-204">System. Void</span><span class="sxs-lookup"><span data-stu-id="f3ce9-204">System.Void</span></span>

## <span data-ttu-id="f3ce9-205">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3ce9-205">NOTES</span></span>

## <span data-ttu-id="f3ce9-206">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3ce9-206">RELATED LINKS</span></span>

[<span data-ttu-id="f3ce9-207">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f3ce9-207">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f3ce9-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f3ce9-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="f3ce9-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f3ce9-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="f3ce9-210">Új – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f3ce9-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="f3ce9-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f3ce9-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="f3ce9-212">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f3ce9-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="f3ce9-213">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f3ce9-213">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
