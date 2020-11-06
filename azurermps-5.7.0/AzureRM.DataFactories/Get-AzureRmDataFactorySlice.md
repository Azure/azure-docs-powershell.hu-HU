---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 77b12c17f46c9a04d1166b3066fa5ea9c2df1d74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492320"
---
# Get-AzureRmDataFactorySlice

## Áttekintés
Adatszeletek beolvasása adatkészlethez az Azure Data Factory-ban

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDataFactorySlice** parancsmag adatszeleteket kap az adatkészletekhez az Azure Data Factory szolgáltatásban.
Adja meg a kezdés időpontját és a befejezési időpontot, és adja meg a megtekinteni kívánt adatszeletek tartományát.

Az adatszeletek állapota az alábbi értékek egyike: 

- PendingExecution.
Nem kezdődött el az adatfeldolgozás. 
- Folyamatban van.
Folyamatban van az adatfeldolgozás. 
- Kész.
Befejeződött az adatfeldolgozás.
Az adatszelet készen áll a függő szeletek elfogyasztására. 
- Sikertelen.
A szeletet előállító Futtatás sikertelen volt. 
- Kihagyhatja.
Az Data Factory kihagyja a szelet feldolgozását. 
- Újra.
Az adatfeldolgozó újból megkísérli a szeletet előállító futtatást. 
- Időtúllépés. Az adatfeldolgozás időkorlátja lejárt. 
- PendingValidation.
Az adatszelet az érvényesítésre vár a feldolgozás előtt. 
- Az érvényesítés ismételt ismétlése
Az adatfeldolgozó újból megkísérli a szelet érvényesítését. 
- Sikertelen érvényesítés
Nem sikerült a szelet érvényesítése.

Minden egyes szeletre vonatkozóan további információkat találhat a szeletet előállító futtatásról a Get-AzureRmDataFactoryRun parancsmag használatával.

## Példák

### 1. példa: adatszeletek beolvasása adatkészlethez
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

Ez a parancs a WikiAggregatedData nevű adatkészlethez tartozó összes adatszeletet megkapja az WikiADF nevű adatfeldolgozóban.
A parancs a StartDateTime paraméter által megadott időpont után a szeleteket kapja.
Az alábbi mintakód a JavaScript Object (JSON) fájlban az adatkészlet elérhetőségét óránkénti értékre állítja.

                        availability: 
                        {
                        period: "Hour",
                        periodMultiplier: 1
                        }

                    Some of the results are Ready and others are PendingExecution.
A kész Slice-elemek már futnak.
A függőben lévő szeletek a Set-AzureRmDataFactoryPipelineActivePeriod parancsmag által megadott intervallumban minden óra végén futnak.
Ebben a példában a csővezeték kezdési és befejezési időszakait (24 óra) is megtalálhatja.

## PARAMÉTEREK

### -DataFactory
Egy **PSDataFactory** -objektumot ad meg.
Ez a parancsmag az adatfeldolgozóhoz tartozó, a paraméter által megadott szeleteket kapja meg.

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
Ez a parancsmag az adatfeldolgozóhoz tartozó, a paraméter által megadott szeleteket kapja meg.

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
Annak az adatkészletnek a nevét adja meg, amelynek a parancsmagja a szeleteket kapja.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDateTime
Az időszak végét **datetime** -objektumként adja meg.
Ez a parancsmag a paraméter által megadott időpont előtt a szeleteket kapja.
A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .

A *EndDateTime* a ISO8601 formátumban kell megadni az alábbi példákban: 

2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific standard Time)

Az alapértelmezett időzóna-kijelölés az UTC.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.
Ez a parancsmag olyan szeleteket kap, amelyek a paraméter által megadott csoportba tartoznak.

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

### -StartDateTime
Az időszak kezdését **datetime** -objektumként adja meg.
Ez a parancsmag a paraméter által megadott időpont után kap szeleteket.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft. WindowsAzure. commands. Utilities, Version = 0.8.2.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureRmDataFactorySliceStatus](./Set-AzureRmDataFactorySliceStatus.md)

[Get-AzureRmDataFactoryRun](./Get-AzureRmDataFactoryRun.md)

[Set-AzureRmDataFactoryPipelineActivePeriod](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


