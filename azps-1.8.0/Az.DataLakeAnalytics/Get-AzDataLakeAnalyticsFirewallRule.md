---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 37c14547712233a025da56180e7a362f25168400
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671098"
---
# Get-AzDataLakeAnalyticsFirewallRule

## Áttekintés
Tűzfal-szabály vagy tűzfalszabályok listájának beolvasása egy Data Lake Analytics-fiókból.

## SZINTAXISA

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzDataLakeAnalyticsFirewallRule** parancsmag az Azure Data Lake Analytics-fiókból letölti a tűzfalszabályok vagy a tűzfalszabályok listáját.

## Példák

### Példa 1: tűzfalszabály beszerzése
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

Ez a parancs a "My Firewall Rule" nevű tűzfal-szabályt kapja meg a "ContosoAdlAcct" fiókból.

### 2. példa: az összes tűzfal-szabály listázása
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

Ez a parancs a "ContosoAdlAcct" fiókból kapja meg az összes tűzfal-szabályt.

## PARAMÉTEREK

### -Fiók
Az Data Lake Analytics-fiókja a tűzfalszabály beszerzéséhez

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Name (név)
A tűzfalszabály neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoport-csoportnak a neve, amelybe be szeretné olvasni a fiókot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
