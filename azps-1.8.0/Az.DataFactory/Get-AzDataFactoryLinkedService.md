---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: a54cdb0a30d0249ccb8fd177646e218e0fe604c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836545"
---
# Get-AzDataFactoryLinkedService

## Áttekintés
Információt kap az Azure Data Factory kapcsolt szolgáltatásairól.

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzDataFactoryLinkedService** parancsmag információkat kap az Azure Data Factory kapcsolt szolgáltatásairól.
Ha egy kapcsolt szolgáltatás nevét adja meg, ez a parancsmag információkat kap a kapcsolt szolgáltatásról.
Ha nem ad meg nevet, ez a parancsmag információkat kap az adatok gyári összes kapcsolt szolgáltatásáról.

## Példák

### 1. példa: információk kérése az összes kapcsolt szolgáltatásról
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

Ez a parancs a WikiADF nevű adatfeldolgozóban található összes kapcsolt szolgáltatásról információt kap, majd a csővezeték-kezelő segítségével átadja a kapcsolt szolgáltatásokat az Format-List parancsmagnak.
Az adott parancsmag formázza az eredményeket.
További információért írja be a következőt: `Get-Help Format-List` .

### 2. példa: információk kérése egy adott kapcsolt szolgáltatásról
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

Ez a parancs információt kap a HDILinkedService nevű kapcsolt szolgáltatásról az WikiADF nevű adatgyárban.

### 3. példa: információk beszerzése egy adott kapcsolt szolgáltatásról a DataFactory paraméter megadásával
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

Az első parancs az Get-AzDataFactory parancsmagot használja az ContosoFactory nevű adatfeldolgozó beolvasásához, majd a $DataFactory változóban tárolja.
A második parancs információt kap az $DataFactory-on tárolt adatfeldolgozóhoz kapcsolt szolgáltatásról, majd ezeket az információkat átadja a Format-Table parancsmagnak a pipeline operátor használatával.
**Formátum – a táblázat** a kimenetet adatkészletként formázza, és a megadott tulajdonságokat adatkészlet-oszlopként adja meg.

## PARAMÉTEREK

### -DataFactory
Egy **PSDataFactory** -objektumot ad meg.
Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.

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
Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.

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
Annak a kapcsolt szolgáltatásnak a neve, amelyről információt szeretne kapni.

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
Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek a paraméter által definiált csoportba tartoznak.

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

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## KIMENETEK

### Microsoft. Azure. Command. DataFactories. models. PSLinkedService

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzDataFactoryLinkedService](./New-AzDataFactoryLinkedService.md)

[Remove-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


