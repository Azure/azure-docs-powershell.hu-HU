---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: ff5dee9a4e072cea7f1ee5bd46898857233ed0d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921089"
---
# Get-AzFirewallFqdnTag

## SYNOPSIS
A rendelkezésre álló Azure Firewall Fqdn-címkéket kapja meg.

## SZINTAXIS

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzFirewallFqdnTag** parancsmag megkapja az Azure tűzfal alkalmazásszabályzához használható FQDN-címkék listáját.

## PÉLDÁK

### 1: Az összes elérhető teljes tartománycímcédulának beolvasása
```
Get-AzFirewallFqdnTag
```

Ez a példa beolvassa az összes elérhető teljes tartománycímkét.

### 2: Az első elérhető FQDN-címke használata alkalmazásszabályban
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

Ebben a példában az első elérhető teljes tartománycímke használatával tűzfalalkalmazási szabályt hoz létre

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

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag

### System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzFirewallApplicationRule](./New-AzFirewallApplicationRule.md)

[New-AzFirewall](./New-AzFirewall.md)
