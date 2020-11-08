---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016387"
---
# Add-AzurePHPWorkerRole

## Áttekintés
Létrehozza a szükséges fájlokat és konfigurációt egy olyan PHP-alkalmazáshoz, amelyet az Azure-on php.exe-ben fog üzemeltetni.

## SZINTAXISA

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A szükséges fájlokat és konfigurációt hozza létre (más néven állványzat) egy olyan PHP-alkalmazáshoz, amelyet az Azure-ban php.exe-ban fog üzemeltetni.

## Példák

### 1. példa: a munkatársi szerepkör létrehozása egyetlen példánnyal
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

Ebben a példában a MyWorkerRole az aktuális alkalmazáshoz nevű egyetlen alkalmazotti szerepkör szükséges fájljait és konfigurációját adja meg.

### 2. példa: munkatársi szerepkör létrehozása több példányban
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

Ez a példa összeadja az új munkatársi szerepkör szükséges fájljait és konfigurációját a jelenlegi alkalmazáshoz, és a MyWorkerRole nevet használja, és a szerepkör-példányok száma 2.

## PARAMÉTEREK

### -Példányok
A munkatársi szerepkörhöz tartozó szerepkör-példányok számát adja meg.
Az alapértelmezett érték 1.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A munkatársi szerepkör nevét adja meg.
A név határozza meg azt a mappát, amely a munkatársi szerepkörben található PHP szolgáltatás szükséges fájljait és konfigurációját tartalmazza.
Az alapértelmezett érték a WorkerRole1.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureServiceProject](./New-AzureServiceProject.md)

[Add-AzurePHPWebRole](./Add-AzurePHPWebRole.md)


