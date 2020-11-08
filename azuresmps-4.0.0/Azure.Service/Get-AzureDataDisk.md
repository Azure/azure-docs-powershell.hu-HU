---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015651"
---
# Get-AzureDataDisk

## Áttekintés
Azure-adatlemezeket kap.

## SZINTAXISA

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureDataDisk** parancsmag olyan objektumot kap, amely az Azure Virtual Machine adatlemezeit jelképezi.
Ha egy adott adatlemez-objektumot szeretne beszerezni, adja meg a merevlemez logikai egységének számát (LUN).

## Példák

### Példa 1: a virtuális gép minden adatlemezének beolvasása
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban.
A parancs a virtuális gépet az aktuális parancsmagba továbbítja a csővezeték-kezelő segítségével.
Az aktuális parancsmag a virtuális gép összes adatlemezét beilleszti.

### 2. példa: adott adatlemez beszerzése egy vituralvirtual-machinevirtual
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

Ez a parancs a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban kapja meg.
A parancs átadja a virtuális gépet az aktuális parancsmagnak.
Az aktuális parancsmag a LUN 2 tároló adatlemezét kapja.

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

### -LUN
A virtuális gép adatmeghajtójának logikai egységét adja meg.
Az érvényes értékek a következők: 0 – 15.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
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
Annak a virtuális gépnek az objektumát adja meg, amelyhez ez a parancsmag adatlemezeket kap.
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

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)


