---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 1ab3d82b494d5598081ea229a7ae50d486b8ca20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156754"
---
# Set-AzFirewall

## SYNOPSIS
Módosított tűzfalat ment.

## SZINTAXIS

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzFirewall** parancsmag frissíti az Azure tűzfalat.

## PÉLDÁK

### 1: A tűzfal alkalmazásszabálycsoport prioritásának frissítése
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

Ez a példa frissíti egy Azure tűzfal meglévő szabálygyűjteményének prioritását.
Ha az "rg" erőforráscsoportban az Azure Firewall "AzureFirewall" egy "ruleCollectionName" nevű alkalmazásszabálygyűjteményt tartalmaz, a fenti parancsok megváltoztatják az adott szabálygyűjtemény prioritását, és később frissítik az Azure tűzfalat. A helyi Set-AzFirewall parancs nélkül a helyi objektumon $azFw műveletek nem jelennek meg a kiszolgálón.

### 2: Azure tűzfal létrehozása és alkalmazásszabály-gyűjtemény beállítása később
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

Ebben a példában először egy tűzfal jön létre alkalmazásszabálygyűjtemények nélkül. Ezután létrejön egy alkalmazásszabály és egy alkalmazásszabálygyűjtemény, majd a tűzfal objektum módosul a memóriában anélkül, hogy ez hatással lenne a felhőbeli valódi konfigurációra. Ahhoz, hogy a módosítások a felhőben is tükröződni Set-AzFirewall meg kell őket.

### 3: A Threat Intel műveletmód frissítése az Azure tűzfalban
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

Ebben a példában az "rg" erőforráscsoportban az Azure Firewall "AzureFirewall" veszélyforrás-intel műveletmódját frissíti.
A helyi Set-AzFirewall parancs nélkül a helyi objektumon $azFw műveletek nem jelennek meg a kiszolgálón.

### 4: A tűzfal áthelyezése és kiosztása
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
Ez a példa beolvassa a tűzfalat, áthelyezi a tűzfalat, és menti azt. A Deallocate parancs eltávolítja a futó szolgáltatást, de megőrzi a tűzfal konfigurációját. Ahhoz, hogy a módosítások a felhőben is tükröződni Set-AzFirewall meg kell őket.
Ha a felhasználó ismét el szeretné kezdeni a szolgáltatást, a Tűzfalon meg kell hívatni a Kiosztás módszert.
Az új VNet és nyilvános IP-címnek ugyanabban az erőforráscsoportban kell lennie, mint a tűzfalnak. Ahhoz, hogy a módosítások a felhőben is Set-AzFirewall meg.

### 5: Kiosztani egy felügyeleti nyilvános IP-címet a kényszerített átvezetési forgatókönyvekhez
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
Ez a példa kiosztja a tűzfalat egy felügyeleti nyilvános IP-címmel és alhálózattal a kényszerített átjárók esetén. A VNetnek tartalmaznia kell egy "AzureFirewallManagementSubnet" nevű alhálózatot.

### 6: Nyilvános IP-cím hozzáadása azure tűzfalhoz
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

Ebben a példában a tűzfalhoz csatolt "azFwPublicIp1" nyilvános IP-cím.

### 7: Nyilvános IP-cím eltávolítása az Azure tűzfalról
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

Ebben a példában az "azFwPublicIp1" nyilvános IP-cím leválasztva a tűzfalról.

### 8: A felügyeleti nyilvános IP-cím módosítása az Azure tűzfalon
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

Ebben a példában a tűzfal felügyeleti nyilvános IP-címe "AzFwMgmtPublicIp2" lesz.

### 9: DNS-konfiguráció hozzáadása azure tűzfalhoz
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

Ebben a példában a DNS-proxy és a DNS-kiszolgáló konfigurációja a tűzfalhoz van csatolva.

### 10: Meglévő szabály célhelyének frissítése a tűzfal alkalmazásszabálygyűjteményében
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

Ez a példa frissíti egy meglévő szabály célhelyét egy Azure tűzfal szabálygyűjteményében. Ez lehetővé teszi, hogy automatikusan frissítse a szabályokat, amikor az IP-címek dinamikusan változnak.

### 11: Az Aktív FTP engedélyezése az Azure tűzfalon
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

Ebben a példában az Aktív FTP engedélyezve van a tűzfalon.

## PARAMETERS

### -AsJob
Parancsmag futtatása a háttérben

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

### -AzureFirewall
The AzureFirewall

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
