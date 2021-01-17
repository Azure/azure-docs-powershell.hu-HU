---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: f04f2d2d96dd0b293850ca3150568eb015ab5bbb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480437"
---
# Get-AzDataFactoryRun

## SYNOPSIS
Egy adatkészlet adatszeletéhez fut az Azure Data Factoryban.

## SZINTAXIS

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

## LEÍRÁS
A **Get-AzDataFactoryRun** parancsmag az Azure Data Factoryban egy adatkészlet adatszeletéhez futtatja az adatokat.
Egy adatüzem adatkészlete szeletekből áll az időtengelyen.
A szeletek szélességét az ütemezés határozza meg óránként vagy naponta.
A futtatás egy szelet feldolgozásának egy mértékegysége.
Egy vagy több futtatás is lehet a szelethez újrajátszások esetén, illetve arra az esetre, ha hibák miatt újrafuttatja a szeletet.
A szeleteket a kezdési időpont azonosítja.
A szelet kezdési idejét a Get-AzDataFactorySlice ki.
A következő szelet futtatásához például használja a 2015-04-02T20:00:00 kezdési időt.
ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingBlogaignEffectivenessBlobDataset Start : 2014.05.02.00:00 End : 2014.05.03 08:00:00 RetryCount: 0 Status: Ready LatencyStatus:

## PÉLDÁK

### 1. példa: Adatkészlet lekérte
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

Ez a parancs a DAWikiAggregatedData nevű adatkészlet szeletei számára fut a WikiADF adatüzemben, amely 2014.05.21-től (GMT) 2014.05.05-től kezdődik.

## PARAMETERS

### -DataFactory
EGY **PSDataFactory-objektumot** ad meg.
Ez a parancsmag a paraméter által megadott adat factoryhoz tartozó szeletekre fut.

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
Ez a parancsmag a paraméter által megadott adat factoryhoz tartozó szeletekre fut.

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
Ez a parancsmag a paraméter által megadott adatkészlethez tartozó szeletekre fut.

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

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.
Ez a parancsmag a paraméter által megadott csoporthoz tartozó szeletek gyári futását adja meg.

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
Ez a parancsmag az adott időszaknak megfelelő adatszeleteket futtatja.
A *StartDateTime* értéket ISO8601 formátumban kell megadni, ahogy az alábbi példákban is látható: 2015-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Csendes-óceáni téli idő) Az alapértelmezett időzóna-tervező az UTC.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun

## MEGJEGYZÉSEK
* Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


