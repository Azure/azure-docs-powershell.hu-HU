---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015528"
---
# New-AzureStorSimpleDeviceBackupScheduleAddConfig

## Áttekintés
Biztonságimásolat-ütemterv konfigurációs objektumának létrehozása

## SZINTAXISA

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorSimpleDeviceBackupScheduleAddConfig** parancsmag létrehoz egy **BackupScheduleBase** konfigurációs objektumot.
Ezzel a konfigurációs objektummal új biztonsági házirendeket hozhat létre a **New-AzureStorSimpleDeviceBackupPolicy** parancsmag használatával.

## Példák

### Példa 1: biztonságimásolat-konfigurációs objektum létrehozása
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

Ez a parancs létrehoz egy biztonsági ütemezési alapobjektumot a felhőalapú pillanatkép biztonsági másolatai számára.
A biztonsági másolat minden nap megismétlődik, és a biztonsági másolatok a 100 napokra kerülnek.
Ez az ütemezés az alapértelmezett időponttól, azaz az aktuális időponttól engedélyezve van.

## PARAMÉTEREK

### -BackupType
A biztonságimásolat-típust adja meg.
Az érvényes értékek a következők: LocalSnapshot és CloudSnapshot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Engedélyezve
Azt jelzi, hogy engedélyezi-e a biztonsági ütemtervet.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Egy Azure-profilt ad meg.

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

### -Naptárkivételhez RecurrenceType érték
A biztonságimásolat-ütemterv ismétlődési típusát adja meg.
Az érvényes értékek a következők: 

- Perc
- Óránkénti
- Napi
- Heti

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecurrenceValue
Megadja, hogy milyen gyakran készítsen biztonsági másolatot.
Ez a paraméter a *naptárkivételhez RecurrenceType érték* paraméter által megadott egységet használja.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionCount
A biztonsági másolat megtartására szolgáló napok számát adja meg.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartFromDateTime
A biztonsági másolatok készítésének kezdési dátumát adja meg.
Az alapértelmezett érték az aktuális idő.

```yaml
Type: String
Parameter Sets: (All)
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

### Nincs

## KIMENETEK

### BackupScheduleBase
Ez a parancsmag egy **BackupScheduleBase** objektumot ad eredményül.
Új biztonsági házirend létrehozása **BackupScheduleBase** használatával

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorSimpleDeviceBackupScheduleUpdateConfig](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[Új – AzureStorSimpleDeviceBackupPolicy](./New-AzureStorSimpleDeviceBackupPolicy.md)


