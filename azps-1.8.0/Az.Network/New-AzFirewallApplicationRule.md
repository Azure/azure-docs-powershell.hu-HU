---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: 6aad78a873b1eb24f1534c9b8c0b38d1567ee2ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670344"
---
# New-AzFirewallApplicationRule

## Áttekintés
Tűzfal-alkalmazási szabályt hoz létre.

## SZINTAXISA

### TargetFqdn (alapértelmezett)
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FqdnTag
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzFirewallApplicationRule** parancsmag létrehoz egy szabályt az Azure tűzfalhoz.

## Példák

### 1: szabály létrehozása az összes HTTPS-forgalom engedélyezéséhez a 10.0.0.0-ból
```
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

Ez a példa létrehoz egy szabályt, amely lehetővé teszi az 443-on lévő összes HTTPS-forgalom használatát a 10.0.0.0.

### 2: szabály létrehozása a 10.0.0.0/24 alhálózat WindowsUpdate engedélyezéséhez
```
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

Ez a példa létrehoz egy szabályt, amely lehetővé teszi a Windows-frissítések 10.0.0.0/24 tartományhoz való forgalmát.

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

### -Leírás
A szabály választható leírását adja meg.

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

### -FqdnTag
A szabályhoz tartozó FQDN-címkék listáját adja meg. A rendelkezésre álló címkéket a [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) parancsmag használatával lehet beolvasni.

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Az alkalmazási szabály nevét adja meg. A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.

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
Adja meg, hogy milyen típusú forgalmat szeretne szűrni a szabály. A formátum <protocol type> : <port> . Például "http: 80" vagy "https: 443".
A protokoll a TargetFqdn használatakor kötelező, de a FqdnTag nem használható. A támogatott protokollok a HTTP és a HTTPS.

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddress
A szabály forrásául szolgáló cím

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

### -TargetFqdn
A szabály által szűrt tartománynevek listáját adja meg.
A formázásával karakter (' *) csak a lista teljes tartománynevének első karaktere. Használatakor a formázásával tetszőleges számú karaktert helyettesít. (például a "* MSN.com" a MSN.com és annak összes altartományával egyezik)

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSAzureFirewallApplicationRule

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzFirewallApplicationRuleCollection](./New-AzFirewallApplicationRuleCollection.md)

[Új – AzFirewall](./New-AzFirewall.md)

[Get-AzFirewall](./Get-AzFirewall.md)

[Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md)
