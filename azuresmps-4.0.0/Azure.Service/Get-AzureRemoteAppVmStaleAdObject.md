---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015630"
---
# Get-AzureRemoteAppVmStaleAdObject

## Áttekintés
Az Azure Active Directory olyan objektumait kapja, amelyek már nem léteznek az Azure RemoteApp virtuális gépekkel társítva.

## SZINTAXISA

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRemoteAppVmStaleAdObject** parancsmag az Azure Active Directory olyan objektumait kapja, amelyek már nem léteznek az Azure RemoteApp virtuális gépekhez társítva.
Ez a parancsmag a kapott objektumok nevét jeleníti meg.

## Példák

### Példa 1: régi objektumok beszerzése gyűjteményhez
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

Ez a második parancs a contoso nevű gyűjtemény elavult objektumait kapja meg.

## PARAMÉTEREK

### -CollectionName
Az Azure RemoteApp-gyűjtemény nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hitelesítő adatok
A művelet végrehajtásához szükséges jogosultságokat adja meg.
Ha **PSCredential** objektumot szeretne beolvasni, használja a **Get-hitelesítőadat** parancsmagot.
Ha nem adja meg ezt a paramétert, ez a parancsmag az aktuális felhasználó hitelesítő adatait használja.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

## KIMENETEK

### Karakterlánc

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Clear-AzureRemoteAppVmStaleAdObject](./Clear-AzureRemoteAppVmStaleAdObject.md)


