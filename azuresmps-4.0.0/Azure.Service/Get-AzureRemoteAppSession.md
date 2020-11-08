---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016577"
---
# Get-AzureRemoteAppSession

## Áttekintés
Az összes aktív és leválasztott Azure RemoteApp-munkamenet listázása egy gyűjteményben.

## SZINTAXISA

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRemoteAppSession** parancsmag az aktív és a kapcsolat nélküli Azure RemoteApp-munkamenetek listáját jeleníti meg egy Azure RemoteApp-gyűjteményben.

## Példák

### Példa 1: egy gyűjtemény összes munkamenetének listázása
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

Ez a parancs felsorolja az Azure RemoteApp-gyűjtemény ContosoApps nevű összes munkamenetét.

## PARAMÉTEREK

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
Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek az Azure RemoteApp-munkameneteket be kell szereznie.
Az egyszerű felhasználónév például a következő formátumú lehet: PattiFuller@contoso.com .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Disconnect-AzureRemoteAppSession](./Disconnect-AzureRemoteAppSession.md)

[Meghívó-AzureRemoteAppSessionLogoff](./Invoke-AzureRemoteAppSessionLogoff.md)

[Küldés-AzureRemoteAppSessionMessage](./Send-AzureRemoteAppSessionMessage.md)


