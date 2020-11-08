---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016066"
---
# Set-AzureDataDisk

## Áttekintés
Módosítja egy meglévő adatlemez gyorsítótárát egy Azure virtuális gépen.

## SZINTAXISA

### Átméretezés
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Átméretezése
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureDataDisk** parancsmag módosította egy meglévő adatlemez gyorsítótár-attribútumait egy Azure virtuális gépen.
Adja meg, hogy melyik adatlemezen frissüljön a logikai egység száma (LUN).

## Példák

### Példa 1: az állomás gyorsítótárának módosítása adatlemezhez
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

Ez a parancs a **Get-AzureVM** parancsmag segítségével a ContosoService nevű szolgáltatáson futó virtuális gépeket kapja.
A parancs a csővezeték-kezelő segítségével átadja őket az aktuális parancsmagnak.
Ez a parancsmag a VirtualMachine07 nevű virtuális gép 2-es verziójában lévő adatlemezt állítja be a ReadOnly-Host gyorsítótárazási szolgáltatás használatára.
A parancs frissíti a virtuális gépet a módosítások tükrözéséhez a **Update-AzureVM** parancsmag használatával.

### 2. példa: az állomás gyorsítótárának módosítása a virtuális gép minden adatlemezén
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

Ez a parancs a VirtualMachine07 nevű virtuális gép objektumát kapja a ContosoService felhő szolgáltatásban.
A parancs a **Get-AzureDataDisk** parancsmagot adja át, amely a virtuális gép adatlemezeit kapja.
Az aktuális parancsmag ekkor beállítja az egyes adatlemezek állomás-gyorsítótárazási módját a ReadWrite-ra.
A parancs frissíti a virtuális gépet a módosítások tükrözéséhez.

## PARAMÉTEREK

### -DiskName
A parancsmag által módosított adatlemez-konfiguráció nevét adja meg.

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching

> [!WARNING]
> A lemezek gyorsítótárazása nem támogatott a 4 TiB és a nagyobb lemezek esetében. Ha több lemez van csatlakoztatva a VM-hez, akkor a 4 TiB-nál kisebb lemezek mindegyike támogatja a gyorsítótárazást.
>
> Az Azure-lemezek gyorsítótár-beállításának módosítása leválik, és újra csatolja a céllemez tartalmát. Ha az operációs rendszer lemeze, a VM újraindul. Állítsa le az összes olyan alkalmazást/szolgáltatást, amelyet esetleg érinthet az ilyen zavarok, mielőtt módosítaná a lemezgyorsítótár beállítását. Ezek az ajánlások nem követik az adatsérülést.

Az állomás szintű gyorsítótár-beállításokat adja meg.
Az érvényes értékek a következők:

- Nincs
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
A virtuális gép adatmeghajtójának logikai egységét adja meg.
Az érvényes értékek a következők: 0 – 15.

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
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
Az adatlemez új méretének meghatározása gigabájtban.
Az új méretnek az aktuális méretnél nagyobbnak kell lennie.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
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

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


