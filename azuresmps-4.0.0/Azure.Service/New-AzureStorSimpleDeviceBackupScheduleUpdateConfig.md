---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015524"
---
# New-AzureStorSimpleDeviceBackupScheduleUpdateConfig

## Áttekintés
Biztonságimásolat-ütemezett frissítési konfigurációs objektum létrehozása.

## SZINTAXISA

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** parancsmag létrehoz egy **BackupScheduleUpdateRequest** konfigurációs objektumot.
Ezzel a konfigurációs objektummal frissítheti a biztonságimásolat-házirendet a **set-AzureStorSimpleDeviceBackupPolicy** parancsmag használatával.

## Példák

### Példa 1: ütemterv frissítési kérésének létrehozása
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

Ez a parancs létrehoz egy biztonságimásolat-ütemterv frissítési kérését a megadott azonosítót tartalmazó ütemtervhez.
A kérés célja, hogy egy olyan felhőalapú pillanatkép-biztonsági másolatot készítsen, amely óránként ismétlődik.
A biztonsági másolatok 50 napra megmaradnak.
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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
A frissítendő biztonsági ütemterv példányának AZONOSÍTÓját adja meg.

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

### BackupScheduleUpdateRequest
Ez a parancsmag egy **BackupScheduleUpdateRequest** objektumot ad eredményül, amely a frissített biztonsági ütemtervekre vonatkozó információkat tartalmazza.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)


