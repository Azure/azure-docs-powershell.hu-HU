---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181924"
---
# Enable-AzDataCollection

## Áttekintés
Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az Azure PowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében. A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható. Az adatokat alapértelmezés szerint gyűjtjük, hacsak nem kifejezetten kikapcsolja.

## SZINTAXISA

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás

A `Enable-AzDataCollection` parancsmag az adatgyűjtéshez való csatlakozáshoz használható. Az Azure PowerShell alapértelmezés szerint automatikusan gyűjti a telemetriai adatokat. A Microsoft összesíti az összegyűjtött adatokat a használati minták meghatározására, a gyakori problémák felismerésére, valamint az Azure PowerShell használatának javítására.
A Microsoft Azure PowerShell nem gyűjt semmilyen személyes vagy személyes adatot. Ha le szeretné tiltani az adatgyűjtést, a végrehajtáshoz explicit módon kell kiválasztania `Disable-AzDataCollection` .

## Példák

### 1. példa: adatgyűjtés engedélyezése az aktuális felhasználónál

Az alábbi példa azt szemlélteti, hogy miként engedélyezheti az aktuális felhasználó adatgyűjtését.

```powershell
Enable-AzDataCollection
```

## PARAMÉTEREK

### -DefaultProfile

Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### – Megerősítés

A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)című témakörben talál.

## BEMENETEK

### Nincs

## KIMENETEK

### System. Void

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
