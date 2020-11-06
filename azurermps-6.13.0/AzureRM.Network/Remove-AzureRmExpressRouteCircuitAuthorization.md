---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 6a8c81f8c130f322e868c91e18c7fff7b1175d4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503536"
---
# Remove-AzureRmExpressRouteCircuitAuthorization

## Áttekintés
A meglévő ExpressRoute-konfiguráció engedélyezésének eltávolítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmExpressRouteCircuitAuthorization** parancsmag eltávolítja a ExpressRoute-áramkörhez rendelt engedélyt. A ExpressRoute-áramkörök a helyszíni hálózatokat az Azure rendszerhez csatlakozva a nyilvános Internet helyett a szolgáltatót használják. Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat az áramkörhöz való csatlakozáshoz. Virtuális hálózatban csak egy engedély lehet. Az áramkör tulajdonosa azonban bármikor eltávolíthatja a **AzureRmExpressRouteCircuitAuthorization** a virtuális hálózathoz rendelt engedély eltávolításához. Amikor ez történik, a megfelelő virtuális hálózat már nem tudja használni a ExpressRoute áramkört az Azure-hoz való csatlakozáshoz.

## Példák

### 1. példa: ExpressRoute áramkör-engedélyezés eltávolítása
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Ez a példa egy ExpressRoute-áramkörből eltávolítja az áramkör-hitelesítést. Az első parancs a **Get-AzureRmExpressRouteCircuit** parancsmagot használja a ContosoCircuit nevű ExpressRoute-áramkörhöz tartozó objektum-hivatkozás létrehozásához, és az eredményt az $Circuit nevű változóban tárolja.
A második parancs az áramkör-engedélyezési ContosoCircuitAuthorization az eltávolításhoz.
A harmadik parancs az Set-AzureRmExpressRouteCircuit parancsmagot használja a $Circuit változóban tárolt ExpressRoute-áramkör eltávolításának megerősítéséhez.

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
A parancsmag által eltávolított ExpressRouteCircuit objektum meghatározása.

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
Annak az áramkör-engedélynek a nevét adja meg, amelyet a parancsmag eltávolít.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Új – AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Set-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
