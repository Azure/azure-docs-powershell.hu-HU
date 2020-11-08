---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016166"
---
# Remove-AzureDataDisk

## Áttekintés
Egy Azure virtuális gépről származó adatlemez eltávolítása.

## SZINTAXISA

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureDataDisk** parancsmag eltávolítja az adatlemezt egy Azure Virtual Machine-webhelyről.
Ez a parancsmag alapértelmezés szerint nem távolítja el az adatlemez blobját a tároló fiókból.

## Példák

### 1. példa: adatlemez eltávolítása
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban.
A parancs a virtuális gépet az aktuális parancsmagba továbbítja a csővezeték-kezelő segítségével.
Az aktuális parancsmag eltávolítja azt az adatlemezt, amelynek a logikai egysége 0.

### 2. példa: adatlemez és a virtuális merevlemez-fájl eltávolítása
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

Ez a parancs a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban kapja meg.
A parancs átadja a virtuális gépet az aktuális parancsmagnak.
Az aktuális parancsmag eltávolítja azt az adatlemezt, amelynek a logikai egysége 0.
A parancs a *DeleteVHD* paramétert tartalmazza.
Emiatt a mögöttes virtuális merevlemez is törlődik.
A parancs frissíti a virtuális gépet a módosítások tükrözéséhez a **Update-AzureVM** parancsmag használatával.

## PARAMÉTEREK

### -DeleteVHD
Jelzi, hogy ez a parancsmag eltávolítja az adatlemezt és a virtuális merevlemezt (VHD) a blob-tárolóból.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### -VM
Az adatlemezhez kapcsolt virtuálisgép-objektumot adja meg.
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

[Add-AzureDataDisk](./Add-AzureDataDisk.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


