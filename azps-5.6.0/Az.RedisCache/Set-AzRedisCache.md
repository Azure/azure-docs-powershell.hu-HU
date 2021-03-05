---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 809939a4e218005c9b4c41846e0885dfca553964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000917"
---
# Set-AzRedisCache

## SYNOPSIS
Módosítja a redis-gyorsítótárat.

## SZINTAXIS

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzRedisCache** parancsmag módosítja az Azure Redis-gyorsítótárat.

## PÉLDÁK

### 1. példa: Redis-gyorsítótár módosítása
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

Ez a parancs frissíti a MyCache nevű Redis cache maxmemory-házirendet.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableNonSslPort
Azt jelzi, hogy engedélyezve van-e a nem SSL-port.
Az alapértelmezett érték $False (a nem SSL-port le van tiltva).

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinimumTlsVersion
Adja meg az ügyfelek által a gyorsítótárhoz való csatlakozáshoz szükséges TLS-verziót.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
A frissítenie kell a redis-gyorsítótár nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RedisConfiguration
A Redis konfigurációs beállításait adja meg.
A paraméter elfogadható értékei a következőek:
- rdb-backup-enabled.
Azt adja meg, hogy a Redis data persistence engedélyezve van.
Csak prémium szint.
- rdb-storage-connection-string.
A Redis adatmegőrzéshez a Tárfiókhoz való kapcsolati karakterláncot adja meg.
Csak prémium szint.
- rdb-backup-frequency.
A redis data persistence biztonsági mentési gyakoriságát határozza meg.
Csak prémium szint. 
- maxmemory-reserved.
A nem gyorsítótáras folyamatok számára fenntartott memóriát konfigurálja.
Normál és Prémium szint. 
- maxmemory-policy.
Konfigurálja a kiviction házirendet a gyorsítótárhoz.
Az összes árazási szint. 
- notify-keyspace-events.
Konfigurálja a keyspace-értesítéseket.
Normál és prémiumszintek. 
- hash-max-ziplist-entries.
A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.
Normál és Prémium szint. 
- hash-max-ziplist-value.
A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.
Normál és Prémium szint. 
- set-max-intset-entries.
A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.
Normál és Prémium szint. 
- zset-max-ziplist-entries.
A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.
Normál és Prémium szint. 
- zset-max-ziplist-value.
A memóriaoptimalizálás konfigurálása kis aggregátum adattípushoz.
Normál és Prémium szint. 
- adatbázisokat.
Az adatbázisok számának beállítása.
Ez a tulajdonság csak gyorsítótár-létrehozáskor konfigurálható.
Normál és Prémium szint.
További információt az Azure Redis Cache kezelése az Azure PowerShell használatával http://go.microsoft.com/fwlink/?LinkId=800051 ( . http://go.microsoft.com/fwlink/?LinkId=800051)

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShardCount
A prémium szintű fürt-gyorsítótárban létrehozható szegmensek számát adja meg.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Size
A Redis Cache mérete.
Érvényes értékek: 
- P1
- P2
- P3
- P4
- P5
- C0
- C1
- C2
- C3
- C4
- C5
- C6
- 250 MB
- 1 GB
- 2,5 GB
- 6 GB
- 13 GB
- 26 GB
- 53 GB
- 120 GB Az alapértelmezett érték 1 GB vagy C1.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Termékváltozat
A létrehozni szükséges redis-gyorsítótár termékváltozatát adja meg.
Érvényes értékek: 
- Alapszintű
- Normál
- Prémium: Az alapértelmezett érték a Standard.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Címkéket képviselő kivonattábla.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantSettings
A paraméter elavult.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Collections.Hashtable

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## KIMENETEK

### Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzRedisCache](./Get-AzRedisCache.md)

[New-AzRedisCache](./New-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)


