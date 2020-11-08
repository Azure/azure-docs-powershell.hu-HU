---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015718"
---
# Add-AzureVhd

## Áttekintés
Egy helyszíni számítógépről egy VHD-fájlt tölt fel egy felhőalapú tárterület-fiókba az Azure-ban.

## SZINTAXISA

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureVhd** parancsmag a helyszíni virtuális merevlemez-(VHD-) képeken rögzített. vhd képként
A feltöltési folyamat konfigurálására szolgáló paramétereket tartalmaz, például megadhatja a feltöltött szálak számát, vagy felülírhatja azokat a blobokat, amelyek már megtalálható a megadott cél URI-ban.
A helyszíni VHD-képek esetében a javítás is támogatott, így a már feltöltött alapképek feltöltése nélkül is feltölthetők a diff-lemezképek. A megosztott hozzáférés-aláírás (SAS) URI-ja is támogatott.

## Példák

### 1. példa: VHD-fájl hozzáadása
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Ez a parancs a. vhd fájlt felveszi a tárterület-fiókba.

### 2. példa: a VHD-fájl hozzáadása és a cél felülírása
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Ez a parancs a. vhd fájlt felveszi a tárterület-fiókba.

### 3. példa: adjon hozzá egy VHD-fájlt, és adja meg a szálak számát
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

Ez a parancs a. vhd fájlt felveszi a tárolási fiókba, és megadja a fájlok feltöltéséhez használható szálak számát.

### 4. példa: a VHD-fájl hozzáadása és a SAS-URI megadása
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

Ez a parancs a. vhd fájlt felveszi egy tárterület-fiókba, és a SAS-URI azonosítót adja meg.

## PARAMÉTEREK

### -BaseImageUriToPatch
Egy URI-azonosítót ad meg az Azure Blob-tárolóban lévő lemezképfájlok számára.
A SAS az URI-bevitelben is támogatott.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Destination (cél)
A Microsoft Azure Blob-tárolóban lévő blob-AZONOSÍTÓkat adja meg.
Az URI-bevitel támogatja a SAS-t.
A javítás során azonban a cél nem lehet SAS-URI.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalFilePath
Faj: a helyi. vhd fájl fájlelérési útja.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
A feltöltéshez használni kívánt szálak számát adja meg.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Átír
Azt adja meg, hogy a parancsmag a megadott cél URI-ban törli a meglévő blobot (ha létezik).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

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

[Mentés-AzureVhd](./Save-AzureVhd.md)


