---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015703"
---
# Clear-AzureRemoteAppVmStaleAdObject

## Áttekintés
Eltávolítja az Azure Active Directory azon objektumait, amelyek már nem léteznek az Azure RemoteApp virtuális gépekhez társítottak.

## SZINTAXISA

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Clear-AzureRemoteAppVmStaleAdObject** parancsmag eltávolítja az Azure Active Directory azon objektumait, amelyek már nem léteznek az Azure RemoteApp virtuális gépekkel társítva.
Az Azure Active Directory-objektumok eltávolításához jogosultsággal rendelkező hitelesítő adatokra van szükség.
Ha a *részletes* általános paramétert adja meg, ez a parancsmag a törölt objektumok nevét jeleníti meg.

## Példák

### 1. példa: egy gyűjtemény elavult objektumainak törlése
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

Az első parancs a **beolvasás-hitelesítő adatok** használatával kéri a Felhasználónév és a jelszó megadását.
A parancs az eredményt a $AdminCredentials változóban tárolja.

A második parancs törli a contoso nevű gyűjtemény régi objektumait.
A parancs a $AdminCredentials változóban tárolt hitelesítő adatokat használja.
Ahhoz, hogy a parancs sikeres legyen, a hitelesítő adatoknak megfelelő jogokkal kell rendelkezniük.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRemoteAppVmStaleAdObject](./Get-AzureRemoteAppVmStaleAdObject.md)


