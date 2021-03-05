---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: 294669fe5b9e5aeb01dfbfa7ab538a0f6d411cca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014006"
---
# Get-AzBatchTaskCount

## SYNOPSIS
A megadott feladathoz a tevékenységek számát adja meg.

## SZINTAXIS

### Azonosító
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzBatchTaskCount** parancsmag begyűjte az Azure Batch-feladatok számát egy kötegfeladathoz.
Adjon meg egy feladatot a *JobId vagy* a *Job paraméter* alapján.
A tevékenységszámok az aktív, futó vagy befejezett tevékenységállapotok, valamint a sikeres vagy sikertelen tevékenységek számát jelentik. Az előkészítési állapotban a feladatok futásnak számítanak. Ha az validationStatus nincs érvényesítés nélkül, akkor a Batch szolgáltatás nem tudta ellenőrizni, hogy az állapotok a Feladatlista API-ban jelentett feladatállapotokkal vannak-e ellenőrizve. Ha a feladat több mint 200 000 feladatot tartalmaz, előfordulhat, hogy az érvényesítésiStatus nem érvényes.

## PÉLDÁK

### 1. példa: Tevékenységszámok lekérte azonosító szerint
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Ez a parancs a Feladat01 feladathoz megszámolandó tevékenységeket kapja meg.
A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.

## PARAMETERS

### -BatchContext
A Batch-szolgáltatáshoz használt BatchAccountContext példány.
Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.
Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.
Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.
A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.

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

### -Job
Azt a feladatot adja meg, amely a parancsmag által lekért feladatokat tartalmazza.
**PSCloudFeladat-objektum** beszerzéséhez használja a Get-AzBatchJob parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Annak a feladatnak az azonosítója, amelynek a tevékenységszámát le kell számítani.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Bat. Models.PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### Microsoft.Azure.Commands.Bat. Models.PSTaskCounts

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchUpp](./Get-AzBatchJob.md)

[Azure Batch-parancsmagok](/powershell/module/Az.Batch/)
