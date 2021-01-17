---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324809"
---
# New-AzStorageBlobRangeToRestore

## SYNOPSIS
Blobtartomány-objektumot hoz létre a tárfiók visszaállításához.

## SZINTAXIS

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzStorageBlobRangeToRestore** parancsmag létrehoz egy Blob-tartomány objektumot, amely használható a Restore-AzStorageBlobRange-ban.

## PÉLDÁK

### 1. példa: Visszaállítható blobtartományt hoz létre
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Ez a parancs létrehoz egy visszaállítandó blobtartományt, amely a container1/blob1 (include) fájllal kezdődik, és a container2/blob2 (kizárva) értéken végződik.

### 2. példa: Olyan blobtartományt hoz létre, amely betűrendben visszaállítja az első blobból egy adott blobba (kizárva)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Ez a parancs létrehoz egy blobtartományt, amely a betűrend szerinti első blobból egy adott blobtárolóba2/blob2-re (kizárva)

### 3. példa: Olyan blobtartományt hoz létre, amely egy adott blobból (include) visszaáll az utolsó blobig betűrendben.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Ezzel a paranccsal olyan blobtartományt hoz létre, amely egy adott blobtárolóból1/blob1-ről (beleértve) az utolsó blobig, betűrendbe rendezve fog visszaállni.

### 4. példa: Blobtartományt hoz létre, amely az összes blobot visszaállítja
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Ez a parancs létrehoz egy blobtartományt, amely visszaállítja az összes blobot.

## PARAMETERS

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

### -EndRange
Adja meg a blob-visszaállítás záró tartományát.
A végponttartományt a visszaállítási blobok nem fogják kizárni.
Állítsa üres strngként a végpontra való visszaállításhoz.

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
Adja meg a blob-visszaállítás kezdési tartományát.
A kezdő tartomány szerepelni fog a visszaállítási blobok között.
Állítsa be üres karakterláncként az elejétől való visszaállításhoz.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
