---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187175"
---
# New-AzStorageBlobRangeToRestore

## Áttekintés
BLOB-tartománnyal létrehozott objektumot hoz létre a tárolási fiók visszaállításához.

## SZINTAXISA

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzStorageBlobRangeToRestore** parancsmag létrehoz egy blob-alapú objektumot, amelyet a Restore-AzStorageBlobRange használhat.

## Példák

### Példa 1: a visszaállítandó blob-tartományok létrehozása
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Ez a parancs a container1/blob1 (include) kezdetű blob-tartománnyal hoz létre, és a container2/blob2 (kizár) végződést adja vissza.

### 2. példa: a blob-intervallumot hozza létre, amely az első blobtól a betűrendes sorrendtől az adott blobba kerül (kihagyva).
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Ez a parancs létrehoz egy blob-intervallumot, amely a betűrendes sorrendtől az első blobtól egy adott blob container2/blob2 (kizár) fog visszaállítani.

### 3. példa: egy blob-intervallumot hoz létre, amely egy adott blobból (belefoglalt), betűrendben az utolsó blobba fog visszaállítani.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Ez a parancs létrehoz egy blob-cellatartományt, amely egy adott blob-container1/blob1 (include), betűrendben az utolsó blobba fog visszaállítani.

### 4. példa: blob-tartománnyal hoz létre minden blobot.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Ez a parancs létrehoz egy blob-cellatartományt, amely az összes blobot visszaállítja.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -EndRange
Adja meg a blob-visszaállítási végpontot.
A végződési tartományok kimaradnak a visszaállítási Blobs bővítményben.
Állítsa üres strng a végére való visszaállításhoz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRange
Adja meg a blob-helyreállítási indítási tartománnyal.
A Start-tartományok szerepelni fognak a visszaállítási festékfoltok között.
Állítsa azt üres karakterláncként az elejétől való visszaállításhoz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. Management. Storage. models. PSBlobRestoreRange

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
