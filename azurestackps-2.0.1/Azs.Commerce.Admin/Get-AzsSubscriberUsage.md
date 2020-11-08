---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015344"
---
# Get-AzsSubscriberUsage

## Áttekintés
Begyűjti a SubscriberUsageAggregates, amely a felhasználóktól UsageAggregates válik.

## SZINTAXISA

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Leírás
Begyűjti a SubscriberUsageAggregates, amely a felhasználóktól UsageAggregates válik.

## Példák

### Példa 1: a használati adatokat naponta összesítve kapja.
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

A használati adatokat az adott nap által összesített szolgáltatónál a minden bérlő számára a december 30 2019 (UTC) szerint kell beszereznie.
A ReportedStartTime és a ReportedEndTime a napokra kell kerekíteni.
Ha a szolgáltatás rendszergazdája néven ismert, az minden bérlői webhelyhez az összes használati adatot megjeleníti.

### 2. példa: a használati adatokat az Hour összesítve kapja meg.
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

A használati adatokat az Hour által összesítve, 2019 december 30-án (UTC-ben) kell 12am.
A ReportedStartTime és a ReportedEndTime órákra kerekítve kell lennie.
Hasonlóképpen, ha a szolgáltatás rendszergazdája néven ismert, az minden bérlői webhelyhez tartozó összes használati adatot hatékonyan jeleníti meg.

## PARAMÉTEREK

### -AggregationGranularity
Összesítési részletesség.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ContinuationToken
A folytatólagos jogkivonat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ReportedEndTime
A jelentés befejezési időpontja (kizárólagos)

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ReportedStartTime
A bejelentett kezdési időpont (beleértve).

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriberId
A bérlői előfizetési azonosító.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. Commerce. models. Api20150601Preview. IUsageAggregate



## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

