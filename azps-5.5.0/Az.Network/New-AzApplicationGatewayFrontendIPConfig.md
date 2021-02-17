---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206854"
---
# New-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Előlapi IP-konfigurációt hoz létre egy alkalmazás-átjáróhoz.

## SZINTAXIS

### SetByResourceId
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzApplicationGatewayFrontendIPConfig** parancsmag előtér-IP-konfigurációt hoz létre egy Azure-alkalmazás átjáróhoz.
Az alkalmazás-átjárók kétféle előlapi IP-konfigurációt támogatnak: 
- Nyilvános IP-címek – Privát IP-címek belső terheléselosztás használatával.
 Az alkalmazás-átjáróknak legalább egy nyilvános IP-címük és egy személyes IP-címük lehet.
A nyilvános IP-címet és a privát IP-címet külön kell hozzáadni előlapi IP-címként.

## PÉLDÁK

### 1. példa: Előlapi IP-konfiguráció létrehozása nyilvános IP-erőforrás-objektum használatával
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

Az első parancs létrehoz egy nyilvános IP-erőforrásobjektumot, és azt a $PublicIP tárolja.
A második parancs $PublicIP FrontEndIP01 nevű új előlapi IP-konfigurációt hoz létre, és a $FrontEnd tárolja.

### 2. példa: Statikus privát IP létrehozása előlapi IP-címként
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Az első parancs egy VNet01 nevű virtuális hálózatot kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $VNet tárolja.
A második parancs egy Alhálózat01 nevű alhálózati konfigurációt kap, $VNet az első parancsból, és a $Subnet tárolja.
A harmadik parancs létrehoz egy FrontEndIP02 nevű előlapi IP-konfigurációt a $Subnet használatával a második parancsból és a 10.0.1.1-es privát IP-címből, majd a $FrontEnd változóban tárolja.

### 3. példa: Dinamikus privát IP létrehozása előlapi IP-címként
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

Az első parancs egy VNet01 nevű virtuális hálózatot kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $VNet tárolja.
A második parancs egy Alhálózat01 nevű alhálózati konfigurációt kap, $VNet az első parancsból, és a $Subnet tárolja.
A harmadik parancs létrehoz egy FrontEndIP03 nevű előlapi IP-konfigurációt a második $Subnet használatával, és azt a $FrontEnd változóban tárolja.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A parancsmag által létrehozott előlapi IP-konfiguráció neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIPAddress
Azt a privát IP-címet adja meg, amelyet a parancsmag az alkalmazás átjárója előlapi IP-címével társít.
Ezt csak alhálózat megadva esetén lehet megadni.
Ez az IP-cím statikusan ki van osztva az alhálózatból.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfiguration
PrivateLinkConfiguration

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfigurationId
PrivateLinkConfigurationId

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddress
Azt a nyilvános IP-címobjektumot adja meg, amelyet ez a parancsmag társít az alkalmazás átjárója előlapi IP-címével.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
Megadja azt a nyilvános IP-címazonosítót, amelyet ez a parancsmag társít az alkalmazás átjárójának előlapi IP-címével.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Alhálózat
Azt az alhálózati objektumot adja meg, amelyet ez a parancsmag társít az alkalmazás átjárója előtér-IP-címével.
Ha ezt a paramétert adja meg, az azt jelenti, hogy az átjáró privát IP-címet használ.
Ha a *PrivateIPAddress* paraméter meg van adva, annak a paraméterben megadott alhálózathoz kell tartozni.
Ha *a PrivateIPAddress* nincs megadva, az alhálózat egyik IP-címe dinamikusan az alkalmazás-átjáró előtér-IP-címeként lesz felvéve.

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Megadja azt az alhálózati azonosítót, amelyet ez a parancsmag társít az alkalmazás átjárójának előtér-IP-konfigurációjával.
Ha megadja az *Alhálózat* paramétert, az azt jelenti, hogy az átjáró privát IP-címet használ.
Ha a *PrivateIPAddress* paraméter meg van adva, annak az alhálózat által megadott *alhálózathoz kell tartozni.*
Ha *a PrivateIPAddress* nincs megadva, az alhálózat egyik IP-címe dinamikusan az alkalmazás-átjáró előtér-IP-címeként lesz felvéve.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


