---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 043e7bf24ce994edd0ce5621d2de8b17616d43f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361295"
---
# <span data-ttu-id="6fe24-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6fe24-101">New-AzBatchTask</span></span>

## <span data-ttu-id="6fe24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe24-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe24-103">Létrehoz egy Batch-feladatot egy feladat alatt.</span><span class="sxs-lookup"><span data-stu-id="6fe24-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="6fe24-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6fe24-104">SYNTAX</span></span>

### <span data-ttu-id="6fe24-105">JobId_Single (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6fe24-105">JobId_Single (Default)</span></span>
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

### <span data-ttu-id="6fe24-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="6fe24-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fe24-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="6fe24-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fe24-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="6fe24-108">JobObject_Single</span></span>
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

## <span data-ttu-id="6fe24-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6fe24-109">DESCRIPTION</span></span>
<span data-ttu-id="6fe24-110">A **New-AzBatchTask** parancsmag létrehoz egy Azure Batch-feladatot a *JobId* vagy a Job paraméter által *megadott feladat* alapján.</span><span class="sxs-lookup"><span data-stu-id="6fe24-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="6fe24-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6fe24-111">EXAMPLES</span></span>

### <span data-ttu-id="6fe24-112">1. példa: Kötegfeladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="6fe24-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="6fe24-113">Ezzel a paranccsal olyan tevékenységet hoz létre, amely a 000001 azonosítójú feladat alatt az Azonosító Tevékenység23 azonosítóval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="6fe24-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="6fe24-114">A feladat a megadott parancsot futtatja.</span><span class="sxs-lookup"><span data-stu-id="6fe24-114">The task runs the specified command.</span></span>
<span data-ttu-id="6fe24-115">A **Get-AzBatchAccountKey** parancsmaggal kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="6fe24-115">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6fe24-116">2. példa: Kötegfeladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="6fe24-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="6fe24-117">Ez a parancs a **Get-AzBatch Job** parancsmag használatával a 000001 azonosítójú kötegfeladatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6fe24-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="6fe24-118">A parancs a folyamat műveleti operátorával átadja a feladatot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="6fe24-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6fe24-119">A parancs létrehoz egy tevékenységet, amely alatt a Feladat26 azonosító van.</span><span class="sxs-lookup"><span data-stu-id="6fe24-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="6fe24-120">A feladat emelt szintű engedélyekkel futtatja a megadott parancsot.</span><span class="sxs-lookup"><span data-stu-id="6fe24-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="6fe24-121">3. példa: Tevékenységek gyűjteményének hozzáadása a megadott feladathoz a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="6fe24-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="6fe24-122">Az első parancs létrehoz egy objektumhivatkozást a ContosoBatchAccount nevű kötegfiók fiókkulcsára a **Get-AzBatchAccountKey paranccsal.**</span><span class="sxs-lookup"><span data-stu-id="6fe24-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="6fe24-123">A parancs ezt az objektumhivatkozást a $Context tárolja.</span><span class="sxs-lookup"><span data-stu-id="6fe24-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="6fe24-124">A következő két parancs **PSCloudTask-objektumokat** hoz létre a New-Object parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="6fe24-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="6fe24-125">A parancsok a feladatokat a $Task 01 és $Task 02 változókban tárolják.</span><span class="sxs-lookup"><span data-stu-id="6fe24-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="6fe24-126">Az utolsó parancs a **Get-AzBatch Job** használatával a 000001 azonosítójú kötegfeladatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6fe24-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="6fe24-127">Ezután a parancs a folyamat műveleti operátorával átadja a feladatot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="6fe24-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6fe24-128">A parancs a feladat alatt felvesz egy feladatgyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="6fe24-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="6fe24-129">A parancs a helyi menüben tárolt $Context.</span><span class="sxs-lookup"><span data-stu-id="6fe24-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="6fe24-130">4. példa: Tevékenységek gyűjteményének hozzáadása a megadott feladathoz</span><span class="sxs-lookup"><span data-stu-id="6fe24-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="6fe24-131">Az első parancs létrehoz egy objektumhivatkozást a ContosoBatchAccount nevű kötegfiók fiókkulcsára a **Get-AzBatchAccountKey paranccsal.**</span><span class="sxs-lookup"><span data-stu-id="6fe24-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="6fe24-132">A parancs ezt az objektumhivatkozást a $Context tárolja.</span><span class="sxs-lookup"><span data-stu-id="6fe24-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="6fe24-133">A következő két parancs **PSCloudTask-objektumokat** hoz létre a New-Object parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="6fe24-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="6fe24-134">A parancsok a feladatokat a $Task 01 és $Task 02 változókban tárolják.</span><span class="sxs-lookup"><span data-stu-id="6fe24-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="6fe24-135">Az utolsó parancs hozzáadja a $Task 01-ben és a $Task 02-ben a 000001 azonosítójú feladat alatt tárolt feladatokat.</span><span class="sxs-lookup"><span data-stu-id="6fe24-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="6fe24-136">5. példa: Feladat hozzáadása kimeneti fájlokkal</span><span class="sxs-lookup"><span data-stu-id="6fe24-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="6fe24-137">6. példa: Feladat hozzáadása hitelesítési jogkivonat-beállításokkal</span><span class="sxs-lookup"><span data-stu-id="6fe24-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="6fe24-138">7. példa: Tárolóban futó feladat hozzáadása</span><span class="sxs-lookup"><span data-stu-id="6fe24-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="6fe24-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fe24-139">PARAMETERS</span></span>

### <span data-ttu-id="6fe24-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="6fe24-140">-AffinityInformation</span></span>
<span data-ttu-id="6fe24-141">Meghatároz egy tippet a helyi beállításról, amellyel a Batch szolgáltatás kiválaszt egy csomópontot, amelyen futtatni kell a feladatot.</span><span class="sxs-lookup"><span data-stu-id="6fe24-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="6fe24-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="6fe24-142">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="6fe24-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="6fe24-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="6fe24-144">A hitelesítési jogkivonat beállításai, amelyek alapján a feladat kötegszolgáltatás-műveleteket hajthat végre.</span><span class="sxs-lookup"><span data-stu-id="6fe24-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="6fe24-145">Ha ez a beállítás meg van állítva, a Batch szolgáltatás egy hitelesítési jogkivonatot biztosít a feladatnak, amely a batch szolgáltatásműveletek hitelesítéséhez használható fiókelérési kulcs nélkül.</span><span class="sxs-lookup"><span data-stu-id="6fe24-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="6fe24-146">A tokent a AZ_BATCH_AUTHENTICATION_TOKEN környezeti változón keresztül lehet biztosítani.</span><span class="sxs-lookup"><span data-stu-id="6fe24-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="6fe24-147">A token használatával a feladat által végrehajtott műveletek a beállításoktól függnek.</span><span class="sxs-lookup"><span data-stu-id="6fe24-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="6fe24-148">Egy tevékenység például engedélyt kérhet a feladathoz, hogy más tevékenységeket is felvessen a feladatba, illetve hogy ellenőrizze a feladat vagy más tevékenységek állapotát.</span><span class="sxs-lookup"><span data-stu-id="6fe24-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

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

### <span data-ttu-id="6fe24-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6fe24-149">-BatchContext</span></span>
<span data-ttu-id="6fe24-150">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="6fe24-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6fe24-151">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="6fe24-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6fe24-152">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="6fe24-152">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6fe24-153">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="6fe24-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6fe24-154">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="6fe24-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6fe24-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="6fe24-155">-CommandLine</span></span>
<span data-ttu-id="6fe24-156">A feladat parancssorát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6fe24-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="6fe24-157">-Constraints</span><span class="sxs-lookup"><span data-stu-id="6fe24-157">-Constraints</span></span>
<span data-ttu-id="6fe24-158">A tevékenységre vonatkozó végrehajtási kényszerek megadása.</span><span class="sxs-lookup"><span data-stu-id="6fe24-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="6fe24-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="6fe24-159">-ContainerSettings</span></span>
<span data-ttu-id="6fe24-160">Annak a tárolónak a beállításai, amely alatt a feladat fut.</span><span class="sxs-lookup"><span data-stu-id="6fe24-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="6fe24-161">Ha a feladatot futtató készlethez containerConfiguration beállítás van beállítva, ezt is be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="6fe24-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="6fe24-162">Ha a feladatot futtató készletben nincs containerConfiguration beállítva, ezt nem kell beállítani.</span><span class="sxs-lookup"><span data-stu-id="6fe24-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="6fe24-163">Ha ez meg van adva, az AZ_BATCH_NODE_ROOT_DIR alatti összes könyvtár (a csomópont Azure Batch-könyvtárának gyökérkönyvtára) megfeleltetve lesz a tárolónak, a feladatkörnyezet összes változója megfeleltetve lesz a tárolónak, és a feladat parancssorát végrehajtja a rendszer a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="6fe24-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

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

### <span data-ttu-id="6fe24-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe24-164">-DefaultProfile</span></span>
<span data-ttu-id="6fe24-165">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6fe24-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fe24-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="6fe24-166">-DependsOn</span></span>
<span data-ttu-id="6fe24-167">Azt adja meg, hogy a tevékenység más tevékenységektől függ.</span><span class="sxs-lookup"><span data-stu-id="6fe24-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="6fe24-168">A tevékenység mindaddig nem lesz ütemezve, amíg az összes függő tevékenység sikeresen be nem fejeződött.</span><span class="sxs-lookup"><span data-stu-id="6fe24-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="6fe24-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6fe24-169">-DisplayName</span></span>
<span data-ttu-id="6fe24-170">A tevékenység megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fe24-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="6fe24-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="6fe24-171">-EnvironmentSettings</span></span>
<span data-ttu-id="6fe24-172">Ez a parancsmag által a feladathoz hozzáadott környezeti beállításokat adja meg kulcs-érték párokként.</span><span class="sxs-lookup"><span data-stu-id="6fe24-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="6fe24-173">A kulcs a környezet beállításának neve.</span><span class="sxs-lookup"><span data-stu-id="6fe24-173">The key is the environment setting name.</span></span>
<span data-ttu-id="6fe24-174">Az érték a környezet beállítása.</span><span class="sxs-lookup"><span data-stu-id="6fe24-174">The value is the environment setting.</span></span>

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

### <span data-ttu-id="6fe24-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="6fe24-175">-ExitConditions</span></span>
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

### <span data-ttu-id="6fe24-176">-Id</span><span class="sxs-lookup"><span data-stu-id="6fe24-176">-Id</span></span>
<span data-ttu-id="6fe24-177">A tevékenység azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fe24-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="6fe24-178">-Job</span><span class="sxs-lookup"><span data-stu-id="6fe24-178">-Job</span></span>
<span data-ttu-id="6fe24-179">Azt a feladatot adja meg, amely alatt ez a parancsmag létrehozza a feladatot.</span><span class="sxs-lookup"><span data-stu-id="6fe24-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="6fe24-180">**PSCloudFeladat-objektum** beszerzéséhez használja a Get-AzBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6fe24-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="6fe24-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="6fe24-181">-JobId</span></span>
<span data-ttu-id="6fe24-182">Annak a feladatnak az azonosítója, amely alatt ez a parancsmag létrehozza a feladatot.</span><span class="sxs-lookup"><span data-stu-id="6fe24-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="6fe24-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="6fe24-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="6fe24-184">A többpéldányos feladatok futtatásával kapcsolatos információkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fe24-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="6fe24-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="6fe24-185">-OutputFile</span></span>
<span data-ttu-id="6fe24-186">Beállítja vagy beállítja a batch szolgáltatás által a számítási csomópontról a parancssor futtatása után feltöltandó fájlok listáját.</span><span class="sxs-lookup"><span data-stu-id="6fe24-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="6fe24-187">Többpéldányos feladatok esetén a fájlok csak abból a számítási csomópontból lesznek feltöltve, amelyen az elsődleges feladat végrehajtása történik.</span><span class="sxs-lookup"><span data-stu-id="6fe24-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

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

### <span data-ttu-id="6fe24-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="6fe24-188">-ResourceFiles</span></span>
<span data-ttu-id="6fe24-189">Megadja a tevékenységhez szükséges erőforrásfájlokat kulcs-/értékpárokként.</span><span class="sxs-lookup"><span data-stu-id="6fe24-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="6fe24-190">A kulcs az erőforrásfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="6fe24-190">The key is the resource file path.</span></span>
<span data-ttu-id="6fe24-191">Az érték az erőforrásfájl blobforrása.</span><span class="sxs-lookup"><span data-stu-id="6fe24-191">The value is the resource file blob source.</span></span>

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

### <span data-ttu-id="6fe24-192">-Feladatok</span><span class="sxs-lookup"><span data-stu-id="6fe24-192">-Tasks</span></span>
<span data-ttu-id="6fe24-193">A hozzáadható feladatok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fe24-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="6fe24-194">Minden tevékenységhez egyedi azonosítónak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6fe24-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="6fe24-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="6fe24-195">-UserIdentity</span></span>
<span data-ttu-id="6fe24-196">Az a felhasználói identitás, amely alatt a feladat fut.</span><span class="sxs-lookup"><span data-stu-id="6fe24-196">The user identity under which the task runs.</span></span>

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

### <span data-ttu-id="6fe24-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe24-197">CommonParameters</span></span>
<span data-ttu-id="6fe24-198">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe24-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe24-199">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fe24-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe24-200">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fe24-200">INPUTS</span></span>

### <span data-ttu-id="6fe24-201">Microsoft.Azure.Commands.Bat. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="6fe24-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="6fe24-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6fe24-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6fe24-203">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fe24-203">OUTPUTS</span></span>

### <span data-ttu-id="6fe24-204">System.Void</span><span class="sxs-lookup"><span data-stu-id="6fe24-204">System.Void</span></span>

## <span data-ttu-id="6fe24-205">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6fe24-205">NOTES</span></span>

## <span data-ttu-id="6fe24-206">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fe24-206">RELATED LINKS</span></span>

[<span data-ttu-id="6fe24-207">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6fe24-207">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6fe24-208">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="6fe24-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="6fe24-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6fe24-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="6fe24-210">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6fe24-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="6fe24-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6fe24-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="6fe24-212">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6fe24-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="6fe24-213">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="6fe24-213">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
