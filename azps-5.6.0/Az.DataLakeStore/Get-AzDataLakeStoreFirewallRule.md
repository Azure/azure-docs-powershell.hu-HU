---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 580b5518e1fc0894a51920e781464258bef9e9cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925946"
---
# Get-AzDataLakeStoreFirewallRule

## SYNOPSIS
A megadott tűzfalszabályt kapja meg a data lake store-ban.
Ha nincs megadva tűzfalszabály, akkor felsorolja a fiók összes tűzfalszabályát.

## SZINTAXIS

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A Get-AzDataLakeStoreFirewallRule parancsmag megkapja a megadott tűzfalszabályt a megadott Data Lake Store-ban.
Ha nincs megadva tűzfalszabály, akkor felsorolja a fiók összes tűzfalszabályát.

## PÉLDÁK

### 1. példa: Adott tűzfalszabály beolvasása
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

A "ContosoADL" fiókból visszaadja a MyFirewallRule nevű tűzfalszabályt.

### 2. példa: Egy fiók összes tűzfalszabályának felsorolása
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

Visszaadja a "ContosoADL" fiók összes tűzfalszabályát.

## PARAMETERS

### -Account
A Data Lake Store-fiók, amelyből beolvassa a tűzfalszabályt.

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Name
A visszakeresni megfelelő tűzfalszabály neve

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
Annak az erőforráscsoportnak a neve, amely alatt be szeretnéolvasni a megadott fiók tűzfalszabályát.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
