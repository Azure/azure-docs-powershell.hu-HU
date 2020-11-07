---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 963dc6391ef5f500b26068e2a407eacd64ce6c16
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843605"
---
# Set-AzNetworkSecurityRuleConfig

## Áttekintés
Egy hálózati biztonsági szabály konfigurációjának cél állapotának beállítása.

## SZINTAXISA

### SetByResource (alapértelmezett)
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResourceId
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzNetworkSecurityRuleConfig** parancsmag az Azure hálózati biztonsági szabályok konfigurációjának cél állapotát állítja be.

## Példák

### Példa 1: az Access-konfiguráció módosítása hálózati biztonsági szabályokban
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

Az első parancs a NSG-FrontEnd nevű hálózati biztonsági csoportot kapja meg, majd az $nsg változóban tárolja.

A második parancs a pipeline operátor segítségével továbbítja a biztonsági $nsg csoportot a Get-AzNetworkSecurityRuleConfig, amely az RDP-Rule nevű biztonsági szabály konfigurációját kapja.

A harmadik parancs az RDP-Rule hozzáférési konfigurációját a Megtagadás értékre módosítja.

## PARAMÉTEREK

### -Access
Megadja, hogy engedélyezve van-e a hálózati forgalom vagy a hozzáférés visszautasítása. A paraméter elfogadható értékei a következők: Allow és deny.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Leírás
A szabályok konfigurációjának leírását adja meg.
A maximális méret 140 karakter.

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

### -DestinationAddressPrefix
A célcím előtagját adja meg.
A paraméter elfogadható értékei a következők:

- Osztály nélküli tartományok közötti útválasztási (CIDR) cím 
- Cél IP-címtartomány 
- Bármely IP-címnek megfelelő helyettesítő karakter (*)

Címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhat.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroup
Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére. Az "DestinationAddressPrefix" paraméterrel nem használható.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroupId
Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére. Az "DestinationAddressPrefix" paraméterrel nem használható.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
A cél portját vagy a kívánt cellatartományt adja meg.
A paraméter elfogadható értékei a következők:

- Egész szám 
- 0 és 65535 közötti egész számok
- Bármely portnak megfelelő helyettesítő karakter (*)

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Irány
Azt adja meg, hogy a rendszer kiértékeli-e a bejövő vagy kimenő forgalom szabályait.
A paraméter elfogadható értékei a következők: bejövő és kimenő.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A parancsmag által beállított hálózati biztonsági szabály konfigurációjának nevét adja meg.

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

### -NetworkSecurityGroup
Azt a **NetworkSecurityGroup** -objektumot adja meg, amely a beállítani kívánt hálózati biztonsági szabály konfigurációját tartalmazza.

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Prioritás
A szabály konfigurációjának prioritását adja meg.
A paraméter elfogadható értékei a következők: az 100 és az 4096 közötti egész szám.

A prioritási számnak egyedinek kell lennie a gyűjtemény mindegyik szabályához.
Minél alacsonyabb a prioritási szám, annál nagyobb a szabály prioritása.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Azt a hálózati protokollt adja meg, amelyre a szabály konfigurációja vonatkozik.
A paraméter elfogadható értékei a következők:

 --TCP
- UDP
- Helyettesítő karakter (*) a két érték egyeztetéséhez

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
A forráscím előtagját adja meg.
A paraméter elfogadható értékei a következők:

- CIDR
- A forrás IP-köre
- Bármely IP-címnek megfelelő helyettesítő karakter (*)

A címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhatja.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroup
Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva. Az "SourceAddressPrefix" paraméterrel nem használható.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroupId
Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva. Az "SourceAddressPrefix" paraméterrel nem használható.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
A forrás portját vagy a tartománnyal adja meg.
A paraméter elfogadható értékei a következők:

- Egész szám
- 0 és 65535 közötti egész számok
- Bármely portnak megfelelő helyettesítő karakter (*)

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSNetworkSecurityGroup
A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[Új – AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)


