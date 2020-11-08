---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016198"
---
# New-AzureVMImageDiskConfigSet

## Áttekintés
Létrehoz egy Disk Configuration set objektumot.

## SZINTAXISA

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureVMImageDiskConfigSet** parancsmag létrehoz egy olyan Disk Configuration set objektumot, amely a képfrissítési parancsmagra lett átadva.
A OSDiskConfig és a DataDiskConfig objektumot ágyazza be.
A **set-AzureVMImageOSDiskConfig** és a **set-AzureVMImageDataDiskConfig** parancsmagok segítségével beállíthatja az operációs rendszer lemez-és adatlemez-tulajdonságait a virtuális gép képére.

## Példák

### Példa 1: Disk Configuration set objektum létrehozása
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

Ez a parancs létrehoz egy Disk Configuration set objektumot, és a találatokat az $Disk nevű változóban tárolja.
A lemez beállítása után a rendszer a OSDiskConfig és a DataDiskConfig beállítását használja.
Ezután a virtuális gép frissíti a konfigurációt.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. WindowsAzure. Command. ServiceManagement. Model. VirtualMachineImageDiskConfigSet

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureVMImageDiskConfigSet](./Get-AzureVMImageDiskConfigSet.md)

[Set-AzureVMImageOSDiskConfig](./Set-AzureVMImageOSDiskConfig.md)

[Set-AzureVMImageDataDiskConfig](./Set-AzureVMImageDataDiskConfig.md)


