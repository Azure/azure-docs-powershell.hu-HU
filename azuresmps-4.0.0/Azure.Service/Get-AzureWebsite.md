---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016274"
---
# Get-AzureWebsite

## Áttekintés
Azure-webhelyeket kap az aktuális előfizetésben.

## SZINTAXISA

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureWebsite** parancsmag a jelenlegi előfizetésben az Azure-webhelyekkel kapcsolatos információkat kapja meg.

Alapértelmezés szerint a **Get-AzureWebsite** megkapja az összes Azure-webhelyet a jelenlegi előfizetésben, és egy olyan objektumot ad eredményül, amely alapvető információkat nyújt a webhelyekről.
A *Name* paraméter használatakor a **Get-AzureWebsite** olyan objektumot ad eredményül, amely részletes információkat tartalmaz, például a konfigurációs adatokat.

A jelenlegi előfizetés a "current" (aktuális) jelölt előfizetés. Az aktuális előfizetés megkereséséhez használja a [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) parancsmag *aktuális* paraméterét.
Az aktuális előfizetés módosításához használja a [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) parancsmagot.

Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

## Példák

### Példa 1: az előfizetés összes webhelyének beszerzése
```
PS C:\> Get-AzureWebsite
```

Ez a parancs a jelenlegi előfizetés összes Azure-webhelyét bekapja.

### 2. példa: webhely beszerzése név alapján
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

Ez a parancs részletes információkat kap a ContosoWeb Azure webhelyről, például a konfigurációs adatokról.
A *Name* paraméter használatakor a **Get-AzureWebsite** olyan **SiteWithConfig** -objektumot ad eredményül, amely a webhellyel kapcsolatos kiterjesztett információkat jeleníti meg.

### 3. példa: részletes információk kérése az összes webhelyről
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

Ez a parancs részletes információkat kap az előfizetésben szereplő összes webhelyről.
A **Get-AzureWebsite** parancsot használja az összes webhely letöltéséhez, majd a **foreach-Object** parancsmagot használja az egyes webhelyek név szerinti beszerzéséhez.

### 4. példa: információk beszerzése a telepítő bővítőhelyről
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

Ez a parancs beolvassa a ContosoWeb webhely átmeneti telepítési tárolóhelyét.
A központi telepítő bővítőhelyek segítségével tesztelheti az Azure-webhely különböző verzióit, és nem szabadíthatja fel őket a nyilvánosság számára.

### Példa 5: webhelyek példányainak beolvasása
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

Az ebben a példában szereplő parancsok az Azure-webhelyek példányok tulajdonságát használják a jelenleg futó webhely-példányokkal kapcsolatos információk megjelenítéséhez.
A **instances** tulajdonság az Azure-modul 0.8.3 a **SiteWithConfig** objektumba lett hozzáadva.

Az első parancs a webhely összes aktuális példányának példány-azonosítóját kapja meg.
A második parancs a webhely futó példányainak számát kapja meg.
Használhatja a **Count** tulajdonságot bármely tömbben.

## PARAMÉTEREK

### -Name (név)
Részletes konfigurációs információkat kap a megadott webhelyről.
Adja meg az előfizetés egyik webhelyének a nevét.
A **Get-AzureWebsite** alapértelmezés szerint a jelenlegi előfizetés összes webhelyét kapja.
A *név* érték nem támogatja a helyettesítő karaktereket.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Slot
A webhely megadott központi telepítő tárolóhelyének beolvasása
Adja meg a bővítőhely nevét (például "staging" vagy "termelés").
A telepítő bővítőhelyekről a Microsoft Azure webhelyek szakaszos központi telepítésének bemutatása című témakörben olvashat bővebben https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .
Ha egy meglévő Azure-webhelyhez szeretne telepítő bővítőhelyet hozzáadni, használja az Set-AzureWebsite parancsmagot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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
A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.

## KIMENETEK

### Microsoft. WindowsAzure. Command. Utilities. websites. Services. webentitások. webhely
Alapértelmezés szerint a **Get-AzureWebsite** a **webhely** objektumainak tömbjét számítja ki.

### Microsoft. WindowsAzure. Command. Utilities. websites. Services. webentitások. SiteWithConfig
A *Name* paraméter használatakor a **Get-AzureWebsite** egy **SiteWithConfig** objektumot ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start-AzureWebsite](./Start-AzureWebsite.md)

[Stop-AzureWebsite](./Stop-AzureWebsite.md)

[Show-AzureWebsite](./Show-AzureWebsite.md)


