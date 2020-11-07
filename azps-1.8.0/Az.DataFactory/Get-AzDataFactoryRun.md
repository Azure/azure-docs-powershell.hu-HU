---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: b3524f0886c5c433c6ec36d907126e6ca04828de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836541"
---
# Get-AzDataFactoryRun

## Áttekintés
Az Azure Data Factory-ban az adatkészletek adatszeleteit futtatja.

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzDataFactoryRun** parancsmag az Azure Data Factory adatkészletben található adatkészletek adatszeletéhez tartozó futásokat kapja.
Az adatfeldolgozó adatkészlete az időtengelyen kívüli szeletekre épül.
A szeletek szélességét az ütemterv határozza meg óránként vagy naponta.
A Run egy szelet feldolgozási egysége.
Lehet, hogy egy vagy több futás van egy slice-ra, ha újból próbálkozik, vagy ha a slice-ot a meghibásodások miatt újra futtatja.
A szeletet a kezdési időpontja azonosítja.
A szelet kezdési időpontjának beolvasásához használja az Get-AzDataFactorySlice parancsmagot.
Ha például a következő slice-hoz szeretne futni, használja a 2015-04-02T20:00:00 kezdési időpontot.
ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingCampaignEffectivenessBlobDataset Start: 5/2/2014 8:00:00 PM End: 5/3/2014 8:00:00 PM RetryCount: 0 Status: Ready LatencyStatus:

## Példák

### Példa 1: adatkészlet beszerzése
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

Ez a parancs minden futást a WikiADF nevű adatDAWikiAggregatedDatai adatkészletnek a 05/21/2014-as verziójában, a 4 PM GMT-től kezdődően futtatja.

## PARAMÉTEREK

### -DataFactory
Egy **PSDataFactory** -objektumot ad meg.
Ez a parancsmag akkor fog futni, ha az adatfeldolgozóhoz tartozó Slice-elemek szerepelnek, és ez a paraméter határozza meg.

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
Ez a parancsmag akkor fog futni, ha az adatfeldolgozóhoz tartozó Slice-elemek szerepelnek, és ez a paraméter határozza meg.

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

### -DatasetName
Az adatkészlet nevét adja meg.
Ez a parancsmag a paraméter által megadott adatkészlethez tartozó szeletekhez fog futni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.
Ez a parancsmag beilleszti a Factory függvényt azokhoz a szeletekhez, amelyek a paraméter által definiált csoportba tartoznak.

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

### -StartDateTime
Az időszak kezdését **datetime** -objektumként adja meg.
Ez a parancsmag az adott időszaknak megfelelő adatszeletek esetén fut.
A *StartDateTime* a ISO8601-formátumban kell megadni, ahogyan az alábbi példákban: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pacific standard Time): az alapértelmezett időzóna-jelző az UTC.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## KIMENETEK

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


