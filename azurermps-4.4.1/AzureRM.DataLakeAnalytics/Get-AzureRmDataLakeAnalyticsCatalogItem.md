---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b12b09c686a2e0a5fcd85854551608b16cb43d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504188"
---
# Get-AzureRmDataLakeAnalyticsCatalogItem

## Áttekintés
Beolvassa az adattó-statisztika-katalógus elemeit vagy típusait.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDataLakeAnalyticsCatalogItem** megkapja az Azure Data Lake-tó elemzési elemét, vagy egy megadott típusú katalógust kap.

## Példák

### Példa 1: megadott adatbázis beszerzése
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

Ez a parancs a megadott adatbázist kapja.

### 2. példa: táblázatok beszerzése egy megadott adatbázisban és sémában
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

Ez a parancs a megadott adatbázisban lévő táblák listáját kapja meg.

## PARAMÉTEREK

### -Fiók
A Lake Analytics-fiók nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ItemType
A beolvasott vagy a listán szereplő elem (ek) katalógus-elemének típusát adja meg.
A paraméter elfogadható értékei a következők:

- Adatbázis
- Séma
- Összeállítási
- Táblázat
- TableValuedFunction
- TableStatistics
- ExternalDataSource
- Nézd
- Eljárás
- Titkos
- Hitelesítőadat
- Típusú
- TablePartition

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases: 
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path (elérési út)
A beolvasandó elem többrészes elérési útja vagy a lista elemeinek a fölérendelt eleme.
Az elérési út egyes részeit ponttal (.) kell elválasztani.

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CatalogItem
A megadott katalógusegyesítési elem.

### Lista<CatalogItem>
A megadott katalógusfájl listája a megfelelő tároló alatt.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Teszt-AzureRmDataLakeAnalyticsCatalogItem](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


