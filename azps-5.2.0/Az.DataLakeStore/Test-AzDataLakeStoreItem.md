---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: 1629e987386998e642df1390ec391444500a6c44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371893"
---
# Test-AzDataLakeStoreItem

## SYNOPSIS
Azt teszteli, hogy van-e fájl vagy mappa a Data Lake Store-ban.

## SZINTAXIS

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Test-AzDataLakeStoreItem** parancsmag teszteli egy fájl vagy mappa meglétét a Data Lake Store-ban.

## PÉLDÁK

### 1. példa: Fájl tesztelése
```powershell
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

Ez a parancs azt teszteli, hogy a Test.csv létezik-e a ContosoADL-fiókban.

### 2. példa

Azt teszteli, hogy van-e fájl vagy mappa a Data Lake Store-ban. (automatikusan generált)

<!-- Aladdin Generated Example -->
```powershell
Test-AzDataLakeStoreItem -Account 'ContosoADL' -Path '/MyFiles/Test.csv' -PathType Any
```

## PARAMETERS

### -Account
A Data Lake Store-fiók nevét adja meg.

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Path
A tesztelni kívánt elem Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).

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

### -PathType
A tesztelni kívánt elem típusát határozza meg.
A paraméter elfogadható értékei a következőek:
- Bármely 
- Fájl 
- Mappa

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

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

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Export-AzDataLakeStoreItem](./Export-AzDataLakeStoreItem.md)

[Get-AzDataLakeStoreItem](./Get-AzDataLakeStoreItem.md)

[Import-AzDataLakeStoreItem](./Import-AzDataLakeStoreItem.md)

[Join-AzDataLakeStoreItem](./Join-AzDataLakeStoreItem.md)

[Move-AzDataLakeStoreItem](./Move-AzDataLakeStoreItem.md)

[Remove-AzDataLakeStoreItem](./Remove-AzDataLakeStoreItem.md)


