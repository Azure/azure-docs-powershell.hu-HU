---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015676"
---
# Get-AzureAccount

## Áttekintés
Az Azure PowerShellhez elérhető Azure-fiókokat kapja meg.

## SZINTAXISA

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureAccount** parancsmag a Windows powershellhez elérhető Azure-fiókokat kapja meg.
Ha a fiókját elérhetővé szeretné tenni a Windows PowerShell számára, használja a **Add-AzureAccount** vagy az **import-PublishSettingsFile** parancsmagot.

## Példák

### Példa 1: az összes fiók lekérése
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

Ez a parancs beolvassa az adott felhasználóhoz társított összes fiókot.

### 2. példa: fiók beszerzése név alapján
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

Ez a parancs a ContosoAdmin-fiókot kapja.

## PARAMÉTEREK

### -Name (név)
Csak a megadott fiók kapja meg.
Az alapértelmezett beállítás a Windows PowerShellhez elérhető összes fiók.
Írja be a fiók nevét.
A **név** érték megkülönbözteti a kis-és nagybetűket.
A helyettesítő karakterek nem engedélyezettek.

```yaml
Type: String
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ebben a parancsmagban nem lehet beírni a bemenetet.

## KIMENETEK

### Nincs
Ez a parancsmag nem ad vissza semmilyen eredményt.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Importálás – AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


