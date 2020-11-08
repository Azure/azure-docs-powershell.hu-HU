---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F619B52A-6BFD-43E4-B313-F4C8D95EA966
online version: ''
schema: 2.0.0
ms.openlocfilehash: 570fdc21d650666e1cededbea597a5ef34023596
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015852"
---
# Set-AzureStorSimpleDeviceBackupPolicy

## Áttekintés
Frissít egy meglévő biztonsági házirendet.

## SZINTAXISA

```
Set-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> -BackupPolicyName <String>
 [-BackupSchedulesToAdd <PSObject[]>] [-BackupSchedulesToUpdate <PSObject[]>]
 [-BackupScheduleIdsToDelete <PSObject[]>] [-VolumeIdsToUpdate <PSObject[]>] [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureStorSimpleDeviceBackupPolicy** parancsmag egy meglévő biztonsági házirendet frissít.
Átnevezheti a házirendet, megadhatja, frissítheti vagy törölheti az ütemezéseket, illetve frissítheti a házirendhez társított köteteket.

## Példák

### 1. példa: biztonsági házirend nevének módosítása
```
PS C:\>Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "e6d9f1b3-a250-4d57-966a-039c8eaef9e9" -BackupPolicyName "UpdatedGeneralPolicy07" -WaitForComplete
VERBOSE: ClientRequestId: f4465b46-26cc-40ff-88da-7a28df88c35c_PS
VERBOSE: ClientRequestId: 5e33a35c-e089-47c1-b760-474635b1ead8_PS
VERBOSE: About to run a task to update your backuppolicy! 
VERBOSE: ClientRequestId: e379ebdb-667f-45a9-aafa-a6cd61e5f6f6_PS


JobId        : 9d621bfd-3faa-4d1c-b28b-45c5f4a96975
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: 4fe965ea-4e12-4869-9d67-e42a24b6c5d8_PS
BackupSchedules          : {58e9cd7c-4c6a-4e33-9109-5ec0b8fcb2cc, b10e1bf4-ef0a-4ad3-8fde-eecfc9971dd2}
Volumes                  : {testvolume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 12/16/2014 2:13:28 PM
NextBackup               : 12/16/2014 3:13:43 PM
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : e6d9f1b3-a250-4d57-966a-039c8eaef9e9
Name                     : UpdatedGeneralPolicy07
OperationInProgress      : None
```

Ez a parancs megváltoztatja annak a biztonságimásolat-házirendnek a nevét, amely a UpdatedGeneralPolicy07 megadott azonosítót tartalmazza.
Ez a parancs a *WaitForComplete* paramétert adja meg, így a parancs végrehajtja a feladatot, majd egy **TaskStatusInfo** objektumot ad a tevékenységhez.

### 2. példa: biztonsági mentési házirend ütemezésének frissítése
```
PS C:\>$UpdateConfig = New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "3a6c6247-6b4d-42e2-aa87-16f4f21476ea" -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 3 -RetentionCount 2 -Enabled $True
PS C:\> $UpdateArray = @()
PS C:\> $UpdateArray += $UpdateConfig
PS C:\> Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "712605f6-eb03-4db8-8f79-e0ce64b2cce1" -BackupSchedulesToUpdate $UpdateArray
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 7b265417-a5f1-45ad-8fbc-33bad4f63ec9
JobSteps   : {Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep...} 
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : d2e10d44e699b371a84db44d19daf1c3
```

Az első parancs létrehoz egy Update Configuration objectt a **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** parancsmag használatával, majd a $UpdateConfig változóban tárolja.

A második parancs létrehoz egy új tömbös változót, az $UpdateArray nevűt.
A következő parancs hozzáadja a $UpdateConfigban tárolt frissítést a tömbhöz.
A tömbhöz több frissítést is hozzáadhat.

A végleges parancs frissíti a Contoso63-AppVm nevű eszközön megadott azonosítót tartalmazó biztonsági házirendet.
A házirend most már a $UpdateArray tárolt frissített ütemtervet tartalmazza.

## PARAMÉTEREK

### -BackupPolicyId
A frissítendő **BackupPolicy** objektum PÉLDÁNYának azonosítóját adja meg.

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

### -BackupPolicyName
A biztonságimásolat-házirend új nevét adja meg.

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

### -BackupScheduleIdsToDelete
A törölni kívánt **BackupSchedule** -objektumok példány-azonosítóinak tömbjét adja meg.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackupSchedulesToAdd
A házirendhez hozzáadni kívánt **BackupScheduleBase** -objektumok tömbjét adja meg.
**BackupScheduleBase** -objektum beolvasásához használja a **New-AzureStorSimpleDeviceBackupScheduleAddConfig** parancsmagot.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackupSchedulesToUpdate
A frissítendő **BackupScheduleUpdateRequest** -objektumok tömbjét adja meg.
**BackupScheduleUpdateRequest** -objektum beolvasásához használja a **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** parancsmagot.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Annak a StorSimple-eszköznek a nevét adja meg, amelyre frissíteni szeretné a biztonsági házirendet.

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

### -NewName
Az eszköz nevét adja meg.

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

### -VolumeIdsToUpdate
A kötetek azonosítóit adja meg, amelyekre a biztonsági házirendek frissíthetők.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
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

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Új – AzureStorSimpleDeviceBackupPolicy](./New-AzureStorSimpleDeviceBackupPolicy.md)

[Remove-AzureStorSimpleDeviceBackupPolicy](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[Új – AzureStorSimpleDeviceBackupScheduleUpdateConfig](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)


