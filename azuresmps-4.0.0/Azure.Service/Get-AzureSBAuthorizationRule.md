---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015614"
---
# Get-AzureSBAuthorizationRule

## Áttekintés
A szolgáltatás busz-engedélyezési szabályait kapja.


## SZINTAXISA

### EntitySAS
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### NamespaceSAS
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A szolgáltatás busz-engedélyezési szabályait kapja.

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## Példák

### 1. példa: engedélyezési szabály kérése a névtér szintjén
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

Az összes rendelkezésre álló engedélyezési szabály a MyNamespace címen szerezhető be.

### 2. példa: engedélyezési szabály kérése egy várólistához
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

Az összes rendelkezésre álló engedélyezési szabály egy MyEntity-várólistára kerül a MyNamespace.

### 3. példa: engedélyezési szabály kérése név szerint
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

A MyRule nevű engedélyezési szabályt MyNamespace szinten kapja.

### 4. példa: engedélyezési szabály kérése engedély szerint
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

Megkapja az összes olyan engedélyezési szabályt, amely a névtér szintjén küldi el az engedélyt.

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

Required: False
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

### – Engedély
A szűrés (küldés, kezelés, figyelés) engedélyezési engedélyei.
Ez a pontos egyezést használja.

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureSBAuthorizationRule](./New-AzureSBAuthorizationRule.md)

[Remove-AzureSBAuthorizationRule](./Remove-AzureSBAuthorizationRule.md)

[Set-AzureSBAuthorizationRule](./Set-AzureSBAuthorizationRule.md)


