---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: be32e761fc854c6ad4a270f36e4c9b6328e00ba1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843126"
---
# Get-AzStorageAccount

## Áttekintés
Megkapja a tárolási fiókot.

## SZINTAXISA

### ResourceGroupParameterSet
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### AccountNameParameterSet
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzStorageAccount** parancsmag egy erőforrás-csoportban vagy az előfizetésben megadott tárolási fiókot vagy minden tárolási fiókot kap.

## Példák

### 1. példa: megadott tárterület-fiók beszerzése
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

Ez a parancs a megadott tárterület-fiókot kapja.

### 2. példa: az erőforráscsoport minden tárolási fiókjának beolvasása
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

Ez a parancs egy erőforráscsoport minden tárolási fiókját beilleszti.

### 3. példa: az előfizetésben lévő összes tárterület-fiók beszerzése
```
PS C:\>Get-AzStorageAccount
```

Ez a parancs az előfizetésben szereplő összes tárolási fiókot beilleszti.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzStorageAccount](./New-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)


