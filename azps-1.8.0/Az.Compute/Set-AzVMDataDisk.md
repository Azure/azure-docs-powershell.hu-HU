---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: 032efea1c892905a41dc141e253cd480c3f3bba7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671233"
---
# Set-AzVMDataDisk

## Áttekintés
Egy virtuális gép adatlemezének tulajdonságait módosítja.

## SZINTAXISA

### ChangeWithName
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ChangeWithLun
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzVMDataDisk** parancsmag a virtuális gép adatlemezének tulajdonságait módosítja.

## Példák

### Példa 1: adatlemez gyorsítótárazási módjának módosítása
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

Az első parancs a **Get-AzVM** segítségével a ContosoVM07 nevű virtuális gépet kapja.
A parancs a $VM változóban tárolja.
A második parancs módosítja a DataDisk01 nevű adatlemez gyorsítótárazási módját az $VM virtuális gépén.
A parancs átadja az eredményt az Update-AzVM parancsmagnak, amely végrehajtja a módosításokat.
A befizetési mód módosítása a virtuális gép újraindítását okozhatja.

## PARAMÉTEREK

### -Gyorsítótárazás
A lemez gyorsítótárazási módját adja meg.
A paraméter elfogadható értékei a következők:
- ReadOnly
- ReadWrite: az alapértelmezett érték a ReadWrite.
Az érték módosításakor a virtuális gép újraindul.
Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
Az adatlemez méretének meghatározása gigabájtban.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LUN
Annak a logikai egységnek a logikai egység számát adja meg, amelyet a parancsmag módosított.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Megadja annak az adatlemeznek a nevét, amelyet a parancsmag módosított.

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
A virtuálisgép-felügyelt lemez fiók típusa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Azt a virtuális gépet adja meg, amelynek a parancsmagja módosította az adatlemezt.
A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Itt adhatja meg, hogy az adatlemezen engedélyezni vagy letiltani kell-e a WriteAccelerator.

```yaml
Type: System.Management.Automation.SwitchParameter
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

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

### System. String

### System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]

### System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. CachingTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[Update-AzVM](./Update-AzVM.md)


