---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015566"
---
# Get-AzureStorSimpleDeviceVolume

## Áttekintés
Kötetet kap egy eszközön.

## SZINTAXISA

### IdentifyByParentObject
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureStorSimpleDeviceVolume** parancsmag egy adott mennyiségi tároló vagy a megadott nevű kötet köteteinek listáját kapja meg.
A visszaadott objektum a következő tulajdonságokat tartalmazza: 

- **AccessType**
- **AcrList**
- **AppType**
- **DataContainer**
- **DataContainerId**
- **InstanceId**
- **IsBackupEnabled**
- **IsDefaultBackupEnabled**
- **IsMonitoringEnabled**
- **név**
- **Online**
- **OperationInProgress**
- **SizeInBytes**
- **VSN**

## Példák

### Példa 1: a megadott tárolóban lévő kötetek beolvasása
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

Ez a parancs a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmag segítségével a Container03 nevű kötet tárolóját kapja a Contoso63-AppVm nevű eszközön.
A parancs a pipeline operátor segítségével átadja az adott tárolót az aktuális parancsmagnak.
A parancsmag a Contoso63-AppVm nevű eszközhöz a tárolóban található összes kötetet megkapja.

### 2. példa: kötet beszerzése a neve alapján
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

Ez a parancs a Volume18 nevű kötetet a Contoso63-AppVm nevű eszközön kapja.

## PARAMÉTEREK

### -DeviceName
Annak a StorSimple-eszköznek a nevét adja meg, amelyből a köteteket be szeretné szerezni.

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

### -VolumeContainer
Itt adhatja meg a **DataContainer** -objektumhoz tartozó kötet tárolóját, amely tartalmazza a beolvasott mennyiségeket.
**DataContainer** beszerzéséhez használja a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmagot.

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Kötetnév
A beolvasott kötet nevét adja meg.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### DataContainer
Ez a parancsmag a beolvasott kötetet tartalmazó **DataContainer** -objektumot fogadja el.

## KIMENETEK

### VirtualDisk, IList\<VirtualDisk\>
Ez a parancsmag **VirtualDisk** -objektumot ad eredményül, ha a *kötetnév* paramétert adja meg.
Ha megadja a *VolumeContainer* , ez a parancsmag egy **IList \<VirtualDisk\>** objektumot ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorSimpleDeviceVolume](./New-AzureStorSimpleDeviceVolume.md)

[Remove-AzureStorSimpleDeviceVolume](./Remove-AzureStorSimpleDeviceVolume.md)

[Set-AzureStorSimpleDeviceVolume](./Set-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)


