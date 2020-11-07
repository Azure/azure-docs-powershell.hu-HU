---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 2003d93a50b1730a162cc910ef289748a86a2954
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848445"
---
# New-AzureRmApplicationGatewayFrontendIPConfig

## Áttekintés
Előtér IP-konfigurációját hozza létre egy alkalmazás-átjáróhoz.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### SetByResourceId
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmApplicationGatewayFrontendIPConfig** parancsmag létrehoz egy előtér IP-configuraton az Azure Application Gateway számára.
Az alkalmazás-átjárók kétféle előtér-IP-konfigurációt támogatnak: 

- Nyilvános IP-címek – privát IP-címek belső terheléselosztási (ILB) használatával.

Az alkalmazás-átjárók legfeljebb egy nyilvános IP-címet és egy privát IP-címet tartalmazhatnak.
A nyilvános IP-címet és a privát IP-címet külön-külön kell hozzáadni az előtér-IP-címekhez.

## Példák

### Példa 1: előtér IP-konfigurációjának létrehozása nyilvános IP-erőforrás-objektum használatával
```
PS C:\>$PublicIP = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

Az első parancs létrehoz egy nyilvános IP-erőforrás-objektumot, és a $PublicIP változóban tárolja.
A második parancs $PublicIP segítségével létrehoz egy FrontEndIP01 nevű új előtér-IP-konfigurációt, és a $FrontEnd változóban tárolja.

### 2. példa: statikus privát IP létrehozása előtér-IP-címként
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.
A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.
A harmadik parancs létrehozza a $Subnet FrontEndIP02 nevű előtér-IP-konfigurációt a második parancs és a privát IP-cím 10.0.1.1, majd a $FrontEnd változóban tárolja.

### 3. példa: dinamikus privát IP-cím létrehozása előtér-IP-címként
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.
A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.
A harmadik parancs a második parancs segítségével létrehoz egy FrontEndIP03 nevű előtér-IP-konfigurációt, és a $FrontEnd változóban tárolja a $Subnet.

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

### -Name (név)
Annak az előtér-IP-konfigurációnak a nevét adja meg, amelyet a parancsmag hoz létre.

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
Annak a magánhálózati IP-címnek a megadása, amelyhez ez a parancsmag társítva van az alkalmazás-átjáró előtér IP-címével.
Ez csak akkor adható meg, ha meg van adva alhálózat.
Az IP-cím statikusan van kiosztva az alhálózatról.

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

### -PublicIPAddress
Annak a nyilvános IP-cím objektumnak a meghatározása, amelyet ez a parancsmag társít az alkalmazás átjárójának előtér-IP-címéhez.

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
Annak a nyilvános IP-címnek az AZONOSÍTÓját adja meg, amely a parancsmag a program átjárójának előtér-IP-címéhez van társítva.

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
Annak az alhálózatnak az objektumát adja meg, amely a parancsmag a program átjárójának előtér-IP-címéhez van társítva.
Ha megadja ezt a paramétert, az azt jelenti, hogy az átjáró privát IP-címet használ.
Ha a *PrivateIPAddresss* paramétert adja meg, akkor az a paraméter által meghatározott alhálózathoz kell tartoznia.
Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.

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

### – NetI
Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag az alkalmazás-átjáró előtér-IP-konfigurációját társítja.
Ha megadja az *alhálózati* paramétert, az azt jelenti, hogy az átjáró privát IP-címet használ.
Ha a *PrivateIPAddress* paramétert adja meg, akkor az *alhálózat* által megadott alhálózathoz kell tartoznia.
Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendIPConfiguration

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmApplicationGatewayFrontendIPConfig](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[Get-AzureRmApplicationGatewayFrontendIPConfig](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[Remove-AzureRmApplicationGatewayFrontendIPConfig](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[Set-AzureRmApplicationGatewayFrontendIPConfig](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


