---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 26e759256f5641f1e38553b8a2db4ab444c2aa53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009477"
---
# Add-AzRouteFilterRuleConfig

## SYNOPSIS
Útvonalszűrő szabályt ad hozzá az útvonalszűrőkhez.

## SZINTAXIS

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A Add-AzRouteFilterRuleConfig parancsmag hozzáad egy útvonalszűrő szabályt egy Azure-útvonalszűrőhez.

## PÉLDÁK

### 1. példa: Útvonalszűrő szabály hozzáadása útvonalszűrőhez
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

Az első parancs egy routefilter01 nevű útvonalszűrőt kap a Get-AzRouteFilter parancsmag használatával.
A parancs a szűrőt a $RouteFilter tárolja.

## PARAMETERS

### -Access
Az útvonalszűrő-szabály hozzáférését adja meg, érvényes értékek az Elutasítás vagy az Allow érték.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommunityList
Az útvonalszűrőt szűrő közösségi értékek listája

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -Name
Megadja annak az útvonalszűrő-szabálynak a nevét, amit hozzá szeretne adni az útvonalszűrőhez.

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

### -RouteFilter
Megadja azt az útvonalszűrőt, amelyhez ez a parancsmag hozzáad egy útvonalszűrő szabályt.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RouteFilterRuleType
Az útvonalszűrő-szabály típusát határozza meg.
Érvényes értékek: Közösség

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSRouteFilter

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSRouteFilter

## MEGJEGYZÉSEK
Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzRouteFilterRuleConfig](./Get-AzRouteFilterRuleConfig.md)

[New-AzRouteFilterRuleConfig](./New-AzRouteFilterRuleConfig.md)

[Remove-AzRouteFilterRuleConfig](./Remove-AzRouteFilterRuleConfig.md)

[Set-AzRouteFilterRuleConfig](./Set-AzRouteFilterRuleConfig.md)

[Get-AzRouteFilter](./Get-AzRouteFilter.md)

[New-AzRouteFilter](./New-AzRouteFilter.md)

[Remove-AzRouteFilter](./Remove-AzRouteFilter.md)

[Set-AzRouteFilter](./Set-AzRouteFilter.md)
