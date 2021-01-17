---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 76cf9e2624c812d99702823b303e4e6427845670
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468901"
---
# Remove-AzLoadBalancerInboundNatRuleConfig

## SYNOPSIS
A bejövő NAT-szabály konfigurációjának eltávolítása a terheléselosztásból.

## SZINTAXIS

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzLoadBalancerInboundNatRuleConfig** parancsmag eltávolítja a bejövő hálózati címfordítási (NAT) szabálykonfigurációt az Azure terheléselegyenlőből.

## PÉLDÁK

### 1: Bejövő NAT-szabály törlése az Azure terheléselosztási szolgáltatásból
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

Az első parancs betölt egy "mylb" nevű, már meglévő terhelésegyenleg-elosztást, és tárolja azt a $load változóban. A második parancs eltávolítja a terheléselosztáshoz társított bejövő NAT-szabályt.

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

### -LoadBalancer
Azt a **LoadBalancer-objektumot** adja meg, amely a parancsmag által eltávolított bejövő NAT-szabályt tartalmazza.

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
Annak a bejövő NAT-szabály-konfigurációnak a nevét adja meg, amelyről a parancsmag eltávolítja.

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

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzLoadBalancerInboundNatRuleConfig](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[Get-AzLoadBalancerInboundNatRuleConfig](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[New-AzLoadBalancerInboundNatRuleConfig](./New-AzLoadBalancerInboundNatRuleConfig.md)

[Set-AzLoadBalancerInboundNatRuleConfig](./Set-AzLoadBalancerInboundNatRuleConfig.md)


