---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 5f24e55042a8be7f36b1a9946c4bd5b87209a0f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502619"
---
# Get-AzureBatchJobPreparationAndReleaseTaskStatus

## Áttekintés
Beolvassa a kötegelt feldolgozást, és felszabadítja a tevékenység állapotát.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Azonosító (alapértelmezett)
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureBatchJobPreparationAndReleaseTaskStatus** parancsmag az Azure kötegelt feladat-előkészítési és kiadási tevékenység állapotát kapja meg egy kötegelt feldolgozáshoz.
Ebben a parancsmagban meg kell adnia az *azonosító* paramétert vagy egy **PSCloudJob** -példányt.

## Példák

### Példa 1: a projekt felkészítési és kiadási állapotának beszerzése
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Ez a parancs beilleszti a feladat-előkészítési és kiadási tevékenység állapotát a "teszt" állásba.
A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.

### 2. példa: a projekt előkészítési és kiadási állapotának beszerzése szűrővel, majd a megadott elem választása
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

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
A Get-AzureRmBatchAccountKeys parancsmag segítségével BatchAccountContext-objektumot kaphat a hozzá tartozó elérési kulcsokkal.

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

### – Kibontás
Az Open Data Protocol (OData) kibontási záradékát adja meg.
Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz tartozó társított entitások beszerzéséhez.

```yaml
Type: String
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
Type: String
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
Type: String
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
**PSCloudJob** objektum beolvasásához használja az Get-AzureBatchJob parancsmagot.

```yaml
Type: PSCloudJob
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
Type: Int32
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
Type: String
Parameter Sets: (All)
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

### System. String
Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### Microsoft.Azure.Commands.BatCH. Modellek. PSJobPreparationAndReleaseTaskExecutionInformation

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Azure-köteg parancsmagok](./AzureRM.Batch.md)
