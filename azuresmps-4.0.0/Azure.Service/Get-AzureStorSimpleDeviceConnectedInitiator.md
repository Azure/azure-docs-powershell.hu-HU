---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016291"
---
# Get-AzureStorSimpleDeviceConnectedInitiator

## Áttekintés
Elérhetővé válik az iSCSI-kapcsolatok StorSimple-eszközön.

## SZINTAXISA

### IdentifyById
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureStorSimpleDeviceConnectedInitiator** parancsmag a StorSimple-eszközökhöz elérhető iSCSI-kapcsolatok listáját kapja meg.
A parancsmag által visszaadott iSCSI-kapcsolati objektumok a következő tulajdonságokat tartalmazzák:

- **AcrInstanceId**
- **AcrName**
- **AllowedVolumeNames**
- **InitiatorAddress**
- **Felületek**
- **IQN**
- **IscsiConnectionId**

Ez a parancsmag csak akkor kapja meg a kapcsolat objektumot, ha az eszközön be van kapcsolva az iSCSI-kapcsolatok.
A kapcsolatok alapértelmezés szerint ki vannak kapcsolva.

## Példák

### Példa 1: egy eszköz minden kapcsolatának lekérése
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

Ez a parancs a Contoso63-AppVm nevű eszköz minden iSCSI-kapcsolatát bekapja.
Ez a parancs csak akkor ad visszaadott kapcsolatokat, ha a kapcsolat be van kapcsolva az eszközön.

## PARAMÉTEREK

### -DeviceId
Annak az StorSimple-eszköznek a példány-AZONOSÍTÓját adja meg, amelyből az iSCSI-kezdeményezőket be szeretné szerezni.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Annak a StorSimple-eszköznek a neve, amelyből az iSCSI-kezdeményezőket be kell szerezni.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Lista\<IscsiConnection\>
Ez a parancsmag egy olyan iSCSI-kapcsolati objektumot ad eredményül, amely a következő tulajdonságokat tartalmazza: 

- **AcrInstanceId**
- **AcrName**
- **AllowedVolumeNames**
- **InitiatorAddress**
- **Felületek**
- **IQN**
- **IscsiConnectionId**

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)


