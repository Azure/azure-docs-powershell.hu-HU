---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016316"
---
# Get-AzureRemoteAppUser

## Áttekintés
Felsorolja az Azure RemoteApp-gyűjtemény felhasználóit.

## SZINTAXISA

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRemoteAppUser** parancsmag felsorolja az Azure RemoteApp-gyűjtemény felhasználóit.

## Példák

### Példa 1: egy gyűjtemény felhasználóinak listázása
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

Ez a parancs felsorolja azokat a felhasználókat, akik hozzáféréssel rendelkeznek az Azure RemoteApp-gyűjteményhez a contoso nevű gyűjteményben.

## PARAMÉTEREK

### -Alias
Egy közzétett program-aliast ad meg.
Ezt a paramétert csak a per-app közzétételi módjában tudja használni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Az Azure RemoteApp-gyűjtemény nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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
Annak a felhasználónak az egyszerű felhasználónevét adja meg, amelynek a listáját információkat listázhatja.
Például: PattiFuller@contoso.com .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRemoteAppUser](./Add-AzureRemoteAppUser.md)

[Get-AzureRemoteAppSession](./Get-AzureRemoteAppSession.md)

[Remove-AzureRemoteAppUser](./Remove-AzureRemoteAppUser.md)


