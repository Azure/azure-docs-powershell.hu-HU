---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 49ddf65a5c32bafab32945b6d5114f65e3c59047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672018"
---
# Get-AzureRmDataLakeAnalyticsFirewallRule

## Áttekintés
Tűzfal-szabály vagy tűzfalszabályok listájának beolvasása egy Data Lake Analytics-fiókból.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDataLakeAnalyticsFirewallRule** parancsmag az Azure Data Lake Analytics-fiókból letölti a tűzfalszabályok vagy a tűzfalszabályok listáját.

## Példák

### Példa 1: tűzfalszabály beszerzése
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

Ez a parancs a "My Firewall Rule" nevű tűzfal-szabályt kapja meg a "ContosoAdlAcct" fiókból.

### 2. példa: az összes tűzfal-szabály listázása
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

Ez a parancs a "ContosoAdlAcct" fiókból kapja meg az összes tűzfal-szabályt.

## PARAMÉTEREK

### -Fiók
Az Data Lake Analytics-fiókja a tűzfalszabály beszerzéséhez

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A tűzfalszabály neve.

```yaml
Type: String
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
Type: String
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
System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule, Microsoft. Azure. commands. DataLakeAnalytics, Version = 2.5.0.0, Culture = semleges, PublicKeyToken = null]]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

