---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A121B341-091D-42AD-B56A-3C75E25A1BF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8383240f9c1db58a6a22f6754f98211580d31a73
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016381"
---
# Add-AzureRemoteAppUser

## Áttekintés
Hozzáad egy felhasználót egy Azure RemoteApp-gyűjteményhez.

## SZINTAXISA

```
Add-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureRemoteAppUser** parancsmag hozzáadja a felhasználót egy Azure RemoteApp-gyűjteményhez.

## Példák

### 1. példa: felhasználó felvétele Microsoft-fiók használatával
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType MicrosoftAccount -UserUpn "PattiFuller@contoso.com"
```

Ez a parancs hozzáadja a Microsoft PattiFuller@contoso.com -fiókot a contoso nevű gyűjteményhez.

### 2. példa: felhasználó hozzáadása Azure Active Directory-fiókkal
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType OrgId -UserUpn "PattiFuller@contoso.com"
```

Ez a parancs hozzáadja az Azure Active Directory PattiFuller@contoso.com -fiókot a contoso nevű gyűjteményhez.

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

### -Type (típus)
A felhasználó típusát adja meg.
A paraméter elfogadható értékei a következők: OrgId vagy MicrosoftAccount.

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserUpn
Egy felhasználó egyszerű felhasználónevét adja meg, például PattiFuller@contoso.com .

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
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

[Get-AzureRemoteAppUser](./Get-AzureRemoteAppUser.md)

[Remove-AzureRemoteAppUser](./Remove-AzureRemoteAppUser.md)


