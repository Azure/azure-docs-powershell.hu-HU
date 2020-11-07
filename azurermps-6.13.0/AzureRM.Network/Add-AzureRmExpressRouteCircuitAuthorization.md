---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 108ea2b0262c34e38ffd7ed2961e3cba9a8d59ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672600"
---
# Add-AzureRmExpressRouteCircuitAuthorization

## Áttekintés
ExpressRoute-áramkör-engedélyezést ad hozzá.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureRmExpressRouteCircuitAuthorization** parancsmag egy ExpressRoute-áramkörhöz ad engedélyt. A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról. Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat az áramkörhöz való csatlakozáshoz (virtuális hálózat esetén egy engedély). A **Add-AzureRmExpressRouteCircuitAuthorization** új meghatalmazást ad hozzá egy áramkörhez, és egyidejűleg létrehozza a megfelelő engedélyezési kulcsot. Ezek a billentyűk bármikor megtekinthetők, ha futtatják az Get-AzureRmExpressRouteCircuitAuthorization parancsmagot, és igény szerint át lehet őket másolni és továbbítani a megfelelő hálózati tulajdonosnak.
Felhívjuk a figyelmét arra, hogy a **AzureRmExpressRouteCircuitAuthorization** futtatása után az Set-AzureRmExpressRouteCircuit parancsmagot kell hívnia a kulcs aktiválásához. Ha nem hívja meg a **set-AzureRmExpressRouteCircuit** , az engedélyt hozzáadja a program az áramkörhez, de nem lesz engedélyezve a használathoz.

## Példák

### 1. példa: engedély hozzáadása a megadott ExpressRoute-áramkörhöz
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Az ebben a példában szereplő parancsok új engedélyt adhatnak egy meglévő ExpressRoute-áramkörhöz. Az első parancs a **Get-AzureRmExpressRouteCircuit** használatával hoz létre egy ContosoCircuit nevű áramkört. Az objektum hivatkozása $Circuit nevű változóban tárolódik.
A második parancsban a **Add-AzureRmExpressRouteCircuitAuthorization** parancsmaggal új engedélyt (ContosoCircuitAuthorization) adhat a ExpressRoute áramkörhöz. Ez a parancs hozzáadja az engedélyt, de nem aktiválja az engedélyt. Az engedély aktiválásához a példában a végleges parancsban látható **set-AzureRmExpressRouteCircuit** van szükség.

## PARAMÉTEREK

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

### -ExpressRouteCircuit
Azt a ExpressRoute-áramkört adja meg, amelyre a parancsmag hozzáadja az engedélyt.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A hozzáadni kívánt áramkör-hitelesítés nevét adja meg.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit
Paraméterek: ExpressRouteCircuit (ByValue)

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Új – AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[Set-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
