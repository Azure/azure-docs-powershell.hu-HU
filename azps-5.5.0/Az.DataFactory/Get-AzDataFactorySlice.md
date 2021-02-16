---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208758"
---
# Get-AzDataFactorySlice

## SYNOPSIS
Adatszeleteket kap egy adatkészlethez az Azure Data Factoryban.

## SZINTAXIS

### ByFactoryName (alapértelmezett)
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzDataFactorySlice** parancsmag adatszeleteket kap egy adatkészlethez az Azure Data Factoryban.
Adjon meg egy kezdési és egy záró időt a megtekinteni kívánt adatszeleteket meghatározó adatszeleteket.
Az adatszelet állapota az alábbi értékek egyike: 
- PendingExecution.
Az adatkezelés még nem kezdődött el. 
- InProgress.
Folyamatban van az adatok feldolgozása. 
- Kész.
Az adatkezelés befejeződött.
Az adatszelet készen áll arra, hogy a függő szeletek felhasználják. 
- Sikertelen.
A szeletet el nem sikerült hozó futtatás. 
- Kihagyás.
A Data Factory kihagyja a szelet feldolgozását. 
- Próbálja meg újból.
A Data Factory újrafuttatja a szeletelő futást. 
- Időkorrekt. Az adatkezelés időkorrekta. 
- Függőben lévőÉrték.
Az adatszelet a feldolgozás előtt érvényesítésre vár. 
- Próbálja meg újból az érvényesítést.
A Data Factory újravágja a szelet érvényesítését. 
- Sikertelen ellenőrzés.
A szelet érvényesítése nem sikerült.
Minden egyes szelethez további információt láthat a futtatásról, amely a szeletet a Get-AzDataFactoryRun parancsmag használatával.

## PÉLDÁK

### 1. példa: Adatszeletek lekérte egy adatkészlethez
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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

Ez a parancs a WikiADF nevű adatüzemben a WikiAggregatedData nevű adatkészlet összes adatszeletét begyűjte.
A parancs a StartDateTime paraméter által megadott idő után jön létre.
Az alábbi példakód óránként beállítja az adatkészlet elérhetőségét a JavaScript objektum-notation (JSON) fájlban.
elérhetőség: { period: "Hour", periodMultiplier: 1 } Az eredmények közül néhány készen áll, míg mások függőben lévőExecution.
A kész szeletek már futnak.
A függőben lévő szeletek az egyes óra végén, a parancsmag által megadott intervallumban Set-AzDataFactoryPipelineActivePeriod futnak.
Ebben a példában a folyamat kezdő és záró periódusa is egy nap (24 óra) értékű.

### 2. példa

Adatszeleteket kap egy adatkészlethez az Azure Data Factoryban. (automatikusan generált)

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## PARAMETERS

### -DataFactory
EGY **PSDataFactory-objektumot** ad meg.
Ez a parancsmag a paraméter által megadott adatüzembe tartozó szeleteket kapja meg.

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
Ez a parancsmag a paraméter által megadott adatüzembe tartozó szeleteket kapja meg.

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
Annak az adatkészletnek a nevét adja meg, amelyhez a parancsmag szeleteket kap.

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
Ez a parancsmag a paraméter által megadott időpont előtt készült szeleteket kap.
A DateTime-objektumokról a **következőt** írja be: `Get-Help Get-Date` .
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
Ez a parancsmag a paraméter által megadott csoporthoz tartozó szeleteket kapja meg.

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
Ez a parancsmag a paraméter által megadott idő után jön létre szeletekkel.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## MEGJEGYZÉSEK
* Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


