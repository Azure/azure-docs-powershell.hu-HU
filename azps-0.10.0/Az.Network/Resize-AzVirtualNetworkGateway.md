---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: bd42d7cec30b7d42dcb1cdb3657f6681bf2cb6b0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843722"
---
# Resize-AzVirtualNetworkGateway

## Áttekintés
Egy meglévő virtuális hálózati átjáró átméretezése.

## SZINTAXISA

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az **átméretezés-AzVirtualNetworkGateway** parancsmag lehetővé teszi a virtuális hálózati átjáró készletezési egységének (SKU) módosítását.
A SKU határozza meg az átjáró funkcióit, így például az átviteli sebességet és az engedélyezett IP-alagutak maximális számát.
Az Azure támogatja az alapvető, normál, nagy teljesítményű, VpnGw1, VpnGw2 és VpnGw3 SKU-ket (más néven kicsi, közepes és nagy méretű SKU).
Az egyes SKU-típusok képességeiről további információt a című témakörben találhat https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .

Tartsa szem előtt, hogy a SKU az árak és a funkciók között eltérő.
További információ: https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## Példák

### Példa 1: virtuális hálózati átjáró méretének módosítása
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

Ez a példa a ContosoVirtualGateway nevű virtuális hálózati átjáró méretét módosítja.

Az első parancs egy objektumra mutató hivatkozást hoz létre a ContosoVirtualGateway-hoz; Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.

A második parancs ezt követően a **Resize-AzVirtualNetworkGateway** parancsmagot használja az *GatewaySku* tulajdonság egyszerű értékre való beállításához.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
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

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Az átméretezni kívánt virtuális hálózati átjáróra mutató objektum hivatkozását adja meg.
Az objektum hivatkozását létrehozhatja a Get-AzVirtualNetworkGateway használatával, és megadhatja az átjáró nevét.

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

###  
Ez a parancsmag a **Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway** objektum pipeline-példányait fogadja el.

## KIMENETEK

###  
Ez a parancsmag módosítja a **Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway** objektum meglévő példányait.

## MEGJEGYZI
Az alap/normál/HighPerformance SKU-ról nem lehet átméretezni az új VpnGw1/VpnGw2/VpnGw3 SKU-ra. Lásd: https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways utasítások.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


