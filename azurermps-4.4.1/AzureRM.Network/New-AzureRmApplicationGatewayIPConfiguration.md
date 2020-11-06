---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 076965d0f63a8c28742cf9853068b9e020403a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502671"
---
# New-AzureRmApplicationGatewayIPConfiguration

## Áttekintés
IP-konfigurációt hoz létre egy alkalmazás-átjáróhoz.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### SetByResourceId
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmApplicationGatewayIPConfiguration** parancsmag IP-konfigurációt hoz létre egy alkalmazás-átjáróhoz.
Az IP-konfiguráció tartalmazza azt az alhálózatot, amelyben az alkalmazás átjárója van telepítve.

## Példák

### Példa 1: IP-konfiguráció létrehozása egy alkalmazás-átjáróhoz.
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik.

A második parancs beilleszti annak az alhálózatnak az alhálózatának konfigurációját, amely az előző parancs virtuális hálózata, és a $Subnet változóban tárolja.

A harmadik parancs az IP-konfigurációt az $Subnet használatával hozza létre.

## PARAMÉTEREK

### -Name (név)
A létrehozandó IP-konfiguráció nevét adja meg.

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

### -Alhálózat
Az alhálózat-objektumot adja meg.
Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – NetI
Az alhálózati azonosítót adja meg.
Ez az az alhálózat, amelyben az alkalmazás-átjárót telepítették.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. commands. Network. models. PSApplicationGatewayIPConfiguration

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmApplicationGatewayIPConfiguration](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[Get-AzureRmApplicationGatewayIPConfiguration](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[Remove-AzureRmApplicationGatewayIPConfiguration](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[Set-AzureRmApplicationGatewayIPConfiguration](./Set-AzureRmApplicationGatewayIPConfiguration.md)


