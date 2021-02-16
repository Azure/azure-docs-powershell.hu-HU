---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 3899bfcd607e4d3e5e5b1d92e8a62096037102a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203194"
---
# Add-AzExpressRouteCrossConnectionPeering

## SYNOPSIS
Társviszony-konfigurációt ad az ExpressRoute-kapcsolathoz.

## SZINTAXIS

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzExpressRouteCrossConnectionPeering** parancsmag társviszony-konfigurációt ad az ExpressRoute-kapcsolathoz. Vegye figyelembe, hogy az **Add-AzExpressRouteCrossConnectionPeering** futtatása után a Set-AzExpressRouteCrossConnection parancsmagot kell felhívnia a konfiguráció aktiválásához.

## PÉLDÁK

### 1. példa: Társ felvétele meglévő ExpressRoute-keresztkapcsolatba
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

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

### -ExpressRouteCrossConnection
Az ExpressRoute-kapcsolat módosítása folyamatban van. Ez a **Get-AzExpressRouteCrossConnection** parancsmag által visszaadott Azure-objektum.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MicrosoftConfigAdvertedPublicPrefix
A MicrosoftPeering társviszony-típusa esetében meg kell adnia a BGP-munkameneten keresztül meghirdetett összes előtag listáját. Csak a nyilvános IP-cím előtagját fogadja el a rendszer. Vesszővel elválasztott listát is küldhet, ha előtagokat tervez küldeni. Ezeket az előtagokat a Routing Registry Name (RIR/IRR) névben kell regisztrálnia.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MicrosoftConfigCustomerAsn
Ha Ön olyan hirdetési előtag, amely nem a társviszony-létesítő AS számhoz van regisztrálva, megadhatja azt az AS-számot, amelyre regisztrálva vannak.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MicrosoftConfigRoutingRegistryName
Az Routing Registry Name (RIR/BRR), amelyre az AS szám és az előtagok regisztrálva vannak.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A hozzáadható társviszony neve.

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

### -PeerAddressType
PeerAddressType

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PeerASN
Az ExpressRoute-keresztkapcsolat AS-száma. Nyilvános ASN-nek kell lennie, ha a Társviszony-típus az AzurePublicPeering.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeeringType
A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryPeerAddressPrefix
Ez a társviszony elsődleges útválasztási útvonalának IP-címtartománya. Ennek egy /30 CIDR alhálózatnak kell lennie. Az alhálózat első páratlan címét hozzá kell rendelni az útválasztó felületéhez. Az Azure beállítja a következő, egyenletesen számmal megadott címet az Azure útválasztó felületéhez.

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

### -SecondaryPeerAddressPrefix
Ez a társviszony másodlagos útválasztási útvonalának IP-címtartománya. Ennek egy /30 CIDR alhálózatnak kell lennie. Az alhálózat első páratlan címét hozzá kell rendelni az útválasztó felületéhez. Az Azure beállítja a következő, egyenletesen számmal megadott címet az Azure útválasztó felületéhez.

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

### -SharedKey
Ez egy opcionális MD5-kivonat, amely elő megosztott kulcsként használatos a társviszony-konfigurációhoz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VlanId
Ez a társviszonyhoz rendelt VLAN azonosítószáma.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### PSExpressRouteCrossConnection
Az "ExpressRouteCrossConnection" paraméter a "PSExpressRouteCrossConnection" típusú értéket fogadja el a folyamatból.

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzExpressRouteCrossConnectionPeering](Get-AzExpressRouteCrossConnectionPeering.md)

[Remove-AzExpressRouteCrossConnectionPeering](Remove-AzExpressRouteCrossConnectionPeering.md)

[Get-AzExpressRouteCrossConnection](Get-AzExpressRouteCrossConnection.md)

[Set-AzExpressRouteCrossConnection](Set-AzExpressRouteCrossConnection.md)
