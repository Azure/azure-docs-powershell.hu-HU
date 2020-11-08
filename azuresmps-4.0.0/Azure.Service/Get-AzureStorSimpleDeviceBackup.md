---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016290"
---
# Get-AzureStorSimpleDeviceBackup

## Áttekintés
Biztonsági másolatot kap egy eszközről.

## SZINTAXISA

### Üres (alapértelmezett)
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById2
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject2
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorSimpleDeviceBackup** parancsmag egy eszközről kap biztonsági másolatot.
Megadhatja a biztonsági mentési házirendet, a kötetet és a létrehozási időpontot a biztonsági mentéshez.

Ez a parancsmag legfeljebb 100 biztonsági másolatot adhat vissza az első oldalon.
Ha több mint 100 biztonsági másolat létezik, az *első* és a *kihagyás* paraméter segítségével beolvashatja a további lapokat.
Ha az 100 értékét adja meg *először* a *kihagyás* és az 50 beállításhoz, ez a parancsmag nem az első 100-találatokat adja vissza.
A 50 a 100 után a következő eredményt ad eredményül.

## Példák

### Példa 1: minden biztonsági másolat beszerzése egy eszközön
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

Ez a parancs minden olyan biztonsági másolatot kap, amely a Contoso63-AppVm nevű eszközön található.
Ha az első oldalnál több 100-biztonsági másolat is engedélyezve van, az *első* és a *kihagyás* paraméterrel további eredményeket jeleníthet meg.

### 2. példa: két dátum között létrehozott biztonsági másolatok beolvasása
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

Ez a parancs biztonsági másolatot kap az 10/7/2014 Contoso63-AppVm nevű eszközről, amely a-on vagy a-on vagy a 10/8/2014 előtt lett létrehozva.
Ez a parancsmag kihagyja az első eredményt, és az első eredmény után az első két találatot adja eredményül.
Módosítsa az értékeket az *első* és a *kihagyás* gombra az egyéb találatok megjelenítéséhez.

### 3. példa: biztonsági másolatok készítése biztonsági házirend-AZONOSÍTÓról
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

Ez a parancs biztonsági másolatot kap a megadott napon vagy azt megelőzően létrehozott Contoso63-AppVm nevű eszközről.
A parancs a megadott azonosítót tartalmazó biztonsági házirend használatával létrehozott biztonsági másolatokat kapja.
Ez a parancs az *első* paramétert adja meg, ezért csak az első 10 találatot adja eredményül.

### 4. példa: biztonsági másolatok készítése biztonsági házirend-objektumról
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

Ez a parancs a **Get-AzureStorSimpleDeviceBackupPolicy** parancsmaggal kapja meg a **BackupPolicyDetails** objektumot, majd a pipeline operátor segítségével átadja az adott objektumot az aktuális parancsmagnak.
Ez a parancsmag a parancs első részéből a biztonsági házirend segítségével készít biztonsági másolatokat a Contoso63-AppVm nevű eszközhöz.
A parancs a megadott napon vagy azt megelőzően létrehozott biztonsági másolatokat kapja, ugyanúgy, mint az előző példában.
Ez a parancs csak az első 10 találatot számítja ki.

### Példa 5: biztonsági másolat kérése mennyiségi AZONOSÍTÓhoz
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

Ez a parancs biztonsági másolatot kap a megadott példány-azonosítót tartalmazó köteten létrehozott eszközről.
Ez a parancs az *első* paramétert adja meg, ezért csak az első eredményt adja eredményül.

### 6. példa: biztonsági másolat készítése a kötet nevéről
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

Ez a parancs a **Get-AzureStorSimpleDeviceVolume** parancsmaggal kapja meg a **VirtualDisk** objektumot, majd a pipeline operátor segítségével átadja az adott objektumot az aktuális parancsmagnak.
Ez a parancsmag biztonsági másolatot kap a parancs első részéből a köteten létrehozott Contoso63-AppVm nevű eszközről.
Ez a parancs csak az első eredményt adja eredményül.

## PARAMÉTEREK

### -BackupPolicy
Egy **BackupPolicyDetails** -objektumot ad meg.
Ez a parancsmag az objektum **InstanceId** határozza meg, hogy mely biztonsági másolatok legyenek elérhetők.
Ha **BackupPolicyDetails** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleDeviceBackupPolicy** parancsmagot.

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupPolicyId
A biztonságimásolat-házirendek példányának AZONOSÍTÓját adja meg.
Ez a parancsmag a paraméter által megadott házirendek biztonsági másolatait kapja meg.

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

### -DeviceName
Annak a StorSimple-eszköznek a nevét adja meg, amelyhez biztonsági másolatot szeretne kapni.

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
Annak a biztonsági másolatnak a kezdési dátumát és időpontját adja meg, amelyre a parancsmag eljut.

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

### -To
A parancsmag által beolvasott biztonsági másolatok befejezési dátumát és idejét adja meg.

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

### -Volume
Egy **VirtualDisk** -objektumot ad meg.
Ez a parancsmag az objektum **InstanceId** határozza meg, hogy melyik köteten találhatók a biztonsági másolatok.
Ha **VirtualDisk** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleDeviceVolume** paramétert.

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VolumeId
Annak a kötetnek a példány-AZONOSÍTÓját adja meg, amelyben a biztonsági másolatok találhatók.

```yaml
Type: String
Parameter Sets: IdentifyById2
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

### BackupPolicyDetails, VirtualDisk
Ez a parancsmag elfogadja a **BackupPolicyDetails** és a **VirtualDisk** objektumokat.

## KIMENETEK

### IList\<Backup\>
Ez a parancsmag a **biztonságimásolat** -objektumok listáját számítja ki.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureStorSimpleDeviceBackup](./Remove-AzureStorSimpleDeviceBackup.md)

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)


