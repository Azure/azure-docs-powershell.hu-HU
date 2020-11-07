---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 3bc870be1628f5fbf22042155e6a889dbdaadc84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672063"
---
# Set-AzureRmVMDataDisk

## Áttekintés
Egy virtuális gép adatlemezének tulajdonságait módosítja.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ChangeWithName
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ChangeWithLun
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzureRmVMDataDisk** parancsmag a virtuális gép adatlemezének tulajdonságait módosítja.

## Példák

### Példa 1: adatlemez gyorsítótárazási módjának módosítása
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

Az első parancs a **Get-AzureRmVM** segítségével a ContosoVM07 nevű virtuális gépet kapja.
A parancs a $VM változóban tárolja.

A második parancs módosítja a DataDisk01 nevű adatlemez gyorsítótárazási módját az $VM virtuális gépén.
A parancs átadja az eredményt az Update-AzureRmVM parancsmagnak, amely végrehajtja a módosításokat.
A befizetési mód módosítása a virtuális gép újraindítását okozhatja.

## PARAMÉTEREK

### -Gyorsítótárazás
A lemez gyorsítótárazási módját adja meg.
A paraméter elfogadható értékei a következők:

- ReadOnly
- ReadWrite

Az alapértelmezett érték a ReadWrite.
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Azt a virtuális gépet adja meg, amelynek a parancsmagja módosította az adatlemezt.
A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Update-AzureRmVM](./Update-AzureRmVM.md)


