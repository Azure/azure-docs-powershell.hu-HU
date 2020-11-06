---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: bc60bbb5b48c4022e7db6a95e26a1f43ef891ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505087"
---
# Get-AzureRmDataFactoryV2Trigger

## Áttekintés
Információt kap az eseményindítókkal kapcsolatban az adatgyárban.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### ByFactoryObject
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## Leírás
A **Get-AzureRmDataFactoryV2Trigger** parancsmag információkat kap az adatgyárban lévő eseményindítókkal kapcsolatban. Ha megad egy trigger nevét, a parancsmag információt kap az adott triggerről. Ha nem ad meg nevet, a parancsmag információkat kap az adatfeldolgozó összes eseményindítóról.


## Példák

### 1. példa: információ kérése egy adott triggerről
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

A "WikiADF" Data Factory "az adatfeldolgozóban" létrehozott összes eseményindító listáját kapja meg.

### 2. példa: információk kérése az összes eseményindítóról

```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

A "WikiADF" Data Factory "ScheduledTrigger" nevű egyetlen triggert kap.

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

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## BEMENETEK

### System. String
Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory


## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]
Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
[Set-AzureRmDataFactoryV2Trigger]()

[Start-AzureRmDataFactoryV2Trigger]()

[Stop-AzureRmDataFactoryV2Trigger]()

[Remove-AzureRmDataFactoryV2Trigger]()
