---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 28e314f5ac7306233c3e2a3619a1a332dd6f3314
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672537"
---
# Get-AzureRmDataLakeStoreItemContent

## Áttekintés
A fájl tartalmának beolvasása az adattó áruházban.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### PreviewFileContent (alapértelmezett)
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### PreviewFileRowsFromHead
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### PreviewFileRowsFromTail
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDataLakeStoreItemContent** parancsmag a fájl tartalmát az Adattó áruházban kapja meg.

## Példák

### 1. példa: fájl tartalmának beolvasása
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

Ez a parancs beolvassa a fájl tartalmát MyFile.txt a ContosoADL-fiókba.

### 2. példa: a fájl első két sorának beolvasása
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

Ez a parancs a ContosoADL-fiókban lévő fájl MyFile.txt az első két új sort elválasztó sort kapja.

## PARAMÉTEREK

### -Fiók
Az adattó-tároló fiók nevét adja meg.

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Encoding
A létrehozandó elem kódolását adja meg.
A paraméter elfogadható értékei a következők:

- Ismeretlen
- Karakterlánc
- Unicode
- Byte
- BigEndianUnicode
- UTF8
- UTF7
- ASCII
- Alapértelmezett
- OEM
- BigEndianUTF32

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

```yaml
Type: SwitchParameter
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Head (Head)
Az előnézethez a fájl elejétől számított sorok száma (új sor tagolt). Ha a program nem észlelt új sort az első 4MB, akkor csak az adat lesz visszaadott adat.

```yaml
Type: Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hosszúság
A beolvasott tartalom hosszát adja meg bájtban.

```yaml
Type: Int64
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Eltolás
Azt adja meg, hogy hány bájtot szeretne kihagyni egy fájlban a tartalom beszerzése előtt.

```yaml
Type: Int64
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path (elérési út)
Az adattó-tároló elérési útját adja meg a gyökérkönyvtártól (/) kezdve.

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Farok
A fájl végéről az előnézethez tartozó sorok száma (az új sor tagolt). Ha a program nem észlelt új sort az első 4MB, akkor csak az adat lesz visszaadott adat.

```yaml
Type: Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases: 

Required: False
Position: 2
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

### byte []
A lekérdezett fájl tartalmát tartalmazó adatfolyamot ábrázoló bájtos adatfolyam.

### karakterlánc
A beolvasott fájl tartalma (a megadott kódolásban) karakterlánc-ábrázolása.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

