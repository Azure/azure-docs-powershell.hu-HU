---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3b84deae0307114efa274cdfa6fc708d1b268ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491734"
---
# Get-AzureStorageFile

## Áttekintés
Az elérési utakhoz tartozó könyvtárak és fájlok felsorolása.

## SZINTAXISA

### Megosztásnév (alapértelmezett)
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Megosztása
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Directory
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorageFile** parancsmag a megadott megosztás vagy könyvtár könyvtárait és fájljait sorolja fel.
Adja meg az *elérésiút* -paramétert, hogy egy adott könyvtár vagy fájl példányát beolvassa a megadott elérési úttal.

Ez a parancsmag **AzureStorageFile** -és **AzureStorageDirectory** -objektumokat ad eredményül.
A **IsDirectory** tulajdonsággal megkülönböztetheti a mappákat és a fájlokat.

## Példák

### Példa 1: megosztásban lévő könyvtárak listázása
```
PS C:\>Get-AzureStorageFile -ShareName "share1" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

Ez a parancs csak a megosztás ContosoShare06 lévő könyvtárakat sorolja fel.
Először a fájlok és könyvtárak beolvasása után átadja őket a **Where** operátornak a pipeline operátor segítségével, majd elveti azokat az objektumokat, amelyeknek a típusa nem "CloudFileDirectory".

### 2. példa: egy fájl címtárának listázása
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

Ez a parancs felsorolja a címtár ContosoWorkingFolder a megosztás ContosoShare06 csoportban található fájlokat és mappákat.
Először megkapja a címtár-példányt, majd a " **Get-AzureStorageFile** parancsmag" értékre helyezi a címtár listáját.

## PARAMÉTEREK

### -ClientTimeoutPerRequest
Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.
Ha az előző hívás nem sikerült a megadott intervallumon belül, ez a parancsmag újból megkísérli a kérést.
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
Ez a paraméter csökkentheti a hálózati kapcsolat problémáinak enyhítését az alacsony sávszélességű környezetekben, például 100 kilobit/másodperc.
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
A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.

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
Ez a parancsmag a paraméter által megadott mappát kapja meg.
Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.
A **Get-AzureStorageFile** parancsmag használatával is beszerezhet egy könyvtárat.

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

Ha kihagyja a *path* paramétert, a **Get-AzureStorageFile** felsorolja a megadott fájlmegosztás vagy címtárban lévő könyvtárakat és fájlokat.
Ha a *path* paramétert adja meg, a **Get-AzureStorageFile** a megadott elérési úton lévő könyvtár vagy fájl példányát adja eredményül.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
A szolgáltatás-időkorlátot adja meg másodpercben a kéréshez.
Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.

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
Ez a parancsmag olyan fájlt vagy könyvtárat ad meg a fájl megosztási mappából, amely ezt a paramétert adja meg.
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
Ez a parancsmag olyan fájlt vagy könyvtárat ad meg a fájl megosztási mappából, amely ezt a paramétert adja meg.

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

[Get-AzureStorageFileContent](./Get-AzureStorageFileContent.md)

[Új – AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Remove-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)

[Remove-AzureStorageFile](./Remove-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)


