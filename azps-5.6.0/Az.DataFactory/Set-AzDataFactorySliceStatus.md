---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 80a471b88856ff4c7425e89fd6e5b73168370789
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942881"
---
# Set-AzDataFactorySliceStatus

## SYNOPSIS
Egy adatkészlet szeletének állapotát állítja be az Azure Data Factoryban.

## SZINTAXIS

### ByFactoryName (alapértelmezett)
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzDataFactorySliceStatus** parancsmag beállítja egy adatkészlet szeletének állapotát az Azure Data Factoryban.

## PÉLDÁK

### 1. példa: Az összes szelet állapotának beállítása
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

Ez a parancs a DAWikiAggregatedData nevű adatkészlet összes szeletének állapotát Várakozásra állítja a WikiADF nevű adathalmazban.
Az *UpdateType* paraméter értéke UpstreamInPipeline, ezért a parancs beállítja az egyes szeletek állapotát az adatkészlethez és az összes függő adatkészlethez.
A függő adatkészletek bemeneti adatkészletekként használatosak a folyamat tevékenységeihez.
Ez a parancs egy számértéket ad $True.

## PARAMETERS

### -DataFactory
EGY **PSDataFactory-objektumot** ad meg.
Ez a parancsmag módosítja a paraméter által megadott adat factoryhoz tartozó szeletek állapotát.

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
Egy adatüzem nevét adja meg.
Ez a parancsmag módosítja a paraméter által megadott adat factoryhoz tartozó szeletek állapotát.

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
Annak az adatkészletnek a nevét adja meg, amelynek a parancsmagja módosítja a szeleteket.

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -EndDateTime
Egy időtartomány végét adja meg **DateTime-objektumként.**
Ez az idő az adatszelet vége.
A **DateTime-objektumokról** további információt ad `Get-Help Get-Date` meg.
Az *EndDateTime* értéket ISO8601 formátumban kell megadni, az alábbi példák szerint: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Csendes-óceáni téli idő) Az alapértelmezett időzóna-tervező az UTC.

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
Ez a parancsmag módosítja a paraméter által megadott csoporthoz tartozó szeletek állapotát.

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
Egy időtartomány kezdő időpontját adja meg **DateTime-objektumként.**
Ez az időpont egy adatszelet elején van.

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
Megadja az adatszelethez hozzárendelni szükséges állapotot.
A paraméter elfogadható értékei a következőek:
- Várakozás.
Az adatszelet a feldolgozás előtt érvényesítési házirendekre vár. 
- Kész.
Az adatkezelés befejeződött, és az adatszelet készen áll.
- InProgress.
Az adatok feldolgozása folyamatban van. 
- Sikertelen.
Az adatkezelés nem sikerült.
- Kihagyva.
Kihagyta az adatszelet feldolgozását.

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
A szelet frissítésének típusát határozza meg.
A paraméter elfogadható értékei a következőek:
- Egyéni.
Beállítja a megadott időtartományban az adatkészlet egyes szeletének állapotát. 
- UpstreamInPipeline.
Beállítja az adatkészlet egyes szeletei és a függő adatkészletek állapotát, amelyek a folyamat tevékenységeinek bemeneti adatkészleteiként használatosak.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK
* Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


