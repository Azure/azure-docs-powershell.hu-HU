---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016393"
---
# Add-AzureDisk

## Áttekintés
Lemez hozzáadása az Azure Disk repositoryhoz.

## SZINTAXISA

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
Az **Add-AzureDisk** parancsmag a jelenlegi előfizetésben az Azure Disk repositoryba helyezi a lemezt.
Ez a parancsmag rendszerlemez vagy adatlemez hozzáadására használható.
Rendszerlemez hozzáadásához *az operációs rendszer paraméter segítségével* adja meg az operációs rendszer típusát.

## Példák

### 1. példa: a Windows operációs rendszert használó indítólemez hozzáadása
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

Ez a parancs rendszerlemezt ad hozzá a merevlemez-tárolóhoz.
A rendszerlemez a Windows operációs rendszert használja.

### 2. példa: adatlemez hozzáadása
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

Ez a parancs adatlemezt ad hozzá.

### 3. példa: Linux rendszerlemez hozzáadása
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

Ez a parancs egy Linux rendszerű rendszerlemezt ad hozzá.

## PARAMÉTEREK

### -DiskName
Annak a lemeznek a neve, amely a parancsmagot adja.

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

### -Label (címke)
Megadja a parancsmag által hozzáadott lemez címkéjét.

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

### -MediaLocation
A lemez fizikai helyét az Azure Storage szolgáltatásban adja meg.
Ez az érték az aktuális előfizetés és a tároló fiók blob lapjára hivatkozik.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OS
A rendszerlemez operációs rendszerének típusát adja meg.
Az érvényes értékek a következők: 

- Windows 
- Linux 

Ha nem adja meg ezt a paramétert, a parancsmag adatlemezként hozzáadja a lemezt.

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

### DiskContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureDisk](./Get-AzureDisk.md)

[Remove-AzureDisk](./Remove-AzureDisk.md)

[Update-AzureDisk](./Update-AzureDisk.md)


