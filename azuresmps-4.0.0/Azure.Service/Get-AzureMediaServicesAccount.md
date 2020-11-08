---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016335"
---
# Get-AzureMediaServicesAccount

## Áttekintés
Megkapja az elérhető Azure Media Services-fiókokat.

**Megjegyzés:** Ez a verzió elavult, kérjük, olvassa el az [újabb verziót](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).

## SZINTAXISA

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

Az összes fiók listázásához használja a `Get-AzureMediaServicesAccount` parancsmagot.
Ha részletesebb információt szeretne kapni egy adott fiókról, használja a `Get-AzureMediaServicesAccount -Name YourAccountName` parancsmagot.

## Példák

### Példa 1: az összes Media Services-fiók listázása
```
PS C:\> Get-AzureMediaServicesAccount
```

Ez a parancs felsorolja az összes rendelkezésre álló Media Services-fiókot.

### 2. példa: részletes információk kérése a Media Services-fiókról
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

Ez a parancs a Media Services-fiók tulajdonságait jeleníti meg.

## PARAMÉTEREK

### -Name (név)
A Media Services-fiók neve.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Az Azure PowerShell for Media Services használata](https://go.microsoft.com/fwlink/?LinkId=324179)


