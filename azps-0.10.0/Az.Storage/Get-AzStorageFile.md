---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: ce48b530adb0cd805559efd4785df0cccf3cf7ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843082"
---
# Get-AzStorageFile

## Áttekintés
Az elérési utakhoz tartozó könyvtárak és fájlok felsorolása.

## SZINTAXISA

### Megosztásnév (alapértelmezett)
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Megosztása
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Directory
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzStorageFile** parancsmag a megadott megosztás vagy könyvtár könyvtárait és fájljait sorolja fel.
Adja meg az *elérésiút* -paramétert, hogy egy adott könyvtár vagy fájl példányát beolvassa a megadott elérési úttal.
Ez a parancsmag **AzureStorageFile** -és **AzureStorageDirectory** -objektumokat ad eredményül.
A **IsDirectory** tulajdonsággal megkülönböztetheti a mappákat és a fájlokat.

## Példák

### Példa 1: megosztásban lévő könyvtárak listázása
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

Ez a parancs csak a megosztás ContosoShare06 lévő könyvtárakat sorolja fel.
Először a fájlok és könyvtárak beolvasása után átadja őket a **Where** operátornak a pipeline operátor segítségével, majd elveti azokat az objektumokat, amelyeknek a típusa nem "CloudFileDirectory".

### 2. példa: egy fájl címtárának listázása
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

Ez a parancs felsorolja a címtár ContosoWorkingFolder a megosztás ContosoShare06 csoportban található fájlokat és mappákat.
Először megkapja a címtár-példányt, majd a " **Get-AzStorageFile** parancsmag" értékre helyezi a címtár listáját.

## PARAMÉTEREK

### -ClientTimeoutPerRequest
Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.
Ha az előző hívás nem sikerült a megadott intervallumon belül, ez a parancsmag újból megkísérli a kérést.
Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.

```yaml
Type: System.Nullable`1[System.Int32]
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
Type: System.Nullable`1[System.Int32]
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
A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Címtár
**CloudFileDirectory** -objektumként adja meg a mappát.
Ez a parancsmag a paraméter által megadott mappát kapja meg.
Címtár beolvasásához használja az New-AzStorageDirectory parancsmagot.
A **Get-AzStorageFile** parancsmag használatával is beszerezhet egy könyvtárat.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
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
Ha kihagyja a *path* paramétert, a **Get-AzStorageFile** felsorolja a megadott fájlmegosztás vagy címtárban lévő könyvtárakat és fájlokat.
Ha a *path* paramétert adja meg, a **Get-AzStorageFile** a megadott elérési úton lévő könyvtár vagy fájl példányát adja eredményül.

```yaml
Type: System.String
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
Type: System.Nullable`1[System.Int32]
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
**CloudFileShare** objektum beolvasásához használja az Get-AzStorageShare parancsmagot.
Ez az objektum a tárolási környezetet tartalmazza.
Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
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
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. WindowsAz. Storage. file. CloudFileShare
Paraméterek: Share (ByValue)

### Microsoft. WindowsAz. Storage. file. CloudFileDirectory
Paraméterek: címtár (ByValue)

### Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext

## KIMENETEK

### Microsoft. WindowsAz. Storage. file. CloudFile

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)

[Új – AzStorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[Remove-AzStorageFile](./Remove-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


