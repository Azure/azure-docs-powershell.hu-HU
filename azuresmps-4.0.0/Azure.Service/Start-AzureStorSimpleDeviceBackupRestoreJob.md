---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015747"
---
# Start-AzureStorSimpleDeviceBackupRestoreJob

## Áttekintés
Elindítja azt a feladatot, amely egy StorSimple-eszköz biztonsági másolatát Visszaállítja.

## SZINTAXISA

### Üres (alapértelmezett)
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureStorSimpleDeviceBackupRestoreJob** parancsmag olyan feladatot kezd el, amely visszaállítja a StorSimple-eszközök biztonsági másolatát.
Adja meg a biztonságimásolat-azonosítót és a választható pillanatkép-azonosítót.

## Példák

### 1. példa: feladat indítása a biztonsági másolat visszaállításához
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

Ez a parancs elindítja azt a feladatot, amely visszaállítja a megadott azonosítót tartalmazó biztonságimásolat-objektumot és a hozzá tartozó pillanatképeket az Contoso63-AppVm nevű eszközön.
A parancs a *WaitForComplete* paramétert adja meg, így a feladat befejeződött, mielőtt a parancsmag a vezérlőt visszaadja a konzolnak.

### 2. példa: feladat indítása egy adott pillanatkép visszaállításához
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

Ez a parancs elindítja azt a feladatot, amely visszaállítja a megadott azonosítót tartalmazó biztonságimásolat-pillanatfelvételt.
A parancs azt adja meg, hogy a Contoso63-AppVm nevű eszközben a biztonsági másolat objektum AZONOSÍTÓval rendelkezik-e.
A parancs az *erő* paramétert adja meg, ezért a feladatot a megerősítést kérő üzenet nélkül indítja el.

## PARAMÉTEREK

### -BackupId
A visszaállítandó biztonsági másolat példányának AZONOSÍTÓját adja meg.

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

### -DeviceName
Annak a StorSimple-eszköznek a nevét adja meg, amelyen a biztonsági másolat létezik.

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

### -Force
Azt jelzi, hogy ez a parancsmag nem kér megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
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

### -SnapshotId
A visszaállítandó pillanatkép példányának AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.

```yaml
Type: SwitchParameter
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

### TaskStatusInfo, TaskResponse
Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.
Ha nem adja meg ezt a paramétert, az eredmény egy **TaskResponse** -objektumot ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)

[Start-AzureStorSimpleDeviceBackupJob](./Start-AzureStorSimpleDeviceBackupJob.md)


