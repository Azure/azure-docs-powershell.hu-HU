---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 30e6a3ec6d3cd9cba978ed51d6545b3f68375779
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492480"
---
# Set-AzureRmDataFactorySliceStatus

## Áttekintés
A szeletek állapotát állítja be egy adatkészlethez az Azure Data Factory-ban.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzureRmDataFactorySliceStatus** parancsmag az Azure Data Factory adatkészlethez tartozó szeletek állapotát állítja be.

## Példák

### Példa 1: az összes szelet állapotának beállítása
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

Ez a parancs beállítja a DAWikiAggregatedData nevű adatkészlet összes szeletének állapotát a WikiADF nevű adatgyárban való várakozáshoz.
A *UpdateType* paraméter a UpstreamInPipeline értékét tartalmazza, így a parancs az adatkészlet minden egyes szeletének állapotát és a függő adatkészletek állapotát állítja be.
A függő adatkészletek beviteli adatkészletként használhatók a csővezetéken végzett tevékenységekhez.
A parancs a $True értékét számítja ki.

## PARAMÉTEREK

### -DataFactory
Egy **PSDataFactory** -objektumot ad meg.
Ez a parancsmag módosítja az adatfeldolgozóhoz tartozó szeletek állapotát, és ezt a paramétert adja meg.

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
Ez a parancsmag módosítja az adatfeldolgozóhoz tartozó szeletek állapotát, és ezt a paramétert adja meg.

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
Annak az adatkészletnek a neve, amelyhez ez a parancsmag módosítja a szeleteket.

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

### -EndDateTime
Az időszak végét **datetime** -objektumként adja meg.
Ez az idő az adatszeletek vége.
A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .

A *EndDateTime* a ISO8601 formátumban kell megadni az alábbi példákban: 

2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific standard Time)

Az alapértelmezett időzóna-kijelölés az UTC.

```yaml
Type: System.DateTime
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
Ez a parancsmag módosítja annak a csoportnak a szeletét, amelyhez a paraméter van meghatározva.

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
Ez az idő az adatszeletek kezdetét jelentik.

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

### -Állapot
Az adatszelethez hozzárendelni kívánt állapotot adja meg.
A paraméter elfogadható értékei a következők:

- Várakozás.
Az adatszeletek az érvényesítési szabályoknak a feldolgozás előtt való érvényesítésére várnak. 
- Kész.
Az adatfeldolgozás befejeződött, és az adatszelet készen áll.
- Folyamatban van.
Folyamatban van az adatfeldolgozás. 
- Sikertelen.
Sikertelen az adatfeldolgozás.
- Kihagyott.
Az adatszelet feldolgozása kihagyva.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateType
A szelet frissítésének típusát adja meg.
A paraméter elfogadható értékei a következők:

- Egyéni.
A megadott időtartományban beállítja az adatkészlet minden egyes szeletének állapotát. 
- UpstreamInPipeline.
Beállítja az adatkészlet minden egyes szeletének állapotát, valamint az összes függő adatkészletet, amely a csővezetéken végzett tevékenységekhez bemeneti adatkészletként van használatban.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### System. Boolean

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmDataFactorySlice](./Get-AzureRmDataFactorySlice.md)


