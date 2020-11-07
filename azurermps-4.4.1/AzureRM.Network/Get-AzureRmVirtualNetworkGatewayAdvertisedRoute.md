---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: a9b8cd9f13de8c1c4e3a7f20a0ffe410211f8973
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672762"
---
# Get-AzureRmVirtualNetworkGatewayAdvertisedRoute

## Áttekintés
Egy Azure virtuális hálózati átjáró által hirdetett útvonalak listázása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A BGP-peer IP-címének meghatározásakor a megadott Azure virtuális hálózati átjáró által az adott partnernek hirdetett útvonalakat sorolja fel. 

## Példák

### Példa 1
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

Ha az Azure Gateway nevű gatewayName az erőforráscsoport resourceGroupName, az IP-10.0.0.254 megkeresi a BGP-partnernek küldött útvonalak listáját.

### 2. példa
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

Ha az Azure Gateway nevű gatewayName az erőforráscsoport resourceGroupName, lekérdezi az útvonalakat, hogy az első BGP-társa Hirdessen az átjáró listáját a BGP-partnerek listájáról.

## PARAMÉTEREK

### -Peer
BGP társközi IP-címe. Ennek a helynek az IP-címének kell lennie az Azure virtuális hálózatról, amelyen az átjáró telepítve van. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális hálózati átjáró erőforráscsoport neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Virtuális hálózati átjáró neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSGatewayRoute []

## MEGJEGYZI
Ez a parancs csak az Azure virtuális hálózati átjárók esetében érvényes, amelyek BGP-kompatibilis kapcsolatokkal rendelkeznek.

## KAPCSOLÓDÓ HIVATKOZÁSOK

