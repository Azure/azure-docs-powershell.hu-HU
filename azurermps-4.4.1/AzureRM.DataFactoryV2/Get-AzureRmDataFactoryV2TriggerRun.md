---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: d5ea2dee1f6023b9505c38a58d364b7aa92591db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679785"
---
# Get-AzureRmDataFactoryV2TriggerRun

## Áttekintés
Információt ad az indításról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### ByFactoryObject
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
```

## Leírás
A **Get-AzureRmDataFactoryV2TriggerRun** parancs részletes információt ad az adott időkeretben megadott triggerről.

## Példák

### 1. példa: a trigger Run-ról szóló információk beszerzése
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded

```

Ez a parancs a "2017-09-01" és a "2019-09-30" között megjelenő "WikiADF" gyári "WikiTrigger"-ra vonatkozó információkat jeleníti meg.

## PARAMÉTEREK

### -DataFactory
Az Data Factory objektum.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DataFactoryName
Az adatgyári név.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Az indító neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforrás csoport neve.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TriggerRunStartedAfter
Az az időpont, amikor az indító futtatása ISO8601 formátumban kezdődik.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TriggerRunStartedBefore
Az a dátum, amelyen vagy amely előtt a trigger futása ISO8601 formátumban lett végrehajtva.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## BEMENETEK

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
System. String


## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSTriggerRun, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]
Microsoft. Azure. Command. DataFactoryV2. models. PSTriggerRun


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
[Start-AzureRmDataFactoryV2Trigger]()

[Stop-AzureRmDataFactoryV2Trigger]()

