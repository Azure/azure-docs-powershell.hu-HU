---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8c16d52db3b2a1606cbab5999a8a165466fcdb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503351"
---
# Set-AzureStorageContainerAcl

## Áttekintés
A nyilvános hozzáférés engedélyének megadása tároló tárolóhoz.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Leírás
A **set-AzureStorageContainerAcl** parancsmag a nyilvános hozzáférés engedélyét az Azure-ban megadott tárterülethez állítja.

## Példák

### 1. példa: az Azure Storage Container-ACL beállítása név szerint
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

Ez a parancs olyan tárolót hoz létre, amelynek nincs nyilvános hozzáférése.

### 2. példa: az Azure Storage Container ACL beállítása a csővezeték használatával
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

Ez a parancs minden olyan tároló tárolót beolvas, amelynek a neve tárolóval kezdődik, majd az eredményt a csővezetéken adja meg a blob-hozzáféréshez.

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
A New-AzureStorageContext parancsmag használatával is létrehozhatja azt.

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
A tároló nevét adja meg.

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

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

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

### – Engedély
A tárolóhoz való nyilvános hozzáférés szintjét adja meg.
Alapértelmezés szerint a tároló és a bennük lévő festékfoltok csak a tárolási fiók tulajdonosa érhetik el.
Ha a névtelen felhasználóknak olvasási engedélyeket szeretne adni egy tárolóhoz és a festékfoltok-hez, a tároló engedélyeinek beállításával engedélyezheti a nyilvános hozzáférést.
A névtelen felhasználók egy nyilvánosan elérhető tárolóban olvashatják a blob-objektumokat a kérés hitelesítése nélkül.
A paraméter elfogadható értékei a következők:

--Container.
Teljes olvasási hozzáférést biztosít egy tárolóhoz és a Blobs-hoz.
Az ügyfelek névtelen kéréssel enumerálják a tárolóban lévő blob-objektumokat, a tárolási fiókban azonban nem lehet enumerálni a tárolókat. ---BLOB.
Névtelen kéréssel olvasási hozzáférést biztosít a blob-adattárolóhoz, de nem biztosít hozzáférést a tárolók adatainak eléréséhez.
Az ügyfelek névtelen kéréssel nem tudják enumerálni a blobokat a tárolóban. --Off.
Korlátozza a hozzáférést csak a tárolási fiók tulajdonosához.

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.
Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.
Kiszolgálóoldali időtúllépés az egyes kérésekhez.

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

### IStorageContext

A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről

### Karakterlánc

A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageContainer

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageContainer](./Get-AzureStorageContainer.md)

[Új – AzureStorageContainer](./New-AzureStorageContainer.md)

[Remove-AzureStorageContainer](./Remove-AzureStorageContainer.md)


