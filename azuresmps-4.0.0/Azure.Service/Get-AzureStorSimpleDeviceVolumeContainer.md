---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015563"
---
# Get-AzureStorSimpleDeviceVolumeContainer

## Áttekintés
Mennyiségi tárolókat kap egy eszközön.

## SZINTAXISA

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorSimpleDeviceVolumeContainer** parancsmag az eszközön lévő mennyiségi tárolók listáját, illetve a megadott nevű kötet-tárolót kapja meg.
A visszaadott objektum a következő tulajdonságokat tartalmazza: 

- **BandwidthRate**
- **EncryptionKey**
- **InstanceId**
- **IsDefault**
- **IsEncryptionEnabled**
- **név**
- **OperationInProgress**
- **Tulajdonú**
- **PrimaryStorageAccountCredential**
- **SecretsEncryptionThumbprint**
- **VolumeCount**

## Példák

### 1. példa: eszközön lévő összes tároló lekérése
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

Ez a parancs a 8600-Bravo 001 nevű eszközön található mennyiségi tárolók listáját kapja meg.

### 2. példa: tároló beszerzése a neve alapján
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

Ez a parancs a Container08 nevű kötet tárolót kapja a Contoso63-AppVm nevű eszközön.

## PARAMÉTEREK

### -DeviceName
Egy StorSimple-eszköz nevét adja meg.
Ez a parancsmag a mennyiségi tárolókat az eszközről kapja, amelyet a paraméter határoz meg.

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

### -VolumeContainerName
A beolvasott kötet tárolójának nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### DataContainer, IList\<DataContainer\>
Ez a parancsmag **DataContainer** -objektumot ad eredményül, ha a *VolumeContainerName* paramétert adja meg.
Ha nem adja meg ezt a paramétert, ez a parancsmag **egy \<DataContainer\> IList** -objektumot ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorSimpleDeviceVolumeContainer](./New-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceVolumeContainer](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


