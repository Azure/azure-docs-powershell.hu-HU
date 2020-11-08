---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016354"
---
# Get-AzureDisk

## Áttekintés
Információt kap az Azure Disk repositoryban lévő lemezekről.

## SZINTAXISA

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureDisk** parancsmag a jelenlegi előfizetés Azure Disk repositoryjában tárolt lemezekről tartalmaz információkat.
Ez a parancsmag a tárház összes lemezére vonatkozó információk listáját jeleníti meg.
Ha meg szeretné tekinteni egy adott lemez adatait, adja meg a lemez nevét.

## Példák

### 1. példa: adatok beszerzése lemezről
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

Ez a parancs információkat kap a ContosoDataDisk nevű lemezről az adattárból.

### 2. példa: információk kérése az összes lemezről
```
PS C:\> Get-AzureDisk
```

Ez a parancs információt kap az összes lemezről a tárházban.

### 3. példa: adatok beszerzése lemezről
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

Ez a parancs a lemezkezelő minden olyan lemezére vonatkozó adatot kap, amely jelenleg nem csatlakozik egy virtuális géphez.
A parancs minden lemezről információt kap, és az egyes objektumokat átadja a **Where-Object** parancsmagnak.
Ez a parancsmag olyan lemezekre esik, amelyek nem rendelkeznek $Null értékkel a **AttachedTo** tulajdonságban.
A parancs táblázatként formázza a listát a **Format-Table** parancsmag használatával.

## PARAMÉTEREK

### -DiskName
Megadja annak a lemeznek a nevét, amelyről a parancsmag információt kap.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

[Remove-AzureDisk](./Remove-AzureDisk.md)

[Update-AzureDisk](./Update-AzureDisk.md)


