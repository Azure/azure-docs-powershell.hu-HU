---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: 6e86ed8cde1297af54ffaf8f8c8fbc912da30e69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933153"
---
# Add-AzVhd

## SYNOPSIS
Virtuális merevlemezt tölt fel egy helyszíni virtuális gépről egy blobba egy felhőbeli tárfiókban az Azure-ban.

## SZINTAXIS

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzVhd** parancsmag .vhd fájlformátumban feltölti a helyszíni virtuális merevlemezeket egy blobtároló fiókba rögzített virtuális merevlemezként.
Beállíthatja, hogy hány feltöltőszálat fog használni, vagy felülírhat egy meglévő blobot a megadott cél URI-ban.
Emellett támogatott a helyszíni .vhd fájlok javítással elérhető verziójának feltöltése is.
Ha már feltöltött egy alap virtuális merevlemezt, különböző lemezeket tölthet fel, amelyek szülőként az alapképet használják.
A megosztott hozzáférés-aláírás (SAS) URI-t is támogatja a rendszer.

## PÉLDÁK

### 1. példa: VHD-fájl hozzáadása
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Ez a parancs .vhd fájlt ad hozzá egy tárfiókhoz.

### 2. példa: VHD-fájl hozzáadása és a cél felülírása
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Ez a parancs .vhd fájlt ad hozzá egy tárfiókhoz.
A parancs felülír egy meglévő fájlt.

### 3. példa: VHD-fájl hozzáadása és a szálak számának megadása
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

Ez a parancs .vhd fájlt ad hozzá egy tárfiókhoz.
A parancs megadja a fájl feltöltésekor használni kívánt szálak számát.

### 4. példa: VHD fájl hozzáadása és az SAS URI megadása
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

Ez a parancs hozzáad egy .vhd fájlt egy tárfiókhoz, és megadja az SAS URI-t.

## PARAMETERS

### -AsJob
Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BaseImageUriToPatch
Az Azure Blob Storage alapkép blobját adja meg URI-nak.
A paraméter értékeként meg lehet adni egy SAS-t.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
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

### -Destination
Egy blob URI-ját adja meg a Blob Storage-ban.
A paraméter támogatja az SAS URI-t, bár a javítási esetek célhelye nem lehet SAS URI.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalFilePath
A helyi .vhd fájl elérési útját adja meg.

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
A .vhd fájl feltöltésekor használt feltöltőszálak számát adja meg.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Felülírás
Azt jelzi, hogy ez a parancsmag felülír egy meglévő blobot a megadott cél URI-ban, ha van ilyen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális gép erőforráscsoportját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Uri

### System.IO.FileInfo

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Management.Automation.SwitchParameter

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.VhdUploadContext

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Save-AzVhd](./Save-AzVhd.md)


