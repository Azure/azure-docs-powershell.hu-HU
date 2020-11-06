---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 6042b62bb7c641cef335834645f29d73b3d4c53a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505092"
---
# Get-AzureRmDataFactoryV2PipelineRun

## Áttekintés
Információt kap a csővezetékről.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryNameByRunId (alapértelmezett)
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String>
```

### ByFactoryObjectByRunId
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
```

### ByFactoryObjectByPipeline
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

### ByFactoryNameByPipeline
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

## Leírás
A **Get-AzureRmDataFactoryV2PipelineRun** parancs a megadott csővezetéken futó futásokra vonatkozó információkat adja eredményül. Ha a PipelineRunId meg van adva, az adott AZONOSÍTÓval végzett Futtatás részleteit jeleníti meg. Ha a PipelineRunId nem adja meg, akkor az a LastUpdatedAfter és a LastUpdatedBefore értékek között megjelenő adott csővezetékre vonatkozó információkat jeleníti meg.

## Példák

### 1. példa: pipline-futtatási adatok beszerzése
```
PS C:\> Get-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :

```

Ez a parancs részletesen ismerteti az "61eb095a-FE23-4591-8a97-fade6c65ca72" AZONOSÍTÓJÚ pipeline-kapcsolat adatait.


## PARAMÉTEREK

### -DataFactory
Az Data Factory objektum.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
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
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LastUpdatedAfter
Az az időpont, amikor a csővezeték-futtatást ISO8601 formátumban frissítették.

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LastUpdatedBefore
Az az időpont, amikor a csővezeték futását ISO8601 formátumban frissítették.

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PipelineName
A csővezeték neve.

```yaml
Type: String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineRunId
A csővezeték Run azonosítója.

```yaml
Type: String
Parameter Sets: ByFactoryObjectByRunId, ByFactoryNameByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforrás csoport neve.

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## BEMENETEK

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
System. String


## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSPipelineRun, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]
Microsoft. Azure. Command. DataFactoryV2. models. PSPipelineRun


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
[Meghívó-AzureRmDataFactoryV2Pipeline]()

[Get-AzureRmDataFactoryV2ActivityRun]()

