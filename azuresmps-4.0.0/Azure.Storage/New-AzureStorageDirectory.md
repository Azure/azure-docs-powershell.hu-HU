---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bd97057cfafc48b3f1edd8539e7808056599117
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491447"
---
# New-AzureStorageDirectory

## Áttekintés
Könyvtárat hoz létre.

## SZINTAXISA

### Megosztásnév (alapértelmezett)
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Megosztása
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Directory
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorageDirectory** parancsmag létrehoz egy könyvtárat.
Ez a parancsmag egy **CloudFileDirectory** objektumot ad eredményül.

## Példák

### 1. példa: mappa létrehozása a fájlmegosztási verzióban
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

Ez a parancs létrehoz egy ContosoWorkingFolder nevű mappát a ContosoShare06 nevű fájlmegosztás-megosztásban.

### 2. példa: a fájlmegosztási objektumban megadott fájlmegosztás mappa létrehozása
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

Ez a parancs a **Get-AzureStorageShare** parancsmagot használja a ContosoShare06 nevű fájlmegosztás beolvasásához, majd átadja azt az aktuális parancsmagnak a pipeline operátor használatával.
Az aktuális parancsmag a ContosoWorkingFolder nevű mappát hozza létre a ContosoShare06-ban.

## PARAMÉTEREK

### -ClientTimeoutPerRequest
Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.
Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.
Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
A párhuzamos hálózati hívásokat adja meg.
Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.
A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.
Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).
Az alapértelmezett érték 10.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Környezet
Az Azure tárolási környezetét adja meg.
A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Címtár
**CloudFileDirectory** -objektumként adja meg a mappát.
Ez a parancsmag hozza létre a mappát abban a helyen, ahol a paraméter meg van határozva.
Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.
A címtár eléréséhez használhatja az Get-AzureStorageFile parancsmagot is.

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Path (elérési út)
A mappa elérési útját adja meg.
Ez a parancsmag létrehoz egy mappát a parancsmag elérési útjának elérési útjához.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
A kérés kiszolgálói részének időtúllépési időszakát adja meg.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Share (megosztás)
Egy **CloudFileShare** -objektumot ad meg.
Ez a parancsmag létrehoz egy mappát a fájlmegosztási fájlban, amelyet ez a paraméter határoz meg.
**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.
Ez az objektum a tárolási környezetet tartalmazza.
Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Megosztásnév
Itt adhatja meg a fájl megosztásának a nevét.
Ez a parancsmag létrehoz egy mappát a fájlmegosztási fájlban, amelyet ez a paraméter határoz meg.

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
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

[Get-AzureStorageFile](./Get-AzureStorageFile.md)

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[Új – AzureStorageContext](./New-AzureStorageContext.md)

[Új – AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Remove-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)
