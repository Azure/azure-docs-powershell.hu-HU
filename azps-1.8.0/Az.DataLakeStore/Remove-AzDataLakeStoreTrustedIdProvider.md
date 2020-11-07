---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: a93eb93a02c0ba1f5654258da0405f723e69873d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671055"
---
# Remove-AzDataLakeStoreTrustedIdProvider

## Áttekintés
A megadott megbízható identitás-szolgáltató eltávolítása a megadott Data Lake Store áruházból.

## SZINTAXISA

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzDataLakeStoreTrustedIdProvider** parancsmag eltávolítja a megadott megbízható identitás-szolgáltatót a megadott Data Lake Store-ban.

## Példák

### Példa 1: a megbízható identitás-szolgáltató eltávolítása.
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

A "MyProvider" szolgáltató eltávolítása a "ContosoADL" fiókból

## PARAMÉTEREK

### -Fiók
Az Data Lake Store fiók a megbízható identitás-szolgáltató eltávolításához

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
A megbízható identitás-szolgáltató neve.

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

### -PassThru
A törlési művelet eredményét jelző logikai választ adja eredményül.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a csoportnak a nevét adja meg, amely tartalmazza azt a fiókot, amelyből el szeretné távolítani a megbízható személyazonosság-szolgáltatót.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. Management. Automation. SwitchParameter

## KIMENETEK

### System. Boolean

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
