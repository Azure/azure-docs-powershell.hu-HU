---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016208"
---
# New-AzureStorSimpleDeviceBackupPolicy

## Áttekintés
Biztonsági házirendet hoz létre.

## SZINTAXISA

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureStorSimpleDeviceBackupPolicy** parancsmag biztonsági mentési házirendet hoz létre.
A biztonsági házirend egy vagy több köteten futtatható biztonsági ütemtervet tartalmaz.
Ha biztonsági ütemtervet szeretne létrehozni, használja a **New-AzureStorSimpleDeviceBackupScheduleAddConfig** parancsmagot.

## Példák

### 1. példa: biztonsági házirend létrehozása
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

Az első parancs a **New-AzureStorSimpleDeviceBackupScheduleAddConfig** parancsmaggal hozza létre a biztonsági ütemterv konfigurációs objektumát, majd az $Schedule 01 változóban tárolja az objektumot.

A második parancs új biztonsági konfigurációs objektumot hoz létre a **New-AzureStorSimpleDeviceBackupScheduleAddConfig** használatával, majd az objektumot a $Schedule 02 változóban tárolja.

A harmadik parancs létrehozza a $ScheduleArray nevű üres tömbös változót.
A következő két parancs hozzáadja az első két parancsban létrehozott objektumokat a $ScheduleArrayhoz.

A hatodik parancs a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmag használatával kapja meg a Contoso63-AppVm nevű eszköz mennyiségi tárolóját, majd a tároló objektumot a $DeviceContainer változóban tárolja.

A hetedik parancs a **Get-AzureStorSimpleDeviceVolume** parancsmaggal az $DeviceContainer első tagjában tárolt mennyiségi tároló kötetét kapja, majd a $Volume változóban tárolja a kötetet.

A nyolcadik parancs létrehozza az $VolumeArray nevű üres tömbös változót.
A következő parancs mennyiségi azonosítót ad a $VolumeArrayhoz.
Ez az érték azonosítja azt a kötetet, amelyet a biztonsági házirend futásakor $Volume tárolnak.
További mennyiségi azonosítókat is hozzáadhat a $VolumeArrayhoz.

A végleges parancs létrehozza a GeneralPolicy07 nevű biztonsági mentési házirendet a Contoso63-AppVm nevű eszközhöz.
A parancs a $ScheduleArrayban tárolt konfiguráció-objektumok ütemezését adja meg.
A parancs azt a kötetet vagy köteteket adja meg, amelyekre a házirendet alkalmazni szeretné $VolumeArrayben.
Ellenőrizheti a biztonságimásolat-házirendet a **Get-AzureStorSimpleDeviceBackupPolicy** parancsmag használatával.

## PARAMÉTEREK

### -BackupPolicyName
A biztonságimásolat-házirend nevét adja meg.

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

### -BackupSchedulesToAdd
A házirendhez hozzáadni kívánt **BackupScheduleBase** -objektumok tömbjét adja meg.
Minden objektum ütemtervet képvisel.
A biztonságimásolat-házirend egy vagy több ütemtervet tartalmaz.
**BackupScheduleBase** -objektum beolvasásához használja a **New-AzureStorSimpleDeviceBackupScheduleAddConfig** parancsmagot.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Annak a StorSimple-eszköznek a nevét adja meg, amelyen létre szeretné hozni a biztonsági házirendet.

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

### -VolumeIdsToAdd
A biztonságimásolat-házirendhez hozzáadni kívánt kötetek azonosítóinak tömbjét adja meg.

```yaml
Type: PSObject[]
Parameter Sets: (All)
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

### BackupPolicy
Ez a parancsmag egy **BackupPolicy** objektumot ad eredményül, amely az új ütemterveket és köteteket tartalmazza.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceBackupPolicy](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[Új – AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


