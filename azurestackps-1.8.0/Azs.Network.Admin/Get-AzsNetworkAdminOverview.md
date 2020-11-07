---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840377"
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

### PÉLDA 1
```
Get-AzsNetworkAdminOverview
```

A hálózati rendszergazda áttekintése című témakörben talál.

### 2. PÉLDA
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

A nyilvános IP-cím használatba vételéhez.

## PARAMÉTEREK

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. AzureStack. Management. Network. admin. models. AdminOverview

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
