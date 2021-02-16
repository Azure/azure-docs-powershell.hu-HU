---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208742"
---
# New-AzDataFactoryDataset

## SYNOPSIS
Adatkészletet hoz létre a Data Factoryban.

## SZINTAXIS

### ByFactoryName (alapértelmezett)
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzDataFactoryDataset** parancsmag létrehoz egy adatkészletet az Azure Data Factoryban.
Ha egy már létező adatkészlet nevét adja meg, ez a parancsmag megerősítést kér, mielőtt lecseréli az adatkészletet.
Ha a Force *paramétert* adja meg, a parancsmag jóváhagyás nélkül lecseréli a meglévő adatkészletet.
Ezeket a műveleteket a következő sorrendben végezze el: 
- Adatüzem létrehozása 
- Csatolt szolgáltatások létrehozása 
- Adatkészletek létrehozása 
- Folyamat létrehozása
Ha egy azonos nevű adatkészlet már létezik az adatüzemben, ez a parancsmag megkérdezi, hogy felül kell-e írnia a meglévő adatkészletet az új adatkészletben.
Ha megerősíti, hogy felülírja a meglévő adatkészletet, az adatkészlet-definíciót is lecseréli a program.

## PÉLDÁK

### 1. példa: Adatkészlet létrehozása
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

Ezzel a paranccsal a WikiADF nevű DA_WikipediaClickEvents nevű adatkészletet hoz létre.
A parancs az adatkészletet a fájlon DAWikipediaClickEvents.jsadatok alapján.

### 2. példa: Új adatkészlet elérhetőségének megtekintése
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

Az első parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet, ahogy az előző példában is volt, majd hozzárendeli az adatkészletet a $Dataset változóhoz.
A második parancs szabványos pontjelekkel jeleníti meg az adatkészlet Elérhetőség tulajdonságának részleteit.

### 3. példa: Új adatkészlet helyének megtekintése
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

Az első parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet, ahogy az előző példában is volt, majd hozzárendeli az adatkészletet a $Dataset változóhoz.
A második parancs megjeleníti az adatkészlet Hely tulajdonságának részleteit.

### 4. példa: Új adatkészlet érvényességi szabályainak megtekintése
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

Az első parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet, ahogy az előző példában is volt, majd hozzárendeli az adatkészletet a $Dataset változóhoz.
A második parancs részletes információkat kap az adatkészlet érvényességi szabályairól, majd a folyamat műveleti Format-List átadja őket a Format-List parancsmagnak.
Ez a Windows PowerShell-parancsmag formázta az eredményeket.
További információért írja be a `Get-Help Format-List` .

## PARAMETERS

### -DataFactory
EGY **PSDataFactory-objektumot** ad meg.
Ez a parancsmag egy adatkészletet hoz létre a paraméter által megadott adatüzemmódban.

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
Ez a parancsmag egy adatkészletet hoz létre a paraméter által megadott adatüzemmódban.

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

### -File
Az adatkészlet leírását tartalmazó JSON-fájl teljes elérési útját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Azt jelzi, hogy ez a parancsmag a megerősítés kérése nélkül lecserél egy meglévő adatkészletet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A létrehozni szükséges adatkészlet nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.
Ez a parancsmag egy adatkészletet hoz létre a paraméter által megadott csoportban.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.DataFactories.Models.PSDataset

## MEGJEGYZÉSEK
* Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDataFactoryDataset](./Get-AzDataFactoryDataset.md)

[Remove-AzDataFactoryDataset](./Remove-AzDataFactoryDataset.md)


