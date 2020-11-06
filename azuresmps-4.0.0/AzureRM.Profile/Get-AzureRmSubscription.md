---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491167"
---
# Get-AzureRmSubscription

## Áttekintés
Az aktuális fiók által elérhető előfizetések beszerzése.

## SZINTAXISA

### ListByIdInTenant (alapértelmezett)
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### ListByNameInTenant
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## Leírás
A Get-AzureRmSubscription parancsmag az előfizetés AZONOSÍTÓját, az előfizetés nevét és az otthoni bérlőt kapja meg az aktuális fiók által elérhető előfizetésekhez.

## Példák

### Példa 1: összes előfizetés lekérése az összes bérlői fiókban
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

Ez a parancs minden előfizetést beolvassa az aktuális fiókhoz engedéllyel rendelkező bérlői fiókokban.

### 2. példa: adott bérlői előfizetések lekérése
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

Az adott bérlői fiók összes előfizetésének listázása, amely az aktuális fiókhoz van engedélyezve.

### 3. példa: a jelenlegi bérlő összes előfizetésének beszerzése
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

Ez a parancs beilleszti az aktuális felhasználó által engedélyezett összes előfizetést az aktuális bérlői fiókba.

### Példa 4: az aktuális környezet módosítása adott előfizetés használatára
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

Ez a parancs beilleszti a megadott előfizetést, majd az aktuális környezetet a használatára állítja be.
A munkamenet minden további parancsmagja alapértelmezés szerint az új előfizetést használja (contoso-előfizetés 1).

## PARAMÉTEREK

### -SubscriptionId
Megadja a beszerzéshez tartozó előfizetés AZONOSÍTÓját.

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
A beolvasott előfizetés nevét adja meg.

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bérlői azonosító megkeresése
Az előfizetéseket tartalmazó bérlő AZONOSÍTÓját adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### PSAzureSubscription

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

