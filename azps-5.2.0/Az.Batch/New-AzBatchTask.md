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
# New-AzBatchTask

## SYNOPSIS
Létrehoz egy Batch-feladatot egy feladat alatt.

## SZINTAXIS

### JobId_Single (alapértelmezett)
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

### JobId_Bulk
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Bulk
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Single
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

## LEÍRÁS
A **New-AzBatchTask** parancsmag létrehoz egy Azure Batch-feladatot a *JobId* vagy a Job paraméter által *megadott feladat* alapján.

## PÉLDÁK

### 1. példa: Kötegfeladat létrehozása
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

Ezzel a paranccsal olyan tevékenységet hoz létre, amely a 000001 azonosítójú feladat alatt az Azonosító Tevékenység23 azonosítóval rendelkezik.
A feladat a megadott parancsot futtatja.
A **Get-AzBatchAccountKey** parancsmaggal kontextust rendelhet a $Context változóhoz.

### 2. példa: Kötegfeladat létrehozása
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

Ez a parancs a **Get-AzBatch Job** parancsmag használatával a 000001 azonosítójú kötegfeladatot kapja meg.
A parancs a folyamat műveleti operátorával átadja a feladatot az aktuális parancsmagnak.
A parancs létrehoz egy tevékenységet, amely alatt a Feladat26 azonosító van.
A feladat emelt szintű engedélyekkel futtatja a megadott parancsot.

### 3. példa: Tevékenységek gyűjteményének hozzáadása a megadott feladathoz a folyamat használatával
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

Az első parancs létrehoz egy objektumhivatkozást a ContosoBatchAccount nevű kötegfiók fiókkulcsára a **Get-AzBatchAccountKey paranccsal.**
A parancs ezt az objektumhivatkozást a $Context tárolja.
A következő két parancs **PSCloudTask-objektumokat** hoz létre a New-Object parancsmag használatával.
A parancsok a feladatokat a $Task 01 és $Task 02 változókban tárolják.
Az utolsó parancs a **Get-AzBatch Job** használatával a 000001 azonosítójú kötegfeladatot kapja meg.
Ezután a parancs a folyamat műveleti operátorával átadja a feladatot az aktuális parancsmagnak.
A parancs a feladat alatt felvesz egy feladatgyűjteményt.
A parancs a helyi menüben tárolt $Context.

### 4. példa: Tevékenységek gyűjteményének hozzáadása a megadott feladathoz
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

Az első parancs létrehoz egy objektumhivatkozást a ContosoBatchAccount nevű kötegfiók fiókkulcsára a **Get-AzBatchAccountKey paranccsal.**
A parancs ezt az objektumhivatkozást a $Context tárolja.
A következő két parancs **PSCloudTask-objektumokat** hoz létre a New-Object parancsmag használatával.
A parancsok a feladatokat a $Task 01 és $Task 02 változókban tárolják.
Az utolsó parancs hozzáadja a $Task 01-ben és a $Task 02-ben a 000001 azonosítójú feladat alatt tárolt feladatokat.

### 5. példa: Feladat hozzáadása kimeneti fájlokkal
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### 6. példa: Feladat hozzáadása hitelesítési jogkivonat-beállításokkal
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### 7. példa: Tárolóban futó feladat hozzáadása
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## PARAMETERS

### -AffinityInformation
Meghatároz egy tippet a helyi beállításról, amellyel a Batch szolgáltatás kiválaszt egy csomópontot, amelyen futtatni kell a feladatot.

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

### -ApplicationPackageReferences
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

### -AuthenticationTokenSettings
A hitelesítési jogkivonat beállításai, amelyek alapján a feladat kötegszolgáltatás-műveleteket hajthat végre.
Ha ez a beállítás meg van állítva, a Batch szolgáltatás egy hitelesítési jogkivonatot biztosít a feladatnak, amely a batch szolgáltatásműveletek hitelesítéséhez használható fiókelérési kulcs nélkül. A tokent a AZ_BATCH_AUTHENTICATION_TOKEN környezeti változón keresztül lehet biztosítani. A token használatával a feladat által végrehajtott műveletek a beállításoktól függnek. Egy tevékenység például engedélyt kérhet a feladathoz, hogy más tevékenységeket is felvessen a feladatba, illetve hogy ellenőrizze a feladat vagy más tevékenységek állapotát.

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

### -BatchContext
Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.
Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer. Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal. Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja. A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.

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

### -CommandLine
A feladat parancssorát határozza meg.

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

### -Constraints
A tevékenységre vonatkozó végrehajtási kényszerek megadása.

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

### -ContainerSettings
Annak a tárolónak a beállításai, amely alatt a feladat fut.
Ha a feladatot futtató készlethez containerConfiguration beállítás van beállítva, ezt is be kell állítani. Ha a feladatot futtató készletben nincs containerConfiguration beállítva, ezt nem kell beállítani. Ha ez meg van adva, az AZ_BATCH_NODE_ROOT_DIR alatti összes könyvtár (a csomópont Azure Batch-könyvtárának gyökérkönyvtára) megfeleltetve lesz a tárolónak, a feladatkörnyezet összes változója megfeleltetve lesz a tárolónak, és a feladat parancssorát végrehajtja a rendszer a tárolóban.

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

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -DependsOn
Azt adja meg, hogy a tevékenység más tevékenységektől függ.
A tevékenység mindaddig nem lesz ütemezve, amíg az összes függő tevékenység sikeresen be nem fejeződött.

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

### -DisplayName
A tevékenység megjelenítendő nevét adja meg.

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

### -EnvironmentSettings
Ez a parancsmag által a feladathoz hozzáadott környezeti beállításokat adja meg kulcs-érték párokként.
A kulcs a környezet beállításának neve.
Az érték a környezet beállítása.

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

### -ExitConditions
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

### -Id
A tevékenység azonosítóját adja meg.

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

### -Job
Azt a feladatot adja meg, amely alatt ez a parancsmag létrehozza a feladatot.
**PSCloudFeladat-objektum** beszerzéséhez használja a Get-AzBatchJob parancsmagot.

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

### -JobId
Annak a feladatnak az azonosítója, amely alatt ez a parancsmag létrehozza a feladatot.

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

### -MultiInstanceSettings
A többpéldányos feladatok futtatásával kapcsolatos információkat adja meg.

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

### -OutputFile
Beállítja vagy beállítja a batch szolgáltatás által a számítási csomópontról a parancssor futtatása után feltöltandó fájlok listáját.
Többpéldányos feladatok esetén a fájlok csak abból a számítási csomópontból lesznek feltöltve, amelyen az elsődleges feladat végrehajtása történik.

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

### -ResourceFiles
Megadja a tevékenységhez szükséges erőforrásfájlokat kulcs-/értékpárokként.
A kulcs az erőforrásfájl elérési útja.
Az érték az erőforrásfájl blobforrása.

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

### -Feladatok
A hozzáadható feladatok gyűjteményét adja meg.
Minden tevékenységhez egyedi azonosítónak kell lennie.

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

### -UserIdentity
Az a felhasználói identitás, amely alatt a feladat fut.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Bat. Models.PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### System.Void

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchUpp](./Get-AzBatchJob.md)

[Get-AzBatchTask](./Get-AzBatchTask.md)

[New-AzBatchTask](./New-AzBatchTask.md)

[Remove-AzBatchTask](./Remove-AzBatchTask.md)

[Stop-AzBatchTask](./Stop-AzBatchTask.md)

[Azure Batch-parancsmagok](/powershell/module/Az.Batch/)
