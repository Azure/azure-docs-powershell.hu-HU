---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2DEF8B3A-4E91-4D39-AD39-1871F9FECE10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a59c93c9de0d2445f2839d9a66f4750751c987f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016510"
---
# Get-AzureWebHostingPlanMetric

## Áttekintés
Az Azure webhelyhez tartozó csomagok metrikáját kapja.

## SZINTAXISA

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **Get-AzureWebHostingPlanMetric** parancsmag metrikákat kap az Azure web hosting csomaghoz egy előfizetésben.

## Példák

### Példa 1: a mérőszámok beszerzése az elmúlt három órában a per-instance szinten
```
PS C:\> Get-AzureWebHostingPlanMetric -WebSpaceName "eastuswebspace" -StartDate (get-date).AddHours(-3) -InstanceDetails $Metrics[1].Data 

Name : CpuPercentage 
Unit : Percent 
StartTime : 8/11/2014 7:00:00 AM 
EndTime : 8/11/2014 5:00:23 PM 
TimeGrain : PT1H 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 8:00:00 AM, Total:2, Min:9, Max:0, 
Time:8/11/2014 9:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 10:00:00 AM, Total:2, Min:8, Max:0...} $metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName
 ----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 8:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 9:00:00 AM 2 9 0 1 RD00155DC24579 
8/11/2014 10:00:00 AM 2 8 0 1 RD00155DC24599 
8/11/2014 11:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 12:00:00 PM 2 6 0 1 RD00155DC24599 
8/11/2014 1:00:00 PM 2 15 0 1 RD00155DC24599 
8/11/2014 2:00:00 PM 3 21 0 1 RD00155DC24599 
8/11/2014 3:00:00 PM 2 13 0 1 RD00155DC24599 
8/11/2014 4:00:00 PM 2 14 0 1 RD00155DC24599
```

Ez a parancs a webes üzemeltetési terv metrikáját adja meg az elmúlt három órában a per-instance szinten.

## PARAMÉTEREK

### -EndDate
A befejezési időpontot **datetime** -objektumként adja meg, amelyből a program visszaadja a metrikákat.
Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.
További információért írja be a következőt: `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceDetails
Azt jelzi, hogy ez a parancsmag a példányok szintjének részleteit tartalmazza.
Ha a webhely-üzemeltetési terv két vagy több számítógépen fut, ez a parancsmag az egyes gépek részletes metrikáját jeleníti meg.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MetricNames
Faj: a mérőszámok tömbje a kezdéshez.
Ha nem ad meg értéket ehhez a paraméterhez, ez a parancsmag minden metrikát kap.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Az előfizetésben szereplő terv nevét adja meg.
A **Get-AzureWebHostingPlanMetric** alapértelmezés szerint a jelenlegi előfizetés összes webhelyét kapja.
Ez a paraméter nem támogatja a helyettesítő karaktereket.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDate
Azt a kezdési időpontot adja meg **datetime** -objektumként, amelyből mérőszámokat szeretne kapni.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeGrain
A mérőszámok beszerzéséhez szükséges időegységet adja meg.
Az érvényes értékek a következők: 

- PT1M (perc) 
- PT1H (óra) 
- P1D (nap)

Az alapértelmezett érték a PT1H.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebSpaceName
Az előfizetésben lévő tárhely nevét adja meg.
A **Get-AzureWebHostingPlanMetric** alapértelmezés szerint az aktuális előfizetéshez tartozó összes csomagot kapja.
Ez a paraméter nem támogatja a helyettesítő karaktereket.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

###  
A parancsmagot név szerint, de nem érték szerint is továbbíthatja.

## KIMENETEK

###  
Microsoft. WindowsAzure. Command. Utilities. websites. Services. webentitások. MetricResponse

Alapértelmezés szerint a **Get-AzureWebHostingPlanMetric** a **MetricResponse** -objektumok tömbjét számítja ki.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureWebHostingPlan](./Get-AzureWebHostingPlan.md)


