---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016157"
---
# Remove-AzureDisk

## Áttekintés
Lemez eltávolítása az Azure Disk repositoryból.

## SZINTAXISA

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureDisk** parancsmag a jelenlegi előfizetésben az Azure Disk repositoryból távolítja el a lemezt.
Ez a parancsmag alapértelmezés szerint nem törli a blob-tárolóból származó virtuális merevlemezt (VHD-fájlt).
A VHD törléséhez adja meg a *DeleteVHD* paramétert.

## Példák

### 1. példa: lemez eltávolítása
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

Ez a parancs eltávolítja a ContosoDataDisk Disk nevű lemezt a repositoryból.
A parancs nem törli a VHD-t.

### 2. példa: lemez eltávolítása és törlése
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

Ez a parancs eltávolítja a ContosoDataDisk Disk nevű lemezt a repositoryból.
Ez a parancs a DeleteVHD paramétert adja meg.
Ezért a parancs a VHD-fájlból törli a VHD-t.

## PARAMÉTEREK

### -DeleteVHD
Azt jelzi, hogy ez a parancsmag eltávolítja a VHD-t a blob-tárolóból.

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

### -DiskName
Itt adhatja meg annak az adatlemeznek a nevét, amely a parancsmag által eltávolított tárolóban van.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

[Add-AzureDisk](./Add-AzureDisk.md)

[Get-AzureDisk](./Get-AzureDisk.md)

[Update-AzureDisk](./Update-AzureDisk.md)


