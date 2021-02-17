---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156923"
---
# New-AzExpressRouteCircuitAuthorization

## SYNOPSIS
ExpressRoute-kapcsolat kapcsolatengedélyt hoz létre.

## SZINTAXIS

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **New-AzExpressRouteCircuitAuthorization** parancsmag létrehoz egy áramkör-engedélyt, amely hozzáadható egy ExpressRoute-áramkörhöz. Az ExpressRoute-áramkörök a nyilvános internet helyett egy kapcsolatszolgáltató használatával csatlakoztatják helyszíni hálózatát a Microsoft-felhőhöz. Az ExpressRoute-áramkörök tulajdonosa akár 10 engedélyt is létrehozhat az egyes áramkörökhöz; ezek az engedélyek olyan engedélyezési kulcsot hoznak létre, amelyet egy virtuális hálózat tulajdonosa használva csatlakoztathat egy hálózatot az áramkörhöz. Virtuális hálózatonként csak egy engedélyezési lehetőség használhatja.
Miután létrehozott egy ExpressRoute-áramkört, az **Add-AzExpressRouteCircuitAuthorization** segítségével adhat hozzá egy engedélyt az áramkörhöz.
Másik lehetőségként a **New-AzExpressRouteCircuitAuthorization** segítségével is létrehozhat egy olyan engedélyt, amely az áramkör létrehozásakor hozzáadható egy új áramkörhöz.

## PÉLDÁK

### 1. példa: Új kapcsolat kapcsolati engedély létrehozása
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Ez a parancs létrehozza a ContosoCircuitAuthorization nevű új kapcsolati kapcsolati engedélyt, majd az objektumot egy "$Authorization" nevű változóban $Authorization. Fontos, hogy egy változóba mentse az objektumot: bár a **New-AzExpressRouteCircuitAuthorization** áramköri hitelesítést tud létrehozni, az adott engedélyt nem tudja hozzáadni egy áramköri útvonalhoz. Ehelyett a $Authorization a New-AzExpressRouteCircuit egy vadonatúj ExpressRoute-áramkör létrehozásakor használatos.
További információt a New-AzExpressRouteCircuit dokumentációjában talál.

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

### -Name
Az új ExpressRoute-kapcsolat kapcsolati engedélyének egyedi nevét adja meg.

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

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

