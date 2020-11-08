---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016389"
---
# Add-AzureNodeWorkerRole

## Áttekintés
Létrehozza a Node.js-alkalmazás szükséges fájljait és mappáit a felhőn keresztül node.exe

## SZINTAXISA

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **Add-AzureNodeWorkerRole** parancsmag létrehozza a szükséges fájlokat és mappákat, amelyeket időnként az állványzatnak is nevezünk, mert egy Node.js alkalmazás a felhőn keresztül node.exeen tárol.

## Példák

### Példa 1: egypéldányos munkatársi szerepkör
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

Ez a példa összeadja az állványzatot egyetlen, a **MyWorkerRole** nevű, a jelenlegi alkalmazáshoz tartozó szerepkörnek.

### 2. példa: több példányos munkatárs szerepkör
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

Ez a példa összeadja az állványzatot egy, a **MyWorkerRole** nevű, a jelenlegi alkalmazáshoz nevű egyetlen munkatársi szerepkörnek, amelynek a szerepkör-példánya 2.

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
Az érték határozza meg a munkatársi szerepkörben szereplő node.js-szolgáltatás állványzatát tartalmazó mappa nevét.
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

[Add-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[Új – AzureServiceProject](./New-AzureServiceProject.md)


