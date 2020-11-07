---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: a8ac31efd77d5b8ff5c07920bb14b44f80ac0955
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844601"
---
# Get-AzVMExtension

## Áttekintés
A virtuálisgép-bővítmények tulajdonságait a virtuális gépen telepítette.

## SZINTAXISA

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzVMExtension** parancsmag a virtuális gépre telepített virtuálisgép-bővítmények tulajdonságait kapja meg.
Adja meg annak a bővítménynek a nevét, amelyhez tulajdonságokat szeretne kapni.
Ha csak a bővítmény példány nézetét szeretné látni, adja meg az állapot paramétert.

## Példák

### Példa 1: bővítmény tulajdonságainak beolvasása
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

Ez a parancs a CustomScriptExtension nevű bővítmény tulajdonságait az erőforráscsoport ResourceGroup11 VirtualMachine22 nevű virtuális gépen kapja meg.

### 2. példa: egy bővítmény példány nézetének beolvasása
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

Ez a parancs a CustomScriptExtension nevű VirtualMachine22 nevű virtuális gép példány nézetét kapja meg az erőforráscsoport ResourceGroup11.

## PARAMÉTEREK

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

### -Name (név)
A kiterjesztés nevét adja meg.
Ez a parancsmag a paraméter által megadott kiterjesztés tulajdonságait kapja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Állapot
Jelzi, hogy ez a parancsmag csak a bővítmény példány nézetét kapja meg.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
A virtuális gép nevét adja meg.
Ez a parancsmag a virtuális gép egy bővítményének tulajdonságait adja meg, és ezt a paramétert adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

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

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzVMExtension](./Remove-AzVMExtension.md)

[Set-AzVMExtension](./Set-AzVMExtension.md)


