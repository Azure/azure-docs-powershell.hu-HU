---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: e45dcbfad9b4b92695f310d7d2c56fc46fc57bd7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492253"
---
# Set-AzureRmOperationalInsightsDataSource

## Áttekintés
Frissít egy adatforrást.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzureRmOperationalInsightsDataSource** parancsmag frissíti az adatforrást.

## Példák

## PARAMÉTEREK

### -DataSource
A parancsmag által frissített adatforrást adja meg.

```yaml
Type: PSDataSource
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSDataSource
A "DataSource" paraméter az "PSDataSource" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmOperationalInsightsDataSource](./Get-AzureRmOperationalInsightsDataSource.md)

[Remove-AzureRmOperationalInsightsDataSource](./Remove-AzureRmOperationalInsightsDataSource.md)


