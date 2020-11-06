---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 68599a48c4b0e608f629a628968c1918e62ec226
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93506023"
---
# New-AzureRmExpressRouteCircuitAuthorization

## Áttekintés
ExpressRoute-áramkör-engedélyezést hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureRmExpressRouteCircuitAuthorization** parancsmag olyan áramkör-hitelesítést hoz létre, amelyet hozzáadhat egy ExpressRoute-áramkörhöz. A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról. Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat a hálózat áramkörhöz való csatlakoztatásához. Egy virtuális hálózatban csak egy engedély használható.

Az ExpressRoute-áramkör létrehozása után a **AzureRmExpressRouteCircuitAuthorization** segítségével adhat hozzá engedélyt az adott áramkörhöz.
Azt is megteheti, hogy **új AzureRmExpressRouteCircuitAuthorization** is létrehozhat olyan engedélyeket, amelyek hozzáadhatók egy új áramkörhez az áramkör létrehozásának időpontjában.

## Példák

### 1. példa: új áramkör-engedélyezés létrehozása
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Ez a parancs létrehoz egy ContosoCircuitAuthorization nevű új áramköri engedélyt, majd az objektumot egy $Authorization nevű változóban tárolja. Az objektum változóra mentése fontos: Habár az **új AzureRmExpressRouteCircuitAuthorization** létrehozhatja az áramköri engedélyt, az nem vehető fel az áramköri útvonalra. Az új ExpressRoute-áramkör létrehozásakor Ehelyett az $Authorization változót használja New-AzureRmExpressRouteCircuit.

További információt az New-AzureRmExpressRouteCircuit parancsmag dokumentációjában talál.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Az új ExpressRoute-adatáramkör-engedélyezés egyedi nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a csővezetékes bevitelt.

## KIMENETEK

### PSExpressRouteCircuitAuthorization
Ez a parancsmag a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitAuthorization** objektum példányait hozza létre.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

