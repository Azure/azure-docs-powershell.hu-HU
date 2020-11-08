---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016390"
---
# Add-AzurePHPWebRole

## Áttekintés
A PHP-alkalmazások szükséges fájljait és konfigurációját hozza létre.

## SZINTAXISA

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

Az **Add-AzurePHPWebRole** parancsmag az azureon keresztül az IIS-ben üzemelő PHP-alkalmazások számára létrehozza a fájlokat és a konfigurációt (más néven állványzat).

## Példák

### 1. példa: webes szerepkör felvétele alapértelmezett értékekkel
```
PS C:\> Add-AzurePHPWebRole
```

Ebben a példában a "WebRole1" nevű szolgáltatásban 1 példányban szereplő, az új webhelyhez szükséges fájlokat és konfigurációt adja meg.

### 2. példa: webes szerepkör felvétele több példányban
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

Ebben a példában a "MyWebRole" nevű új webes szerepkör, a "" és a 2-es számú szerepkör

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
A név határozza meg annak a könyvtárnak a nevét, amely a PHP alkalmazás szükséges fájljait és konfigurációját tartalmazza.
Az alapértelmezett: webrole #, ahol # a szolgáltatásban elérhető webes szerepkörök száma.

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

[Add-AzurePHPWorkerRole](./Add-AzurePHPWorkerRole.md)

[Új – AzureServiceProject](./New-AzureServiceProject.md)


