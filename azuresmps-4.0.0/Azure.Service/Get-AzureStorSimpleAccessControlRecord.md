---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016552"
---
# Get-AzureStorSimpleAccessControlRecord

## Áttekintés
A szolgáltatás-konfigurációban hozzáférés-vezérlési rekordokat kap.

## SZINTAXISA

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorSimpleAccessControlRecord** parancsmag hozzáférés-vezérlési rekordokat kap a StorSimple-kezelő szolgáltatás konfigurációjában.
Ez a parancsmag minden rekordot vagy névvel ellátott rekordot kap.

A hozzáférés-vezérlési rekordok az iSCSI-kezdeményező paramétereinek tárolói.
Ezek a paraméterek azt adják meg, hogy mely kezdeményezők érhetik el a kötetet.
Ha egy iSCSI-kezdeményező megkísérel kapcsolódni egy kötethez, a készülék ellenőrzi a kötethez rendelt hozzáférés-vezérlési rekordokat.
Ha az iSCSI-kezdeményező paraméterei megegyeznek az adott kötethez rendelt Access-vezérlők rekordjainak egyikével, az iSCSI-kezdeményező csatlakozni tud.

## Példák

### Példa 1: a hozzáférés-vezérlési rekordok beszerzése
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

Ez a parancs a hozzáférés-vezérlési rekordokat kapja meg.

### 2. példa: speciális hozzáférés-szabályozási rekord beszerzése
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

Ez a parancs a Acr11 nevű hozzáférés-vezérlési rekordot kapja meg.

## PARAMÉTEREK

### -ACRName
A beolvasott hozzáférés-vezérlési rekord nevét adja meg.

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

### AccessControlRecord, IList\<AccessControlRecord\>
Ez a parancsmag egy **AccessControlRecord** -objektumot vagy **egy \<AccessControlRecord\> IList** objektumot ad eredményül.
A **AccessControlRecord** -objektumok az alábbi mezőket tartalmazzák: 

- **GlobalId** ( **karakterlánc** ) 
- **InitiatorName** ( **karakterlánc** ) 
- **InstanceId** ( **karakterlánc** ) 
- **Name** ( **karakterlánc** ) 
- **OperationInProgress** ( **OperationInProgress** ) 
- **VolumeCount** ( **int** )

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Remove-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)


