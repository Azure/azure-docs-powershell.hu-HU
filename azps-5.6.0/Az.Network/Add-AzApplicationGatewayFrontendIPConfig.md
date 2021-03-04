---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 32e8671267efddd94252e592de45cb014b5dd0de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926602"
---
# Add-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Előlapi IP-konfigurációt ad egy alkalmazás-átjáróhoz.

## SZINTAXIS

### SetByResourceId
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzApplicationGatewayFrontendIPConfig** parancsmag előtér-IP-konfigurációt ad egy alkalmazás-átjáróhoz.
Az alkalmazásátjárók kétféle előlapi IP-konfigurációt támogatnak: 
- Nyilvános IP-címek
- Privát IP-címek belső terheléselosztással (ILB) Az alkalmazás-átjáróknak legalább egy nyilvános IP-címük és egy privát IP-címük lehet.
Vegye fel a nyilvános IP-címet és a privát IP-címet külön előlapi IP-címként.

## PÉLDÁK

### 1. példa: Nyilvános IP-cím hozzáadása előlapi IP-címként
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

Az első parancs létrehoz egy nyilvános IP-címobjektumot, és azt a $PublicIp tárolja.
A második parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $AppGw tárolja.
A harmadik parancs hozzáadja a FrontEndIp01 nevű előlapi IP-konfigurációt az $AppGw-beli átjáróhoz a $PublicIp.

### 2. példa: Statikus privát IP-cím hozzáadása előlapi IP-címként
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Az első parancs egy VNet01 nevű virtuális hálózatot kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $VNet tárolja.
A második parancs egy Alhálózat01 nevű alhálózati konfigurációt kap, $VNet az első parancsból, és a $Subnet tárolja.
A harmadik parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $AppGw tárolja.
A negyedik parancs hozzáad egy FrontendIP02 nevű előlapi IP-konfigurációt a második parancs $Subnet és a 10.0.1.1-es privát IP-cím használatával.

### 3. példa: Dinamikus privát IP-cím hozzáadása előlapi IP-címként
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

Az első parancs egy VNet01 nevű virtuális hálózatot kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $VNet tárolja.
A második parancs egy Alhálózat01 nevű alhálózati konfigurációt kap, $VNet az első parancsból, és a $Subnet tárolja.
A harmadik parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $AppGw tárolja.
A negyedik parancs hozzáad egy FrontendIP02 nevű előlapi IP-konfigurációt $Subnet második parancsból származó adatok használatával.

## PARAMETERS

### -ApplicationGateway
Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag előlapi IP-konfigurációt ad.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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
Az előlapi IP-konfiguráció nevét adja meg.

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
Megadja az alkalmazás átjárója előlapi IP-címeként hozzáadni szükséges személyes IP-címet.
Ha meg van adva, az IP-cím statikusan ki van osztva az alhálózatból.

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
Azt a nyilvános IP-címet adja meg, amelyet ez a parancsmag előlapi IP-címként ad hozzá az alkalmazás-átjáróhoz.

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
Annak a nyilvános IP-címnek az azonosítója, amelyet ez a parancsmag előlapi IP-címként ad hozzá az alkalmazás-átjáróhoz.

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
Azt az alhálózatot adja meg, amelyet ez a parancsmag előtér-IP-konfigurációként ad hozzá.
Ha ezt a paramétert adja meg, az azt jelenti, hogy az alkalmazás átjárója támogatja a privát IP-alapú konfigurációt.
Ha a *PrivateIPAddress* paraméter meg van adva, annak ehhez az alhálózathoz kell tartozni.
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
Azt az alhálózati azonosítót adja meg, amelyet ez a parancsmag az előtér-IP-konfigurációként ad hozzá.
Az alhálózat átadása magánjellegű IP-címet jelent.
Ha a *PrivateIPAddress* paraméter meg van adva, annak ehhez az alhálózathoz kell tartozni.
Ellenkező esetben az alhálózat egyik IP-címe dinamikusan az alkalmazás átjárója előtér-IP-címeként lesz felveve.

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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[New-AzApplicationGatewayFrontendIPConfig](./New-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


