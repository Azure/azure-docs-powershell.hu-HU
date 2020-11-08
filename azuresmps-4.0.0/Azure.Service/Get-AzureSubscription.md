---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015537"
---
# Get-AzureSubscription

## Áttekintés
Azure-előfizetéseket kap az Azure-fiókban.

## SZINTAXISA

### ByName (alapértelmezett)
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ById
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Alapértelmezett
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Aktuális
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureSubscription** parancsmag az Azure-fiókjában kapja meg az előfizetéseket.
Ezzel a parancsmaggal információkat kaphat az előfizetésről, és bekapcsolhatja az előfizetést más parancsmagokra.

A **Get-AzureSubscription** hozzáférést kell biztosítani az Azure-fiókokhoz.
A **Get-AzureSubscription** futtatása előtt futtatnia kell a **Add-AzureAccount** parancsmagot vagy azokat a parancsmagokat, amelyekkel letöltheti és telepítheti a közzétételi beállításokat tartalmazó fájlt ( **Get-AzurePublishSettingsFile** , **import-AzurePublishSettingsFile** ).

Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

## Példák

### Példa 1: az összes előfizetés lekérése
```
C:\PS>Get-AzureSubscription
```

Ez a parancs beilleszti az összes előfizetést a fiókba.

### 2. példa: előfizetés kérése név alapján
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

Ez a parancs csak az "MyProdSubsciption" előfizetést kapja meg.

### 3. példa: az alapértelmezett előfizetés beszerzése
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

Ez a parancs csak az alapértelmezett előfizetés nevét kapja meg.
A parancs először megkapja az előfizetést, majd a dot metódus segítségével beolvassa az előfizetés **SubscriptionName** tulajdonságát.

### 4. példa: a kijelölt előfizetés tulajdonságainak beolvasása
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

Ez a parancs a jelenlegi előfizetés nevével és tanúsítvánnyal rendelkező listát ad eredményül.
A **Get-AzureSubscription** parancsot használja a jelenlegi előfizetés beszerzéséhez.
Ezután az előfizetést a **Formátum – lista** parancsra, amely a listában kijelölt tulajdonságokat jeleníti meg.

### Példa 5: alternatív előfizetési adatfájl használata
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

Ez a parancs előfizetéseket kap az C:\Temp\MySubscriptions.xml előfizetési adatfájlból.
Ha a **Add-AzureAccount** vagy az **Importálás-PublishSettingsFile** parancsmagok futtatásakor megadta a másodlagos előfizetési adatfájlt, használja a **SubscriptionDataFile** paramétert.

## PARAMÉTEREK

### -Current
Csak a jelenlegi előfizetést kapja meg, azaz az "aktuális" néven kijelölt előfizetést. A **Get-AzureSubscription** alapértelmezés szerint az Azure-fiókokban található összes előfizetést kapja.
Ha egy előfizetést "current"-ként szeretne kijelölni, használja a **Select-AzureSubscription** parancsmag **aktuális** paraméterét.

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Alapértelmezett
Csak az alapértelmezett előfizetést kapja meg, azaz az alapértelmezettként megjelölt előfizetést. A **Get-AzureSubscription** alapértelmezés szerint az Azure-fiókokban található összes előfizetést kapja.
Ha egy előfizetést "alapértelmezettként" szeretne kijelölni, használja a **Select-AzureSubscription** parancsmag **alapértelmezett** paraméterét.

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtendedDetails
Az előfizetéshez tartozó kvóta-információkat ad eredményül, a szokásos beállítások mellett.

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

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható. Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

### -SubscriptionId
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Csak a megadott előfizetést kapja.
Adja meg az előfizetés nevét.
Az érték megkülönbözteti a kis-és nagybetűket.
A helyettesítő karakterek használata nem támogatott.
A **Get-AzureSubscription** alapértelmezés szerint az Azure-fiókokban található összes előfizetést kapja.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
A **SubscriptionName** tulajdonságot név szerint, de nem érték szerint is beírhatja.

## KIMENETEK

### Microsoft. WindowsAzure. commands. Utilities. Common. WindowsAzureSubscription

## MEGJEGYZI
* A Get-AzureSubscription a **Add-AzureAccount** és az **import-PublishSettingsFile** parancsmagok által létrehozott előfizetési adatfájlból kapja meg az adatforrást.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Importálás – AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Set-AzureSubscription](./Set-AzureSubscription.md)


