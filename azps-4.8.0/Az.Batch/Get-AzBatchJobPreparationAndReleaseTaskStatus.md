---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024909"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## Áttekintés
Beolvassa a kötegelt feldolgozást, és felszabadítja a tevékenység állapotát.

## SZINTAXISA

### Azonosító (alapértelmezett)
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzBatchJobPreparationAndReleaseTaskStatus** parancsmag az Azure kötegelt feladat-előkészítési és kiadási tevékenység állapotát kapja meg egy kötegelt feldolgozáshoz.
Ebben a parancsmagban meg kell adnia az *azonosító* paramétert vagy egy **PSCloudJob** -példányt.

## Példák

### Példa 1: a projekt felkészítési és kiadási állapotának beszerzése
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Ez a parancs beilleszti a feladat-előkészítési és kiadási tevékenység állapotát a "teszt" állásba.
A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.

### 2. példa: a projekt előkészítési és kiadási állapotának beszerzése szűrővel, majd a megadott elem választása
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Ez a parancs beolvassa a feladat-előkészítési és kiadási tevékenység állapotát a "TVM-2316545714_1-20170613t201733z" ("teszt") csomóponton, és a Select záradékot használja az JobPreparationTaskExecutionInformation adatok visszaadására.

## PARAMÉTEREK

### -BatchContext
A kötegelt szolgáltatással való interakció során használandó BatchAccountContext-példány.
A Get-AzBatchAccountKey parancsmag segítségével BatchAccountContext-objektumot kaphat a hozzá tartozó elérési kulcsokkal.

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

### – Kibontás
Az Open Data Protocol (OData) kibontási záradékát adja meg.
Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz tartozó társított entitások beszerzéséhez.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Szűrő
Egy OData-szűrő záradékot ad meg.
Ha nem ad meg szűrőt, ez a parancsmag visszaadja a projekthez tartozó összes feladat-előkészítési és kiadási tevékenység állapotát.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
Annak a feladatnak az AZONOSÍTÓját adja meg, amelynek az előkészítési és kiadási feladatait le kell olvasni.
A helyettesítő karakterek nem adhatók meg.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Itt adhatja meg azt a **PSCloudJob** -objektumot, amely a feladatra vonatkozó előkészítő és kiadási tevékenység állapotát reprezentálja.
**PSCloudJob** objektum beolvasásához használja az Get-AzBatchJob parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
Megadja, hogy a program a munkafolyamatok elkészítési és kiadási tevékenységének maximális számát adja vissza.
Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.
Az alapértelmezett érték a 1000.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Válassza a
Egy OData Select záradékot ad meg.
Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### Microsoft.Azure.Commands.BatCH. Modellek. PSJobPreparationAndReleaseTaskExecutionInformation

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Azure-köteg parancsmagok](/powershell/module/Az.Batch/)
