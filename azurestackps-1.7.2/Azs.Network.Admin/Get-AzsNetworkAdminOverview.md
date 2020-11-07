---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839839"
---
# Get-AzsNetworkAdminOverview

## Áttekintés
Áttekintés a hálózati erőforrás-szolgáltató állapotáról

## SZINTAXISA

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## Leírás
Áttekintés a hálózati erőforrás-szolgáltató állapotáról Az egyes tulajdonságok az Erőforrás kihasználtsága és az állapot szerinti részletezés részletes számát adja meg.

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsNetworkAdminOverview
```

A hálózati rendszergazda áttekintése című témakörben talál.

### --------------------------PÉLDA 2--------------------------
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

A nyilvános IP-cím használatba vételéhez.

## PARAMÉTEREK

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. AzureStack. Management. Network. admin. models. AdminOverview

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

