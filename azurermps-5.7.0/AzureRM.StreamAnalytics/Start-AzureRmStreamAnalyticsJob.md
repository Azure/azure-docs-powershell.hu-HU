---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/start-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a4e6ac26eeca6150feabaa07dc28a787ea01112d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492114"
---
# Start-AzureRmStreamAnalyticsJob

## Áttekintés
Adatfolyam-elemzési feladat indítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Start-AzureRmStreamAnalyticsJob** parancsmag aszinkron módon telepíti és elindítja az adatfolyam-elemzési feladatot az Azure-ban.

## Példák

### 1. példa: adatfolyam-elemzési feladat indítása
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

Ez a parancs elindítja a feladat StreamingJob, és azt adja meg, hogy a kimeneti esemény folyama az időbélyegző 2014 – 07 – 03T01:00Z.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Name (név)
A kezdéshez az Azure stream Analytics-feladat nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputStartMode
A feladat indítási módját adja meg.
Az érvényes értékek a következők: 

- JobStartTime – ez az érték azt jelzi, hogy a kimeneti esemény folyam kezdőpontjának meg kell kezdődnie a feladat indításakor.
- CustomTime – ez az érték azt jelzi, hogy a kimenet-esemény folyam kezdőpontjának a *OutputStartTime* paraméterben megadott egyéni időpontra kell kezdődnie. 
 ---LastOutputEventTime – ez az érték azt jelzi, hogy a kimeneti esemény folyam kezdőpontja a legutóbbi esemény kimeneti időpontjától kezdődik.

Ha a tulajdonság hiányzik, az alapértelmezett érték a JobStartTime.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputStartTime
A kimenet kezdési időpontját adja meg.
Ez az érték az ISO-8601 formázott időbélyegzője, amely jelzi a kimeneti esemény folyam kezdőpontját, vagy $Null jelzi, hogy a kimeneti esemény folyama elindul a folyamatos adatfolyam-továbbítási feladat indításakor.
Ennek a tulajdonságnak tartalmaznia kell egy értéket, ha a *OutputStartMode* értéke CustomTime.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.

```yaml
Type: String
Parameter Sets: (All)
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

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### System. Object (rendszer. objektum)

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmStreamAnalyticsJob](./Get-AzureRmStreamAnalyticsJob.md)

[Új – AzureRmStreamAnalyticsJob](./New-AzureRmStreamAnalyticsJob.md)

[Remove-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[Stop-AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)


