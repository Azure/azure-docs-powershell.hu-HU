---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017677"
---
# New-AzRedisCache

## Áttekintés
Redis-gyorsítótárat hoz létre.

## SZINTAXISA

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **New-AzRedisCache** parancsmag Azure Redis-gyorsítótárat hoz létre.

## Példák

### Példa 1: Redis-gyorsítótár létrehozása
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

Ez a parancs Redis-gyorsítótárat hoz létre.

### 2. példa: szabványos SKU Redis-gyorsítótár létrehozása
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
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

Ez a parancs Redis-gyorsítótárat hoz létre.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
Az alapértelmezett érték $False (a nem SSL-port van letiltva).

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

### -Hely
A Redis-gyorsítótár létrehozásának helyét adja meg.
Az érvényes értékek a következők: 
- Közép-amerikai Észak-amerikai
- Dél-Közép-amerikai
- Közép-amerikai
- Nyugat-Európa
- Észak-Európa
- Nyugat-amerikai
- Kelet-amerikai
- Kelet-amerikai 2
- Japán (kelet)
- Japán West
- Dél-Brazília
- Dél-ázsiai
- Kelet-ázsiai
- Ausztrália – Kelet
- Ausztrália délkeleti

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

### -Name (név)
A létrehozandó Redis-gyorsítótár nevét adja meg.

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
A paraméter elfogadható értékei a következők:
- RDB – biztonsági másolat engedélyezve
Megadja, hogy a Redis-adatmegőrzés engedélyezve van.
Prémium szint
- RDB – tárolási kapcsolat – karakterlánc.
A Redis-adatmegőrzéshez a tárolási fiókhoz tartozó kapcsolati karakterláncot adja meg.
Prémium szint
- RDB-Backup-frekvencia.
A Redis adatmegőrzési gyakoriságát adja meg.
Prémium szint 
- maxmemory – fenntartva.
A nem gyorsítótárban lévő folyamatok számára fenntartott memória beállítása.
Standard és prémium szintek. 
- maxmemory – házirend.
A gyorsítótár kilakoltatási házirendjének beállítása.
Minden árazási szint. 
- értesítés – a szóköz – események.
A szóközökkel kapcsolatos értesítések beállítása.
Standard és prémium szintek. 
- hash-Max-ZipList-bejegyzéseket.
A kis összesített adattípusok memória-optimalizálását állítja be.
Standard és prémium szintek. 
- hash-Max-ZipList-érték.
A kis összesített adattípusok memória-optimalizálását állítja be.
Standard és prémium szintek. 
- set-Max-intset-bejegyzéseket.
A kis összesített adattípusok memória-optimalizálását állítja be.
Standard és prémium szintek. 
- zset-Max-ZipList-bejegyzéseket.
A kis összesített adattípusok memória-optimalizálását állítja be.
Standard és prémium szintek. 
- zset-Max-ZipList-érték.
A kis összesített adattípusok memória-optimalizálását állítja be.
Standard és prémium szintek. 
- adatbázisok.
Az adatbázisok számának beállítása.
Ezt a tulajdonságot csak a gyorsítótár létrehozásakor lehet konfigurálni.
Standard és prémium szintek.
További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) .

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
Annak az erőforráscsoportnek a nevét adja meg, amelybe a Redis-gyorsítótárat létre szeretné hozni.

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

### -ShardCount
A prémium szektorcsoport-gyorsítótárban létrehozandó szilánkok számát adja meg.
A paraméter elfogadható értékei a következők:
- 1
- 2
- 3
- 4
- 5
- 6
- 7
- 8
- 9 
- 10

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

### -Méret
A Redis-gyorsítótár méretét adja meg.
Az érvényes értékek a következők: 
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
- 250 MB méretű
- GIGABÁJTNÁL szükséges
- 2.5 GB
- 6GB
- 13GB
- 26GB
- 53GB az alapértelmezett érték 1GB vagy C1.

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

### -SKU
Megadja a létrehozandó Redis-gyorsítótár SKU-ának számát.
Az érvényes értékek a következők: 
- Egyszerű
- Standard
- Prémium: az alapértelmezett érték a standard.

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

### -StaticIP
Egy egyedi IP-címet ad meg a Redis-gyorsítótár alhálózatában.
Ha nem ad meg értéket ehhez a paraméterhez, ez a parancsmag egy IP-címet választ az alhálózatról.

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

### – NetI
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

### -Címke
A címkéket jelképező kivonatoló táblázat.

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
Ezt a paramétert érvénytelenítették.

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

### -Zone (zóna)
A zónák listája.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

### System. Collections. Hashtable

### System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]

### System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]

### System. string []

## KIMENETEK

### Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzRedisCache](./Get-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)

[Set-AzRedisCache](./Set-AzRedisCache.md)


