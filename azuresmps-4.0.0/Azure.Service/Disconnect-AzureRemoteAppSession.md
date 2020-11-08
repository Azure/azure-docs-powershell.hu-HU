---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015686"
---
# Disconnect-AzureRemoteAppSession

## Áttekintés
Leválasztja az Azure RemoteApp-munkamenetet.

## SZINTAXISA

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **leválasztási AzureRemoteAppSession** parancsmag leválasztja a felhasználó Azure RemoteApp-munkamenetét.
A felhasználó ügyfele leválasztja az Azure RemoteApp-munkamenetét, de a felhasználó programjai továbbra is futnak.

## Példák

### 1. példa: felhasználó munkamenetének leválasztása
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

Ez a parancs leválasztja az Azure RemoteApp-munkamenetet az ContosoApps-gyűjteményben annak a felhasználónak, akinek az UPN-je PattiFuller@contoso.com .

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
Egy felhasználó egyszerű felhasználónevét adja meg PattiFuller@contoso.com .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
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

[Get-AzureRemoteAppSession](./Get-AzureRemoteAppSession.md)

[Meghívó-AzureRemoteAppSessionLogoff](./Invoke-AzureRemoteAppSessionLogoff.md)

[Küldés-AzureRemoteAppSessionMessage](./Send-AzureRemoteAppSessionMessage.md)


