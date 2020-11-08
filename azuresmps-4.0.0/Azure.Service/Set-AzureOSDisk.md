---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015828"
---
# Set-AzureOSDisk

## Áttekintés
Egy Azure Virtual Machine állomás-gyorsítótári üzemmódjának módosítása.

## SZINTAXISA

### Átméretezés
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Átméretezése
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureOSDisk** parancsmag az Azure Virtual Machine operációs rendszer lemezének állomás-gyorsítótári üzemmódját módosítja.
A támogatott állomás-gyorsítótári üzemmódok ReadOnly és ReadWrite.
Ha futtatja ezt a parancsmagot egy futó virtuális gépen, a virtuális gép újraindul.

## Példák

### 1. példa: az állomás-gyorsítótári mód beállítása ReadOnly értékre a csővezeték használatával
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine02 nevű virtuális gépet a ContosoService nevű szolgáltatásban.
A parancs a virtuális gépet az aktuális parancsmagba továbbítja a csővezeték-kezelő segítségével.
Az aktuális parancsmag a virtuális gép operációsrendszer-lemezének állomás-gyorsítótári üzemmódját a ReadOnly értékre állítja.

### 2. példa: az állomás gyorsítótári módjának beállítása ReadWrite
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

Az első parancs megkapja a VirtualMachine02 nevű virtuális gépet a ContosoService nevű szolgáltatásban, majd a változóban tárolja.

A második parancs beállítja a ReadWrite a virtuális gép operációs rendszer lemezének állomás-gyorsítótári módját.

## PARAMÉTEREK

### -HostCaching
Az operációs rendszer merevlemezének az állomás-gyorsítótár attribútumát adja meg.
Az érvényes értékek a következők: 

- ReadOnly 
- ReadWrite

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
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

### -ResizedSizeInGB
Új méretet ad meg az operációs rendszer merevlemezének gigabájtjában.
A méretnek az aktuális méretnél nagyobbnak kell lennie.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Azt a virtuális gépet adja meg, amelyre a parancsmag az operációs rendszer lemezét módosítja.
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

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureOSDisk](./Get-AzureOSDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


