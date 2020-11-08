---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A4E9C9A7-7FD2-4FD5-AB35-CFF717607B44
online version: ''
schema: 2.0.0
ms.openlocfilehash: c6da222e6cbfe02e181e4a863d8ce8d585215bdd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016147"
---
# Remove-AzureRemoteAppUserDisk

## Áttekintés
Egy felhasználó felhasználói lemezének eltávolítása Azure RemoteApp-gyűjteményéből

## SZINTAXISA

```
Remove-AzureRemoteAppUserDisk [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRemoteAppUserDisk** parancsmag eltávolítja egy felhasználó felhasználói lemezét egy Azure RemoteApp-gyűjteményből.

## Példák

### 1. példa: felhasználó lemezének eltávolítása
```
PS C:\> Remove-AzureRemoteAppUserDisk -CollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com"
```

Ez a parancs eltávolítja egy olyan Azure Active Directory-felhasználó merevlemezét, aki az egyszerű felhasználónév a PattiFuller@contoso.com gyűjtemény Contoso01.

## PARAMÉTEREK

### -CollectionName
Az Azure RemoteApp-gyűjtemény nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -UserUpn
Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek a parancsmagja eltávolítja a lemezt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Copy-AzureRemoteAppUserDisk](./Copy-AzureRemoteAppUserDisk.md)


