---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351414"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Eltávolítja az alapértelmezett webhelyet egy virtuális hálózati átjáróból.

## SZINTAXIS

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzVirtualNetworkGatewayDefaultSite** parancsmag eltávolítja a virtuális hálózati átjáróból az alapértelmezett kényszerített átjárót.
A kényszerített átjárók használatával átirányíthatja az internetes forgalmat az Azure virtuális gépeiből a helyszíni hálózatba; ez lehetővé teszi a forgalom vizsgálatát és naplózását, mielőtt felengedi azt.
A kényszerített alagutaszás virtuális magánhálózati alagutat használ; Ehhez az átjáróhoz egy alapértelmezett webhelyre, egy helyi átjáróra van szükség, ahol az Összes Azure internetes forgalmat átirányítják.
**A Remove-AzVirtualNetworkGatewayDefaultSite** eltávolítja az átjárókhoz rendelt alapértelmezett webhelyet.
Ha ezt a beállítást használja, a Set-AzVirtualNetworkGatewayDefaultSite kell hozzárendelni egy új alapértelmezett webhelyet, mielőtt az átjárót használva kényszerített átjárót használna.

## PÉLDÁK

### 1. példa: Virtuális hálózati átjáróhoz rendelt alapértelmezett webhely eltávolítása
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

Ez a példa eltávolítja a ContosoVirtualGateway nevű virtuális hálózati átjáróhoz jelenleg hozzárendelt alapértelmezett webhelyet.
Az első parancs **a Get-AzVirtualNetworkGateway** segítségével hoz létre objektumhivatkozást az átjáróra; Ezt az objektumhivatkozást egy $Gateway.
A második parancs ezután **a Remove-AzVirtualNetworkGatewayDefaultSite** paranccsal eltávolítja az átjáróhoz társított alapértelmezett webhelyet.

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

### -VirtualNetworkGateway
Egy objektumhivatkozást ad meg a virtuális hálózati átjáróra, amely az alapértelmezett eltávolítható webhelyet tartalmazza.
Virtuális hálózati átjáróra való hivatkozás létrehozásához használja a Get-AzVirtualNetworkGateway és adja meg az átjáró nevét.

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

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


