---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183006"
---
# New-AzExpressRouteCircuitAuthorization

## Áttekintés
ExpressRoute-áramkör-engedélyezést hoz létre.

## SZINTAXISA

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **New-AzExpressRouteCircuitAuthorization** parancsmag olyan áramkör-hitelesítést hoz létre, amelyet hozzáadhat egy ExpressRoute-áramkörhöz. A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról. Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat a hálózat áramkörhöz való csatlakoztatásához. Egy virtuális hálózatban csak egy engedély használható.
Az ExpressRoute-áramkör létrehozása után a **AzExpressRouteCircuitAuthorization** segítségével adhat hozzá engedélyt az adott áramkörhöz.
Azt is megteheti, hogy **új AzExpressRouteCircuitAuthorization** is létrehozhat olyan engedélyeket, amelyek hozzáadhatók egy új áramkörhez az áramkör létrehozásának időpontjában.

## Példák

### 1. példa: új áramkör-engedélyezés létrehozása
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Ez a parancs létrehoz egy ContosoCircuitAuthorization nevű új áramköri engedélyt, majd az objektumot egy $Authorization nevű változóban tárolja. Az objektum változóra mentése fontos: Habár az **új AzExpressRouteCircuitAuthorization** létrehozhatja az áramköri engedélyt, az nem vehető fel az áramköri útvonalra. Az új ExpressRoute-áramkör létrehozásakor Ehelyett az $Authorization változót használja New-AzExpressRouteCircuit.
További információt az New-AzExpressRouteCircuit parancsmag dokumentációjában talál.

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

### -Name (név)
Az új ExpressRoute-adatáramkör-engedélyezés egyedi nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitAuthorization

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

