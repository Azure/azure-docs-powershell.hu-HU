---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015558"
---
# Get-AzureStorSimpleJob

## Áttekintés
Megkapja a StorSimple munkákat.

## SZINTAXISA

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureStorSimpleJob** parancsmag Azure StorSimple-feladatokat kap.
Adjon meg egy példány-azonosítót egy adott feladat beszerzéséhez.
Adjon meg további paramétereket a parancsmag által kapott feladatok korlátozásához.

Ez a parancsmag legfeljebb 200 feladatot ad eredményül.
Ha több mint 200-feladatot tartalmaz, a hátralévő feladatokat az *első* és a *kihagyás* paraméter segítségével érheti el.
Ha az 100 értékét adja meg *először* a *kihagyás* és az 50 beállításhoz, ez a parancsmag nem az első 100-találatokat adja vissza.
A 50 a 100 után a következő eredményt ad eredményül.

## Példák

### Példa 1: feladat beszerzése azonosító használatával
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

Ez a parancs a megadott azonosítót tartalmazó feladatra vonatkozó információkat tartalmaz.

### 2. példa: a feladatok eszköz nevének beszerzése
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

Ez a parancs a 8600-Bravo 001 nevű eszközhöz tartozó feladatok adatait kapja meg.
A parancs az első két feladatot kapja az eszközhöz.

### 3. példa: Befejezett feladatok beszerzése
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

Ez a parancs befejezte a feladatok elvégzését.
A parancs csak az első két feladatot kapja, miután az első tíz feladatot kihagyja.

### Példa 4: kézi mentési feladatok kérése
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

Ez a parancs a kézi biztonsági másolat típusának megfelelő feladatokat kapja.

### Példa 5: a feladatok beszerzése a megadott időpontok között
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

Az első két parancs a **datetime** -objektumokat hozza létre a Get-Date parancsmag használatával.
A parancsok az új időpontokat tárolják a $StartTime és $EndTime változókban.
További információért írja be a következőt: `Get-Help Get-Date` .

A végleges parancs a Device07 nevű eszköznek a $StartTime-ban és a $EndTime-ban tárolt idő között kap munkahelyeket.

## PARAMÉTEREK

### -DeviceName
Egy StorSimple-eszköz nevét adja meg.

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

### – Első
Csak a megadott számú objektumot kapja meg.
Adja meg a bejutni kívánt objektumok számát.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -From
A parancsmag által kapott feladatok kezdési dátumát és idejét adja meg.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
A beolvasott feladat AZONOSÍTÓját adja meg.

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

### -Skip (kihagyás)
Figyelmen kívül hagyja a megadott számú objektumot, majd Kinyeri a fennmaradó objektumokat.
Adja meg, hogy hány objektum legyen kihagyva.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Állapot
Az állapotot adja meg.
A paraméter elfogadható értékei a következők:

- Fut
- Kész
- Lemondott
- Sikertelen
- Megszüntetésével lehet megszüntetni
- CompletedWithErrors

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

### -To
A parancsmag által kapott feladatok befejezési dátumát és idejét adja meg.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type (típus)
A feladattípust adja meg.
A paraméter elfogadható értékei a következők:

- Hát
- ManualBackup
- Visszaállítása
- CloneWorkflow
- DeviceRestore
- Frissítés
- SupportPackage
- VirtualApplianceProvisioning

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
Ebben a parancsmagban nem lehet beírni a bemenetet.

## KIMENETEK

### IList \<DeviceJobDetails\> , DeviceJobDetails
Ez a parancsmag a projektfeladat-adatobjektumok listáját adja eredményül, vagy ha a *InstanceId* paramétert adja meg, akkor az egyetlen feladat részlet objektumot adja eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Stop-AzureStorSimpleJob](./Stop-AzureStorSimpleJob.md)


