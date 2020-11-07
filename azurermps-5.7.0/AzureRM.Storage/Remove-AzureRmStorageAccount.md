---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: e6a6a35b5e744218c3afc6db396e875ad0acf242
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679649"
---
# Remove-AzureRmStorageAccount

## Áttekintés
Eltávolít egy tárterület-fiókot az Azure-ról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmStorageAccount** parancsmag eltávolítja a tárolási fiókot az Azure-ról.

## Példák

### 1. példa: tárterület-fiók eltávolítása
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

Ez a parancs eltávolítja a megadott tárterület-fiókot.

## PARAMÉTEREK

### -Force
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Az eltávolítandó tárolási fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az eltávolítandó tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[Új – AzureRmStorageAccount](./New-AzureRmStorageAccount.md)

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)
