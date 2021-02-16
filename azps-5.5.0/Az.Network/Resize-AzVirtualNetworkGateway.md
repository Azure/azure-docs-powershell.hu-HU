---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: dd48af6a0f20cafea5911adb629a83323faa94a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151475"
---
# Resize-AzVirtualNetworkGateway

## SYNOPSIS
Átméretez egy meglévő virtuális hálózati átjárót.

## SZINTAXIS

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Resize-AzVirtualNetworkGateway** parancsmag segítségével módosíthatja egy virtuális hálózati átjáró készletezési egységét.
Az SKUs meghatározza az átjárók képességeit, többek között az átviteli sebességet és az engedélyezett IP-átjárók maximális számát.
Az Azure alapszintű, szabványos, nagy teljesítményű, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (más néven Kis, Közepes és Nagy SKUs) támogatja.
Az egyes termékváltozat-típusokkal kapcsolatos részletes információkért https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ lásd: .
Ne feledje, hogy a termékkódja az árazásban és a képességekben is különbözik.
További információ: https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## PÉLDÁK

### 1. példa: Virtuális hálózati átjáró méretének módosítása
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

Ez a példa módosítja a ContosoVirtualGateway nevű virtuális hálózati átjáró méretét.
Az első parancs létrehoz egy objektumhivatkozást a ContosoVirtualGatewayre; Ezt az objektumhivatkozást egy $Gateway.
A második parancs ezután az **Resize-AzVirtualNetworkGateway** parancsmagot használva alapszintűre állíthatja az *ÁtjáróKku* tulajdonságot.

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

### -GatewaySku
Az átjárók termékváltozatának új típusát adja meg.
A paraméter elfogadható értékei a következőek:
- Alapszintű
- Normál
- Nagy teljesítmény
- VpnGw1
- VpnGw2
- VpnGw3
- VpnGw1AZ 
- VpnGw2AZ 
- VpnGw3AZ 
- ErGw1AZ 
- ErGw2AZ 
- ErGw3AZ 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Az átméretezni szükséges virtuális hálózati átjáró objektumhivatkozását adja meg.
Ezt az objektumhivatkozást a Get-AzVirtualNetworkGateway és az átjáró nevének megadásával hozhatja létre.

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

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## MEGJEGYZÉSEK
Alapszintű/Standard/HighPerformance SKUs-ból nem lehet átméretezni az új VpnGw1/VpnGw2/VpnGw3-SKUs-ra. A vpnGw1AZ/VpnGw2AZ/VpnGw3AZ vagy ErGw1AZ/ErGw2AZ/ErGw2AZ/ErGw3AZ nem engedélyezett további átméretezések. Az átméretezés csak az SKU "adatsorában" engedélyezett, például a VpnGw1AZ átméretezhetők a VpnGw2AZ/VpnGw3AZ/VpnGw3AZ és az ErGw1AZ termékváltozatba vagy az ErGw2AZ/ErGw3AZ alkalmazásba. Útmutatást https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways itt láthat.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
