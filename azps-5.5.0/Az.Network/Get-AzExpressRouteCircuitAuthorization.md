---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151978"
---
# Get-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Információkat kap az ExpressRoute-kapcsolat kapcsolatengedélyeiről.

## SZINTAXIS

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzExpressRouteCircuitAuthorization** parancsmag információkat kap az ExpressRoute-áramkörhöz rendelt engedélyekről. Az ExpressRoute-áramkörök a nyilvános internet helyett egy kapcsolatszolgáltató használatával csatlakoztatják helyszíni hálózatát a Microsoft-felhőhöz. Az ExpressRoute-áramkörök tulajdonosa akár 10 engedélyt is létrehozhat az egyes áramkörökhöz; ezek az engedélyek egy engedélyezési kulcsot hoznak létre, amelyet a virtuális hálózat tulajdonosa használva csatlakoztathatja a hálózatát az áramkörhöz (virtuális hálózatonként egy engedélyt). Az engedélyezési kulcsok, valamint az engedélyezésre vonatkozó egyéb információk bármikor megtekinthetők a **Get-AzExpressRouteCircuitAuthorization futtatásával.**

## PÉLDÁK

### 1. példa: Az összes ExpressRoute-engedély kérése
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Ezek a parancsok információt adnak az ExpressRoute-áramkörökkel társított ExpressRoute-engedélyekről. Az első parancs a **Get-AzExpressRouteCircuit** parancsmaggal létrehoz egy ContosoCircuit nevű áramkörre hivatkozó objektumhivatkozást; ezt az objektumhivatkozást a következő változóban $Circuit. A második parancs ezután az objektumhivatkozást és a **Get-AzExpressRouteCircuitAuthorization** parancsmagot használja a ContosoCircuithoz társított engedélyekre vonatkozó információk visszaadása érdekében.

### 2. példa: Az összes ExpressRoute-engedély lekértése a Where-Object parancsmaggal
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Ezek a parancsok az 1. példában használt parancsok változatának jelképeznek. Ebben az esetben azonban csak a használatra rendelkezésre álló engedélyekhez (például virtuális hálózathoz nem hozzárendelt engedélyekhez) kap adatokat a rendszer. Ehhez a 2. parancs visszaadja a kapcsolat kapcsolatengedélyezési adatait, és a **where-object** parancsmagba lesz becsökkentve.
**A Where-Object** ezután csak azokat az engedélyeket adja meg, *amelyeknél az AuthorizationUseStatus* tulajdonság Elérhetőre van állítva. Ha csak azokat az engedélyeket sorolja fel, amelyek nem érhetők el, használja az alábbi szintaxist a Where záradékhoz: `{$_.AuthorizationUseStatus -ne "Available"}`

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
Az ExpressRoute-kapcsolat kapcsolati engedélyének megadása.

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
Annak az ExpressRoute-kapcsolati engedélynek a nevét adja meg, amelybe a parancsmagot beszerzi.
-Name "ContosoCircuitAuthorization"

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
