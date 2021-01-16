---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360750"
---
# Remove-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Eltávolít egy meglévő ExpressRoute-konfigurációengedélyt.

## SZINTAXIS

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzExpressRouteCircuitAuthorization** parancsmag eltávolítja az ExpressRoute-áramkörhöz rendelt engedélyt. Az ExpressRoute-áramkörök a nyilvános internet helyett egy kapcsolatszolgáltató használatával csatlakoztatják helyszíni hálózatát az Azure-hoz. Az ExpressRoute-áramkörök tulajdonosa akár 10 engedélyt is létrehozhat az egyes áramkörökhöz; ezek az engedélyek olyan engedélyezési kulcsot hoznak létre, amelyet a virtuális hálózat tulajdonosa használva csatlakoztathatja a hálózatát az áramkörhöz. Virtuális hálózatonként csak egy engedélyezési lehetőség lehet. A kapcsolatcsoport tulajdonosa azonban bármikor használhatja a **Remove-AzExpressRouteCircuitAuthorization** kapcsolót a virtuális hálózathoz rendelt engedély eltávolításához. Ilyen esetben a megfelelő virtuális hálózat már nem tudja használni az ExpressRoute-áramkört az Azure-hoz való csatlakozáshoz.

## PÉLDÁK

### 1. példa: Áramkör-hitelesítés eltávolítása Egy ExpressRoute-áramkörből
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Ez a példa eltávolítja az áramkör-hitelesítést egy ExpressRoute-áramkörből. Az első parancs a **Get-AzExpressRouteCircuit** parancsmag segítségével létrehoz egy ContosoCircuit nevű ExpressRoute-áramkörre való objektumhivatkozást, és az eredményt a $Circuit.
A második parancs az eltávolításra használt ContosoCircuitAuthorization áramkör-hitelesítést jelöli.
A harmadik parancs a Set-AzExpressRouteCircuit parancsmag segítségével erősítse meg a $Circuit ExpressRoute-áramkör eltávolítását.

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
A parancsmag által eltávolított ExpressRouteCircuit-objektumot adja meg.

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
A parancsmag által eltávolított kapcsolati engedély nevét adja meg.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
