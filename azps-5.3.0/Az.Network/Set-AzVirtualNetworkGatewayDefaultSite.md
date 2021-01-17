---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470118"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Beállítja egy virtuális hálózati átjáró alapértelmezett webhelyét.

## SZINTAXIS

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzVirtualNetworkGatewayDefaultSite** parancsmag egy kényszerített alagutas alapértelmezett webhelyet rendel egy virtuális hálózati átjáróhoz.
A kényszerített átjárók használatával átirányíthatja az internetes forgalmat az Azure virtuális gépeiből a helyszíni hálózatba; ez lehetővé teszi a forgalom vizsgálatát és naplózását, mielőtt felengedi azt.
A kényszerített alagutaszás virtuális magánhálózati alagutat használ; Ehhez az átjáróhoz egy alapértelmezett webhelyre, egy helyi átjáróra van szükség, ahol az Összes Azure internetes forgalmat átirányítják.
**A Set-AzVirtualNetworkGatewayDefaultSite** segítségével módosíthatja az átjárókhoz rendelt alapértelmezett webhelyet.

## PÉLDÁK

### 1. példa: Alapértelmezett webhely hozzárendelése virtuális hálózati átjáróhoz
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

Ez a példa hozzárendel egy alapértelmezett webhelyet a ContosoVirtualGateway nevű virtuális hálózati átjáróhoz.
Az első parancs létrehoz egy objektumhivatkozást a ContosoLocalGateway nevű helyi átjáróra.
Ez az objektumhivatkozás, amely a $LocalGateway nevű változóban van tárolva, az alapértelmezett webhelyként konfigurált átjárót jelöli.
A második parancs ezután létrehoz egy objektumhivatkozást a virtuális hálózati átjáróra, és az eredményt a következő nevű változóban $VirtualGateway.
A harmadik parancs a **Set-AzVirtualNetworkGatewayDefaultSite parancsmag** használatával rendeli hozzá az alapértelmezett webhelyet a ContosoVirtualGatewayhez.

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

### -GatewayDefaultSite
Egy objektumhivatkozást ad meg, amely a megadott virtuális hálózat alapértelmezett webhelyeként a helyi hálózati átjáróra hivatkozik.
A Get-AzLocalNetworkGateway parancsmagot használva létrehozhat egy objektumhivatkozást egy helyi átjáróra.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Egy objektumhivatkozást ad meg arra a virtuális hálózati átjáróra, ahol az alapértelmezett webhely lesz hozzárendelve.
Virtuális hálózati átjáróra a **Get-AzVirtualNetworkGateway** használatával hozhat létre objektumhivatkozást, és megadhatja az átjáró nevét.
A $VirtualGateway ezután használható a *VirtualNetworkGateway* paraméter paraméterértékeként:

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


