---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 8a6553547bd75aeaaca8e96a85c9697d00ee65a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504443"
---
# Get-AzureRmDataFactoryLinkedService

## Áttekintés
Információt kap az Azure Data Factory kapcsolt szolgáltatásairól.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
Get-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDataFactoryLinkedService** parancsmag információkat kap az Azure Data Factory kapcsolt szolgáltatásairól.
Ha egy kapcsolt szolgáltatás nevét adja meg, ez a parancsmag információkat kap a kapcsolt szolgáltatásról.
Ha nem ad meg nevet, ez a parancsmag információkat kap az adatok gyári összes kapcsolt szolgáltatásáról.

## Példák

### 1. példa: információk kérése az összes kapcsolt szolgáltatásról
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

Ez a parancs a WikiADF nevű adatfeldolgozóban található összes kapcsolt szolgáltatásról információt kap, majd a csővezeték-kezelő segítségével átadja a kapcsolt szolgáltatásokat az Format-List parancsmagnak.
Az adott parancsmag formázza az eredményeket.
További információért írja be a következőt: `Get-Help Format-List` .

### 2. példa: információk kérése egy adott kapcsolt szolgáltatásról
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

Ez a parancs információt kap a HDILinkedService nevű kapcsolt szolgáltatásról az WikiADF nevű adatgyárban.

### 3. példa: információk beszerzése egy adott kapcsolt szolgáltatásról a DataFactory paraméter megadásával
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzureRmDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

Az első parancs az Get-AzureRmDataFactory parancsmagot használja az ContosoFactory nevű adatfeldolgozó beolvasásához, majd a $DataFactory változóban tárolja.
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

[Új – AzureRmDataFactoryLinkedService](./New-AzureRmDataFactoryLinkedService.md)

[Remove-AzureRmDataFactoryLinkedService](./Remove-AzureRmDataFactoryLinkedService.md)


