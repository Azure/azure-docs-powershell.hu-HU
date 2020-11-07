---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: c733c071bb0c7c2bc1c0c2d1fe1c2142d89e8590
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846366"
---
# Start-AzStreamAnalyticsJob

## Áttekintés
Adatfolyam-elemzési feladat indítása.

## SZINTAXISA

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Start-AzStreamAnalyticsJob** parancsmag aszinkron módon telepíti és elindítja az adatfolyam-elemzési feladatot az Azure-ban.

## Példák

### 1. példa: adatfolyam-elemzési feladat indítása
```
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

Ez a parancs elindítja a feladat StreamingJob, és azt adja meg, hogy a kimeneti esemény folyama az időbélyegző 2014 – 07 – 03T01:00Z.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
A kezdéshez az Azure stream Analytics-feladat nevét adja meg.

```yaml
Type: System.String
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
 - LastOutputEventTime – ez az érték azt jelzi, hogy a kimeneti esemény folyam kezdőpontja a legutóbbi esemény kimeneti időpontjától kezdődik.
Ha a tulajdonság hiányzik, az alapértelmezett érték a JobStartTime.

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

### -OutputStartTime
A kimenet kezdési időpontját adja meg.
Ez az érték az ISO-8601 formázott időbélyegzője, amely jelzi a kimeneti esemény folyam kezdőpontját, vagy $Null jelzi, hogy a kimeneti esemény folyama elindul a folyamatos adatfolyam-továbbítási feladat indításakor.
Ennek a tulajdonságnak tartalmaznia kell egy értéket, ha a *OutputStartMode* értéke CustomTime.

```yaml
Type: System.Nullable`1[System.DateTime]
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. null ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]

## KIMENETEK

### System. Boolean

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStreamAnalyticsJob](./Get-AzStreamAnalyticsJob.md)

[Új – AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


