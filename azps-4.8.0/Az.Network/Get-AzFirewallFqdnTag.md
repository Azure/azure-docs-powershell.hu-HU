---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184148"
---
# Get-AzFirewallFqdnTag

## Áttekintés
Az elérhető Azure Firewall FQDN-címkéket kapja.

## SZINTAXISA

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzFirewallFqdnTag** parancsmag az Azure Firewall alkalmazás szabályaihoz használható FQDN-címkék listáját kapja meg.

## Példák

### 1: az összes elérhető FQDN-címke beolvasása
```
Get-AzFirewallFqdnTag
```

Ez a példa beolvassa az összes elérhető FQDN-címkét.

### 2: az első elérhető FQDN címke használata az alkalmazási szabályokban
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

Ez a példa létrehoz egy tűzfal-alkalmazási szabályt az első FQDN címke használatával.

## PARAMÉTEREK

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSAzureFirewallFqdnTag

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. models. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. parancsmagok. Network, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzFirewallApplicationRule](./New-AzFirewallApplicationRule.md)

[Új – AzFirewall](./New-AzFirewall.md)
