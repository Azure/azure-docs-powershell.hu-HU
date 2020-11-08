---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 75320133-E7B1-40D4-B16D-567686D5AE99
online version: ''
schema: 2.0.0
ms.openlocfilehash: 40d3bdc73ce6bcbb199cf99bb0586de52f05e132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015987"
---
# New-AzureSBAuthorizationRule

## Áttekintés
Új szolgáltatási busz engedélyezési szabályát hozza létre.

## SZINTAXISA

### EntitySAS
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### NamespaceSAS
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureSBAuthorizationRule** parancsmag létrehoz egy szolgáltatási busz engedélyezési szabályát.

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## Példák

### Példa 1: engedélyezési szabály létrehozása a generált elsődleges kulccsal
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

Új engedélyezési szabály létrehozása a névtér szintjén a küldési engedéllyel.

### 2. példa: engedélyezési szabály létrehozása az elsődleges kulcs megadásával
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Manage", "Listen", "Send") -EntityName MyEntity -EntityType Queue -PrimaryKey P+lL/Mnd2Z9sj5hwMrRyAxQDdX8RHfbdqU2eIAqs1rc=
```

Új engedélyezési szabályt hoz létre a MyEntity-várólistán az összes engedéllyel.

## PARAMÉTEREK

### -EntityName
Annak a szervezetnek a nevét adja meg, amelyre a szabályt alkalmazni kívánja.

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EntityType
Az egyed típusát adja meg.
Az érvényes értékek a következők:
  
- Várólista
- Témakör
- Relé
- NotificationHub

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Az egyedi engedélyezési szabály nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Annak a névtérnek a nevét adja meg, amely az engedélyezési szabályt alkalmazza.
Ha nincs *EntityName* , feltéve, hogy a szabály a névtér szintjén lesz.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Engedély
Az engedélyezési engedélyek (küldés, kezelés, figyelés)

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryKey
A megosztott hozzáférés-aláírás elsődleges kulcsát adja meg.
Akkor fog létrejönni, ha nincs megadva.

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

### -SecondaryKey
A megosztott hozzáférés-aláírás másodlagos kulcsát adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSBAuthorizationRule](./Get-AzureSBAuthorizationRule.md)

[Remove-AzureSBAuthorizationRule](./Remove-AzureSBAuthorizationRule.md)

[Set-AzureSBAuthorizationRule](./Set-AzureSBAuthorizationRule.md)


