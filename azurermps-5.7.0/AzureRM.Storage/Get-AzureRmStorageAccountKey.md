---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 23066206607289d531f2e2eaa14f90660360a705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492978"
---
# Get-AzureRmStorageAccountKey

## Áttekintés
Egy Azure-tárterülethez tartozó hozzáférési kulcsokat kapja meg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## Leírás
A **Get-AzureRmStorageAccountKey** parancsmag a hozzáférési kulcsokat kapja meg egy Azure Storage-fiókban.

## Példák

### Példa 1: a tárolási fiók hozzáférési kulcsainak beolvasása
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

Ez a parancs a megadott Azure Storage-fiók kulcsait kapja meg.

### 2. példa: speciális hozzáférési kulcs beszerzése tárterület-fiókhoz
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## PARAMÉTEREK

### -Name (név)
Annak a tároló fióknak a nevét adja meg, amelyhez ez a parancsmag kulcsokat kap.

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
A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmStorageAccountKey](./New-AzureRmStorageAccountKey.md)
