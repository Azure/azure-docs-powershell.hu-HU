---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: 904c3a40f8f153a97bf8016f3708a310adfea3bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679896"
---
# New-AzureBatchTask

## Áttekintés
Kötegelt feladatot hoz létre a projektben.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### JobId_Single (alapértelmezett)
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobId_Bulk
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Bulk
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Single
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureBatchTask** parancsmag egy Azure-köteg feladatot hoz létre a *JobId* paraméterben vagy a *Job* paraméterben megadott munkához.

## Példák

### 1. példa: köteg-tevékenység létrehozása
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

Ez a parancs létrehoz egy feladatot, amely a Task23 AZONOSÍTÓval rendelkezik a 000001 azonosítójú projektben.
A tevékenység futtatja a megadott parancsot.
A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.

### 2. példa: köteg-tevékenység létrehozása
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

Ez a parancs a **Get-AzureBatchJob** parancsmaggal kapja meg a 000001 azonosítójú kötegelt feladatot.
A parancs a munkafolyamatot a csővezeték-kezelő használatával továbbítja az aktuális parancsmaghoz.
A parancs létrehoz egy feladatot, amely az azonosító Task26 tartalmazza az adott feladatban.
A feladat a megadott parancsot a magasabb szintű engedélyek használatával futtatja.

### 3. példa: tevékenység-gyűjtemény felvétele a megadott feladatba a csővezeték használatával
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

Az első parancs a **Get-AzureRmBatchAccountKeys** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.
A parancs a $Context változóban tárolja az objektum hivatkozását.

A következő két parancs **PSCloudTask** -objektumokat hoz létre a New-Object parancsmag használatával.
A parancsok a $Task 01 és $Task 02 változóban található feladatokat tárolják.

A végleges parancs a **Get-AzureBatchJob** segítségével a 000001 azonosítójú kötegelt feladatot kapja.
Ezután a parancs átadja ezt a feladatot az aktuális parancsmagnak a pipeline operátorral.
A parancs felveszi a feladatok gyűjteményét az adott feladatba.
A parancs a $Contextban tárolt környezetet használja.

### 4. példa: tevékenység-gyűjtemény felvétele a megadott feladatba
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

Az első parancs a **Get-AzureRmBatchAccountKeys** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.
A parancs a $Context változóban tárolja az objektum hivatkozását.

A következő két parancs **PSCloudTask** -objektumokat hoz létre a New-Object parancsmag használatával.
A parancsok a $Task 01 és $Task 02 változóban található feladatokat tárolják.

A végleges parancs felveszi a $Task 01-ben tárolt feladatokat, és a "000001" AZONOSÍTÓJÚ munkahelyhez $Task a 02-et.

### Példa 5: tevékenység hozzáadása kimeneti fájlokkal
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### 6. példa: tevékenység hozzáadása a hitelesítési jogkivonat beállításaival
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### 7. példa: egy tárolóban futó tevékenység felvétele
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## PARAMÉTEREK

### -AffinityInformation
Itt adhatja meg azt a területi célzást, amellyel a kötegelt szolgáltatás kijelöli a feladatot futtató csomópontot.

```yaml
Type: PSAffinityInformation
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
Type: PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationTokenSettings
A kötegelt szolgáltatási műveletek elvégzéséhez használható hitelesítő jogkivonat beállításai.

Ha be van állítva ez a beállítás, a köteg szolgáltatás olyan hitelesítési jogkivonattal látja el a feladatot, amely a kötegelt szolgáltatás műveleteinek hitelesítéséhez használható a fiók-hozzáférési kulcs megkövetelése nélkül. A token a AZ_BATCH_AUTHENTICATION_TOKEN környezeti változón keresztül érhető el. A tevékenység által a jogkivonattal végezhető műveletek a beállításoktól függnek. A feladatok például kérhetik a feladatok megadását az egyéb feladatok hozzáadásához, illetve a feladat vagy más feladatok állapotát.

```yaml
Type: PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BatchContext
Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.
Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni. Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével. A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos. A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.

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

### -CommandLine
A tevékenységhez tartozó parancssort adja meg.

```yaml
Type: String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kényszerek
A feladatra vonatkozó végrehajtási kényszert adja meg.

```yaml
Type: PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerSettings
Annak a tárolónak a beállításai, amely alatt a tevékenység fut.

Ha a feladatot futtató készlet containerConfiguration van beállítva, akkor ezt is be kell állítania. Ha a feladatot futtató készlet nem rendelkezik containerConfiguration beállítással, akkor ez a beállítás nem állítható be. Ha ez az érték van megadva, az összes olyan könyvtár, amelyet a AZ_BATCH_NODE_ROOT_DIR (az Azure-kötegek gyökerét tartalmazó kötegek gyökerében) a tárolóhoz rendelt, a tárolóhoz társít minden környezeti változót, és a program végrehajtja a feladat parancssorát a tárolóban.

```yaml
Type: PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -DependsOn
Azt adja meg, hogy a tevékenység más tevékenységtől függ.
A tevékenység addig nem lesz ütemezve, amíg az összes függő tevékenység sikeresen el nem fejeződött.

```yaml
Type: TaskDependencies
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
Type: String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentSettings
A környezeti beállításokat adja meg kulcs/érték párokként, hogy a parancsmag hozzáadja a tevékenységhez.
A kulcs a környezet beállításának neve.
Az érték a környezet beállítása.

```yaml
Type: IDictionary
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
Type: PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
A tevékenység AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Azt a feladatot adja meg, amely alatt a parancsmag létrehozta a feladatot.
**PSCloudJob** objektum beolvasásához használja az Get-AzureBatchJob parancsmagot.

```yaml
Type: PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Annak a feladatnak az AZONOSÍTÓját adja meg, amely alatt a parancsmag létrehozta a feladatot.

```yaml
Type: String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MultiInstanceSettings
Itt adhatja meg, hogy miként futtathat több példányos tevékenységet.

```yaml
Type: PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
A parancssor futtatása után megkezdi vagy beállítja a kötegelt szolgáltatás által a számítási csomópontról feltöltendő fájlok listáját.

A többpéldányos feladatok esetében a fájlok csak arra a számítási csomópontra lesznek feltöltve, amelyen az elsődleges feladat van végrehajtva.

```yaml
Type: PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceFiles
A tevékenységhez szükséges erőforrás-fájlokat (kulcs/érték párokként) adja meg.
A kulcs az erőforrás fájlelérési útja.
Az érték az erőforrás fájl blob-forrása.

```yaml
Type: IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Feladatok
A felvenni kívánt feladatok gyűjteményét adja meg.
Minden tevékenységhez egyedi AZONOSÍTÓval kell rendelkeznie.

```yaml
Type: PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserIdentity
A tevékenység által futtatott felhasználó identitása.

```yaml
Type: PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### BatchAccountContext
A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről

### PSCloudJob
A ' Job ' paraméter elfogadja a "PSCloudJob" típusú értéket a csővezetékről

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Get-AzureBatchTask](./Get-AzureBatchTask.md)

[Új – AzureBatchTask](./New-AzureBatchTask.md)

[Remove-AzureBatchTask](./Remove-AzureBatchTask.md)

[Stop-AzureBatchTask](./Stop-AzureBatchTask.md)

[Azure-köteg parancsmagok](./AzureRM.Batch.md)


