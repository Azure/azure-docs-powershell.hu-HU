---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 0a8a5c4084813bac74ea907575d2bd26c3d8c5f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503480"
---
# Resize-AzureRmVirtualNetworkGateway

## Áttekintés
Egy meglévő virtuális hálózati átjáró átméretezése.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az **átméretezés-AzureRmVirtualNetworkGateway** parancsmag lehetővé teszi a virtuális hálózati átjáró készletezési egységének (SKU) módosítását.
A SKU határozza meg az átjáró funkcióit, így például az átviteli sebességet és az engedélyezett IP-alagutak maximális számát.
Az Azure támogatja az alapvető, normál, nagy teljesítményű, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ, (néha kicsi, közepes és nagy méretű SKU) használatát.
Az egyes SKU-típusok képességeiről további információt a című témakörben találhat https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .
Tartsa szem előtt, hogy a SKU az árak és a funkciók között eltérő.
További információ: https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## Példák

### Példa 1: virtuális hálózati átjáró méretének módosítása
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

Ez a példa a ContosoVirtualGateway nevű virtuális hálózati átjáró méretét módosítja.
Az első parancs egy objektumra mutató hivatkozást hoz létre a ContosoVirtualGateway-hoz; Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.
A második parancs ezt követően a **Resize-AzureRmVirtualNetworkGateway** parancsmagot használja az *GatewaySku* tulajdonság egyszerű értékre való beállításához.

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

### -GatewaySku
Az átjáró új típusú SKU-típusát adja meg.
A paraméter elfogadható értékei a következők:
- Egyszerű
- Standard
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
Az átméretezni kívánt virtuális hálózati átjáróra mutató objektum hivatkozását adja meg.
Az objektum hivatkozását létrehozhatja a Get-AzureRmVirtualNetworkGateway használatával, és megadhatja az átjáró nevét.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway
Paraméterek: VirtualNetworkGateway (ByValue)

### System. String

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway

## MEGJEGYZI
Az alap/normál/HighPerformance SKU-ról nem lehet átméretezni az új VpnGw1/VpnGw2/VpnGw3 SKU-ra. A további átméretezés nem engedélyezett a VpnGw1AZ/VpnGw2AZ/VpnGw3AZ vagy a ErGw1AZ/ErGw2AZ/ErGw3AZ. Az átméretezés csak a SKU "sorozat"-ban engedélyezett, például a VpnGw1AZ átméretezhetők a VpnGw2AZ/VpnGw3AZ és a ErGw1AZ átméretezhetők a ErGw2AZ/ErGw3AZ. Lásd: https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways utasítások.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmVpnClientPackage](./Get-AzureRmVpnClientPackage.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


