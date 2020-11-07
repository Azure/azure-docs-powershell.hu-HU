---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: 07fdf5a05f5099facabb78f35c44856545d1efe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672560"
---
# Get-AzureRmStorageAccount

## Áttekintés
Megkapja a tárolási fiókot.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ResourceGroupParameterSet
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### AccountNameParameterSet
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmStorageAccount** parancsmag egy erőforrás-csoportban vagy az előfizetésben megadott tárolási fiókot vagy minden tárolási fiókot kap.

## Példák

### 1. példa: megadott tárterület-fiók beszerzése
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

Ez a parancs a megadott tárterület-fiókot kapja.

### 2. példa: az erőforráscsoport minden tárolási fiókjának beolvasása
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

Ez a parancs egy erőforráscsoport minden tárolási fiókját beilleszti.

### 3. példa: az előfizetésben lévő összes tárterület-fiók beszerzése
```
PS C:\>Get-AzureRmStorageAccount
```

Ez a parancs az előfizetésben szereplő összes tárolási fiókot beilleszti.

## PARAMÉTEREK

### -Name (név)
A beszerzéshez használandó tárolási fiók nevét adja meg.

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a csoportnak a neve, amely a beszerzéshez használt tárolási fiókot tartalmazza.

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmStorageAccount](./New-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)


