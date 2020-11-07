---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 2f08d81820ab28688b645ef3ec6a8f519985585c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671161"
---
# Get-AzDataFactoryPipeline

## Áttekintés
Információt kap a csővezetékekről az Azure Data Factory-ban.

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzDataFactoryPipeline** parancsmag információkat kap az Azure Data Factory csővezetékekről.
Ha megad egy csővezeték nevét, ez a parancsmag információkat kap a csővezetékről.
Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes csővezetékről.

## Példák

### 1. példa: adatok beolvasása az összes csővezetékről
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

Ez a parancs információkat kap az WikiADF nevű adatfeldolgozóban található összes csővezetékről.
Az alábbi parancsok közül választhat.
A második egy **DataFactory** -objektumot használ paraméterként.

### 2. példa: információk kérése egy adott csővezetékről
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

Ez a parancs információt kap a DPWikisample nevű csővezetékről az WikiADF nevű adatgyárban.
A parancs a pipeline operátorral továbbítja ezeket az információkat az Format-List parancsmaghoz.
Az adott parancsmag formázza az eredményeket.
További információért írja be a következőt: `Get-Help Format-List` .

### 3. példa: adott csővezeték tulajdonságainak beolvasása
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **Tulajdonságok** tulajdonságot.

### Példa 4: adott csővezeték tevékenységének beszerzése
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **tevékenységek** tulajdonságot.

### Példa 5: a futásidejű adatok beszerzése egy adott csővezetékhez
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

Ez a parancs információt kap az WikiADF nevű adatDPWikisamplei nevű csővezetékről, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **RuntimeInfo** tulajdonságot.

### Példa 6: információk beszerzése az első tevékenységhez tartozó bemenetekről
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **tevékenységek** tulajdonságot.
A parancs a **tevékenységek** tömb első elemének **bemenet** tulajdonságát jeleníti meg a **Format listával**.

## PARAMÉTEREK

### -DataFactory
Egy **PSDataFactory** -objektumot ad meg.
Ez a parancsmag azokat a csővezetékeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Az adatfeldolgozó nevét adja meg.
Ez a parancsmag azokat a csővezetékeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Name (név)
Annak a csővezetéknek a nevét adja meg, amelyről információt szeretne kapni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.
Ez a parancsmag olyan csővezetékeket kap, amelyek a paraméter által definiált csoportba tartoznak.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## KIMENETEK

### Microsoft. Azure. Command. DataFactories. models. PSPipeline

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Önéletrajz – AzDataFactoryPipeline](./Resume-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Felfüggesztés – AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


