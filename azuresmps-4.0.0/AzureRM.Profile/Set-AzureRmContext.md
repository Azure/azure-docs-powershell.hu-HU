---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491323"
---
# Set-AzureRmContext

## Áttekintés
A bérlői fiók, az előfizetés és a környezet beállítása az aktuális munkamenetben használható parancsmagok esetében.

## SZINTAXISA

### SubscriptionName (alapértelmezett)
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Összefüggésben
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SubscriptionId
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A Set-AzureRmContext parancsmag az aktuális munkamenetben futtatott parancsmagok hitelesítési adatait állítja be.
A környezet a bérlői, az előfizetési és a környezeti információkat tartalmazza.

## Példák

### Példa 1: az előfizetés környezetének beállítása
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

Ez a parancs beállítja a megadott előfizetéshez használt környezetet.

## PARAMÉTEREK

### -Környezet
Az aktuális munkamenet környezetét adja meg.

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SubscriptionId
Annak a környezetnek az előfizetési AZONOSÍTÓját adja meg, amelyhez az adott parancsmag az aktuális munkamenetet állítja be.

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Annak az előfizetésnek a nevét adja meg, amely az aktuális munkamenethez a parancsmag által beállított környezethez tartozik.

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bérlői azonosító megkeresése
Annak a környezetnek az AZONOSÍTÓját adja meg a bérlői fiók számára, amelyre a parancsmag az aktuális munkamenetet állítja be.

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### PSAzureContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRMContext]()

