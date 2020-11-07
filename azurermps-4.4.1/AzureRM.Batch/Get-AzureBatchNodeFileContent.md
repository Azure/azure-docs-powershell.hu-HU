---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 92c485a743372eff7ddb8725172ac4d9bb030d22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679795"
---
# Get-AzureBatchNodeFileContent

## Áttekintés
Beolvassa a köteg-csomópontot tartalmazó fájlt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Task_Id_Path
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_Id_Stream
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Path
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Stream
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureBatchNodeFileContent** parancsmag egy Azure batch csomópontot tartalmazó fájlt kap, és fájlként vagy adatfolyamként menti.

## Példák

### Példa 1: egy tevékenységhez társított köteg-csomópont beszerzése és a fájl mentése
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Name "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Ez a parancs beilleszti a StdOut.txt nevű csomópontot, és a helyi számítógép E:\PowerShell\StdOut.txt elérési útjára menti a fájlt.
A StdOut.txt csomópont-fájl társítva van egy olyan tevékenységhez, amelynek azonosító Task01 az azonosító Job01 tartalmazó projekthez tartozik.
A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.

### 2. példa: kötegfájl-fájl beszerzése és mentése a megadott fájlelérési útra a csővezeték használatával
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Name "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Ez a parancs a Get-AzureBatchNodeFile parancsmaggal StdErr.txt nevű csomópontot kapja meg.
A parancs átadja a fájlt az aktuális parancsmagnak a pipeline operátor használatával.
Az aktuális parancsmag a fájlt a helyi számítógép E:\PowerShell\StdOut.txt fájlelérési útjára menti.
A StdOut.txt csomópont-fájl társítva van azzal a tevékenységgel, amelynek azonosító Task02 az azonosító Job02 tartalmazó projekthez tartozik.

### 3. példa: egy tevékenységhez társított köteg-csomópont beszerzése és az adatfolyamhoz irányítása
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Name "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

Az első parancs az New-Object parancsmag segítségével hoz létre adatfolyamot, és a $Stream változóban tárolja.

A második parancs beolvassa az StdOut.txt nevű csomópontot az azonosítót tartalmazó Task11 az azonosító Job03 tartalmazó feladathoz.
A parancs a fájl tartalmát az adatfolyamra irányítja a $Streamban.

### Példa 4: node-fájl beszerzése egy számítási csomópontról és mentése
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Ez a parancs a csomópontot Startup\StdOut.txt a számítási csomópontról, amelynek azonosító ComputeNode01 az azonosító Pool01 tartalmazó készletben.
A parancs a fájlt a helyi számítógép E:\PowerShell\StdOut.txt fájlelérési útjára menti.

### Példa 5: csomópont kinyerése a számítási csomópontból, és mentése a csővezeték használatával
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Ez a parancs a csomópont-fájlt Startup\StdOut.txt Get-AzureBatchNodeFile segítségével az ID ComputeNode01 tartalmazó számítási csomópontból.
A számítási csomópont abban a készletben található, amely az azonosító Pool01 tartalmazza.
A parancs átadja ezt a csomópont-fájlt az aktuális parancsmagnak.
Ez a parancsmag a fájlt a helyi számítógép E:\PowerShell\StdOut.txt fájlelérési útjára menti.

### Példa 6: a csomópontok kinyerése a számítási csomópontból és az adatfolyamhoz való közvetlen átvétele
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

Az első parancs az New-Object parancsmag segítségével hoz létre adatfolyamot, és a $Stream változóban tárolja.

A második parancs beolvassa az StdOut.txt nevű csomópontot a számítási csomópontról, amelynek azonosító ComputeNode01 az azonosító Pool01 tartalmazó készletben.
A parancs a fájl tartalmát az adatfolyamra irányítja a $Streamban.

## PARAMÉTEREK

### -BatchContext
Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.
Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.

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

### -ByteRangeEnd
A letöltendő bájtok hatókörének vége.
```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ByteRangeStart
A letöltendő bájtok hatókörének kezdete.
```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeNodeId
Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amely a parancsmag által megadott csomópont-fájlt tartalmazza.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DestinationPath
Annak a fájlnak az elérési útját adja meg, ahol ez a parancsmag menti a csomópontot.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
Azt a adatfolyamot adja meg, amelybe ez a parancsmag a csomópont-fájl tartalmát írja be.
Ez a parancsmag nem zárja be vagy hagyja vissza az adatfolyamot.

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Azt a fájlt adja meg, amelyet a parancsmag **PSNodeFile** objektumként kap.
A Node file objektum beolvasásához használja az Get-AzureBatchNodeFile parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Annak a feladatnak az AZONOSÍTÓját adja meg, amely a célként megadott feladatot tartalmazza.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Annak a csomópontnak a nevét adja meg, amelyre a parancsmag bekéri.
A helyettesítő karakterek nem adhatók meg.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Annak a készletnek az AZONOSÍTÓját adja meg, amely a parancsmagot tartalmazó csomópontot tartalmazó csomópontot tartalmazza.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TaskId
A tevékenység AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### BatchAccountContext
A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről

### PSNodeFile
A ' InputObject ' paraméter az "PSNodeFile" típusú értéket fogadja el a csővezetékről

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchNodeFile](./Get-AzureBatchNodeFile.md)

[Azure-köteg parancsmagok](./AzureRM.Batch.md)


