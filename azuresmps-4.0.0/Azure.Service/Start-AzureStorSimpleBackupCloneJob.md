---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015748"
---
# Start-AzureStorSimpleBackupCloneJob

## Áttekintés
Elindítja azt a feladatot, amely egy eszköz biztonsági másolatát klónja.

## SZINTAXISA

### Üres (alapértelmezett)
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureStorSimpleBackupCloneJob** parancsmag olyan feladatot kezd el, amely egy StorSimple-eszköz meglévő biztonsági másolatát klónja.

## Példák

### Példa 1: biztonsági másolat másolása másik kötetre az eszközök neveivel
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

Az első parancs a **Get-AzureStorSimpleDeviceBackup** parancsmag használatával kapja meg a ContosoDev07 nevű eszköz első biztonsági másolatát.
A parancs a $Backup változóban tárolja a biztonsági másolatot.

A második parancs a **Get-AzureStorSimpleAccessControlRecord** parancsmag használatával érheti el a rekordok vezérlését.
A parancs az eredményt a $Acrs változóban tárolja.

A végleges parancs egy olyan munkafolyamatot kezd el, amely egy eszköz adott kötetének meghatározott biztonsági másolatát ugyanazon eszközön lévő másik kötetre másolta.
Ez a példa megadja az eszközt név szerint.
A parancs a $Backup és a $Acrsban tárolt értékeket használja.
A parancs a feladat AZONOSÍTÓját számítja ki.

### 2. példa: biztonsági másolat másolása másik kötethez az eszközök azonosítói segítségével
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

Az első parancs a **Get-AzureStorSimpleDeviceBackup** parancsmag használatával kapja meg a ContosoDev07 nevű eszköz első biztonsági másolatát.
A parancs a $Backup változóban tárolja a biztonsági másolatot.

A második parancs a **Get-AzureStorSimpleAccessControlRecord** parancsmag használatával érheti el a rekordok vezérlését.
A parancs az eredményt a $Acrs változóban tárolja.

A végleges parancs egy olyan munkafolyamatot kezd el, amely egy eszköz adott kötetének meghatározott biztonsági másolatát ugyanazon eszközön lévő másik kötetre másolta.
Ez a példa az eszköz azonosító szerinti azonosítóját adja meg.
A parancs a $Backup és a $Acrsban tárolt értékeket használja.
A parancs a feladat AZONOSÍTÓját számítja ki.

### 3. példa: biztonsági másolatok másolása egy másik eszközön lévő kötetre az eszközök neveivel
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

Az első parancs a **Get-AzureStorSimpleDeviceBackup** parancsmag használatával kapja meg a ContosoDev07 nevű eszköz első biztonsági másolatát.
A parancs a $Backup változóban tárolja a biztonsági másolatot.

A második parancs a **Get-AzureStorSimpleAccessControlRecord** parancsmag használatával érheti el a rekordok vezérlését.
A parancs az eredményt a $Acrs változóban tárolja.

A végleges parancs egy olyan munkafolyamatot kezd el, amely a kötet egy másik eszközön lévő kötetének meghatározott biztonsági másolatát az eszközön lévő kötetre másolta.
Ez a példa megadja az eszközöket név szerint.
A parancs a $Backup és a $Acrsban tárolt értékeket használja.
A parancs a feladat AZONOSÍTÓját számítja ki.

### Példa 4: biztonsági másolat másolása másik kötetre az eszközök neveivel és a csővezeték-kezelővel
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

Az első parancs a **Get-AzureStorSimpleDeviceBackup** parancsmag használatával kapja meg a ContosoDev07 nevű eszköz első biztonsági másolatát.
A parancs a $Backup változóban tárolja a biztonsági másolatot.

A második parancs a **Get-AzureStorSimpleAccessControlRecord** parancsmag használatával érheti el a rekordok vezérlését.
A parancs a csővezeték-kezelő segítségével átadja az eredményét az aktuális parancsmagnak.
Az aktuális parancsmag egy olyan feladatot kezd el, amely egy eszközön lévő kötet meghatározott biztonsági másolatát egy másik kötetre másolta ugyanazon az eszközön.
Ez a példa megadja az eszközt név szerint.
A parancs a $Backupban tárolt értéket használja.
A parancs a *TargetAccessControlRecords* paraméter értékét a csővezetékről veszi át.
A parancs a feladat AZONOSÍTÓját számítja ki.

## PARAMÉTEREK

### -BackupId
A klónozás biztonsági másolatának példányát adja meg.

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

### -CloneVolumeName
A céleszköz új klónozott kötetének nevét adja meg.

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
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -Snapshot
Annak a pillanatkép-objektumnak a meghatározása, amelyet a parancsmag klónja tartalmaz.

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDeviceId
A forrás eszköz példány-AZONOSÍTÓját adja meg.
Ezzel a parancsmaggal a program visszamásolja a forrást az eszközről.

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

### -SourceDeviceName
A forrás eszköz nevét adja meg.
Ezzel a parancsmaggal a program visszamásolja a forrást az eszközről.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAccessControlRecords
A hozzáférés-vezérlési rekordokat adja meg.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TargetDeviceId
A céleszköz példányának AZONOSÍTÓját adja meg.

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

### -TargetDeviceName
Annak az eszköznek a nevét adja meg, amelyre a parancsmag klónja a biztonsági másolatot.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Pillanatkép a AccessControlRecord listájáról
Ezt a parancsmagot kikapcsolhatja a **AccessControlRecord** **-objektumok vagy** a hozzájuk tartozó objektumok listájával.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)


