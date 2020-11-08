---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016329"
---
# Get-AzureRemoteAppCollection

## Áttekintés
Beolvassa az Azure RemoteApp-gyűjtemény adatait.

## SZINTAXISA

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRemoteAppCollection** parancsmag információkat keres az Azure RemoteApp-gyűjteményekről a Microsoft Azure-ban.
Egy olyan objektumot ad eredményül, amely egy adott gyűjtemény adataival rendelkezik, vagy ha nem ad meg gyűjteményt, az aktuális előfizetéshez tartozó összes gyűjtemény esetében.

## Példák

### Példa 1: az összes gyűjtemény listájának beszerzése
```
PS C:\> Get-AzureRemoteAppCollection
```

Ez a parancs az összes Azure RemoteApp-gyűjtemény listáját visszaküldi az előfizetésben.

### 2. példa: információk kérése egy adott gyűjteményről
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

Ez a parancs információt ad a ContosoApps nevű Azure RemoteApp-gyűjteményről.

### 3. példa: gyűjtemények listájának beszerzése helyettesítő karakterrel
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

Ez a parancs az összes Azure RemoteApp-gyűjtemény listáját visszaállítja.

## PARAMÉTEREK

### -CollectionName
Az Azure RemoteApp-gyűjtemény nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
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

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


