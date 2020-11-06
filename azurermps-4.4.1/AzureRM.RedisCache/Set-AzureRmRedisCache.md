---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494719"
---
# Set-AzureRmRedisCache

## Áttekintés
Módosítja egy Redis-gyorsítótárat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureRmRedisCache** parancsmag az Azure Redis-gyorsítótárát módosítja.

## Példák

### Példa 1: Redis-gyorsítótár módosítása
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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
```

Ez a parancs frissíti a MyCache nevű Redis-gyorsítótár maxmemory-házirendjét.

## PARAMÉTEREK

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

### -MaxMemoryPolicy
Ezt a paramétert érvénytelenítették.
A *RedisConfiguration* paraméterrel megadhatja a maxmemory-házirendet.
Példa: 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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
A frissítendő Redis-gyorsítótár nevét adja meg.

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

További információt az Azure Redis-gyorsítótár kezelése az Azure PowerShell használatával című témakörben talál https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) .

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
A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.

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
- 53GB

Az alapértelmezett érték az 1GB vagy a C1.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

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
- Prémium verzió

Az alapértelmezett érték a standard.

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
A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.

## KIMENETEK

### Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributesWithAccessKeys
A Redis-gyorsítótár összes attribútumát számítja ki, az elsődleges és másodlagos elérési kulcsokat is beleszámítva.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[Új – AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)


