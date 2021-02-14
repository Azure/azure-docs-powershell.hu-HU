---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161210"
---
# Add-AzExpressRouteCircuitAuthorization

## SYNOPSIS
ExpressRoute-kapcsolat kapcsolatengedélyt ad hozzá.

## SZINTAXIS

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzExpressRouteCircuitAuthorization** parancsmag engedélyt ad egy ExpressRoute-áramkörhöz. Az ExpressRoute-áramkörök a nyilvános internet helyett egy kapcsolatszolgáltató használatával csatlakoztatják helyszíni hálózatát a Microsoft-felhőhöz. Az ExpressRoute-áramkörök tulajdonosa akár 10 engedélyt is létrehozhat az egyes áramkörökhöz; ezek az engedélyek olyan engedélyezési kulcsot hoznak létre, amelyet a virtuális hálózat tulajdonosa használva csatlakoztathatja a hálózatát az áramkörhöz (virtuális hálózatonként egy engedélyt). **Az Add-AzExpressRouteCircuitAuthorization** új engedélyt ad egy áramkörhöz, és ezzel egyidejűleg létrehozza a megfelelő engedélyezési kulcsot. Ezek a kulcsok bármikor megtekinthetők a Get-AzExpressRouteCircuitAuthorization parancsmag futtatásával, majd szükség esetén másolhatók és továbbíthatók a megfelelő hálózattulajdonosnak.
Vegye figyelembe, hogy az **Add-AzExpressRouteCircuitAuthorization** futtatása után a kulcs aktiválásához Set-AzExpressRouteCircuit a Set-AzExpressRouteCircuit parancsmagot. Ha nem hívja fel a **Set-AzExpressRouteCircuitot,** a rendszer hozzáadja az engedélyt az áramkörhöz, de nem engedélyezi a használatát.

## PÉLDÁK

### 1. példa: Engedély hozzáadása a megadott ExpressRoute-áramkörhöz
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

A példában lévő parancsok új engedélyt adnak hozzá egy meglévő ExpressRoute-áramkörhöz. Az első parancs **a Get-AzExpressRouteCircuit** segítségével létrehoz egy ContosoCircuit nevű áramkörre hivatkozó objektumhivatkozást. Ezt az objektumhivatkozást egy $Circuit.
A második parancsban az **Add-AzExpressRouteCircuitAuthorization** parancsmaggal lehet új engedélyezési parancsot (ContosoCircuitAuthorization) hozzáadni az ExpressRoute-áramkörhöz. Ez a parancs hozzáadja az engedélyt, de nem aktiválja azt. Az engedélyezéshez a példában az utolsó parancsban látható **Set-AzExpressRouteCircuit** szükséges.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -ExpressRouteCircuit
Megadja azt az ExpressRoute-áramkört, amelybe ez a parancsmag hozzáadja az engedélyt.

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

### -Name
A hozzáadható kapcsolati engedély nevét adja meg.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
