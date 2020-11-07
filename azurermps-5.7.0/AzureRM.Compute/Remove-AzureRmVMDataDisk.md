---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 3c1edb8302ac0921a8f396230637b842d88eab77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672544"
---
# Remove-AzureRmVMDataDisk

## Áttekintés
Az adatlemez eltávolítása egy virtuális gépről.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmVMDataDisk** parancsmag egy virtuális gépről eltávolítja az adatlemezt.

## Példák

### 1. példa: adatlemez eltávolítása virtuális gépről
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Az első parancs a **Get-AzureRmVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.
A parancs a virtuális gépet a $VirtualMachine változóban tárolja.

A második parancs eltávolítja a Disk3 nevű adatlemezt a $VirtualMachineban tárolt virtuális gépről.

A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.

## PARAMÉTEREK

### -DataDiskNames
A parancsmag által eltávolított egy vagy több adatlemez nevét adja meg.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Annak a helyi virtuális gépnek az objektumát adja meg, amelyből el szeretné távolítani az adatlemezt.
A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmVMDataDisk](./Add-AzureRmVMDataDisk.md)

[Get-AzureRmVM](./Get-AzureRmVM.md)


