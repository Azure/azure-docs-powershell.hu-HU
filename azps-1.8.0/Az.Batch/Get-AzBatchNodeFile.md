---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: 3337cfa2423d6bc3a26c96ea734ce517f2707a04
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671879"
---
# Get-AzBatchNodeFile

## Áttekintés
A kötegfájl-fájlok tulajdonságainak lekérdezése.

## SZINTAXISA

### ComputeNode_Id (alapértelmezett)
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_Id
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_ODataFilter
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentTask
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_ODataFilter
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ParentComputeNode
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzBatchNodeFile** parancsmag a tevékenység vagy a számítási csomópont Azure batch csomópont-fájljainak tulajdonságait kapja meg.
Ha szűkíteni szeretné az eredményeket, megadhat egy Open Data Protocol (OData) szűrőt.
Ha olyan tevékenységet ad meg, amely nem szűrő, akkor ez a parancsmag a tevékenységhez tartozó összes csomópont-fájl tulajdonságait adja eredményül.
Ha olyan számítási csomópontot ad meg, amely nem szűrő, akkor ez a parancsmag a számítási csomópont összes csomópont-fájljának tulajdonságait adja eredményül.

## Példák

### Példa 1: a tevékenységhez társított csomópont-fájl tulajdonságainak beolvasása
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

Ez a parancs beolvassa a tevékenységhez társított StdOut.txt csomópont-fájl tulajdonságait, amely a Task26 azonosítóval rendelkezik – 000001.
A Get-AzBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.

### 2. példa: a tevékenységhez társított csomópont-fájlok tulajdonságainak lekérdezése szűrő használatával
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

Ez a parancs beolvassa a St-val kezdődő csomópontok tulajdonságait, és társítva van egy olyan feladathoz, amely a Task26-00002 azonosítójú projekthez tartozik.

### 3. példa: egy tevékenységhez társított csomópont-fájlok tulajdonságainak rekurzív beolvasása
```
PS C:\>Get-AzBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

Ez a parancs beolvassa a tevékenységhez társított összes fájl tulajdonságait a Job Job-00003 AZONOSÍTÓJÚ Task31.
Ez a parancs a *rekurzív* paramétert adja meg.
A parancsmag ezért végrehajt egy rekurzív fájlok keresését, és a wd\newFile.txt csomópontot adja eredményül.

### Példa 4: egyetlen fájl beszerzése egy számítási csomópontból
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

Ez a parancs beilleszti az Startup\StdOut.txt nevű fájlt a számítási csomópontról, amelynek azonosító ComputeNode01 az azonosító Pool22 tartalmazó készletben.

### 5. példa: a mappa alatti fájlok beolvasása egy számítási csomópontból
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

Ez a parancs beilleszti az indítási mappa alatti összes fájlt a számítási csomópontból, amely az id-Pool22 tartalmazó készlet ComputeNode01 rendelkezik.
Ez a parancsmag a *rekurzív* paramétert adja meg.

### 6. példa: fájlok beolvasása a számítási csomópont gyökérkönyvtárába
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

Ez a parancs beolvassa a számítási csomópont gyökerének minden fájlját, amely az id-Pool22 tartalmazó készlet ComputeNode01 rendelkezik.

## PARAMÉTEREK

### -BatchContext
Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.
Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni. Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével. A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos. A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.

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

### -ComputeNode
A **PSComputeNode** -objektum számítási csomópontját adja meg, amely a köteg csomópont-fájlokat tartalmazza.
A számítási csomópont objektum beolvasásához használja az Get-AzBatchComputeNode parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentComputeNode
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amely a köteg csomópont-fájlokat tartalmazza.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Szűrő
Egy OData-szűrő záradékot ad meg.
Ez a parancsmag azokat a csomópont-fájlokat adja meg, amelyek megfelelnek a paraméter által megadott szűrőnek.

```yaml
Type: System.String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Annak a feladatnak az AZONOSÍTÓját adja meg, amely a célként megadott feladatot tartalmazza.

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
Annak a csomópontnak a maximális számát adja meg, amelyre a parancsmag tulajdonságot ad.
Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.
Az alapértelmezett érték a 1000.

```yaml
Type: System.Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path (elérési út)
Annak a csomópontnak az elérési útját adja meg, amelynek a parancsmagja a tulajdonságokat lekérdezi.
A helyettesítő karakterek nem adhatók meg.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Annak a készletnek az AZONOSÍTÓját adja meg, amely a csomópont-fájlok tulajdonságainak beolvasására szolgáló számítási csomópontot tartalmazza.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Rekurzív
Azt jelzi, hogy ez a parancsmag a fájlok rekurzív listáját adja eredményül.
Ellenkező esetben csak a gyökérmappa fájljait számítja ki.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tevékenység
Azt a feladatot adja meg **PSCloudTask** objektumként, amellyel a csomópontok fájljait társította.
Tevékenység-objektum beolvasásához használja az Get-AzBatchTask parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentTask
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskId
Annak a tevékenységnek az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag a csomópont-fájlok tulajdonságait kapja.

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask

### Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### Microsoft.Azure.Commands.BatCH. Modellek. PSNodeFile

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzBatchAccountKeys](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Get-AzBatchNodeFileContent](./Get-AzBatchNodeFileContent.md)

[Get-AzBatchTask](./Get-AzBatchTask.md)

[Azure-köteg parancsmagok](/powershell/module/az.batch)


