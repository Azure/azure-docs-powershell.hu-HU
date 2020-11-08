---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015735"
---
# Add-AzureDataDisk

## Áttekintés
Adatlemez felvétele virtuális gépre.

## SZINTAXISA

### CreateNew (alapértelmezett)
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Importálása
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ImportFrom
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureDataDisk** parancsmag új vagy meglévő adatlemezt ad hozzá egy Azure Virtual Machine objektumhoz.
A *createnew* paraméterrel új adatlemezt hozhat létre, amelyben a megadott méret és címke található.
Az *importálási* paraméter segítségével egy meglévő lemezt csatolhat a képtárházból.
A *ImportFrom* paraméterrel meglévő merevlemezt csatolhat a tároló fiókban lévő blob-fájlokhoz.
Megadhatja a csatolt adatlemez Host-cache üzemmódját is.

## Példák

### 1. példa: adatlemez importálása a tárházból
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

Ez a parancs a **Get-AzureVM** parancsmag használatával kap egy virtuálisgép-objektumot a VirtualMachine07 nevű virtuális géphez a ContosoService Felhőbeli szolgáltatásban.
A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmagnak.
A parancs egy meglévő adatlemezt csatol a tárházból a virtuális gépre.
Az adatlemez 0 logikai egységgel rendelkezik.
A parancs frissíti a virtuális gépet a módosítások tükrözéséhez a **Update-AzureVM** parancsmag használatával.

### 2. példa: új adatlemez hozzáadása
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Ez a parancs egy virtuálisgép-objektumot kap a VirtualMachine08 nevű virtuális gépnek.
A parancs átadja az aktuális parancsmagnak.
A parancs a MyNewDisk. vhd nevű új adatlemezt csatolja.
A parancsmag a jelenlegi előfizetés alapértelmezett tárolási fiókjában hozza létre a merevlemezt a VHD-tárolóban.
A parancs frissíti a virtuális gépet a módosítások tükrözéséhez.

### 3. példa: adatlemez hozzáadása adott helyről
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Ez a parancs egy virtuálisgép-objektumot kap az adatbázis nevű virtuális gépnek.
A parancs átadja az aktuális parancsmagnak.
A parancs egy Disk14. vhd nevű meglévő adatlemezt csatol a megadott helyről.
A parancs frissíti a virtuális gépet a módosítások tükrözéséhez.

## PARAMÉTEREK

### -CreateNew
Azt jelzi, hogy ez a parancsmag adatlemezt hoz létre.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskLabel
Egy új adatlemez lemezének címkéjét adja meg.

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskName
A lemezkezelő adatlemezének a nevét adja meg.

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
A logikai méretet adja meg az új adatlemezhez gigabájtban.

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Az állomás szintű gyorsítótár-beállításokat adja meg.
Az érvényes értékek a következők: 

- Nincs 
- ReadOnly 
- ReadWrite

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Import
Jelzi, hogy ez a parancsmag egy meglévő adatlemezt importál a képtárházból.

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportFrom
Azt jelzi, hogy ez a parancsmag egy meglévő adatlemezt importál egy tárolóban lévő blobból.

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

### -LUN
Annak a logikai egységnek a logikai egység számát adja meg, amely a virtuális gép adatmeghajtójának logikai egysége.
Az érvényes értékek a következők: 0 – 15.
Az egyes adatlemezeknek egyedi logikai egységgel kell rendelkezniük.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
Megadja a blob helyét az Azure Storage-fiókban, ahol ez a parancsmag tárolja az adatlemezt.
Ha nem ad meg helyet, a parancsmag az aktuális előfizetés alapértelmezett tárolási fiókjának VHD-tárolójában tárolja az adatlemezt.
Ha egy VHD-tároló nem létezik, a parancsmag létrehoz egy VHD-tárolót.

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
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

### -VM
Annak a virtuális gépnek az objektumát adja meg, amelyre a parancsmag adatlemezt csatol.
Virtuális gép objektum beszerzéséhez használja a **Get-AzureVM** parancsmagot.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


