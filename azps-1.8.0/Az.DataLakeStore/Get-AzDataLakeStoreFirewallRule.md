---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 39450f979a4c79e453c66845b522aba91757f672
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671072"
---
# Get-AzDataLakeStoreFirewallRule

## Áttekintés
A megadott tűzfalszabályok beolvasása a megadott adattó-tárolóban.
Ha nem adja meg a tűzfal szabályát, akkor a rendszer megjeleníti a fiókhoz tartozó összes tűzfal-szabályt.

## SZINTAXISA

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A Get-AzDataLakeStoreFirewallRule parancsmag a megadott adattó-tárolóban kapja meg a megadott tűzfalszabályok szabályait.
Ha nem adja meg a tűzfal szabályát, akkor a rendszer megjeleníti a fiókhoz tartozó összes tűzfal-szabályt.

## Példák

### Példa 1: adott tűzfalszabály beolvasása
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

A "MyFirewallRule" nevű tűzfal-szabályt számítja ki a "ContosoADL" fiókból.

### 2. példa: az összes tűzfal-szabály listázása egy fiókban
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

A "ContosoADL" fiók minden tűzfal-szabályát visszaállítja.

## PARAMÉTEREK

### -Fiók
Az adattó-tároló fiókja a tűzfalszabály beolvasásához.

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
A lekérdezni kívánt tűzfalszabály neve

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
Annak az erőforráscsoport-csoportnak a neve, amely alatt le szeretné olvasni a megadott fiók megadott tűzfalszabályét.

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

### Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreFirewallRule

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
