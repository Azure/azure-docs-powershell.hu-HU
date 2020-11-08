---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 049201C9-590F-47EB-9030-25F80CD8DFA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f3337556a9d7bd52e5800af5cdbd65b71ab9818
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015523"
---
# New-AzureStorSimpleDeviceVolume

## Áttekintés
Kötetet hoz létre a megadott mennyiségi tárolóban.

## SZINTAXISA

```
New-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer> -VolumeName <String>
 -VolumeSizeInBytes <Int64>
 -AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>
 -VolumeAppType <AppType> -Online <Boolean> -EnableDefaultBackup <Boolean> -EnableMonitoring <Boolean>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorSimpleDeviceVolume** parancsmag egy kötetet hoz létre egy megadott mennyiségi tárolóban.
Ez a parancsmag minden kötethez társít egy vagy több hozzáférés-vezérlési rekordot.
Ha **AccessControlRecord** -objektumokat szeretne beolvasni, használja a **Get-AzureStorSimpleAccessControlRecord** parancsmagot.
Adjon meg egy nevet, méretet és AppType a kötethez.
Azt is megadhatja, hogy az online kötetet szeretné-e létrehozni, legyen szó akár az alapértelmezett biztonsági mentés engedélyezéséről, akár a figyelés engedélyezéséről.

## Példák

### Példa 1: kötet létrehozása
```
PS C:\>$AcrList = Get-AzureStorSimpleAccessControlRecord
PS C:\> Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer07" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Size 2000000000 -AccessControlRecords $AcrList -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False

VERBOSE: ClientRequestId: a29d1a84-1f81-4f20-9130-7adfe45e41fb_PS
VERBOSE: ClientRequestId: 8fa63df1-3f81-4029-a536-b536a70068ad_PS
VERBOSE: ClientRequestId: 964c5744-8bb1-4f70-beda-95ca4c7f3eb6_PS
VERBOSE: ClientRequestId: f09fff3a-54fa-4a0e-93db-b079260ed2dd_PS
VERBOSE: ClientRequestId: 59aa29e3-8044-411a-adae-b64a2681ffed_PS
VERBOSE: ClientRequestId: 0ffd0297-19be-40fe-a64e-6a2947d831b4_PS
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90 for tracking the task's status
VERBOSE: Volume container with name: VolumeContainer07 is found.
```

Az első parancs a **Get-AzureStorSimpleAccessControlRecord** parancsmaggal kapja meg a hozzáférés-vezérlési rekordokat az StorSimple-kezelő szolgáltatás beállításai között, majd a $AcrList változóban tárolja őket.

A második parancs a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmaggal kapja meg a VolumeContainer07 nevű kötet tárolóját a Contoso63-AppVm nevű eszközhöz.
A parancs átadja az adott tárolót az aktuális parancsmagnak a pipeline operátor használatával.
Ezzel a parancsmaggal létrehozhatja a hangerőt.
A parancs a $AcrListban tárolt kötet, méret és hozzáférés-vezérlési rekordok nevét adja meg.
Ez a parancs elindítja a feladatot, majd egy **TaskResponse** objektumot ad eredményül.
A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.

### 2. példa: kötet létrehozása Access-Controlaccess vezérlő recordsaccess-vezérlő nélkül
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer01" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume22" -Size 2000000000 -AccessControlRecords @() -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False -WaitForComplete
VERBOSE: ClientRequestId: 3f359790-7e1f-48e7-acf8-ecabba850966_PS
VERBOSE: ClientRequestId: 2723ebcf-cd72-47bb-99b5-0c099d45641b_PS
VERBOSE: ClientRequestId: e605091f-dd63-42a7-bda2-24753cbc1f9a_PS
VERBOSE: ClientRequestId: b3fd08c3-67c5-4309-9591-15d92c360469_PS
VERBOSE: ClientRequestId: 15a024a3-b0c9-4f83-9c34-0ed8b95d024b_PS
VERBOSE: ClientRequestId: c13f92f9-aea1-40dd-af80-3affe273adbe_PS


TaskId       : ceef657e-390e-4f7a-aab7-669a29c29e7f
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 1d79febf-f752-4255-af2d-230d40773bc6_PS
AccessType             : NoAccess
AcrIdList              : {}
AcrList                : {}
AppType                : PrimaryVolume
DataContainer          : Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainer
DataContainerId        : 68b63d15-6aa5-4e69-9f9d-4a0bc607d6e9
InstanceId             : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd
InternalInstanceId     : 
IsBackupEnabled        : False
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
Name                   : Volume22
Online                 : True
OperationInProgress    : None
SizeInBytes            : 2000000000
VSN                    : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd

VERBOSE: Volume container with name: VolumeContainer01 is found.
```

Ez a parancs a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmaggal kapja meg a VolumeContainer01 nevű kötet tárolóját a Contoso63-AppVm nevű eszközhöz.
A parancs átadja az adott tárolót az aktuális parancsmagnak a pipeline operátor használatával.
Ezzel a parancsmaggal létrehozhatja a hangerőt.
A parancs a kötet nevét, a méretet és a hozzáférés-vezérlési rekordok üres értékét adja meg.
Ez a parancs a *WaitForComplete* paramétert adja meg, így a kötet létrehozása után egy **TaskStatusInfo** ad eredményül.

Mivel a parancs nem tud hozzáférés-vezérlési rekordokat megadni, ez a kötet nem érhető el.
A **set-AzureStorSimpleDeviceVolume** parancsmaggal később is hozzáadhat hozzáférést.

## PARAMÉTEREK

### -AccessControlRecords
A kötethez társítani kívánt hozzáférés-vezérlési rekordok listáját adja meg.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceName
Annak a StorSimple-eszköznek a nevét adja meg, amelybe a kötetet létre szeretné hozni.

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

### -EnableDefaultBackup
Megadja, hogy engedélyezve van-e az alapértelmezett biztonsági másolat a köteten.

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

### -EnableMonitoring
Itt adhatja meg, hogy engedélyezi-e a kötet figyelését.

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

### -Online
Itt adhatja meg, hogy az online kötetet szeretné-e létrehozni.

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

### -VolumeAppType
Itt adhatja meg, hogy elsődleges vagy archív kötetet szeretne-e létrehozni.
Az érvényes értékek a következők: PrimaryVolume és ArchiveVolume.

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumeContainer
A tárolót **DataContainer** objektumként adja meg, amelybe a kötetet hozza létre.
Ha **VirtualDisk** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmagot.

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Kötetnév
Az új kötet nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumeSizeInBytes
A kötet méretét adja meg bájtban.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

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

### DataContainer, lista\<AccessControlRecord\>
Ez a parancsmag elfogadja a **DataContainer** objektumot és az új kötet **AccessControlRecord** objektumait.

## KIMENETEK

### TaskStatusInfo
Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[Remove-AzureStorSimpleDeviceVolume](./Remove-AzureStorSimpleDeviceVolume.md)

[Set-AzureStorSimpleDeviceVolume](./Set-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


