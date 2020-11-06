---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 33deeafce23267d1b2dbc594251bc58de1914280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492321"
---
# Get-AzureRmDataFactoryActivityWindow

## Áttekintés
Információt kap az adatgyárhoz társított tevékenység-ablakokról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDataFactoryActivityWindow** parancsmag információt kap az adatfeldolgozó ablakokkal társított tevékenységekről.

## Példák

### 1. példa: az adatfeldolgozóhoz társított Windows-tevékenységek beszerzése
```
PS C:\>Get-AzureRmDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

Ez a parancs információt kap a WikiADF nevű adatfeldolgozóval társított összes tevékenység ablakról.

## PARAMÉTEREK

### -ActivityName
A tevékenység nevét adja meg.
Ez a parancsmag a Windows tevékenységeit a paraméter által megadott tevékenységhez kapja.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactory
Egy parancsmag által visszaadott **PSDataFactory** -objektumot adja meg.
Ez a parancsmag azokat a Windows-tevékenységeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.

```yaml
Type: PSDataFactory
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
Ez a parancsmag azokat a Windows-tevékenységeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.

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

### -DatasetName
Az adatkészlet nevét adja meg.
Ez a parancsmag olyan Windows-tevékenységekre ad választ, amelyek a paraméter által megadott adatkészlethez tartoznak.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Szűrő
A tevékenység ablak az Azure keresési szűrési nyelvhelyességi szolgáltatással.
A nyelvhelyességről további információt az Azure Search OData kifejezés szintaxisa című témakörben talál https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) az MSDN webhelyen.
A tevékenység Windows-listáját a paraméter által megadott keresési karakterlánc szűri.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
Azt adja meg, hogy a tevékenység ablak lista paramétereinek egyike szerint rendelje a választ.
Ez a pontosvesszővel tagolt tulajdonságok listája.
Például: WindowStart, KészültségiSzint paraméter értéke.

Alapértelmezés szerint a sorrend növekvő sorrendű (ASC).
Ha csökkenő sorrendben szeretné rendezni a listát, adja meg a LEÍRÁSát.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineName
A csővezeték nevét adja meg.
Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek a paraméter által megadott csővezetékhez tartoznak.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport nevét adja meg.
Ez a parancsmag olyan Windows-tevékenységekre ad választ, amelyek a paraméter által megadott erőforráscsoport csoportjába tartoznak.

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

### -RunEnd
A tevékenység ablak befejezési időpontját adja meg.
Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek futási ideje a *RunStart* és a *RunEnd* között esik.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunStart
A tevékenység ablak kezdési időpontját adja meg.
Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek futási ideje a *RunStart* és a *RunEnd* között esik.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
Itt adhatja meg, hogy a Windows hány tevékenységet ad eredményül.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowEnd
A tevékenység befejezése ablak befejezési időpontját adja meg.
Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek időpontja a *WindowStart* és a *WindowEnd* időpontja között esik.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowStart
A tevékenység ablak kezdési időpontját adja meg.
Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek időpontja a *WindowStart* és a *WindowEnd* időpontja között esik.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowState
A tevékenység ablak állapotát adja meg.
A paraméter elfogadható értékei a következők:

- Nincs
- Várakozás
- Előrehaladás
- Kész
- Sikertelen
- Kihagyott

Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek abban az állapotban vannak, hogy ez a paraméter adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowSubstate
A tevékenység ablak alállapotát adja meg.
A paraméter elfogadható értékei a következők:

- Visszavont
- timedOut
- Érvényesítése

Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek abban az alállamban vannak, hogy ez a paraméter adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. WindowsAzure. Command. Utilities. PSActivyWindow, Microsoft. WindowsAzure. commands. Utilities, Version = 0.8.2.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure adatgyárak parancsmagok](./AzureRM.DataFactories.md)


