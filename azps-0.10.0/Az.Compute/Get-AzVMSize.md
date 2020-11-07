---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: 46a0ffcaece93328447405f78af2af0785b329c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844558"
---
# Get-AzVMSize

## Áttekintés
Elérhetővé válik a virtuális gépek mérete.

## SZINTAXISA

### ListVirtualMachineSizeParamSet (alapértelmezett)
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAvailableSizesForAvailabilitySet
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAvailableSizesForVirtualMachine
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzVMSize** parancsmag a virtuális gépek méreteit érheti el.

## Példák

### Példa 1: a virtuális gépek méretének beszerzése egy helyhez
```
PS C:\> Get-AzVMSize -Location "Central US"
```

Ez a parancs a virtuális gépek elérhető méretét a megadott helyen kapja meg.

### 2. példa: az elérhetőségi készlet méretének beszerzése
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

Ez a parancs elérhetővé válik a virtuális gépek számára, amelyeket a AvailabilitySet17 nevű elérhetőségi készletben lehet telepíteni.

### Példa 3: a meglévő virtuális gép méretének beszerzése
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

Ez a parancs elérhetővé válik a meglévő, VirtualMachine12 nevű virtuális gép méretéhez.
A virtuális gépet átméretezheti a parancs által beolvasott méretben.

## PARAMÉTEREK

### -AvailabilitySetName
Annak az elérhetőségi készletnek a nevét adja meg, amelyhez ez a parancsmag a rendelkezésre álló virtuális gépek méretét kapja.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
Azt a helyet adja meg, ahol ez a parancsmag a rendelkezésre álló virtuális gépek méreteit kapja.

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális gép erőforráscsoport-csoportjának nevét adja meg.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag az átméretezéshez elérhető virtuális gépek méretét kapja.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineSize

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)


