---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015710"
---
# Add-AzureWorkerRole

## Áttekintés
Az egyéni munkatársi szerepkör szükséges fájljait és konfigurációját hozza létre.

## SZINTAXISA

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **Add-AzureWorkerRole** parancsmag szükséges fájlokat és konfigurációt hoz létre, olykor állványzat néven, egyéni munkatársi szerepkör esetén.

## Példák

### 1. példa: egypéldányos munkatársi szerepkör létrehozása
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

Ez a példa összeadja az állványzatot egyetlen, a MyWorkerRole nevű, a jelenlegi alkalmazáshoz tartozó szerepkörnek.

### 2. példa: több példányos munkatársi szerepkör létrehozása
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

Ez a példa összeadja az állványzatot egy új, MyWorkerRole nevű munkatársi szerepkörhez, amelynek a szerepkör-példánya 2.

### 3. példa: a munkatársi szerepkör létrehozása egyéni állványzattal
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

Ez a példa létrehoz egy munkatársi szerepkört az egyéni állványzattal.

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
Ez az érték határozza meg azt a mappát, amely a munkatársi szerepkörben üzemeltetni kívánt egyéni alkalmazás állványzatát tartalmazza.
Az alapértelmezett érték a WorkerRolenumber, ahol a szám a szolgáltatásban alkalmazott szerepkörök száma.

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

### -TemplateFolder
A munkatársi szerepkör létrehozásához használandó állványzat sablon mappáját adja meg.

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

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureWebRole](./Add-AzureWebRole.md)

[Új – AzureRoleTemplate](./New-AzureRoleTemplate.md)


