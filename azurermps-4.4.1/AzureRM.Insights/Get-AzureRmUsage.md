---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: CA67985F-C5D5-4CF4-81A4-C35FD769AF0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
ms.openlocfilehash: 9f02a1c9dfe0c4c41fa1e873201dbeb1d849dd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501847"
---
# Get-AzureRmUsage

## Áttekintés
Az erőforrás használati metrikáját kapja meg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmUsage [-ResourceId] <String> [-ApiVersion <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-MetricNames <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmUsage** parancsmag a megadott erőforrás használati metrikáját kapja meg.

## Példák

### Példa 1: használati metrikák beszerzése erőforrás-AZONOSÍTÓval
```
PS C:\>Get-AzureRmUsage -ResourceId "/subscriptions/bcdeb07f-1c43-20be-1f3b-4f0febc10f5b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/pattifuller"
```

Ez a parancs a megadott webhely használati metrikáját kapja meg.

## PARAMÉTEREK

### -ApiVersion
Egy API-verzió karakterláncát adja meg, például 2014-04-01, amelyet az erőforrás-szolgáltató fogad el.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -A befejezési időpont
A keresés legkésőbbi időpontját és dátumát adja meg.

A Get-Date parancsmaggal **datetime** -objektumot is beszerezhet.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MetricNames
A metrikák neveinek tömbjét adja meg.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
A metrika erőforrás-AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kezdő időpont
A kereséshez legkorábbi dátumot és dátumot adja meg.

A Get-Date parancsmaggal **datetime** -objektumot is beszerezhet.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### Microsoft. Azure. Command. detekintés. OutputClasses. PSUsageMetric []

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmMetric](./Get-AzureRmMetric.md)


