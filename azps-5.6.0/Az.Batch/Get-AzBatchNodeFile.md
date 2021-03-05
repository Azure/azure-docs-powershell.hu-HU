---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: 0169748ffc6fa2004fe8b0ade542d288677776b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007366"
---
# Get-AzBatchNodeFile

## SYNOPSIS
A Batch-csomópontfájlok tulajdonságait kapja meg.

## SZINTAXIS

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

## LEÍRÁS
A **Get-AzBatchNodeFile** parancsmag begyűjte egy feladat vagy számítási csomópont Azure Batch-csomópontfájljának tulajdonságait.
Az eredmények szűkítéséhez OData-szűrőt is megadhat.
Ha egy feladatot ad meg, szűrőt azonban nem, ez a parancsmag az adott feladat összes csomópontfájljának tulajdonságait adja vissza.
Ha egy számítási csomópontot ad meg, szűrőt azonban nem, ez a parancsmag az adott számítási csomópont összes csomópontfájljának tulajdonságait adja vissza.

## PÉLDÁK

### 1. példa: A feladathoz társított csomópontfájl tulajdonságainak lekérte
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

Ez a parancs annak a StdOut.txt csomópontfájlnak a tulajdonságait kapja meg, amely a Feladat26 azonosítót tartalmazza a 000001 azonosítójú feladatban.
A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.

### 2. példa: A feladathoz társított csomópontfájlok tulajdonságainak lekérte egy szűrő használatával
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

Ez a parancs azoknak a csomópontfájloknak a tulajdonságait kapja meg, amelyeknek a neve st-sel kezdődik, és olyan feladathoz van társítva, amelynek feladatazonosítója Feladat26 azonosítót tartalmaz 00002-es azonosítójú feladat alatt.

### 3. példa: A feladathoz társított csomópontfájlok tulajdonságainak rekurzív be szerezze
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

Ez a parancs a Feladat 00003-as feladatban lévő Feladat31 azonosítóval társított feladathoz társított összes fájl tulajdonságait beveszi.
Ez a parancs a *rekurzív paramétert adja* meg.
Ezért a parancsmag rekurzív fájlkeresést hajt végre, és visszaadja a wd\newFile.txt csomópontfájlt.

### 4. példa: Egyetlen fájl lekérte egy számítási csomópontból
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

Ez a parancs a Startup\StdOut.txt az id ComputeNode01 azonosítóval rendelkezik a készletben, amely az azonosítókészletet22 tartalmazza, a számítási csomópontból kapja meg a Startup\StdOut.txt nevű fájlt.

### 5. példa: Az összes fájl bekérte egy mappa alá egy számítási csomópontból
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

Ez a parancs az indítómappa alatt található összes fájlt abból a számítási csomópontból kapja meg, amelynél a ComputeNode01 azonosító található az azonosítókészletet tartalmazó készletben22.
Ez a parancsmag megadja a *rekurzív* paramétert.

### 6. példa: Fájlok letöltése egy számítási csomópont gyökérmappába
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso...
True        startup                         https://cmdletexample.westus.Batch.contoso...
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

Ez a parancs annak a számítási csomópontnak a gyökérmappában lévő összes fájlt begyakorlja, amelynél a ComputeNode01 azonosító található az azonosítókészletet tartalmazó készletben22.

## PARAMETERS

### -BatchContext
Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.
Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer. Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal. Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja. A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.

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
A Batch csomópontfájlokat tartalmazó számítási csomópontOT adja meg **PSComputeNode-objektumként.**
Számítási csomópontobjektum beszerzéséhez használja a Get-AzBatchComputeNode parancsmagot.

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
A Batch csomópontfájlokat tartalmazó számítási csomópont azonosítója.

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

### -Filter
OData-szűrő záradékot ad meg.
Ez a parancsmag a paraméterben megadott szűrőnek megfelelő csomópontfájlok tulajdonságait adja eredményül.

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
A cél tevékenységet tartalmazó feladat azonosítója.

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
Azt adja meg, hogy legfeljebb hány csomópontfájlt ad vissza a parancsmag.
Ha nullát (0) vagy kisebb értéket ad meg, a parancsmag nem használ felső korlátot.
Az alapértelmezett érték 1000.

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

### -Path
Annak a csomópontfájlnak az elérési útját adja meg, amelynek tulajdonságait a parancsmag beolvassa.
Helyettesítő karakterek nem adhatók meg.

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
Annak a készletnek az azonosítóját adja meg, amely azt a számítási csomópontot tartalmazza, amelyből a csomópontfájlok tulajdonságait meg szeretné kapni.

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
Azt jelzi, hogy ez a parancsmag egy rekurzív fájllistát ad vissza.
Ellenkező esetben csak a gyökérmappában lévő fájlokat adja vissza.

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

### -Task
Azt a feladatot adja meg **PSCloudTask-objektumként,** amellyel a csomópontfájlok társítva vannak.
Feladatobjektum beszerzéséhez használja a Get-AzBatchTask parancsmagot.

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
Annak a feladatnak az azonosítója, amelynek a parancsmagja a csomópontfájlok tulajdonságait kapja.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Bat. Models.PSCloudTask

### Microsoft.Azure.Commands.Bat. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### Microsoft.Azure.Commands.Bat. Models.PSNodeFile

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Get-AzBatchNodeFileContent](./Get-AzBatchNodeFileContent.md)

[Get-AzBatchTask](./Get-AzBatchTask.md)

[Azure Batch-parancsmagok](/powershell/module/Az.Batch/)
