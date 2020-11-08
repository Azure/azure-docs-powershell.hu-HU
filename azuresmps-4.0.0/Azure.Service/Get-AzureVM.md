---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016547"
---
# Get-AzureVM

## Áttekintés
Beolvassa az adatokat egy vagy több Azure virtuális gépre.

## SZINTAXISA

### ListAllVMs (alapértelmezett)
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### GetVMByServiceAndVMName
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureVM** parancsmag információkat keres az Azure-ban futó virtuális gépekről.
Egy olyan objektumot ad eredményül, amely egy adott virtuális gépen információt ad, vagy ha nincs megadva virtuális gép, az aktuális előfizetéshez megadott szolgáltatásban lévő összes virtuális gépen.

## Példák

### Példa 1: adatok beolvasása egy adott virtuális gépen
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

Ez a parancs egy olyan objektumot ad eredményül, amely a ContosoService01 felhőben futó VirtualMachine02 virtuális gépén található.

### 2. példa: adatok beolvasása az összes virtuális gépen
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

Ez a parancs a ContosoService01 felhőben futó összes virtuális gépen információt tartalmazó lista-objektumot keres.

### 3. példa: a virtuális gép állapotait tartalmazó táblázat megjelenítése
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

Ez a parancs megjeleníti a ContosoService01 szolgáltatásban futó virtuális gépeket, azok frissítési tartományát, valamint az egyes virtuális gépek pillanatnyi állapotát.

## PARAMÉTEREK

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

### -Name (név)
Annak a virtuális gépnek a neve, amelyhez információt szeretne beolvasni.
Ha ez a paraméter nincs megadva, a parancsmag egy lista objektumot ad eredményül, amely a megadott szolgáltatás összes virtuális gépre vonatkozó információt tartalmaz.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
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

### -Szolgáltatásnév
Annak a felhőalapú szolgáltatásnak a nevét adja meg, amelyből vissza szeretné adni a virtuálisgép-információkat.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
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

[Új – AzureVM](./New-AzureVM.md)

[Új – AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzureVM](./Remove-AzureVM.md)

[Újraindítás – AzureVM](./Restart-AzureVM.md)

[Start-AzureVM](./Start-AzureVM.md)

[Stop-AzureVM](./Stop-AzureVM.md)

[Update-AzureVM](./Update-AzureVM.md)


