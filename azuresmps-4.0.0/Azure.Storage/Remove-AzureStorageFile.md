---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24b4ddfa86027885b5094b164f24da36e9604900
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491312"
---
# Remove-AzureStorageFile

## Áttekintés
Töröl egy fájlt.

## SZINTAXISA

### Megosztásnév (alapértelmezett)
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Megosztása
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Directory
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Fájl
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzureStorageFile** parancsmag töröl egy fájlt.

## Példák

### 1. példa: fájl törlése a fájl-megosztásból
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

Ez a parancs törli a ContosoFile22 nevű fájlt a ContosoShare06 nevű fájlmegosztás-megosztásból.

### 2. példa: fájlmegosztás-objektum használatával beolvashatja a fájlt a fájlból.
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

Ez a parancs a **Get-AzureStorageShare** parancsmagot használja a ContosoShare06 nevű fájlmegosztás beszerzéséhez, majd a csővezeték-kezelő segítségével átadja az objektumot az aktuális parancsmagnak.
A jelenlegi parancs törli a ContosoFile22 nevű fájlt a ContosoShare06.

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
Ez a parancsmag eltávolítja a fájl azon mappáját, amelyet a paraméter határoz meg.

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

### -Fájl
A fájlt **CloudFile** -objektumként adja meg.
Ez a parancsmag eltávolítja a paraméter által megadott fájlt.
**CloudFile** objektum beolvasásához használja az Get-AzureStorageFile parancsmagot.

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.
Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.

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

### -Path (elérési út)
A fájl elérési útját adja meg.
Ez a parancsmag törli a paraméter által megadott fájlt.

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
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
Ez a parancsmag eltávolítja a fájlt a megosztás ebben a paraméterben beállításban.
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
Ez a parancsmag eltávolítja a fájlt a megosztás ebben a paraméterben beállításban.

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

[Get-AzureStorageFile](./Get-AzureStorageFile.md)

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[Új – AzureStorageContext](./New-AzureStorageContext.md)
