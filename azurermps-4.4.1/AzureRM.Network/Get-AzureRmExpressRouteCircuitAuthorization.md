---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: a99b2ce5364e256f19069e1142b49abaf7f5e938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505612"
---
# Get-AzureRmExpressRouteCircuitAuthorization

## Áttekintés
Információt kap a ExpressRoute-áramköri engedélyekről.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmExpressRouteCircuitAuthorization** parancsmag információkat kap a ExpressRoute-áramkörhöz rendelt engedélyekről. A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról. Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat az áramkörhöz való csatlakozáshoz (virtuális hálózat esetén egy engedély). Az engedélyezési kulcsok, valamint az engedélyezéssel kapcsolatos egyéb információk bármikor megtekinthetők a **Get-AzureRmExpressRouteCircuitAuthorization** segítségével.

## Példák

### Példa 1: az összes ExpressRoute-engedély beolvasása
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

Ezekkel a parancsokkal információt adhat meg az ExpressRoute-áramkörhöz társított összes ExpressRoute-engedélyről. Az első parancs a **Get-AzureRmExpressRouteCircuit** parancsmagot használja a ContosoCircuit nevű áramkör-hivatkozás létrehozásához; az objektum hivatkozását az $Circuit változóban tárolja. A második parancs ezután az Object Reference és a **Get-AzureRmExpressRouteCircuitAuthorization** parancsmag segítségével visszaadja a ContosoCircuit társított engedélyekkel kapcsolatos információkat.

### 2. példa: az összes ExpressRoute-engedély beszerzése az Where-Object parancsmag használatával
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Ezek a parancsok a példaként használt parancsok variációját jelentik. Ebben az esetben azonban csak azokat az engedélyeket adja vissza, amelyek használatra elérhetők (azaz a virtuális hálózathoz nem rendelt engedélyek esetén). Ehhez az áramkör-engedélyezési információkat a 2-es parancs adja vissza, és a vezetékes a **Where-Object** parancsmaghoz.
**Where-objektum** : csak azokat az engedélyeket adja meg, amelyekben a *AuthorizationUseStatus* tulajdonság elérhető értékre van állítva. Ha csak azokat az engedélyeket szeretné listázni, amelyek nem érhetők el, használja a WHERE záradék következő szintaxisát:

`{$_.AuthorizationUseStatus -ne "Available"}`

## PARAMÉTEREK

### -ExpressRouteCircuit
A ExpressRoute-áramkör engedélyezését adja meg.

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
Annak a ExpressRoute-áramköri engedélynek a nevét adja meg, amely a parancsmagot kapja.

-Név "ContosoCircuitAuthorization"

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSExpressRouteCircuit
A **Get-AzureRmExpressRouteCircuitAuthorization** elfogadja a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit** objektum csővezetékes példányait.

## KIMENETEK

### PSExpressRouteCircuitAuthorization
A **Get-AzureRmExpressRouteCircuitAuthorization** a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitAuthorization** objektum példányait számítja ki.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Új – AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
