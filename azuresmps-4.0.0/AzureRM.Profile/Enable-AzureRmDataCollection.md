---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491176"
---
# Enable-AzureRmDataCollection

## Áttekintés
Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az AzurePowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében.
A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható.
Csak akkor gyűjtünk adatokat, ha kifejezetten bekapcsolta.

## SZINTAXISA

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Javíthatja a Microsoft Cloud és az Azure PowerShell használatával kapcsolatos tapasztalatokat az adatgyűjtés kiválasztásával.
Az Azure PowerShell nem gyűjti össze az adatokat a hozzájárulása nélkül – az engedélyezés – AzureRmDataCollection, vagy ha az Azure PowerShell kéri az adatok gyűjtését a parancsmag első futtatásakor.
A Microsoft összesíti az összegyűjtött adatokat a használati minták meghatározására, a gyakori problémák felismerésére és az Azure PowerShell használatba vétele érdekében.
A Microsoft Azure PowerShell semmilyen személyes adatot nem gyűjt, vagy bármilyen személyazonosításra alkalmas információt tartalmaz.

Futtassa az Enable-AzureRMDataCollection parancsmagot az aktuális számítógépen az aktuális felhasználó adatgyűjtése engedélyezéséhez.
Ez megakadályozza, hogy az aktuális felhasználó Kérdezzen az adatgyűjtésről az első időparancsmagok végrehajtása során.

Az aktuális felhasználó adatgyűjtésének letiltásához futtassa az Disable-AzureRmDataCollection parancsmagot.

## Példák

### 1. példa: adatgyűjtés engedélyezése az aktuális felhasználónál
```
PS C:\> Enable-AzureRmDataCollection
```

Ebben a példában bemutatjuk, hogy miként engedélyezheti az aktuális felhasználó adatgyűjtését.

## PARAMÉTEREK

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

### Nincs

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Disable-AzureRmDataCollection]()

