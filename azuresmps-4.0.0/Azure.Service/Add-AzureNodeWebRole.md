---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016392"
---
# Add-AzureNodeWebRole

## Áttekintés
A Node.js-alkalmazások szükséges fájljait és mappáit hozza létre.

## SZINTAXISA

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

Az **Add-AzureNodeWebRole** létrehozza a szükséges fájlokat és mappákat, amelyeket néha állványzatnak is neveznek, ha egy Node.js alkalmazást a felhőbe az IIS-en keresztül tárol.

## Példák

### Példa 1: Single instance web role
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

Ez a példa összeadja az állványzatot az **MyWebRole** nevű webszerephez az aktuális alkalmazáshoz.

### 2. példa: több példányos webszerepkör
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

Ez a példa összeadja az állványzatot a **MyWebRole** nevű új webszerephez, amelynek a szerepkör-példánya 2.

## PARAMÉTEREK

### -Példányok
A webes szerepkörhöz tartozó szerepkör-példányok számát adja meg.
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
A webes szerepkör nevét adja meg.
Annak a könyvtárnak a nevét adja meg, amely a webes szerepkörben üzemeltetni kívánt node.js-alkalmazás állványzatát tartalmazza.
Az alapértelmezett: webrole #, ahol a # a szolgáltatásban a webes szerepkörök számát adja meg.

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

[Add-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[Új – AzureServiceProject](./New-AzureServiceProject.md)


