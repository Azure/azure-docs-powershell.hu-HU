---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5AB916CB-A141-4662-8220-6C1FBB58FC69
online version: ''
schema: 2.0.0
ms.openlocfilehash: aab5e0f3ef432333eeb4aff68673c0d5c2219521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016464"
---
# Remove-AzureStorSimpleDeviceBackupPolicy

## Áttekintés
Eltávolít egy meglévő biztonsági házirendet.

## SZINTAXISA

### IdentifyById (alapértelmezett)
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureStorSimpleDeviceBackupPolicy** parancsmag eltávolítja a meglévő **BackupPolicy** -objektumokat.
Miután eltávolította a biztonsági házirendet, az adott házirend alapján további biztonsági másolatokat nem kell mentenie.
Ez a parancsmag a törölt házirendhez társított összes ütemtervet is törli.

## Példák

### 1. példa: biztonsági házirend eltávolítása
```
PS C:\>Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "03710b4c-82c1-40ca-be5c-40289dc49642" -Force
VERBOSE: ClientRequestId: b3e4d485-eae4-4cf4-a43b-815f3abcd2dd_PS
VERBOSE: ClientRequestId: a260ee98-46aa-49e0-91ac-31d4155f4cae_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: 92a9c264-90df-4345-a495-92767dd266f2_PS
695be190-ac81-4cf2-b1c5-03ef6b08d005
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
695be190-ac81-4cf2-b1c5-03ef6b08d005 for tracking the task's status
```

Ez a parancs eltávolítja azt a **BackupPolicy** , amely a példány-azonosítóval rendelkezik, így a rendszer nem készít további biztonsági másolatokat a 03710b4c-82c1-40Ca-be5c-40289dc49642.
A parancs törli az ehhez a házirendhez társított összes ütemtervet is.
A parancs elindítja azt a műveletet, amely eltávolítja a **BackupPolicy** objektumot, majd egy **TaskResponse** objektumot ad eredményül.
A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.

### 2. példa: az eszközre vonatkozó biztonságimásolat-házirendek első részének eltávolítása
```
PS C:\>$Policies = Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId $Policies[0].InstanceId -Force -WaitForComplete
VERBOSE: ClientRequestId: db3b49fa-cffa-446d-ba52-daa6802e00f7_PS
VERBOSE: ClientRequestId: 70e2b56f-c2df-40d0-a1e5-d7a4d7e25962_PS
VERBOSE: About to run a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: f8eb3d4d-2c57-4fc9-9f40-79d0f2ea1b6a_PS


JobId        : 820a246e-54b6-41a9-bdd5-15d5daea9b0a
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your remove operation has completed successfully.
```

Az első parancs a Contoso63-AppVm nevű eszköz biztonságimásolat-házirendjeit kapja, majd a $Policies változóban tárolja őket.

A második parancs eltávolítja az első biztonsági házirendet a Contoso63-AppVm.
A parancs a standard dot szintaxist használja a $Policies első elemének **InstanceId** tulajdonságának meghatározására.
Ez a parancs a *WaitForComplete* paramétert adja meg, így a parancs végrehajtja a feladatot, majd egy **TaskStatusInfo** objektumot ad a tevékenységhez.

### 3. példa: biztonsági házirend eltávolítása a csővezeték használatával
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQAVolume01_Default" | Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -Force -WaitForComplete
VERBOSE: ClientRequestId: 60080fb1-2f88-4c17-bfd7-21aa73440a9c_PS
VERBOSE: ClientRequestId: 04c91121-50d7-4796-9af6-fc6a7d6b6a0e_PS
VERBOSE: ClientRequestId: 47ceb37c-672f-42e8-bd19-1190925c46cd_PS
VERBOSE: ClientRequestId: cbc39757-f2cc-4cc5-93ea-4ec0fbfb0ca8_PS
VERBOSE: ClientRequestId: 3614d47a-51fc-4500-a5f1-5401301ca4e3_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: dbd7166e-1888-4b11-9af9-8d49712a8c8b_PS
702ad240-5730-4015-b051-56055bd2c2d3
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
702ad240-5730-4015-b051-56055bd2c2d3 for tracking the task's status
VERBOSE: BackupPolicy with id bfe0bf8a-2d09-4690-93da-38a4f24e9f4f found!
```

Ez a parancs beolvassa a **BackupPolicyDetails** objektumot a **Get-AzureStorSimpleDeviceBackupPolicy** függvénnyel, majd a pipeline operátor segítségével átadja az aktuális parancsmagnak.
Az aktuális parancsmag eltávolítja a TSQAVolume01_Default nevű biztonsági házirendet.

## PARAMÉTEREK

### -BackupPolicy
A törlendő **BackupPolicyDetails** objektumot adja meg.
Ha **BackupPolicyDetails** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleDeviceBackupPolicy** parancsmagot.

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupPolicyId
A törlendő **BackupPolicy** objektum PÉLDÁNYának azonosítóját adja meg.

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
Annak a StorSimple-eszköznek a nevét adja meg, amelyen törölni szeretné a biztonsági házirendet.

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

### BackupPolicyDetails
Ez a parancsmag a törölni kívánt **BackupPolicyDetails** objektumot fogadja.

## KIMENETEK

### TaskStatusInfo, TaskResponse
Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.
Ha nem adja meg ezt a paramétert, az eredmény egy **TaskResponse** -objektumot ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Új – AzureStorSimpleDeviceBackupPolicy](./New-AzureStorSimpleDeviceBackupPolicy.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


