---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azbgpservicecommunity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
ms.openlocfilehash: 649fb6734caf2df11a65c43c59d123db425e90bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942458"
---
# Get-AzBgpServiceCommunity

## SYNOPSIS
Az összes szolgáltatás/régió, BGP-közösségek és kapcsolódó előtagok listája.

## SZINTAXIS

```
Get-AzBgpServiceCommunity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Ez a parancsmag az összes szolgáltatás/régió, BGP-közösségek és kapcsolódó előtagok listáját tartalmazza.

## PÉLDÁK

### 1. példa
```
Get-AzBgpServiceCommunity

...

Name           : AzureCentralIndia
Id             : /subscriptions//resourceGroups//providers/Microsoft.Network/bgpServiceCommunities/AzureCentralIndia
Type           : Microsoft.Network/bgpServiceCommunities
BgpCommunities : [
                   {
                     "ServiceSupportedRegion": "Global",
                     "CommunityName": "Azure Central India",
                     "CommunityValue": "12076:51017",
                     "CommunityPrefixes": [
                       "13.71.0.0/18",
                       "20.190.146.0/25",
                       "40.79.214.0/24",
                       "40.81.224.0/19",
                       "40.87.224.0/22",
                       "40.112.39.0/25",
                       "40.112.39.128/26",
                       "40.126.18.0/25",
                       "52.136.24.0/24",
                       "52.140.64.0/18",
                       "52.159.64.0/19",
                       "52.172.128.0/17",
                       "52.239.135.64/26",
                       "52.239.202.0/24",
                       "52.245.96.0/22",
                       "52.253.168.0/22",
                       "104.47.210.0/23",
                       "104.211.64.0/20",
                       "104.211.81.0/24",
                       "104.211.82.0/23",
                       "104.211.84.0/22",
                       "104.211.88.0/21",
                       "104.211.96.0/19"
                     ],
                     "IsAuthorizedToUse": true,
                     "ServiceGroup": "Azure"
                   }
                 ]
...
```

Ez a parancsmag az összes szolgáltatás/régió, BGP-közösségek és kapcsolódó előtagok listáját tartalmazza.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSBgpServiceCommunity

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Move-AzExpressRouteCircuit](Move-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuit](New-AzExpressRouteCircuit.md)

[Remove-AzExpressRouteCircuit](Remove-AzExpressRouteCircuit.md)

[Set-AzExpressRouteCircuit](Set-AzExpressRouteCircuit.md)

[Get-AzRouteFilter](Get-AzRouteFilter.md)

[Get-AzRouteFilterRuleConfig](Get-AzRouteFilterRuleConfig.md)

[Remove-AzRouteFilter](Remove-AzRouteFilter.md)

[Remove-AzRouteFilterRuleConfig](Remove-AzRouteFilterRuleConfig.md)

[Set-AzRouteFilter](Set-AzRouteFilter.md)

[Set-AzRouteFilterRuleConfig](Set-AzRouteFilterRuleConfig.md)

[New-AzRouteFilter](New-AzRouteFilter.md)

[New-AzRouteFilterRuleConfig](New-AzRouteFilterRuleConfig.md)
