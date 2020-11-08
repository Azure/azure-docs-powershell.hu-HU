---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0b272732cf6c1e1b2025c8e7f48b58e4807cdb3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015595"
---
# Get-AzureSiteRecoveryJob

## Áttekintés
A webhely-helyreállítási boltozat üzemeltetési adatait kapja meg.

## SZINTAXISA

### ByParam (alapértelmezett)
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByObject
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureSiteRecoveryJob** parancsmag Azure webhely-helyreállítási feladatokat kap.
Ezzel a parancsmaggal megtekintheti az aktuális webhely-helyreállítási boltozat üzemeltetési adatait.

## Példák

### Példa 1: egy azonosító megadásával munka beszerzése
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

Ez a parancs a megadott AZONOSÍTÓJÚ Azure webhely-helyreállítási feladatot kapja.

### 2. példa: a munka időben alapul
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

Ez a parancs a megadott kezdési és befejezési időpontot tartalmazó webhely-helyreállítási feladatokat kap.

## PARAMÉTEREK

### -A befejezési időpont
A feladatok befejezési időpontját adja meg.
Ez a parancsmag a megadott időpontig kezdődő összes feladatot beilleszti.
Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.
További információért írja be a következőt: `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
A beolvasott feladat AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
A beolvasott feladatot adja meg.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Kezdő időpont
A feladatok kezdési időpontját adja meg.
Ez a parancsmag minden olyan feladatra bekerül, amely a megadott idő után elindult.

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State (állami)
A webhely-helyreállítási feladatok beviteli állapotát adja meg.
Ez a parancsmag minden olyan feladatra bekerül, amely megfelel a megadott állapotnak.
A paraméter elfogadható értékei a következők:

- NotStarted
- Előrehaladás
- Sikerességéről
- Más
- Sikertelen
- Lemondott
- Felfüggesztve

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
A feladat által célzott objektum AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

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

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure site Recovery Services-parancsmagok](./Azure.SiteRecoveryServices.md)

[Újraindítás – AzureSiteRecoveryJob](./Restart-AzureSiteRecoveryJob.md)

[Önéletrajz – AzureSiteRecoveryJob](./Resume-AzureSiteRecoveryJob.md)

[Stop-AzureSiteRecoveryJob](./Stop-AzureSiteRecoveryJob.md)


