---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: d59bb27608e1ccf614048dcd27eb6643695ba523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006486"
---
# Add-AzLoadBalancerOutboundRuleConfig

## SYNOPSIS
Kimenő szabálykonfigurációt ad a terheléselosztáshoz.

## SZINTAXIS

### SetByResource (alapértelmezett)
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByResourceId
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzLoadBalancerOutboundRuleConfig** parancsmag kimenő szabálykonfigurációt ad egy Azure-terheléselegyenlőhez.

## PÉLDÁK

### 1. példa: Kimenő szabálykonfiguráció hozzáadása terheléselosztáshoz
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

Az első parancs lejátsa a MyLoadBalancer nevű terheléselosztási törlőt, majd tárolja azt a $slb.
A második parancs a folyamat műveleti jelével adja át a $slb terheléselegyenlőt az **Add-AzLoadBalancerOutRuleConfig** bővítménynek, amely kimenő szabálykonfigurációt ad a terheléselegyenlőnek.

## PARAMETERS

### -AllocatedOutboundPort
A NAT-hoz használt kimenő portok száma.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackendAddressPool
Hivatkozás dip-eket készletre.
A kimenő forgalom véletlenszerűen terheléselosztást biztosít a háttér-IP-k IP-i között.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackendAddressPoolId
Hivatkozás dip-eket készletre.
A kimenő forgalom véletlenszerűen terheléselosztást biztosít a háttér-IP-k IP-i között.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -EnableTcpReset
Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.
Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.

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

### -FrontendIpConfiguration
A terheléselosztás előlapi IP-címei.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
A TCP-inaktív kapcsolat időkorlátja

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancer
A terheléselosztási erőforrás hivatkozása.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name
A kimenő szabály neve.

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

### -Protocol
Protocol - TCP, UDP vagy All

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

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

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

### System.Int32

### System.String

### Microsoft.Azure.Commands.Network.Models.PSResourceId[]

### Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzLoadBalancerOutboundRuleConfig](./Get-AzLoadBalancerOutboundRuleConfig.md)

[New-AzLoadBalancerOutboundRuleConfig](./New-AzLoadBalancerOutboundRuleConfig.md)

[Remove-AzLoadBalancerOutboundRuleConfig](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[Set-AzLoadBalancerOutboundRuleConfig](./Set-AzLoadBalancerOutboundRuleConfig.md)
