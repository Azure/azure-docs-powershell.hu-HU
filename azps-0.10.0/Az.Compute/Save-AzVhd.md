---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: f178b6aca1cf3747bc53807290585c01b91f3c2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844317"
---
# Save-AzVhd

## Áttekintés
A letöltött. vhd képek helyi mentése

## SZINTAXISA

### ResourceGroupParameterSetName
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### StorageKeyParameterSetName
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Save-AzVhd** parancsmag. vhd képeket ment egy blobról, ahol fájlt tárolnak.
Megadhatja, hogy hány letöltött hozzászólásláncot használ a folyamat, és hogy lecseréli-e a már meglévő fájlt.

Ez a parancsmag a tartalom letöltését is letölti.
A virtuális merevlemez (VHD) formátum konvertálása nem érvényes.

## Példák

### Példa 1: kép letöltése
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

Ez a parancs letölti a. vhd fájlt, és a helyi elérési út C:\vhd\Win7Image.vhd. tárolja.

### 2. példa: kép letöltése és a helyi fájl felülírása
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

Ez a parancs letölti a. vhd fájlt, és a helyi elérési útra menti.
A parancs a *felülírás* paramétert tartalmazza.
Ha a C:\vhd\Win7Image.vhd már létezik, ez a parancs a helyére lép.

### 3. példa: képek letöltése megadott számú szál használatával
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

Ez a parancs letölti a. vhd fájlt, és a helyi elérési útra menti.
A parancs a 32 értékét adja meg a *NumberOfThreads* paraméterhez.
Ezért a parancsmag 32-szálakat használ ehhez a tevékenységhez.

### Példa 4: kép letöltése és a tárolási kulcs megadása
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

Ez a parancs letölti a. vhd fájlt, és megadja a tárterület kulcsát.

## PARAMÉTEREK

### -AsJob
Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.

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

### -LocalFilePath
A mentett kép helyi fájlelérési útját adja meg.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumberOfThreads
A parancsmag által a letöltés során használt letöltési szálak számát adja meg.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Átír
Jelzi, hogy ez a parancsmag a *LocalFilePath* -fájl által megadott fájlt cseréli le, ha létezik.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A tárolási fiók erőforráscsoport-csoportjának nevét adja meg.

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceUri
A blob azonosítójának egységes erőforrás-azonosítóját adja meg `Azure` .

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
A blob-tároló fiók tárolási kulcsát adja meg.
Ha nem ad meg billentyűt, ez a parancsmag megkísérli meghatározni az Azure-ról az *SourceUri* -ról származó fiók tárolási kulcsát.

```yaml
Type: String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. VhdDownloadContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzVhd](./Add-AzVhd.md)


