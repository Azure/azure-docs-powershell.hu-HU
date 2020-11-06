---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: ''
schema: 2.0.0
ms.openlocfilehash: d80a8a75082503cf8cde9df7a779ca7f0d7d4b92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491711"
---
# New-AzureStorageContainer

## Áttekintés
Azure-tároló tárolót hoz létre.

## SZINTAXISA

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorageContainer** parancsmag Azure tároló tárolót hoz létre.

## Példák

### Példa 1: Azure Storage tároló létrehozása
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

A parancs létrehoz egy tároló tárolót.

### 2. példa: több Azure-tároló tároló létrehozása
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

Ebben a példában több tároló tárolót hoz létre.
A .NET **String** osztály **felosztott** metódusát használja, és a neveket átadja a csővezetéken.

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
Az új tároló környezetét adja meg.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name (név)
Az új tároló nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### – Engedély
A tárolóhoz való nyilvános hozzáférés szintjét adja meg.
Alapértelmezés szerint a tároló és a bennük lévő festékfoltok csak a tárolási fiók tulajdonosa érhetik el.
Ha a névtelen felhasználóknak olvasási engedélyeket szeretne adni egy tárolóhoz és a festékfoltok-hez, a tároló engedélyeinek beállításával engedélyezheti a nyilvános hozzáférést.
A névtelen felhasználók egy nyilvánosan elérhető tárolóban olvashatják a blob-objektumokat a kérés hitelesítése nélkül.
A paraméter elfogadható értékei a következők:

- Konténer.
Teljes olvasási hozzáférést biztosít egy tárolóhoz és a Blobs-hoz.
Az ügyfelek névtelen kéréssel enumerálják a tárolóban lévő blob-objektumokat, a tárolási fiókban azonban nem lehet enumerálni a tárolókat. 
- BLOB.
Névtelen kéréssel olvasási hozzáférést biztosít a blob-adatforrásokhoz, de nem biztosít hozzáférést a tárolók adatainak eléréséhez.
Az ügyfelek névtelen kéréssel nem tudják enumerálni a blobokat a tárolóban. 
- Ki.
Amely korlátozza a hozzáférést csak a tárterület-tulajdonoshoz.

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageContainer](./Get-AzureStorageContainer.md)

[Remove-AzureStorageContainer](./Remove-AzureStorageContainer.md)

[Set-AzureStorageContainerAcl](./Set-AzureStorageContainerAcl.md)


