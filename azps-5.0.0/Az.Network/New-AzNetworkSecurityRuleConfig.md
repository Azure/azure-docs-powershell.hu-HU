---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301478"
---
# New-AzNetworkSecurityRuleConfig

## Áttekintés
Hálózati biztonsági szabály konfigurációjának létrehozása.

## SZINTAXISA

### SetByResource (alapértelmezett)
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzNetworkSecurityRuleConfig** parancsmag az Azure hálózat biztonsági szabályának konfigurációját hozza létre egy hálózati biztonsági csoport számára.

## Példák

### Példa 1: hálózati biztonsági szabály létrehozása az RDP protokoll engedélyezéséhez
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

Ez a parancs létrehoz egy biztonsági szabályt, amely lehetővé teszi az internetről a 3389-as port elérését

### 2. példa: hálózati biztonsági szabály létrehozása, amely lehetővé teszi a HTTP-t
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

Ez a parancs létrehoz egy biztonsági szabályt, amely lehetővé teszi az internetről a 80-as port elérését

## PARAMÉTEREK

### -Access
Megadja, hogy engedélyezve van-e a hálózati forgalom vagy a hozzáférés visszautasítása.
A paraméter elfogadható értékei a következők: Allow és deny.

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Leírás
A létrehozandó hálózati biztonsági szabály konfigurációjának leírását adja meg.

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

### -DestinationAddressPrefix
A célcím előtagját adja meg.
A paraméter elfogadható értékei a következők:
- Osztály nélküli tartományok közötti útválasztási (CIDR) cím 
- Cél IP-címtartomány 
- A helyettesítő karakter (*) tetszőleges IP-címnek megfelelő (például VirtualNetwork, AzureLoadBalancer és Internet) használható.

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

### -DestinationApplicationSecurityGroup
Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére. Az "DestinationAddressPrefix" paraméterrel nem használható.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
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
Type: System.String[]
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
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Irány
Azt adja meg, hogy a rendszer kiértékeli-e a szabályt a bejövő vagy kimenő forgalomban.
A paraméter elfogadható értékei a következők: bejövő és kimenő.

```yaml
Type: System.String
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
A parancsmag által létrehozott hálózati biztonsági szabály konfigurációjának nevét adja meg.

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

### – Prioritás
A szabály konfigurációjának prioritását adja meg.
A paraméter elfogadható értékei a következők: az 100 és az 4096 közötti egész szám.
A prioritási számnak egyedinek kell lennie a gyűjtemény mindegyik szabályához.
Minél alacsonyabb a prioritási szám, annál nagyobb a szabály prioritása.

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

### -Protocol
Azt a hálózati protokollt adja meg, amelyre az új szabály-konfiguráció vonatkozik.
A paraméter elfogadható értékei a következők:
- TCP
- UDP
- a helyettesítő karakter (*) a két érték egyeztetéséhez.

```yaml
Type: System.String
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
- Egy helyettesítő karakter (*) az IP-cím megegyezéséhez.
A címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhatja.

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

### -SourceApplicationSecurityGroup
Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva. Az "SourceAddressPrefix" paraméterrel nem használható.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
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
Type: System.String[]
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
Type: System.String[]
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

### Nincs

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSSecurityRule

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


