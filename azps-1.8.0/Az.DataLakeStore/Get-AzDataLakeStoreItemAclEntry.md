---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 3279ebd2b505a2d6563cdcabd497f83637c9c42c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671071"
---
# Get-AzDataLakeStoreItemAclEntry

## Áttekintés
Beilleszt egy bejegyzést az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájába.

## SZINTAXISA

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzDataLakeStoreItemAclEntry** parancsmag egy bejegyzés (ACE) beírása az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában.

## Példák

### 1. példa: mappa HOZZÁFÉRÉSének beszerzése
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

Ez a parancs beilleszti a megadott Data Lake Store-fiók gyökérkönyvtárának hozzáférés-vezérlési listáját.

## PARAMÉTEREK

### -Fiók
Az adattó-tároló fiók nevét adja meg.

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

### -Path (elérési út)
Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyre ez a parancsmag beilleszti az ACE-t, a gyökérkönyvtártól kezdve

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance

## KIMENETEK

### Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItemAce

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzDataLakeStoreItemAclEntry](./Remove-AzDataLakeStoreItemAclEntry.md)

[Set-AzDataLakeStoreItemAclEntry](./Set-AzDataLakeStoreItemAclEntry.md)


