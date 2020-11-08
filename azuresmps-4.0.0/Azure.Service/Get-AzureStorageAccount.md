---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015549"
---
# Get-AzureStorageAccount

## Áttekintés
Az aktuális Azure-előfizetés tárolási fiókjainak beolvasása

## SZINTAXISA

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorageAccount** parancsmag egy olyan objektumot ad eredményül, amely az aktuális előfizetés tárolási fiókjaival kapcsolatos információkat tartalmazza.
Ha meg van adva a *StorageAccountName* paraméter, akkor csak az adott tárterület-fiókról kapott információkat adja vissza a rendszer.

## Példák

### 1. példa: az összes tárterület-fiók visszaadása
```
PS C:\> Get-AzureStorageAccount
```

Ez a parancs egy olyan objektumot ad eredményül, amely az aktuális előfizetéshez társított összes tárolási fiókot adja eredményül.

### 2. példa: adott fiókhoz tartozó fiókadatok visszaadása
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

Ez a parancs olyan objektumot ad eredményül, amely csak a ContosoStore01-fiók adatait jeleníti meg.

### 3. példa: a tárolási fiókok táblázatának megjelenítése
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

Ez a parancs egy olyan objektumot ad eredményül, amely az aktuális előfizetéshez társított összes tárolási fiókot tartalmazza, és a fiók nevét, a fiók címkéjét és a tárolási helyét tartalmazó táblázatként jeleníti meg őket.

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
Ha meg van adva, ez a parancsmag csak a megadott tárterület-objektumot adja eredményül.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### ManagementOperationContext

## MEGJEGYZI
* `help node-dev`Ha segítségre van szüksége Node.js fejlesztéssel kapcsolatos parancsmagokkal kapcsolatban, adja meg a súgót. `help php-dev`Ha segítségre van szüksége a PHP fejlesztéssel kapcsolatos parancsmagokhoz, írja be a segítséget.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorageAccount](./New-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


