---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e816d29784ea8b2e69ba4b36162938f7a82007d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491718"
---
# Get-AzureStorageShare

## Áttekintés
Megkapja a fájlmegosztás listáját.

## SZINTAXISA

### MatchingPrefix (alapértelmezett)
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Adott
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorageShare** parancsmag a tárolási fiókban található fájlmegosztás listáját kapja meg.

## Példák

### Példa 1: fájlmegosztás beszerzése
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

Ez a parancs a ContosoShare06 nevű fájlt kapja meg.

### 2. példa: a karakterláncmal kezdődő összes fájlmegosztás beolvasása
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

Ez a parancs minden olyan fájlmegosztás esetén beilleszti a fájlt, amelyben a contoso kezdetű nevek szerepelnek.

### 3. példa: az összes fájlmegosztás beolvasása egy megadott környezetben
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

Az első parancs a **New-AzureStorageContext** parancsmagot használja a *helyi* paraméterrel létrehozott környezet létrehozásához, majd a $Context változóban tárolja a környezet objektumát.

A második parancs beolvassa a $Contextban tárolt környezeti objektumhoz tartozó fájlokat.

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
Környezet beolvasásához használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.

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
Itt adhatja meg a fájl megosztásának a nevét.
Ez a parancsmag a fájl megosztását adja meg, vagy semmit, ha nem létező fájlmegosztás nevét adja meg.

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Prefix
A fájlmegosztás előtagját adja meg.
Ez a parancsmag olyan fájlmegosztásokat kap, amelyek megegyeznek a paraméter által megadott előtaggal, vagy ha nincs fájlmegosztás, ha nem egyeznek meg a megadott előtaggal.

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorageShare](./New-AzureStorageShare.md)

[Remove-AzureStorageShare](./Remove-AzureStorageShare.md)
