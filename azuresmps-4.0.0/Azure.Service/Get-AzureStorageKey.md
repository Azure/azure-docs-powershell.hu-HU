---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015548"
---
# Get-AzureStorageKey

## Áttekintés
Egy Azure-tárterülethez tartozó elsődleges és másodlagos tárolási fiók kulcsait számítja ki.

## SZINTAXISA

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorageKey** parancsmag egy olyan objektumot ad eredményül, amely az Azure Storage fiók nevét, az elsődleges fiók kulcsát és a megadott Azure Storage-fiók másodlagos fiók kulcsát adja meg tulajdonságként.

## Példák

### Példa 1: elsődleges és másodlagos tárolási kulcsokat tartalmazó objektum beszerzése
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

Ez a parancs az ContosoStore01-tároló fiók elsődleges és másodlagos tárolási kulcsaival kap egy objektumot.

### 2. példa: az elsődleges tárterület-fiók lekérése és tárolása egy változóban
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

Ez a parancs az elsődleges tárterület-fiókot a ContosoStore01-tároló fiókhoz rendeli az $ContosoStoreKey változóban.

## PARAMÉTEREK

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

### -StorageAccountName
A tárolási fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI
* Ha segítségre van szüksége az Node.js-hoz, használja a `help node-dev` parancsot. Ha segítségre van szüksége a PHP-bővítményekhez, használja a `help php-dev` parancsot.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[Új – AzureStorageAccount](./New-AzureStorageAccount.md)

[Új – AzureStorageKey](./New-AzureStorageKey.md)

[Remove-AzureStorageAccount](./Remove-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


