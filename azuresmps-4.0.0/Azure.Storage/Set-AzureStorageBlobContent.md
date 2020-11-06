---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1caded810569225bfa269e7c0d29c60be87d4fb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491673"
---
# Set-AzureStorageBlobContent

## Áttekintés
Egy helyi fájlt tölt fel egy Azure Storage blob-webhelyre.

## SZINTAXISA

### SendManual (alapértelmezett)
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ContainerPipeline
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### BlobPipeline
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureStorageBlobContent** parancsmag egy helyi fájlt tölt fel egy Azure Storage blob-webhelyre.

## Példák

### 1. példa: névvel ellátott fájl feltöltése
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

Ez a parancs feltölti a PlanningData nevű fájlt egy Planning2015 nevű blobtal.

### 2. példa: az aktuális mappa alatti fájlok feltöltése
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

Ez a parancs az alapszintű Windows PowerShell-parancsmagot használja Get-ChildItem az aktuális mappában és az almappákban lévő összes fájl letöltéséhez, majd a csővezeték-kezelő használatával átadja őket az aktuális parancsmagnak.
A **set-AzureStorageBlobContent** parancsmag a fájlokat a ContosoUploads nevű tárolóba tölti fel.

### 3. példa: meglévő blob felülírása
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

Ez a parancs a Planning2015 nevű blobot az ContosoUploads-tárolóban kapja meg az Get-AzureStorageBlob parancsmag használatával, majd ezt a blobot átadja az aktuális parancsmagnak.
A parancs feltölti a ContosoPlanning nevű fájlt Planning2015-ként.
Ez a parancs nem adja meg az *erő* paramétert.
A parancs a megerősítést kéri.
Ha jóváhagyja a parancsot, a parancsmag felülírja a meglévő blobot.

### 4. példa: fájlok feltöltése tárolóba a csővezeték használatával
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

Ez a parancs a **Get-AzureStorageContainer** parancsmaggal kezdődően a karakterlánc ContosoUpload kezdődő tárolót kapja, majd az adott blobot átadja az aktuális parancsmagnak.
A parancs feltölti a ContosoPlanning nevű fájlt Planning2015-ként.

### Példa 5: fájl és metaadatok feltöltése
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata
```

Az első parancs létrehoz egy hash-táblázatot, amely egy blob metaadatait tartalmazza, és a hash-táblázatot a $Metadata változóban tárolja.

A második parancs feltölti a ContosoPlanning nevű fájlt a ContosoUploads nevű tárolóba.
A blob a $Metadataban tárolt metaadatokat tartalmazza.

## PARAMÉTEREK

### -BLOB
A blob nevét adja meg.
Ez a parancsmag olyan fájlt tölt fel az Azure Storage blob szolgáltatásba, amelyet ez a paraméter határoz meg.

```yaml
Type: String
Parameter Sets: SendManual, ContainerPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobType
A parancsmag által feltöltött blob típusának meghatározása.
A paraméter elfogadható értékei a következők:

- Letiltása
- Lap

Az alapértelmezett érték a blokk.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -CloudBlob
Egy **CloudBlob** -objektumot ad meg.
**CloudBlob** objektum beolvasásához használja az Get-AzureStorageBlob parancsmagot.

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CloudBlobContainer
Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.
Ez a parancsmag feltölti a tartalmat a tárolóban lévő blobra, amelyet a paraméter határoz meg.
**CloudBlobContainer** objektum beolvasásához használja az Get-AzureStorageContainer parancsmagot.

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Container
A tároló nevét adja meg.
Ez a parancsmag a paraméter által megadott tárolóban lévő blobra tölti fel a fájlt.

```yaml
Type: String
Parameter Sets: SendManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Környezet
Az Azure tárolási környezetét adja meg.
A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.

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

### -Fájl
Annak a fájlnak a helyi elérési útját adja meg, amely blob-fájlként tölthető fel.

```yaml
Type: String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Jelzi, hogy ez a parancsmag felülír egy meglévő blobot, és nem kér megerősítést.

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

### -Metadata
A feltöltött blob metaadatait adja meg.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tulajdonságok
A feltöltött blob tulajdonságait adja meg.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageBlobContent](./Get-AzureStorageBlobContent.md)

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[Remove-AzureStorageBlob](./Remove-AzureStorageBlob.md)
