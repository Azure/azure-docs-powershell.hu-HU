---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015911"
---
# New-AzureMediaServicesAccount

## Áttekintés
Azure Media Services-fiókot hoz létre.

**Megjegyzés:** Ez a verzió elavult, kérjük, olvassa el az [újabb verziót](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).

## SZINTAXISA

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **New-AzureMediaServicesAccount** parancsmag létrehoz egy új Media Services-fiókot, amelyen a megadott Media Services-fiók neve, Datacenter-hely, ahol létre szeretné hozni a fiókot, és egy meglévő tárolási fiók nevét.
A tárolási fióknak az új Media Services-fiókkal megegyező adatközpontban kell lennie.

## Példák

### Példa 1: új Media Services-fiók létrehozása
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## PARAMÉTEREK

### -Hely
A Media Services-adatközpont helyét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A Media Services-fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -StorageAccountName
A tárolási fiók nevét adja meg.
A tárterület-fióknak már léteznie kell ugyanabban az adatközpontban, mint az új Media Services-fiók.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Az Azure PowerShell for Media Services használata](https://go.microsoft.com/fwlink/?LinkId=324179)

[Get-AzureMediaServicesAccount](./Get-AzureMediaServicesAccount.md)

[Remove-AzureMediaServicesAccount](./Remove-AzureMediaServicesAccount.md)


