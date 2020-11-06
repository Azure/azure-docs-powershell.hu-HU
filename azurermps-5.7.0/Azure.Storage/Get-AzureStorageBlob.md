---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
ms.openlocfilehash: da3b5f969bfa8beafab20f256df237588ed87048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493304"
---
# Get-AzureStorageBlob

## Áttekintés
A tárolóban lévő Blobs listák.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### BlobName (alapértelmezett)
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPrefix
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorageBlob** parancsmag a megadott tárolóban lévő blobokat az Azure Storage-fiókban sorolja fel.

## Példák

### Példa 1: blobos név beszerzése
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

Ez a parancs egy blob-nevet és egy helyettesítő karaktert használ a blob beszerzéséhez.

### 2. példa: a festékfoltok beolvasása a tárolóban a csővezeték használatával
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False      
```

Ez a parancs a csővezetéken a tárolóban lévő összes blobot (a törölt állapotban lévő Blobs-objektumokat is tartalmazza) fogja használni.

### 3. példa: a festékfoltok beolvasása név előtaggal
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

Ez a parancs egy név előtagot használ a festékfoltok beolvasásához.

### Példa 4: a lista festékfoltok több kötegben
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

Ebben a példában a *MaxCount* és a *ContinuationToken* paraméterrel több kötegben listázhatja az Azure Storage blob-ket.
Az első négy parancs az értékeket a példában használt változókhoz rendeli.

Az ötödik parancs a **Get-AzureStorageBlob** parancsmagot használó **do-while** utasítást ad meg a Blobs-adatok beszerzéséhez.
Az utasítás tartalmazza a $Token változóban tárolt folytatólagos tokent.
$Token az érték ismétléssel változik.
További információért írja be a következőt: `Get-Help About_Do` .

A végleges parancs a **echo** parancs segítségével jeleníti meg a végösszeget.

## PARAMÉTEREK

### -BLOB
A helyettesítő karakteres kereséshez használható név vagy név mintázatát adja meg.
Ha nincs megadva blob-név, a parancsmag a megadott tároló összes blobját megjeleníti.
Ha meg van adva egy érték a paraméterhez, a parancsmag az összes olyan blobot felsorolja, amely megfelel a paraméternek.

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Környezet
Azt az Azure Storage-fiókot adja meg, amelyből meg szeretné kapni a Blobok listáját.
A New-AzureStorageContext parancsmagot használhatja a tárolási környezet létrehozására.

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

### -ContinuationToken
A blob-lista folytatólagos jogkivonatát adja meg.
Ezzel a paraméterrel és a *MaxCount* paraméterrel több kötegben is listázhatja a Blobs-ket.

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeDeleted
A törölt blob hozzáadásával a blob alapértelmezés szerint nem fogja tartalmazni a törölt blobot.

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

### -MaxCount
A parancsmag által visszaadott objektumok maximális számát adja meg.

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

### -Prefix
Itt adhatja meg, hogy milyen blob-neveket szeretne kapni.
Ez a paraméter nem támogatja reguláris kifejezések és helyettesítő karakterek használatát a kereséshez.
Ez azt jelenti, hogy ha a tárolóban csak az "én", "MyBlob1", "MyBlob2" és "" nevű blobot adja meg, és a "-prefix My *" értéket adja meg, akkor a parancsmag nem tartalmaz blobot.
Ha azonban a "-prefix My" értéket adja meg, a parancsmag a "saját", "MyBlob1" és a "MyBlob2" karakterláncot adja eredményül.

```yaml
Type: String
Parameter Sets: BlobPrefix
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### IStorageContext
A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről

## KIMENETEK

### AzureStorageBlob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageBlobContent](./Get-AzureStorageBlobContent.md)

[Remove-AzureStorageBlob](./Remove-AzureStorageBlob.md)

[Set-AzureStorageBlobContent](./Set-AzureStorageBlobContent.md)


