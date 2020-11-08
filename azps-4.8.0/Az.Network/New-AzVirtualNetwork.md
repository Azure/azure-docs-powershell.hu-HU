---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: d131b4aa22f46fed151486ed2d87f32684b6035a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184357"
---
# New-AzVirtualNetwork

## Áttekintés
Virtuális hálózatot hoz létre.

## SZINTAXISA

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzVirtualNetwork** parancsmag egy Azure virtuális hálózatot hoz létre.

## Példák

### Példa 1: virtuális hálózat létrehozása két alhálózattal
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

Ebben a példában két alhálózatot tartalmazó virtuális hálózat jön létre. Először egy új erőforráscsoport jön létre a CentralUS-régióban. Ezután a példa két alhálózat memóriában ábrázolt példányait hozza létre. A New-AzVirtualNetworkSubnetConfig parancsmag nem hoz létre alhálózatokat a kiszolgálón. Egy frontendSubnet nevű alhálózatot és egy backendSubnet nevű alhálózatot tartalmaz. A New-AzVirtualNetwork parancsmag ezután virtuális hálózatot hoz létre a CIDR 10.0.0.0/16 segítségével a cím előtagként és két alhálózattal.

### 2. példa: virtuális hálózat létrehozása a DNS-beállításokkal
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

Ebben a példában egy virtuális hálózat jön létre két alhálózattal és két DNS-kiszolgálóval. A DNS-kiszolgálók virtuális hálózaton való megadásának hatásai az, hogy a virtuális hálózatba telepített hálózati adapterek/VMs-kiszolgálók alapértelmezés szerint öröklik ezeket a DNS-kiszolgálókat. Ezek az alapértelmezett beállítások a NIC-es hálózati adapteren keresztül felülíródnak. Ha a VNET nem ad meg DNS-kiszolgálókat, és nem a hálózati adaptereken, akkor az alapértelmezett Azure DNS-kiszolgálók használhatók a DNS-feloldáshoz.

### 3. példa: virtuális hálózat létrehozása hálózati biztonsági csoportra hivatkozó alhálózattal
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

Ez a példa virtuális hálózatot hoz létre olyan alhálózatokkal, amelyek hálózati biztonsági csoportra hivatkoznak. Először a példa létrehoz egy erőforráscsoportot tárolóként a létrehozandó erőforrásokhoz. Ezután egy hálózati biztonsági csoport jön létre, amely lehetővé teszi a bejövő RDP-elérést, de egyéb módon kényszeríti az alapértelmezett hálózati biztonsági csoport szabályait. A New-AzVirtualNetworkSubnetConfig parancsmag két alhálózat memóriában ábrázolt példányait hozza létre, amelyek a létrehozott hálózati biztonsági csoportra hivatkoznak. A New-AzVirtualNetwork parancs a virtuális hálózatot hozza létre.

## PARAMÉTEREK

### -AddressPrefix
Egy virtuális hálózat IP-címeinek egy-egy IP-címét adja meg.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
A parancsmag futtatása a háttérben

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

### -BgpCommunity
A BGP-Közösség hirdetett át a ExpressRoute.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DdosProtectionPlanId
Hivatkozás a virtuális hálózathoz társított DDoS védelmi terv erőforrásra.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DnsServer
Az alhálózat DNS-kiszolgálóját adja meg.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableDdosProtection
Egy kapcsoló paraméter, amely akkor jelenik meg, ha a DDoS védelem engedélyezve van vagy nem.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -IpAllocation
A virtuális hálózat IpAllocations adja meg.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
A virtuális hálózat területét adja meg.

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

### -Name (név)
Annak a virtuális hálózatnak a neve, amelyet a parancsmag hoz létre.

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

### -ResourceGroupName
A virtuális hálózatot tartalmazó erőforráscsoport nevét adja meg.

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

### -Alhálózat
A virtuális hálózattal társítani kívánt alhálózatok listáját adja meg.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

### System. string []

### Microsoft. Azure. commands. Network. models. PSSubnet []

### System. Collections. Hashtable

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSVirtualNetwork

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)

[Remove-AzVirtualNetwork](./Remove-AzVirtualNetwork.md)

[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)

[Új – AzDdosProtectionPlan](./New-AzDdosProtectionPlan.md)
