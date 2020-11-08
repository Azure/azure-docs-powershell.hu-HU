---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016467"
---
# Remove-AzureStorSimpleDeviceBackup

## Áttekintés
Törli a biztonsági másolatot tartalmazó objektumot.

## SZINTAXISA

### IdentifyById (alapértelmezett)
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureStorSimpleDeviceBackup** parancsmag egyetlen biztonságimásolat-objektumot töröl.
Ha már törölt biztonsági másolatot próbál törölni, ez a parancsmag hibát jelez.

## Példák

### 1. példa: biztonsági másolat eltávolítása az eszközről
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

Ez a parancs eltávolítja a Contoso63-AppVm nevű eszközhöz megadott azonosítót tartalmazó biztonsági másolatot.
A parancs elindítja azt a műveletet, amely eltávolítja a **biztonságimásolat** -objektumot, majd egy **TaskResponse** objektumot ad eredményül.
A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.

### 2. példa: az eszköz első biztonsági másolatának eltávolítása az azonosító használatával
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

Az első parancs a Contoso63-AppVm nevű eszköz biztonsági másolatait kapja, majd a $Backup változóban tárolja őket.

A második parancs törli az Contoso63-AppVm nevű eszköz biztonsági másolatát.
A parancs normál képpont jelöléssel hivatkozik a $Backup tömb első eleme **InstanceId** tulajdonságára.
Ez a parancs a *WaitForComplete* paramétert adja meg, ezért a parancs mindaddig megvárja, amíg a művelet be nem fejeződik, majd egy **TaskStatusInfo** objektumot ad eredményül.

### 3. példa: az eszköz első biztonsági másolatának eltávolítása a csővezeték használatával
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

Az első parancs a Contoso63-AppVm nevű eszköz biztonsági másolatait kapja, majd a $Backup változóban tárolja őket.

A második parancs átadja az első objektumot a $Backup tömbben az aktuális parancsmaghoz.
Ez a parancsmag törli azt a biztonsági másolatot a Contoso63-AppVm nevű eszközről.
Ez a parancs a *WaitForComplete* paramétert adja meg, ezért a parancs mindaddig megvárja, amíg a művelet be nem fejeződik, majd egy **TaskStatusInfo** objektumot ad eredményül.

## PARAMÉTEREK

### -Backup
A törlendő **biztonságimásolat** -objektumot adja meg.
**Biztonsági másolat készítéséhez** használja a **Get-AzureStorSimpleDeviceBackup** parancsmagot.

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupId
A törlendő biztonsági másolat példányának AZONOSÍTÓját adja meg.

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
Annak a StorSimple-eszköznek a nevét adja meg, amelyen törölni szeretne egy biztonsági másolatot.

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

### Hát

## KIMENETEK

### TaskStatusInfo, TaskResponse
Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg, ha nem adja meg ezt a paramétert, hanem egy **TaskResponse** objektumot ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)


