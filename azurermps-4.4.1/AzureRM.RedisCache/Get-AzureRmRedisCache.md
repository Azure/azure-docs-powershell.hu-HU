---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 4cdd81b0cf9f83482192fbe6f484fb0b0d1beaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503968"
---
# Get-AzureRmRedisCache

## Áttekintés
Redis-gyorsítótárat kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### All in előfizetés (alapértelmezett)
```
Get-AzureRmRedisCache [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Minden az erőforrás csoportban
```
Get-AzureRmRedisCache -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Adott Redis-gyorsítótár
```
Get-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmRedisCache** parancsmag a megadott Azure Redis-gyorsítótárat kapja.
Ha nem ad meg paramétereket, ez a művelet minden Redis-gyorsítótárban megkapja az aktuális előfizetést.

## Példák

### Példa 1: Redis-gyorsítótár beszerzése név alapján
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup" -Name "myexists"

          ResourceGroupName  : myGroup


          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
          Location           : North Central US
          Name               : myexists
          Type               : Microsoft.Cache/Redis
          HostName           : myexists.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}

          EnableNonSslPort   : False

          RedisVersion       : 2.8

          Size               : 1GB

          Sku                : Basic
```

Ez a parancs a myexists nevű Redis-gyorsítótárat kapja meg.

### 2. példa: az erőforráscsoport minden Redis-gyorsítótárának beolvasása
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"


          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
          Location           : North Central US
          Name               : myexists
          Type               : Microsoft.Cache/Redis
          HostName           : myexists.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Basic

          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
          Location           : North Central US
          Name               : myearlier
          Type               : Microsoft.Cache/Redis
          HostName           : myearlier.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : True
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
```

Ez a parancs a megadott erőforráscsoport minden Redis-gyorsítótárát beolvassa.

### 3. példa: a jelenlegi előfizetés minden Redis-gyorsítótárának beszerzése
```
PS C:\>Get-AzureRmRedisCache


          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
          Location           : North Central US
          Name               : myexists
          Type               : Microsoft.Cache/Redis
          HostName           : myexists.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Basic

          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
          Location           : North Central US
          Name               : myearlier
          Type               : Microsoft.Cache/Redis
          HostName           : myearlier.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : True
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard


          ResourceGroupName  : myGroup2
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
          Location           : North Central US
          Name               : myearlier2
          Type               : Microsoft.Cache/Redis
          HostName           : myearlier2.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Basic
```

Ez a parancs minden Redis-gyorsítótárba bekerül az aktuális előfizetésben.

## PARAMÉTEREK

### -Name (név)
A beolvasott Redis-gyorsítótár nevét adja meg.
Használja a *ResourceGroupName* paramétert.

```yaml
Type: System.String
Parameter Sets: Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a csoportnak a neve, amely a Redis-gyorsítótárat tartalmazza.

Ha csak a *ResourceGroupName* paramétert adja meg, ez a művelet a megadott erőforráscsoport minden Redis-gyorsítótárát megkapja.

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
A parancsmagot név szerint, de nem érték szerint is beírhatja.

## KIMENETEK

### Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributes
**RedisCacheAttributes** -objektumok tömbjét számítja ki.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)


