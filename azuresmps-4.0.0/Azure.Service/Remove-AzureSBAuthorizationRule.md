---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E246C177-EAEE-4D7A-A544-664F47862FC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92d450a10628ea7e85a49962ac262d4dece8e4c8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016131"
---
# Remove-AzureSBAuthorizationRule

## Áttekintés
Eltávolítja a meglévő szolgáltatás-busz engedélyezési szabályát.

## SZINTAXISA

### EntitySAS
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> -EntityName <String>
 -EntityType <ServiceBusEntityType> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### NamespaceSAS
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
Eltávolítja a meglévő szolgáltatás-busz engedélyezési szabályát.

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## Példák

### Példa 1: engedélyezési szabály eltávolítása a névtér szintjén
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

Eltávolítja az engedélyezési szabály MyRule a MyNamespace.

### 2. példa: a várólista engedélyezési szabályának eltávolítása
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

Eltávolítja az MyNamespace nevű MyEntity-várólistára vonatkozó MyRule nevű engedélyezési szabályt.

## PARAMÉTEREK

### -EntityName
Az entitás neve, amelyre a szabályt alkalmazni kell.

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EntityType
Az egyed típusa (várólista, témakör, továbbítás, NotificationHub)

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Az egyedi engedélyezési szabály neve.

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

### -Namespace
A névtér neve az engedélyezési szabály alkalmazásához.
Ha nincs EntityName, feltéve, hogy a szabály a névtér szintjén lesz.

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

### -PassThru
Azt jelzi, hogy ez a parancsmag egy olyan objektumot ad eredményül, amely a működéséhez szükséges elemet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

```yaml
Type: SwitchParameter
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

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSBAuthorizationRule](./Get-AzureSBAuthorizationRule.md)

[Új – AzureSBAuthorizationRule](./New-AzureSBAuthorizationRule.md)

[Set-AzureSBAuthorizationRule](./Set-AzureSBAuthorizationRule.md)


