---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369471"
---
# Get-AzVMSize

## SYNOPSIS
Elérhetővé válik virtuális gépméretek.

## SZINTAXIS

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

## LEÍRÁS
A **Get-AzVMSize parancsmag** elérhetővé válik virtuális gépméretekben.

## PÉLDÁK

### 1. példa: Virtuális gépméretek lekérte egy helyhez
```
PS C:\> Get-AzVMSize -Location "Central US"
```

Ez a parancs a megadott helyen lévő virtuális gépekhez elérhető méreteket kapja meg.

### 2. példa: Elérhetőségi készlet méretei
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

Ez a parancs elérhető méretű virtuális gépekhez, amelyek telepíthetők az ElérhetőségiKészlet17 nevű rendelkezésre állási halmazban.

### 3. példa: Meglévő virtuális gép méretének lekérte
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

Ez a parancs elérhető méretű lesz a VirtualMachine12 nevű meglévő virtuális géphez.
Ezt a virtuális gépet átméretezheti a parancs méretének megfelelőre.

## PARAMETERS

### -AvailabilitySetName
Annak az elérhetőségi halmaznak a nevét adja meg, amelynek a parancsmagja a rendelkezésre álló virtuális gépméreteket kapja.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Location
Azt a helyet adja meg, ahol a parancsmag a rendelkezésre álló virtuális gépméreteket kapja.

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális gép erőforráscsoportját adja meg.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Megadja annak a virtuális gépnek a nevét, amelybe ez a parancsmag az átméretezéshez elérhető virtuális gépméreteket kapja.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)


